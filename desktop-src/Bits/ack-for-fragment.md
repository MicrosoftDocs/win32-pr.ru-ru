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
ms.openlocfilehash: ef28381313ce00fd6089ebf845ed342ccae455c7
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "103987976"
---
# <a name="ack-for-fragment"></a><span data-ttu-id="0e820-104">Подтверждение для фрагмента</span><span class="sxs-lookup"><span data-stu-id="0e820-104">Ack for Fragment</span></span>

<span data-ttu-id="0e820-105">Используйте **ACK для пакета фрагмента** , чтобы подтвердить запрос [**фрагмента**](fragment.md) клиента.</span><span class="sxs-lookup"><span data-stu-id="0e820-105">Use the **Ack for Fragment** packet to acknowledge the client's [**Fragment**](fragment.md) request.</span></span>

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

## <a name="headers"></a><span data-ttu-id="0e820-106">Заголовки</span><span class="sxs-lookup"><span data-stu-id="0e820-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="0e820-107"><span id="reason-code"></span><span id="REASON-CODE"></span>код причины</span><span class="sxs-lookup"><span data-stu-id="0e820-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="0e820-108">Замените код причины кодом причины HTTP.</span><span class="sxs-lookup"><span data-stu-id="0e820-108">Replace reason-code with an HTTP reason code.</span></span> <span data-ttu-id="0e820-109">В следующей таблице показаны типичные коды причин ответа на запрос [**фрагмента**](fragment.md) .</span><span class="sxs-lookup"><span data-stu-id="0e820-109">The following table shows the typical reason codes for a response to a [**Fragment**](fragment.md) request.</span></span> <span data-ttu-id="0e820-110">Список кодов причин HTTP см. в [документе RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="0e820-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>



| <span data-ttu-id="0e820-111">Код причины</span><span class="sxs-lookup"><span data-stu-id="0e820-111">Reason code</span></span>    | <span data-ttu-id="0e820-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0e820-112">Description</span></span>                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e820-113">200</span><span class="sxs-lookup"><span data-stu-id="0e820-113">200</span></span><br/> | <span data-ttu-id="0e820-114">Все в порядке.</span><span class="sxs-lookup"><span data-stu-id="0e820-114">OK.</span></span> <span data-ttu-id="0e820-115">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="0e820-115">The request was successful.</span></span><br/>                                                                             |
| <span data-ttu-id="0e820-116">416</span><span class="sxs-lookup"><span data-stu-id="0e820-116">416</span></span><br/> | <span data-ttu-id="0e820-117">Диапазон — невыполнимый.</span><span class="sxs-lookup"><span data-stu-id="0e820-117">Range-Not-Satisfiable.</span></span> <span data-ttu-id="0e820-118">Клиент отправил фрагмент, диапазон которого не является смежным с предыдущим фрагментом.</span><span class="sxs-lookup"><span data-stu-id="0e820-118">The client sent a fragment whose range is not contiguous with the previous fragment.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0e820-119"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Описание причины</span><span class="sxs-lookup"><span data-stu-id="0e820-119"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="0e820-120">Замените Reason — Description на HTTP-описание, связанное с кодом причины.</span><span class="sxs-lookup"><span data-stu-id="0e820-120">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="0e820-121">Например, задайте для параметра reason-Description значение ОК, если причина — код 200.</span><span class="sxs-lookup"><span data-stu-id="0e820-121">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="0e820-122"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span><span class="sxs-lookup"><span data-stu-id="0e820-122"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="0e820-123">Определяет этот пакет ответа как пакет подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0e820-123">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="0e820-124"><span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>БИТ-получено-Content-Range</span><span class="sxs-lookup"><span data-stu-id="0e820-124"><span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-Received-Content-Range</span></span>
</dt> <dd>

<span data-ttu-id="0e820-125">Отсчитываемое от нуля смещение до следующего байта, которое сервер ждет отправить клиенту.</span><span class="sxs-lookup"><span data-stu-id="0e820-125">Zero-based offset to the next byte the server expects the client to send.</span></span> <span data-ttu-id="0e820-126">Например, если фрагмент содержал диапазон 128 212, значение Range должно быть равно 213.</span><span class="sxs-lookup"><span data-stu-id="0e820-126">For example, if the fragment contained the range 128 212, you would set range to 213.</span></span>

</dd> <dt>

<span data-ttu-id="0e820-127"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS — Session-ID</span><span class="sxs-lookup"><span data-stu-id="0e820-127"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="0e820-128">Строковый идентификатор GUID, определяющий сеанс клиента.</span><span class="sxs-lookup"><span data-stu-id="0e820-128">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="0e820-129">Замените {GUID} идентификатором сеанса, отправленным клиентом в пакете запроса [**фрагмента**](fragment.md) .</span><span class="sxs-lookup"><span data-stu-id="0e820-129">Replace {guid} with the session identifier that the client sent in the [**Fragment**](fragment.md) request packet.</span></span> <span data-ttu-id="0e820-130">Если вы не распознаете идентификатор сеанса, установите для заголовка "BITS-Error-code" \_ ( \_ не найден) сеанс BG E \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0e820-130">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="0e820-131"><span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-Reply-URL</span><span class="sxs-lookup"><span data-stu-id="0e820-131"><span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-Reply-URL</span></span>
</dt> <dd>

