---
title: Подтверждение для Cancel-Session
description: Используйте подтверждение для пакета Cancel-Session, чтобы подтвердить запрос Cancel-Session клиента. Сервер отправляет подтверждение после освобождения всех ресурсов, связанных с сеансом передачи.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Подтверждение для битов Cancel-Session
topic_type:
- apiref
api_name:
- Ack for Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b85ff937b720a69ee2722cef2f02b25273ea58d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104070828"
---
# <a name="ack-for-cancel-session"></a>Подтверждение для Cancel-Session

Чтобы подтвердить запрос на [**отмену сеанса**](cancel-session.md) клиента, используйте **Подтверждение ACK для пакета отмены сеанса** . Сервер отправляет подтверждение после освобождения всех ресурсов, связанных с сеансом передачи.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Заголовки

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>код причины
</dt> <dd>

Замените код причины кодом причины HTTP. Например, в случае успешного выполнения задайте для кода причины значение 200. Список кодов причин HTTP см. в [документе RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Описание причины
</dt> <dd>

Замените Reason — Description на HTTP-описание, связанное с кодом причины. Например, задайте для параметра reason-Description значение ОК, если причина — код 200.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Определяет этот пакет ответа как пакет подтверждения.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS — Session-ID
</dt> <dd>

Строковый идентификатор GUID, определяющий сеанс клиента. Замените {GUID} идентификатором сеанса, отправленным клиентом в пакете запроса на [**отмену сеанса**](cancel-session.md) . Если вы не распознаете идентификатор сеанса, установите для заголовка "BITS-Error-code" \_ ( \_ не найден) сеанс BG E \_ \_ .

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Длина содержимого
</dt> <dd>

Замените length числом байтов, включаемых в текст ответа. Требуется, даже если текст ответа не содержит содержимого.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-code
</dt> <dd>

Замените Error-code шестнадцатеричным числом, представляющим значение HRESULT, связанное с ошибкой на стороне сервера. Включайте этот заголовок только в том случае, если код причины не 200 или 201.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-ошибка-контекст
</dt> <dd>

Replace Error-context с шестнадцатеричным числом, представляющим контекст, в котором произошла ошибка. Укажите шестнадцатеричное число для [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5), если ошибка произошла на сервере. В противном случае укажите шестнадцатеричное число для **\_ \_ \_ удаленного \_ приложения с контекстом ошибки BG** (0x7), если ошибка была создана приложением, куда передается файл передачи. Включайте этот заголовок только в том случае, если код причины не 200 или 201.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Клиент BITS повторно отправляет пакет [**отмены сеанса**](cancel-session.md) , если код причины находится в диапазоне от 500 до 599, если не указан заголовок BITS-Error-code со значением \_ \_ \_ не найденного сеанса BG E \_ . Клиент не будет пытаться повторять коды причин с 100 по 499.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Подтверждение для закрытия сеанса**](ack-for-close-session.md)
</dt> <dt>

[**Отмена — сеанс**](cancel-session.md)
</dt> </dl>

 

 




