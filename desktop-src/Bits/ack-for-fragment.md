---
title: Подтверждение для фрагмента
description: Используйте ACK для пакета фрагмента, чтобы подтвердить запрос фрагмента клиента.
ms.assetid: f5466489-2d5e-4850-a39c-37bc4923a7ac
keywords:
- Подтверждение для битов фрагмента
topic_type:
- apiref
api_name:
- Ack for Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd4b8bf5580a5724c689ced1886051006d34cd3c9ba0561d253f36428178c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702124"
---
# <a name="ack-for-fragment"></a>Подтверждение для фрагмента

Используйте **ACK для пакета фрагмента** , чтобы подтвердить запрос [**фрагмента**](fragment.md) клиента.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
BITS-Received-Content-Range: range
BITS-Reply-URL: url
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Заголовки

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>код причины
</dt> <dd>

Замените код причины кодом причины HTTP. В следующей таблице показаны типичные коды причин ответа на запрос [**фрагмента**](fragment.md) . Список кодов причин HTTP см. в [документе RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Код причины    | Описание                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| 200<br/> | Все в порядке. Запрос выполнен успешно.<br/>                                                                             |
| 416<br/> | Диапазон — невыполнимый. Клиент отправил фрагмент, диапазон которого не является смежным с предыдущим фрагментом.<br/> |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Описание причины
</dt> <dd>

Замените Reason — Description на HTTP-описание, связанное с кодом причины. Например, задайте для параметра reason-Description значение ОК, если причина — код 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Определяет этот пакет ответа как пакет подтверждения.

</dd> <dt>

<span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>БИТ-получено-Content-Range
</dt> <dd>

Отсчитываемое от нуля смещение до следующего байта, которое сервер ждет отправить клиенту. Например, если фрагмент содержал диапазон 128 212, значение Range должно быть равно 213.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS — Session-ID
</dt> <dd>

Строковый идентификатор GUID, определяющий сеанс клиента. Замените {GUID} идентификатором сеанса, отправленным клиентом в пакете запроса [**фрагмента**](fragment.md) . Если вы не распознаете идентификатор сеанса, установите для заголовка "BITS-Error-code" \_ ( \_ не найден) сеанс BG E \_ \_ .

</dd> <dt>

<span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-Reply-URL
</dt> <dd>

Содержит URL-адрес данных ответа для задания отправки и ответа. Включите этот заголовок в окончательный ответ фрагмента после завершения передачи и получения ответа от серверного приложения, если это применимо.

Используйте заголовок Content-Range из запроса фрагмента, чтобы определить, завершена ли передача. Отправка завершается, если конечное смещение значения диапазона равно значению общей длины минус единица.

Сервер BITS отправляет файл отправки в серверное приложение после того, как он определит, что передача завершена. Серверное приложение обрабатывает файл и создает ответ. Сервер BITS задает для параметра BITS-Reply-URL URL-адрес файла ответов из серверного приложения.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Длина содержимого
</dt> <dd>

Замените length числом байтов, включаемых в текст ответа. Требуется длина содержимого, даже если текст ответа не содержит содержимого.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-code
</dt> <dd>

Замените Error-code шестнадцатеричным числом, представляющим значение HRESULT, связанное с ошибкой на стороне сервера. Включайте этот заголовок только в том случае, если код причины не 200 или 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-ошибка-контекст
</dt> <dd>

Replace Error-context с шестнадцатеричным числом, представляющим контекст, в котором произошла ошибка. Укажите шестнадцатеричное число для [**\_ \_ \_ удаленного \_ файла контекста ошибки BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5), если сервер сгенерировал ошибку. В противном случае укажите шестнадцатеричное число для **\_ \_ \_ удаленного \_ приложения с контекстом ошибки BG** (0x7), если ошибка была создана приложением, куда передается файл передачи. Включайте этот заголовок только в том случае, если код причины не 200 или 201.

</dd> </dl>

## <a name="remarks"></a>Remarks

Если сеанс предназначен для задания отправки и ответа, может возникнуть задержка до того, как клиент получит окончательное **подтверждение ответа фрагмента** . Продолжительность задержки зависит от времени, в течение которого серверное приложение (приложение, на которое сервер отправляет файл отправки) создает ответ.

## <a name="see-also"></a>См. также

<dl> <dt>

[**Создание сеанса**](create-session.md)
</dt> <dt>

[**Fragment**](fragment.md)
</dt> </dl>

 

 





