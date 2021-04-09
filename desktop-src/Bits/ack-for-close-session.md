---
title: Подтверждение для Close-Session
description: Используйте подтверждение для пакета Close-Session, чтобы подтвердить запрос Close-Session клиента. Сервер отправляет подтверждение после освобождения всех ресурсов, связанных с сеансом передачи.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Подтверждение для битов Close-Session
topic_type:
- apiref
api_name:
- Ack for Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7142bfd8d1d5d65d1f669a328c75a2c8cdfb036
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104134767"
---
# <a name="ack-for-close-session"></a><span data-ttu-id="20e68-105">Подтверждение для Close-Session</span><span class="sxs-lookup"><span data-stu-id="20e68-105">Ack for Close-Session</span></span>

<span data-ttu-id="20e68-106">Чтобы подтвердить запрос на [**закрытие сеанса**](close-session.md) клиента, используйте **подтверждение для пакета с закрытым сеансом** .</span><span class="sxs-lookup"><span data-stu-id="20e68-106">Use the **Ack for Close-Session** packet to acknowledge the client's [**Close-Session**](close-session.md) request.</span></span> <span data-ttu-id="20e68-107">Сервер отправляет подтверждение после освобождения всех ресурсов, связанных с сеансом передачи.</span><span class="sxs-lookup"><span data-stu-id="20e68-107">The server sends the acknowledgment after releasing all resources associated with the upload session.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="20e68-108">Заголовки</span><span class="sxs-lookup"><span data-stu-id="20e68-108">Headers</span></span>

<dl> <dt>

<span data-ttu-id="20e68-109"><span id="reason-code"></span><span id="REASON-CODE"></span>код причины</span><span class="sxs-lookup"><span data-stu-id="20e68-109"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="20e68-110">Замените код причины кодом причины HTTP.</span><span class="sxs-lookup"><span data-stu-id="20e68-110">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="20e68-111">Например, в случае успешного выполнения задайте для кода причины значение 200.</span><span class="sxs-lookup"><span data-stu-id="20e68-111">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="20e68-112">Список кодов причин HTTP см. в [документе RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="20e68-112">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="20e68-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Описание причины</span><span class="sxs-lookup"><span data-stu-id="20e68-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="20e68-114">Замените Reason — Description на HTTP-описание, связанное с кодом причины.</span><span class="sxs-lookup"><span data-stu-id="20e68-114">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="20e68-115">Например, задайте для параметра reason-Description значение ОК, если причина — код 200.</span><span class="sxs-lookup"><span data-stu-id="20e68-115">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="20e68-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span><span class="sxs-lookup"><span data-stu-id="20e68-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="20e68-117">Определяет этот пакет ответа как пакет подтверждения.</span><span class="sxs-lookup"><span data-stu-id="20e68-117">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="20e68-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS — Session-ID</span><span class="sxs-lookup"><span data-stu-id="20e68-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="20e68-119">Строковый идентификатор GUID, определяющий сеанс клиента.</span><span class="sxs-lookup"><span data-stu-id="20e68-119">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="20e68-120">Замените {GUID} идентификатором сеанса, отправленным клиентом в пакете запроса на [**закрытие сеанса**](close-session.md) .</span><span class="sxs-lookup"><span data-stu-id="20e68-120">Replace {guid} with the session identifier that the client sent in the [**Close-Session**](close-session.md) request packet.</span></span> <span data-ttu-id="20e68-121">Если вы не распознаете идентификатор сеанса, установите для заголовка "BITS-Error-code" \_ ( \_ не найден) сеанс BG E \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="20e68-121">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="20e68-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Длина содержимого</span><span class="sxs-lookup"><span data-stu-id="20e68-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="20e68-123">Замените length числом байтов, включаемых в текст ответа.</span><span class="sxs-lookup"><span data-stu-id="20e68-123">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="20e68-124">Требуется длина содержимого, даже если текст ответа не содержит содержимого.</span><span class="sxs-lookup"><span data-stu-id="20e68-124">Content-Length is required, even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="20e68-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-code</span><span class="sxs-lookup"><span data-stu-id="20e68-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="20e68-126">Замените Error-code шестнадцатеричным числом, представляющим значение HRESULT, связанное с ошибкой на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="20e68-126">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="20e68-127">Включайте этот заголовок только в том случае, если код причины не 200 или 201.</span><span class="sxs-lookup"><span data-stu-id="20e68-127">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="20e68-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-ошибка-контекст</span><span class="sxs-lookup"><span data-stu-id="20e68-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="20e68-129">Replace Error-context с шестнадцатеричным числом, представляющим контекст, в котором произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="20e68-129">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="20e68-130">Укажите шестнадцатеричное число для [**\_ \_ \_ удаленного \_ файла контекста ошибки BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5), если сервер сгенерировал ошибку.</span><span class="sxs-lookup"><span data-stu-id="20e68-130">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="20e68-131">В противном случае укажите шестнадцатеричное число для **\_ \_ \_ удаленного \_ приложения с контекстом ошибки BG** (0x7), если ошибка была создана приложением, куда передается файл передачи.</span><span class="sxs-lookup"><span data-stu-id="20e68-131">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="20e68-132">Включайте этот заголовок только в том случае, если код причины не 200 или 201.</span><span class="sxs-lookup"><span data-stu-id="20e68-132">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20e68-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20e68-133">Remarks</span></span>

<span data-ttu-id="20e68-134">Клиент BITS повторно отправляет пакет с [**закрытым сеансом**](close-session.md) , если код причины находится в диапазоне от 500 до 599, если не указан заголовок BITS-Error-code со значением \_ \_ \_ не найденного сеанса BG E \_ .</span><span class="sxs-lookup"><span data-stu-id="20e68-134">The BITS client resends the [**Close-Session**](close-session.md) packet if the reason-code is in the range 500 through 599, unless the BITS-Error-Code header is present with a value of BG\_E\_SESSION\_NOT\_FOUND.</span></span> <span data-ttu-id="20e68-135">Клиент не будет пытаться повторять коды причин с 100 по 499.</span><span class="sxs-lookup"><span data-stu-id="20e68-135">The client will not retry for reason codes 100 through 499.</span></span>

## <a name="see-also"></a><span data-ttu-id="20e68-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20e68-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20e68-137">**Подтверждение для отмены сеанса**</span><span class="sxs-lookup"><span data-stu-id="20e68-137">**Ack for Cancel-Session**</span></span>](ack-for-cancel-session.md)
</dt> <dt>

[<span data-ttu-id="20e68-138">**Закрыть — сеанс**</span><span class="sxs-lookup"><span data-stu-id="20e68-138">**Close-Session**</span></span>](close-session.md)
</dt> </dl>

 

 