<span data-ttu-id="0e820-132">Содержит URL-адрес данных ответа для задания отправки и ответа.</span><span class="sxs-lookup"><span data-stu-id="0e820-132">Contains the URL to the reply data of an upload-reply job.</span></span> <span data-ttu-id="0e820-133">Включите этот заголовок в окончательный ответ фрагмента после завершения передачи и получения ответа от серверного приложения, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="0e820-133">Include this header in the final fragment response after the upload is complete and you receive a response from the server application, if applicable.</span></span>

<span data-ttu-id="0e820-134">Используйте заголовок Content-Range из запроса фрагмента, чтобы определить, завершена ли передача.</span><span class="sxs-lookup"><span data-stu-id="0e820-134">Use the Content-Range header from the Fragment request to determine whether the upload is complete.</span></span> <span data-ttu-id="0e820-135">Отправка завершается, если конечное смещение значения диапазона равно значению общей длины минус единица.</span><span class="sxs-lookup"><span data-stu-id="0e820-135">The upload is complete if the end offset of the range value equals the total-length value minus one.</span></span>

<span data-ttu-id="0e820-136">Сервер BITS отправляет файл отправки в серверное приложение после того, как он определит, что передача завершена.</span><span class="sxs-lookup"><span data-stu-id="0e820-136">The BITS server posts the upload file to the server application after it determines the upload is complete.</span></span> <span data-ttu-id="0e820-137">Серверное приложение обрабатывает файл и создает ответ.</span><span class="sxs-lookup"><span data-stu-id="0e820-137">The server application processes the file and generates the reply.</span></span> <span data-ttu-id="0e820-138">Сервер BITS задает для параметра BITS-Reply-URL URL-адрес файла ответов из серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="0e820-138">The BITS server sets the value of BITS-Reply-URL to the URL of the reply file from the server application.</span></span>

</dd> <dt>

<span data-ttu-id="0e820-139"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Длина содержимого</span><span class="sxs-lookup"><span data-stu-id="0e820-139"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="0e820-140">Замените length числом байтов, включаемых в текст ответа.</span><span class="sxs-lookup"><span data-stu-id="0e820-140">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="0e820-141">Требуется длина содержимого, даже если текст ответа не содержит содержимого.</span><span class="sxs-lookup"><span data-stu-id="0e820-141">Content-Length is required, even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="0e820-142"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-code</span><span class="sxs-lookup"><span data-stu-id="0e820-142"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="0e820-143">Замените Error-code шестнадцатеричным числом, представляющим значение HRESULT, связанное с ошибкой на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="0e820-143">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="0e820-144">Включайте этот заголовок только в том случае, если код причины не 200 или 201.</span><span class="sxs-lookup"><span data-stu-id="0e820-144">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="0e820-145"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-ошибка-контекст</span><span class="sxs-lookup"><span data-stu-id="0e820-145"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="0e820-146">Replace Error-context с шестнадцатеричным числом, представляющим контекст, в котором произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="0e820-146">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="0e820-147">Укажите шестнадцатеричное число для [**\_ \_ \_ удаленного \_ файла контекста ошибки BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5), если сервер сгенерировал ошибку.</span><span class="sxs-lookup"><span data-stu-id="0e820-147">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="0e820-148">В противном случае укажите шестнадцатеричное число для **\_ \_ \_ удаленного \_ приложения с контекстом ошибки BG** (0x7), если ошибка была создана приложением, куда передается файл передачи.</span><span class="sxs-lookup"><span data-stu-id="0e820-148">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="0e820-149">Включайте этот заголовок только в том случае, если код причины не 200 или 201.</span><span class="sxs-lookup"><span data-stu-id="0e820-149">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e820-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e820-150">Remarks</span></span>

<span data-ttu-id="0e820-151">Если сеанс предназначен для задания отправки и ответа, может возникнуть задержка до того, как клиент получит окончательное **подтверждение ответа фрагмента** .</span><span class="sxs-lookup"><span data-stu-id="0e820-151">If the session is for an upload-reply job, there may be a delay before the client receives the final **Ack for Fragment** response.</span></span> <span data-ttu-id="0e820-152">Продолжительность задержки зависит от времени, в течение которого серверное приложение (приложение, на которое сервер отправляет файл отправки) создает ответ.</span><span class="sxs-lookup"><span data-stu-id="0e820-152">The length of the delay depends on the amount of time the server application (application to which the server posts the upload file) takes to generate the reply.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e820-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e820-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e820-154">**Создание сеанса**</span><span class="sxs-lookup"><span data-stu-id="0e820-154">**Create-Session**</span></span>](create-session.md)
</dt> <dt>

[<span data-ttu-id="0e820-155">**Fragment**</span><span class="sxs-lookup"><span data-stu-id="0e820-155">**Fragment**</span></span>](fragment.md)
</dt> </dl>

 

 





