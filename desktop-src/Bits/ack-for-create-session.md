---
title: Подтверждение для Create-Session
description: Используйте подтверждение для пакета Create-Session, чтобы подтвердить запрос Create-Session клиента.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Подтверждение для битов Create-Session
topic_type:
- apiref
api_name:
- Ack for Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9dbfcaeab897d55064fe11a506cefbc9d85dd6852a32d279133e6fe7a33a692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588804"
---
# <a name="ack-for-create-session"></a>Подтверждение для Create-Session

Используйте **подтверждение для пакета создания сеанса** , чтобы подтвердить запрос на [**Создание сеанса**](create-session.md) клиента.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Protocol: {guid}
BITS-Session-Id: {guid}
BITS-Host-Id: PublicHostName
BITS-Host-Id-Fallback-Timeout: Timeout
Accept-Encoding: Identity
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Заголовки

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>код причины
</dt> <dd>

Замените код причины кодом причины HTTP. В следующей таблице показаны типичные коды причин ответа на запрос [**создания сеанса**](create-session.md) . Список кодов причин HTTP см. в [документе RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Код причины    | Описание                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| 200<br/> | Все в порядке. Запрос выполнен успешно.<br/>                                          |
| 201<br/> | Создан. Сеанс создан.<br/>                                        |
| 403<br/> | Запрещено. Пользователю не разрешено отправлять файлы по указанному URL-адресу.<br/> |
| 404<br/> | Не найден. Указанный URL-адрес не существует.<br/>                             |
| 409<br/> | Конфликт. Файл существует на сервере и не может быть перезаписан.<br/>       |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Описание причины
</dt> <dd>

Замените Reason — Description на HTTP-описание, связанное с кодом причины. Например, задайте для параметра reason-Description значение ОК, если причина — код 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Определяет этот пакет ответа как пакет подтверждения.

</dd> <dt>

<span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS — протокол
</dt> <dd>

Строковый идентификатор GUID, определяющий протокол, который сервер хочет использовать для этого сеанса. Замените {GUID} идентификатором протокола из списка протоколов, включенных клиентом в запрос на [**Создание сеанса**](create-session.md) . в заголовке BITS-Supported-Protocol содержится список. Включайте этот заголовок только в том случае, если код причины — 200 или 201.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS — Session-ID
</dt> <dd>

Строковый идентификатор GUID, обозначающий этот сеанс с клиентом. Замените {GUID} идентификатором сеанса, который клиент отправляет во всех последующих пакетах запроса.

Служба BITS использует идентификатор GUID для задания сеанса, но вы можете использовать любую строку, допустимую в HTTP, до 100 символов.

</dd> <dt>

<span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-Host-ID
</dt> <dd>

Необязательный элемент. Включайте этот заголовок, только если задано [свойство расширения IIS BITS](bits-iis-extension-properties.md)битшостид. Замените Публичостнаме на имя сервера или IP-адрес из свойства Битшостид.

Клиент должен заменить серверную часть удаленного URL-адреса во всех последующих пакетах. Если клиент не указал это имя узла в последующих пакетах, это может привести к повторному запуску задания на другом сервере в ферме, при этом на предыдущем сервере будет размещен файл частичной передачи.

</dd> <dt>

<span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-Host-ID — резервное время ожидания
</dt> <dd>

Необязательный элемент. Включайте этот заголовок только в том случае, если указан заголовок BITS-Host-ID. Замените время ожидания значением времени ожидания из свойства Битшостидфаллбакктимеаут. Свойство Битшостидфаллбакктимеаут является одним из [свойств расширения IIS BITS](bits-iis-extension-properties.md).

Клиент использует период времени ожидания, чтобы определить, как долго будет пытаться подключиться к серверу, указанному в заголовке BITS-Host-ID, прежде чем вернуть имя узла, указанное в имени удаленного файла задания. Таймер начинается, когда службе BITS не удается подключиться к серверу BITS-Host-ID. Таймер сбрасывается при восстановлении соединения с сервером. Если интервал времени ожидания не указан, клиент никогда не возвращается к имени узла, указанному в имени удаленного файла.

</dd> <dt>

<span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding
</dt> <dd>

Определяет схему кодирования, используемую для фрагментов, отправляемых на сервер. Пакет фрагмента содержит закодированный фрагмент в тексте пакета. Серверу BITS требуется кодировка удостоверений (открытый текст). Включайте этот заголовок только в том случае, если код причины — 200 или 201.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Длина содержимого
</dt> <dd>

Замените length числом байтов, включаемых в текст ответа. Требуется, даже если текст ответа не содержит содержимого.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-code
</dt> <dd>

Замените Error-code шестнадцатеричным числом, представляющим значение HRESULT, связанное с ошибкой на стороне сервера. Включайте этот заголовок, только если код причины не 200 или 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-ошибка-контекст
</dt> <dd>

Replace Error-context с шестнадцатеричным числом, представляющим контекст, в котором произошла ошибка. Укажите шестнадцатеричное число для [**\_ \_ \_ удаленного \_ файла контекста ошибки BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5), если сервер сгенерировал ошибку. В противном случае укажите шестнадцатеричное число для **\_ \_ \_ удаленного \_ приложения с контекстом ошибки BG** (0x7), если ошибка была создана приложением, куда передается файл передачи. Включайте этот заголовок только в том случае, если код причины не 200 или 201.

</dd> </dl>

## <a name="see-also"></a>См. также

<dl> <dt>

[**Создание сеанса**](create-session.md)
</dt> </dl>

 

 





