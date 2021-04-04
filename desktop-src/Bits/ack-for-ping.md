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
# <a name="ack-for-ping"></a><span data-ttu-id="bc3a1-104">Подтверждение проверки связи</span><span class="sxs-lookup"><span data-stu-id="bc3a1-104">Ack for Ping</span></span>

<span data-ttu-id="bc3a1-105">Используйте **подтверждение для пакета ping** , чтобы подтвердить запрос [**проверки связи**](ping.md) клиента.</span><span class="sxs-lookup"><span data-stu-id="bc3a1-105">Use the **Ack for Ping** packet to acknowledge the client's [**Ping**](ping.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="bc3a1-106">Заголовки</span><span class="sxs-lookup"><span data-stu-id="bc3a1-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="bc3a1-107"><span id="reason-code"></span><span id="REASON-CODE"></span>код причины</span><span class="sxs-lookup"><span data-stu-id="bc3a1-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="bc3a1-108">Замените код причины кодом причины HTTP.</span><span class="sxs-lookup"><span data-stu-id="bc3a1-108">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="bc3a1-109">Например, в случае успешного выполнения задайте для кода причины значение 200.</span><span class="sxs-lookup"><span data-stu-id="bc3a1-109">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="bc3a1-110">Список кодов причин HTTP см. в [документе RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="bc3a1-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="bc3a1-111"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Описание причины</span><span class="sxs-lookup"><span data-stu-id="bc3a1-111"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="bc3a1-112">Замените Reason — Description на HTTP-описание, связанное с кодом причины.</span><span class="sxs-lookup"><span data-stu-id="bc3a1-112">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="bc3a1-113">Например, задайте для параметра reason-Description значение ОК, если причина — код 200.</span><span class="sxs-lookup"><span data-stu-id="bc3a1-113">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="bc3a1-114"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span><span class="sxs-lookup"><span data-stu-id="bc3a1-114"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="bc3a1-115">Определяет этот пакет ответа как пакет подтверждения.</span><span class="sxs-lookup"><span data-stu-id="bc3a1-115">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="bc3a1-116"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Длина содержимого</span><span class="sxs-lookup"><span data-stu-id="bc3a1-116"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="bc3a1-117">Замените length числом байтов, включаемых в текст ответа.</span><span class="sxs-lookup"><span data-stu-id="bc3a1-117">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="bc3a1-118">Требуется, даже если текст ответа не содержит содержимого.</span><span class="sxs-lookup"><span data-stu-id="bc3a1-118">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="bc3a1-119"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-code</span><span class="sxs-lookup"><span data-stu-id="bc3a1-119"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="bc3a1-120">Замените Error-code шестнадцатеричным числом, представляющим значение HRESULT, связанное с ошибкой на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="bc3a1-120">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="bc3a1-121">Включайте этот заголовок, только если код причины не 200 или 201.</span><span class="sxs-lookup"><span data-stu-id="bc3a1-121">Include this header only if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="bc3a1-122"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-ошибка-контекст</span><span class="sxs-lookup"><span data-stu-id="bc3a1-122"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="bc3a1-123">Replace Error-context с шестнадцатеричным числом, представляющим контекст, в котором произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="bc3a1-123">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="bc3a1-124">Укажите шестнадцатеричное число для [**\_ \_ \_ удаленного \_ файла контекста ошибки BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5), если сервер сгенерировал ошибку.</span><span class="sxs-lookup"><span data-stu-id="bc3a1-124">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="bc3a1-125">В противном случае укажите шестнадцатеричное число для **\_ \_ \_ удаленного \_ приложения с контекстом ошибки BG** (0x7), если ошибка была создана приложением, куда передается файл передачи.</span><span class="sxs-lookup"><span data-stu-id="bc3a1-125">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="bc3a1-126">Включайте этот заголовок только в том случае, если код причины не 200 или 201.</span><span class="sxs-lookup"><span data-stu-id="bc3a1-126">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="bc3a1-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc3a1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc3a1-128">**Проверок**</span><span class="sxs-lookup"><span data-stu-id="bc3a1-128">**Ping**</span></span>](ping.md)
</dt> </dl>

 

 




