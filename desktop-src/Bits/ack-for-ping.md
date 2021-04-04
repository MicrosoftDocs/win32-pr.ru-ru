---
title: Подтверждение проверки связи
description: Используйте подтверждение для пакета ping, чтобы подтвердить запрос проверки связи клиента.
ms.assetid: 2e288564-d06f-4b45-b0c0-7aab1897da40
keywords:
- Подтверждение для бит проверки связи
topic_type:
- apiref
api_name:
- Ack for Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a3ca765c8bd7758f19abe396ad0449a5895d8e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "103987975"
---
# <a name="ack-for-ping"></a>Подтверждение проверки связи

Используйте **подтверждение для пакета ping** , чтобы подтвердить запрос [**проверки связи**](ping.md) клиента.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
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

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Проверок**](ping.md)
</dt> </dl>

 

 




