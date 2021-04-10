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
# <a name="ack-for-cancel-session"></a><span data-ttu-id="021a4-105">Подтверждение для Cancel-Session</span><span class="sxs-lookup"><span data-stu-id="021a4-105">Ack for Cancel-Session</span></span>

<span data-ttu-id="021a4-106">Чтобы подтвердить запрос на [**отмену сеанса**](cancel-session.md) клиента, используйте **Подтверждение ACK для пакета отмены сеанса** .</span><span class="sxs-lookup"><span data-stu-id="021a4-106">Use the **Ack for Cancel-Session** packet to acknowledge the client's [**Cancel-Session**](cancel-session.md) request.</span></span> <span data-ttu-id="021a4-107">Сервер отправляет подтверждение после освобождения всех ресурсов, связанных с сеансом передачи.</span><span class="sxs-lookup"><span data-stu-id="021a4-107">The server sends the acknowledgment after releasing all resources associated with the upload session.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="021a4-108">Заголовки</span><span class="sxs-lookup"><span data-stu-id="021a4-108">Headers</span></span>

<dl> <dt>

<span data-ttu-id="021a4-109"><span id="reason-code"></span><span id="REASON-CODE"></span>код причины</span><span class="sxs-lookup"><span data-stu-id="021a4-109"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="021a4-110">Замените код причины кодом причины HTTP.</span><span class="sxs-lookup"><span data-stu-id="021a4-110">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="021a4-111">Например, в случае успешного выполнения задайте для кода причины значение 200.</span><span class="sxs-lookup"><span data-stu-id="021a4-111">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="021a4-112">Список кодов причин HTTP см. в [документе RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="021a4-112">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="021a4-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Описание причины</span><span class="sxs-lookup"><span data-stu-id="021a4-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="021a4-114">Замените Reason — Description на HTTP-описание, связанное с кодом причины.</span><span class="sxs-lookup"><span data-stu-id="021a4-114">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="021a4-115">Например, задайте для параметра reason-Description значение ОК, если причина — код 200.</span><span class="sxs-lookup"><span data-stu-id="021a4-115">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="021a4-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span><span class="sxs-lookup"><span data-stu-id="021a4-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="021a4-117">Определяет этот пакет ответа как пакет подтверждения.</span><span class="sxs-lookup"><span data-stu-id="021a4-117">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="021a4-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS — Session-ID</span><span class="sxs-lookup"><span data-stu-id="021a4-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="021a4-119">Строковый идентификатор GUID, определяющий сеанс клиента.</span><span class="sxs-lookup"><span data-stu-id="021a4-119">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="021a4-120">Замените {GUID} идентификатором сеанса, отправленным клиентом в пакете запроса на [**отмену сеанса**](cancel-session.md) .</span><span class="sxs-lookup"><span data-stu-id="021a4-120">Replace {guid} with the session identifier that the client sent in the [**Cancel-Session**](cancel-session.md) request packet.</span></span> <span data-ttu-id="021a4-121">Если вы не распознаете идентификатор сеанса, установите для заголовка "BITS-Error-code" \_ ( \_ не найден) сеанс BG E \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="021a4-121">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="021a4-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Длина содержимого</span><span class="sxs-lookup"><span data-stu-id="021a4-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="021a4-123">Замените length числом байтов, включаемых в текст ответа.</span><span class="sxs-lookup"><span data-stu-id="021a4-123">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="021a4-124">Требуется, даже если текст ответа не содержит содержимого.</span><span class="sxs-lookup"><span data-stu-id="021a4-124">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="021a4-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-code</span><span class="sxs-lookup"><span data-stu-id="021a4-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="021a4-126">Замените Error-code шестнадцатеричным числом, представляющим значение HRESULT, связанное с ошибкой на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="021a4-126">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="021a4-127">Включайте этот заголовок только в том случае, если код причины не 200 или 201.</span><span class="sxs-lookup"><span data-stu-id="021a4-127">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="021a4-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-ошибка-контекст</span><span class="sxs-lookup"><span data-stu-id="021a4-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="021a4-129">Replace Error-context с шестнадцатеричным числом, представляющим контекст, в котором произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="021a4-129">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="021a4-130">Укажите шестнадцатеричное число для [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5), если ошибка произошла на сервере.</span><span class="sxs-lookup"><span data-stu-id="021a4-130">Specify the hexadecimal number for [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="021a4-131">В противном случае укажите шестнадцатеричное число для **\_ \_ \_ удаленного \_ приложения с контекстом ошибки BG** (0x7), если ошибка была создана приложением, куда передается файл передачи.</span><span class="sxs-lookup"><span data-stu-id="021a4-131">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="021a4-132">Включайте этот заголовок только в том случае, если код причины не 200 или 201.</span><span class="sxs-lookup"><span data-stu-id="021a4-132">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="021a4-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="021a4-133">Remarks</span></span>

<span data-ttu-id="021a4-134">Клиент BITS повторно отправляет пакет [**отмены сеанса**](cancel-session.md) , если код причины находится в диапазоне от 500 до 599, если не указан заголовок BITS-Error-code со значением \_ \_ \_ не найденного сеанса BG E \_ .</span><span class="sxs-lookup"><span data-stu-id="021a4-134">The BITS client resends the [**Cancel-Session**](cancel-session.md) packet if the reason-code is in the range from 500 through 599, unless the BITS-Error-Code header is present with a value of BG\_E\_SESSION\_NOT\_FOUND.</span></span> <span data-ttu-id="021a4-135">Клиент не будет пытаться повторять коды причин с 100 по 499.</span><span class="sxs-lookup"><span data-stu-id="021a4-135">The client will not retry for reason codes 100 through 499.</span></span>

## <a name="see-also"></a><span data-ttu-id="021a4-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="021a4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="021a4-137">**Подтверждение для закрытия сеанса**</span><span class="sxs-lookup"><span data-stu-id="021a4-137">**Ack for Close-Session**</span></span>](ack-for-close-session.md)
</dt> <dt>

[<span data-ttu-id="021a4-138">**Отмена — сеанс**</span><span class="sxs-lookup"><span data-stu-id="021a4-138">**Cancel-Session**</span></span>](cancel-session.md)
</dt> </dl>

 

 




