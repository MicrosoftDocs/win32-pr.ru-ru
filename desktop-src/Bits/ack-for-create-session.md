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
ms.openlocfilehash: 2d978ec4c5693a5087734975c412b999ed7d5890
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "105654389"
---
# <a name="ack-for-create-session"></a><span data-ttu-id="a00ce-104">Подтверждение для Create-Session</span><span class="sxs-lookup"><span data-stu-id="a00ce-104">Ack for Create-Session</span></span>

<span data-ttu-id="a00ce-105">Используйте **подтверждение для пакета создания сеанса** , чтобы подтвердить запрос на [**Создание сеанса**](create-session.md) клиента.</span><span class="sxs-lookup"><span data-stu-id="a00ce-105">Use the **Ack for Create-Session** packet to acknowledge the client's [**Create-Session**](create-session.md) request.</span></span>

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

## <a name="headers"></a><span data-ttu-id="a00ce-106">Заголовки</span><span class="sxs-lookup"><span data-stu-id="a00ce-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="a00ce-107"><span id="reason-code"></span><span id="REASON-CODE"></span>код причины</span><span class="sxs-lookup"><span data-stu-id="a00ce-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="a00ce-108">Замените код причины кодом причины HTTP.</span><span class="sxs-lookup"><span data-stu-id="a00ce-108">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="a00ce-109">В следующей таблице показаны типичные коды причин ответа на запрос [**создания сеанса**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="a00ce-109">The following table shows the typical reason codes for a response to a [**Create-Session**](create-session.md) request.</span></span> <span data-ttu-id="a00ce-110">Список кодов причин HTTP см. в [документе RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="a00ce-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>



| <span data-ttu-id="a00ce-111">Код причины</span><span class="sxs-lookup"><span data-stu-id="a00ce-111">Reason code</span></span>    | <span data-ttu-id="a00ce-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a00ce-112">Description</span></span>                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a00ce-113">200</span><span class="sxs-lookup"><span data-stu-id="a00ce-113">200</span></span><br/> | <span data-ttu-id="a00ce-114">Все в порядке.</span><span class="sxs-lookup"><span data-stu-id="a00ce-114">OK.</span></span> <span data-ttu-id="a00ce-115">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="a00ce-115">The request was successful.</span></span><br/>                                          |
| <span data-ttu-id="a00ce-116">201</span><span class="sxs-lookup"><span data-stu-id="a00ce-116">201</span></span><br/> | <span data-ttu-id="a00ce-117">Создан.</span><span class="sxs-lookup"><span data-stu-id="a00ce-117">Created.</span></span> <span data-ttu-id="a00ce-118">Сеанс создан.</span><span class="sxs-lookup"><span data-stu-id="a00ce-118">The session was created.</span></span><br/>                                        |
| <span data-ttu-id="a00ce-119">403</span><span class="sxs-lookup"><span data-stu-id="a00ce-119">403</span></span><br/> | <span data-ttu-id="a00ce-120">Запрещено.</span><span class="sxs-lookup"><span data-stu-id="a00ce-120">Forbidden.</span></span> <span data-ttu-id="a00ce-121">Пользователю не разрешено отправлять файлы по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="a00ce-121">The user is not allowed to upload files to the specified URL.</span></span><br/> |
| <span data-ttu-id="a00ce-122">404</span><span class="sxs-lookup"><span data-stu-id="a00ce-122">404</span></span><br/> | <span data-ttu-id="a00ce-123">Не найден.</span><span class="sxs-lookup"><span data-stu-id="a00ce-123">Not Found.</span></span> <span data-ttu-id="a00ce-124">Указанный URL-адрес не существует.</span><span class="sxs-lookup"><span data-stu-id="a00ce-124">The specified URL does not exist.</span></span><br/>                             |
| <span data-ttu-id="a00ce-125">409</span><span class="sxs-lookup"><span data-stu-id="a00ce-125">409</span></span><br/> | <span data-ttu-id="a00ce-126">Конфликт.</span><span class="sxs-lookup"><span data-stu-id="a00ce-126">Conflict.</span></span> <span data-ttu-id="a00ce-127">Файл существует на сервере и не может быть перезаписан.</span><span class="sxs-lookup"><span data-stu-id="a00ce-127">The file exists on the server and cannot be overwritten.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="a00ce-128"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Описание причины</span><span class="sxs-lookup"><span data-stu-id="a00ce-128"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="a00ce-129">Замените Reason — Description на HTTP-описание, связанное с кодом причины.</span><span class="sxs-lookup"><span data-stu-id="a00ce-129">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="a00ce-130">Например, задайте для параметра reason-Description значение ОК, если причина — код 200.</span><span class="sxs-lookup"><span data-stu-id="a00ce-130">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="a00ce-131"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span><span class="sxs-lookup"><span data-stu-id="a00ce-131"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="a00ce-132">Определяет этот пакет ответа как пакет подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a00ce-132">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="a00ce-133"><span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS — протокол</span><span class="sxs-lookup"><span data-stu-id="a00ce-133"><span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-Protocol</span></span>
</dt> <dd>

<span data-ttu-id="a00ce-134">Строковый идентификатор GUID, определяющий протокол, который сервер хочет использовать для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="a00ce-134">String GUID that identifies the protocol that the server wants to use for this session.</span></span> <span data-ttu-id="a00ce-135">Замените {GUID} идентификатором протокола из списка протоколов, включенных клиентом в запрос на [**Создание сеанса**](create-session.md) . в заголовке BITS-Supported-Protocol содержится список.</span><span class="sxs-lookup"><span data-stu-id="a00ce-135">Replace {guid} with the protocol identifier from the list of protocols the client includes in the [**Create-Session**](create-session.md) request; the BITS-Supported-Protocol header contains the list.</span></span> <span data-ttu-id="a00ce-136">Включайте этот заголовок только в том случае, если код причины — 200 или 201.</span><span class="sxs-lookup"><span data-stu-id="a00ce-136">Include this header only if the reason-code is 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="a00ce-137"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS — Session-ID</span><span class="sxs-lookup"><span data-stu-id="a00ce-137"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="a00ce-138">Строковый идентификатор GUID, обозначающий этот сеанс с клиентом.</span><span class="sxs-lookup"><span data-stu-id="a00ce-138">String GUID that identifies this session to the client.</span></span> <span data-ttu-id="a00ce-139">Замените {GUID} идентификатором сеанса, который клиент отправляет во всех последующих пакетах запроса.</span><span class="sxs-lookup"><span data-stu-id="a00ce-139">Replace {guid} with the session identifier that the client sends in all subsequent request packets.</span></span>

<span data-ttu-id="a00ce-140">Служба BITS использует идентификатор GUID для задания сеанса, но вы можете использовать любую строку, допустимую в HTTP, до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="a00ce-140">BITS uses a GUID to identify the session, but you can use any HTTP-legal string up to 100 characters.</span></span>

</dd> <dt>

<span data-ttu-id="a00ce-141"><span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-Host-ID</span><span class="sxs-lookup"><span data-stu-id="a00ce-141"><span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-Host-Id</span></span>
</dt> <dd>

<span data-ttu-id="a00ce-142">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a00ce-142">Optional.</span></span> <span data-ttu-id="a00ce-143">Включайте этот заголовок, только если задано [свойство расширения IIS BITS](bits-iis-extension-properties.md)битшостид.</span><span class="sxs-lookup"><span data-stu-id="a00ce-143">Include this header only if the [BITS IIS extension property](bits-iis-extension-properties.md), BITSHostId, is set.</span></span> <span data-ttu-id="a00ce-144">Замените Публичостнаме на имя сервера или IP-адрес из свойства Битшостид.</span><span class="sxs-lookup"><span data-stu-id="a00ce-144">Replace PublicHostName with the server name or IP address from the BITSHostId property.</span></span>

<span data-ttu-id="a00ce-145">Клиент должен заменить серверную часть удаленного URL-адреса во всех последующих пакетах.</span><span class="sxs-lookup"><span data-stu-id="a00ce-145">The client must replace the server portion of the remote-URL on all subsequent packets.</span></span> <span data-ttu-id="a00ce-146">Если клиент не указал это имя узла в последующих пакетах, это может привести к повторному запуску задания на другом сервере в ферме, при этом на предыдущем сервере будет размещен файл частичной передачи.</span><span class="sxs-lookup"><span data-stu-id="a00ce-146">If the client does not specify this host name on subsequent packets, it is possible that the job will begin again on another server in the farm, leaving a partial upload file on the previous server.</span></span>

</dd> <dt>

<span data-ttu-id="a00ce-147"><span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-Host-ID — резервное время ожидания</span><span class="sxs-lookup"><span data-stu-id="a00ce-147"><span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-Host-Id-Fallback-Timeout</span></span>
</dt> <dd>

<span data-ttu-id="a00ce-148">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a00ce-148">Optional.</span></span> <span data-ttu-id="a00ce-149">Включайте этот заголовок только в том случае, если указан заголовок BITS-Host-ID.</span><span class="sxs-lookup"><span data-stu-id="a00ce-149">Include this header only if the BITS-Host-Id header is specified.</span></span> <span data-ttu-id="a00ce-150">Замените время ожидания значением времени ожидания из свойства Битшостидфаллбакктимеаут.</span><span class="sxs-lookup"><span data-stu-id="a00ce-150">Replace Timeout with the time-out value from the BITSHostIdFallbackTimeout property.</span></span> <span data-ttu-id="a00ce-151">Свойство Битшостидфаллбакктимеаут является одним из [свойств расширения IIS BITS](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="a00ce-151">The BITSHostIdFallbackTimeout property is one of the [BITS IIS extension properties](bits-iis-extension-properties.md).</span></span>

<span data-ttu-id="a00ce-152">Клиент использует период времени ожидания, чтобы определить, как долго будет пытаться подключиться к серверу, указанному в заголовке BITS-Host-ID, прежде чем вернуть имя узла, указанное в имени удаленного файла задания.</span><span class="sxs-lookup"><span data-stu-id="a00ce-152">The client uses the time-out period to determine how long it tries to reconnect to the server name specified in the BITS-Host-Id header before reverting to the host name specified in the remote file name of the job.</span></span> <span data-ttu-id="a00ce-153">Таймер начинается, когда службе BITS не удается подключиться к серверу BITS-Host-ID.</span><span class="sxs-lookup"><span data-stu-id="a00ce-153">The timer begins when BITS is unable to connect to the BITS-Host-Id server.</span></span> <span data-ttu-id="a00ce-154">Таймер сбрасывается при восстановлении соединения с сервером.</span><span class="sxs-lookup"><span data-stu-id="a00ce-154">The timer is reset when a connection to the server is restored.</span></span> <span data-ttu-id="a00ce-155">Если интервал времени ожидания не указан, клиент никогда не возвращается к имени узла, указанному в имени удаленного файла.</span><span class="sxs-lookup"><span data-stu-id="a00ce-155">If a time-out period is not specified, the client never reverts to the host name specified in the remote file name.</span></span>

</dd> <dt>

<span data-ttu-id="a00ce-156"><span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding</span><span class="sxs-lookup"><span data-stu-id="a00ce-156"><span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding</span></span>
</dt> <dd>

<span data-ttu-id="a00ce-157">Определяет схему кодирования, используемую для фрагментов, отправляемых на сервер.</span><span class="sxs-lookup"><span data-stu-id="a00ce-157">Identifies the encoding scheme to use on the fragments sent to the server.</span></span> <span data-ttu-id="a00ce-158">Пакет фрагмента содержит закодированный фрагмент в тексте пакета.</span><span class="sxs-lookup"><span data-stu-id="a00ce-158">The Fragment packet contains the encoded fragment in the body of the packet.</span></span> <span data-ttu-id="a00ce-159">Серверу BITS требуется кодировка удостоверений (открытый текст).</span><span class="sxs-lookup"><span data-stu-id="a00ce-159">The BITS server requires Identity encoding (plaintext).</span></span> <span data-ttu-id="a00ce-160">Включайте этот заголовок только в том случае, если код причины — 200 или 201.</span><span class="sxs-lookup"><span data-stu-id="a00ce-160">Include this header only if the Reason-code is 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="a00ce-161"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Длина содержимого</span><span class="sxs-lookup"><span data-stu-id="a00ce-161"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="a00ce-162">Замените length числом байтов, включаемых в текст ответа.</span><span class="sxs-lookup"><span data-stu-id="a00ce-162">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="a00ce-163">Требуется, даже если текст ответа не содержит содержимого.</span><span class="sxs-lookup"><span data-stu-id="a00ce-163">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="a00ce-164"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-code</span><span class="sxs-lookup"><span data-stu-id="a00ce-164"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="a00ce-165">Замените Error-code шестнадцатеричным числом, представляющим значение HRESULT, связанное с ошибкой на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="a00ce-165">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="a00ce-166">Включайте этот заголовок, только если код причины не 200 или 201.</span><span class="sxs-lookup"><span data-stu-id="a00ce-166">Include this header only if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="a00ce-167"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-ошибка-контекст</span><span class="sxs-lookup"><span data-stu-id="a00ce-167"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="a00ce-168">Replace Error-context с шестнадцатеричным числом, представляющим контекст, в котором произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="a00ce-168">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="a00ce-169">Укажите шестнадцатеричное число для [**\_ \_ \_ удаленного \_ файла контекста ошибки BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5), если сервер сгенерировал ошибку.</span><span class="sxs-lookup"><span data-stu-id="a00ce-169">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="a00ce-170">В противном случае укажите шестнадцатеричное число для **\_ \_ \_ удаленного \_ приложения с контекстом ошибки BG** (0x7), если ошибка была создана приложением, куда передается файл передачи.</span><span class="sxs-lookup"><span data-stu-id="a00ce-170">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="a00ce-171">Включайте этот заголовок только в том случае, если код причины не 200 или 201.</span><span class="sxs-lookup"><span data-stu-id="a00ce-171">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="a00ce-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a00ce-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a00ce-173">**Создание сеанса**</span><span class="sxs-lookup"><span data-stu-id="a00ce-173">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 





