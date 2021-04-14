---
title: Коды состояния HTTP (WinInet. h)
description: В следующей таблице содержатся константы и соответствующие значения для кодов состояния HTTP, возвращаемых серверами в Интернете.
ms.assetid: 28a5e889-c8f3-4996-a1ca-c48866fa59d7
topic_type:
- apiref
api_name:
- HTTP_STATUS_CONTINUE
- HTTP_STATUS_SWITCH_PROTOCOLS
- HTTP_STATUS_OK
- HTTP_STATUS_CREATED
- HTTP_STATUS_ACCEPTED
- HTTP_STATUS_PARTIAL
- HTTP_STATUS_NO_CONTENT
- HTTP_STATUS_RESET_CONTENT
- HTTP_STATUS_PARTIAL_CONTENT
- HTTP_STATUS_AMBIGUOUS
- HTTP_STATUS_MOVED
- HTTP_STATUS_REDIRECT
- HTTP_STATUS_REDIRECT_METHOD
- HTTP_STATUS_NOT_MODIFIED
- HTTP_STATUS_USE_PROXY
- HTTP_STATUS_REDIRECT_KEEP_VERB
- HTTP_STATUS_BAD_REQUEST
- HTTP_STATUS_DENIED
- HTTP_STATUS_PAYMENT_REQ
- HTTP_STATUS_FORBIDDEN
- HTTP_STATUS_NOT_FOUND
- HTTP_STATUS_BAD_METHOD
- HTTP_STATUS_NONE_ACCEPTABLE
- HTTP_STATUS_PROXY_AUTH_REQ
- HTTP_STATUS_REQUEST_TIMEOUT
- HTTP_STATUS_CONFLICT
- HTTP_STATUS_GONE
- HTTP_STATUS_LENGTH_REQUIRED
- HTTP_STATUS_PRECOND_FAILED
- HTTP_STATUS_REQUEST_TOO_LARGE
- HTTP_STATUS_URI_TOO_LONG
- HTTP_STATUS_UNSUPPORTED_MEDIA
- HTTP_STATUS_RETRY_WITH
- HTTP_STATUS_SERVER_ERROR
- HTTP_STATUS_NOT_SUPPORTED
- HTTP_STATUS_BAD_GATEWAY
- HTTP_STATUS_SERVICE_UNAVAIL
- HTTP_STATUS_GATEWAY_TIMEOUT
- HTTP_STATUS_VERSION_NOT_SUP
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6933617b0488e059c029dd783af238a3ddbb3ecb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416100"
---
# <a name="http-status-codes-winineth"></a><span data-ttu-id="8ae19-103">Коды состояния HTTP (WinInet. h)</span><span class="sxs-lookup"><span data-stu-id="8ae19-103">HTTP Status Codes (Wininet.h)</span></span>

<span data-ttu-id="8ae19-104">В следующей таблице содержатся константы и соответствующие значения для кодов состояния HTTP, возвращаемых серверами в Интернете.</span><span class="sxs-lookup"><span data-stu-id="8ae19-104">The following table contains the constants and corresponding values for the HTTP status codes returned by servers on the Internet.</span></span>

<dl> <dt>

<span data-ttu-id="8ae19-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**\_продолжение состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="8ae19-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-106">100</span><span class="sxs-lookup"><span data-stu-id="8ae19-106">100</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-107">Запрос можно продолжить.</span><span class="sxs-lookup"><span data-stu-id="8ae19-107">The request can be continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_ \_ протоколы переключения состояния HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="8ae19-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP\_STATUS\_SWITCH\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-109">101</span><span class="sxs-lookup"><span data-stu-id="8ae19-109">101</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-110">Сервер переключил протоколы в заголовке обновления.</span><span class="sxs-lookup"><span data-stu-id="8ae19-110">The server has switched protocols in an upgrade header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**состояние HTTP " \_ \_ ОК"**</span><span class="sxs-lookup"><span data-stu-id="8ae19-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP\_STATUS\_OK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-112">200</span><span class="sxs-lookup"><span data-stu-id="8ae19-112">200</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-113">Запрос успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="8ae19-113">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**\_состояние HTTP \_ создано**</span><span class="sxs-lookup"><span data-stu-id="8ae19-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP\_STATUS\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-115">201</span><span class="sxs-lookup"><span data-stu-id="8ae19-115">201</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-116">Запрос был выполнен и привел к созданию нового ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ae19-116">The request has been fulfilled and resulted in the creation of a new resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_состояние HTTP \_ принято**</span><span class="sxs-lookup"><span data-stu-id="8ae19-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP\_STATUS\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-118">202</span><span class="sxs-lookup"><span data-stu-id="8ae19-118">202</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-119">Запрос принят на обработку, но обработка не завершена.</span><span class="sxs-lookup"><span data-stu-id="8ae19-119">The request has been accepted for processing, but the processing has not been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**\_ \_ частичное состояние HTTP**</span><span class="sxs-lookup"><span data-stu-id="8ae19-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP\_STATUS\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-121">203</span><span class="sxs-lookup"><span data-stu-id="8ae19-121">203</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-122">Возвращенные метаданные в заголовке сущности не являются определяющим набором, доступным на сервере-источнике.</span><span class="sxs-lookup"><span data-stu-id="8ae19-122">The returned meta information in the entity-header is not the definitive set available from the origin server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**\_состояние HTTP \_ без \_ содержимого**</span><span class="sxs-lookup"><span data-stu-id="8ae19-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP\_STATUS\_NO\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-124">204</span><span class="sxs-lookup"><span data-stu-id="8ae19-124">204</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-125">Сервер выполнил запрос, но нет новых данных для отправки обратно.</span><span class="sxs-lookup"><span data-stu-id="8ae19-125">The server has fulfilled the request, but there is no new information to send back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_ \_ содержимое сброса состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="8ae19-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP\_STATUS\_RESET\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-127">205</span><span class="sxs-lookup"><span data-stu-id="8ae19-127">205</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-128">Запрос завершен, и клиентская программа должна сбросить представление документа, вызвавшее отправку запроса, чтобы позволить пользователю легко инициировать другое Входное действие.</span><span class="sxs-lookup"><span data-stu-id="8ae19-128">The request has been completed, and the client program should reset the document view that caused the request to be sent to allow the user to easily initiate another input action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ частичное содержимое состояния HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="8ae19-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP\_STATUS\_PARTIAL\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-130">206</span><span class="sxs-lookup"><span data-stu-id="8ae19-130">206</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-131">Сервер выполнил частичный запрос GET для ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ae19-131">The server has fulfilled the partial GET request for the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-132"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_неоднозначное состояние HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="8ae19-132"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP\_STATUS\_AMBIGUOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-133">300</span><span class="sxs-lookup"><span data-stu-id="8ae19-133">300</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-134">Серверу не удалось определить возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="8ae19-134">The server couldn't decide what to return.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-135"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_состояние HTTP \_ перемещено**</span><span class="sxs-lookup"><span data-stu-id="8ae19-135"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP\_STATUS\_MOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-136">301</span><span class="sxs-lookup"><span data-stu-id="8ae19-136">301</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-137">Запрошенному ресурсу был назначен новый постоянный универсальный код ресурса (URI), и все будущие ссылки на этот ресурс следует выполнять с помощью одного из возвращенных URI.</span><span class="sxs-lookup"><span data-stu-id="8ae19-137">The requested resource has been assigned to a new permanent URI (Uniform Resource Identifier), and any future references to this resource should be done using one of the returned URIs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-138"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**\_Перенаправление состояния HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="8ae19-138"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP\_STATUS\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-139">302</span><span class="sxs-lookup"><span data-stu-id="8ae19-139">302</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-140">Запрошенный ресурс временно находится под другим URI (универсальный идентификатор ресурса).</span><span class="sxs-lookup"><span data-stu-id="8ae19-140">The requested resource resides temporarily under a different URI (Uniform Resource Identifier).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-141"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_ \_ метод ПЕРЕНАПРАВЛЕНИЯ HTTP-состояния \_**</span><span class="sxs-lookup"><span data-stu-id="8ae19-141"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP\_STATUS\_REDIRECT\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-142">303</span><span class="sxs-lookup"><span data-stu-id="8ae19-142">303</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-143">Ответ на запрос можно найти по другому универсальному коду ресурса (URI), и его следует получить с помощью команды GET HTTP для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ae19-143">The response to the request can be found under a different URI (Uniform Resource Identifier) and should be retrieved using a GET HTTP verb on that resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-144"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_состояние HTTP \_ не \_ изменено**</span><span class="sxs-lookup"><span data-stu-id="8ae19-144"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP\_STATUS\_NOT\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-145">304</span><span class="sxs-lookup"><span data-stu-id="8ae19-145">304</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-146">Запрошенный ресурс не был изменен.</span><span class="sxs-lookup"><span data-stu-id="8ae19-146">The requested resource has not been modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-147"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**\_ \_ использование \_ прокси-сервера состояния HTTP**</span><span class="sxs-lookup"><span data-stu-id="8ae19-147"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP\_STATUS\_USE\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-148">305</span><span class="sxs-lookup"><span data-stu-id="8ae19-148">305</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-149">Доступ к запрошенному ресурсу должен осуществляться через прокси-сервер, заданный в поле Location.</span><span class="sxs-lookup"><span data-stu-id="8ae19-149">The requested resource must be accessed through the proxy given by the location field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-150"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_команда сохранения состояния HTTP- \_ перенаправления \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8ae19-150"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP\_STATUS\_REDIRECT\_KEEP\_VERB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-151">307</span><span class="sxs-lookup"><span data-stu-id="8ae19-151">307</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-152">Перенаправленный запрос сохраняет ту же команду HTTP.</span><span class="sxs-lookup"><span data-stu-id="8ae19-152">The redirected request keeps the same HTTP verb.</span></span> <span data-ttu-id="8ae19-153">Поведение HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="8ae19-153">HTTP/1.1 behavior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-154"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_ \_ неправильный запрос состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="8ae19-154"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP\_STATUS\_BAD\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-155">400</span><span class="sxs-lookup"><span data-stu-id="8ae19-155">400</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-156">Серверу не удалось обработать запрос из-за недопустимого синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="8ae19-156">The request could not be processed by the server due to invalid syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-157"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**состояние HTTP " \_ \_ отклонено"**</span><span class="sxs-lookup"><span data-stu-id="8ae19-157"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP\_STATUS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-158">401</span><span class="sxs-lookup"><span data-stu-id="8ae19-158">401</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-159">Запрошенный ресурс требует проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ae19-159">The requested resource requires user authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-160"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**\_ \_ Заявка на оплату состояния HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="8ae19-160"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP\_STATUS\_PAYMENT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-161">402</span><span class="sxs-lookup"><span data-stu-id="8ae19-161">402</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-162">В настоящее время не реализовано в протоколе HTTP.</span><span class="sxs-lookup"><span data-stu-id="8ae19-162">Not currently implemented in the HTTP protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-163"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**\_состояние HTTP \_ запрещено**</span><span class="sxs-lookup"><span data-stu-id="8ae19-163"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP\_STATUS\_FORBIDDEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-164">403</span><span class="sxs-lookup"><span data-stu-id="8ae19-164">403</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-165">Сервер понял запрос, но отказывается его выполнить.</span><span class="sxs-lookup"><span data-stu-id="8ae19-165">The server understood the request, but is refusing to fulfill it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-166"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_состояние HTTP \_ не \_ Найдено**</span><span class="sxs-lookup"><span data-stu-id="8ae19-166"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP\_STATUS\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-167">404</span><span class="sxs-lookup"><span data-stu-id="8ae19-167">404</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-168">Сервер не нашел ничего, соответствующего запрошенному URI (универсальный идентификатор ресурса).</span><span class="sxs-lookup"><span data-stu-id="8ae19-168">The server has not found anything matching the requested URI (Uniform Resource Identifier).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-169"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**\_ \_ неправильный метод состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="8ae19-169"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP\_STATUS\_BAD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-170">405</span><span class="sxs-lookup"><span data-stu-id="8ae19-170">405</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-171">Используемая команда HTTP не разрешена.</span><span class="sxs-lookup"><span data-stu-id="8ae19-171">The HTTP verb used is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-172"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**состояние HTTP " \_ \_ нет \_ допустимого"**</span><span class="sxs-lookup"><span data-stu-id="8ae19-172"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP\_STATUS\_NONE\_ACCEPTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-173">406</span><span class="sxs-lookup"><span data-stu-id="8ae19-173">406</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-174">Не найдены ответы, приемлемые для клиента.</span><span class="sxs-lookup"><span data-stu-id="8ae19-174">No responses acceptable to the client were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-175"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**\_состояние HTTP \_ \_ Проверка подлинности прокси \_**</span><span class="sxs-lookup"><span data-stu-id="8ae19-175"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP\_STATUS\_PROXY\_AUTH\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-176">407</span><span class="sxs-lookup"><span data-stu-id="8ae19-176">407</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-177">Требуется проверка подлинности прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="8ae19-177">Proxy authentication required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-178"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_ \_ время ожидания запроса состояния HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="8ae19-178"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP\_STATUS\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-179">408</span><span class="sxs-lookup"><span data-stu-id="8ae19-179">408</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-180">Истекло время ожидания запроса сервером.</span><span class="sxs-lookup"><span data-stu-id="8ae19-180">The server timed out waiting for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-181"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_конфликт состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="8ae19-181"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP\_STATUS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-182">409</span><span class="sxs-lookup"><span data-stu-id="8ae19-182">409</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-183">Не удалось выполнить запрос из-за конфликта с текущим состоянием ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ae19-183">The request could not be completed due to a conflict with the current state of the resource.</span></span> <span data-ttu-id="8ae19-184">Пользователю следует повторить отправку с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="8ae19-184">The user should resubmit with more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-185"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**\_состояние HTTP \_ пропала**</span><span class="sxs-lookup"><span data-stu-id="8ae19-185"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP\_STATUS\_GONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-186">410</span><span class="sxs-lookup"><span data-stu-id="8ae19-186">410</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-187">Запрошенный ресурс больше не доступен на сервере, и адрес пересылки неизвестен.</span><span class="sxs-lookup"><span data-stu-id="8ae19-187">The requested resource is no longer available at the server, and no forwarding address is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-188"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_ \_ требуется длина состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="8ae19-188"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP\_STATUS\_LENGTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-189">411</span><span class="sxs-lookup"><span data-stu-id="8ae19-189">411</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-190">Сервер отказывается принимать запрос без определенной длины содержимого.</span><span class="sxs-lookup"><span data-stu-id="8ae19-190">The server refuses to accept the request without a defined content length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-191"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**\_Ошибка HTTP Status \_ преконд \_**</span><span class="sxs-lookup"><span data-stu-id="8ae19-191"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP\_STATUS\_PRECOND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-192">412</span><span class="sxs-lookup"><span data-stu-id="8ae19-192">412</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-193">Предусловие, заданное в одном или нескольких полях заголовка запроса, выдает значение false при проверке на сервере.</span><span class="sxs-lookup"><span data-stu-id="8ae19-193">The precondition given in one or more of the request header fields evaluated to false when it was tested on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-194"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_ \_ \_ слишком \_ большой запрос состояния HTTP**</span><span class="sxs-lookup"><span data-stu-id="8ae19-194"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP\_STATUS\_REQUEST\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-195">413</span><span class="sxs-lookup"><span data-stu-id="8ae19-195">413</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-196">Сервер отказывается обработать запрос, так как сущность запроса больше, чем сервер готов или может обработать.</span><span class="sxs-lookup"><span data-stu-id="8ae19-196">The server is refusing to process a request because the request entity is larger than the server is willing or able to process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-197"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_ \_ \_ слишком \_ длинный URI состояния HTTP**</span><span class="sxs-lookup"><span data-stu-id="8ae19-197"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP\_STATUS\_URI\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-198">414</span><span class="sxs-lookup"><span data-stu-id="8ae19-198">414</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-199">Сервер отказывается обслуживать запрос, так как URI запроса (универсальный идентификатор ресурса) длиннее, чем сервер может интерпретироваться.</span><span class="sxs-lookup"><span data-stu-id="8ae19-199">The server is refusing to service the request because the request URI (Uniform Resource Identifier) is longer than the server is willing to interpret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-200"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**\_ \_ неподдерживаемый носитель состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="8ae19-200"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP\_STATUS\_UNSUPPORTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-201">415</span><span class="sxs-lookup"><span data-stu-id="8ae19-201">415</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-202">Сервер отказывается обслуживать запрос, так как сущность запроса имеет формат, не поддерживаемый запрошенным ресурсом для запрошенного метода.</span><span class="sxs-lookup"><span data-stu-id="8ae19-202">The server is refusing to service the request because the entity of the request is in a format not supported by the requested resource for the requested method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-203"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**\_Повтор состояния HTTP \_ \_ с**</span><span class="sxs-lookup"><span data-stu-id="8ae19-203"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP\_STATUS\_RETRY\_WITH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-204">449</span><span class="sxs-lookup"><span data-stu-id="8ae19-204">449</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-205">После выполнения соответствующего действия запрос должен быть выполнен повторно.</span><span class="sxs-lookup"><span data-stu-id="8ae19-205">The request should be retried after doing the appropriate action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-206"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_ \_ Ошибка сервера состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="8ae19-206"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP\_STATUS\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-207">500</span><span class="sxs-lookup"><span data-stu-id="8ae19-207">500</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-208">Сервер обнаружил непредвиденное условие, препятствующее выполнению запроса.</span><span class="sxs-lookup"><span data-stu-id="8ae19-208">The server encountered an unexpected condition that prevented it from fulfilling the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-209"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_состояние HTTP \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="8ae19-209"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP\_STATUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-210">501</span><span class="sxs-lookup"><span data-stu-id="8ae19-210">501</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-211">Сервер не поддерживает функции, необходимые для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="8ae19-211">The server does not support the functionality required to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-212"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**\_ \_ неправильный шлюз состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="8ae19-212"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP\_STATUS\_BAD\_GATEWAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-213">502</span><span class="sxs-lookup"><span data-stu-id="8ae19-213">502</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-214">Сервер, выполняющий роль шлюза или прокси-сервера, получил недопустимый ответ от вышестоящего сервера, к которому он обращался при попытке выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="8ae19-214">The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-215"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**недоступный для \_ службы состояния HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8ae19-215"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP\_STATUS\_SERVICE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-216">503</span><span class="sxs-lookup"><span data-stu-id="8ae19-216">503</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-217">Служба временно перегружена.</span><span class="sxs-lookup"><span data-stu-id="8ae19-217">The service is temporarily overloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-218"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**\_ \_ время ожидания шлюза состояния HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="8ae19-218"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP\_STATUS\_GATEWAY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-219">504</span><span class="sxs-lookup"><span data-stu-id="8ae19-219">504</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-220">При выполнении запроса было превышено время ожидания шлюза.</span><span class="sxs-lookup"><span data-stu-id="8ae19-220">The request was timed out waiting for a gateway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ae19-221"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_версия состояния \_ HTTP \_ не \_ SUP**</span><span class="sxs-lookup"><span data-stu-id="8ae19-221"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP\_STATUS\_VERSION\_NOT\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ae19-222">505</span><span class="sxs-lookup"><span data-stu-id="8ae19-222">505</span></span>
</dt> <dt>



<span data-ttu-id="8ae19-223">Сервер не поддерживает или отказывается поддерживать версию протокола HTTP, которая использовалась в сообщении запроса.</span><span class="sxs-lookup"><span data-stu-id="8ae19-223">The server does not support, or refuses to support, the HTTP protocol version that was used in the request message.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ae19-224">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ae19-224">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8ae19-225">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="8ae19-225">WinINet does not support server implementations.</span></span> <span data-ttu-id="8ae19-226">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="8ae19-226">In addition, it should not be used from a service.</span></span> <span data-ttu-id="8ae19-227">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="8ae19-227">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ae19-228">Требования</span><span class="sxs-lookup"><span data-stu-id="8ae19-228">Requirements</span></span>



| <span data-ttu-id="8ae19-229">Требование</span><span class="sxs-lookup"><span data-stu-id="8ae19-229">Requirement</span></span> | <span data-ttu-id="8ae19-230">Значение</span><span class="sxs-lookup"><span data-stu-id="8ae19-230">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae19-231">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ae19-231">Minimum supported client</span></span><br/> | <span data-ttu-id="8ae19-232">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8ae19-232">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8ae19-233">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ae19-233">Minimum supported server</span></span><br/> | <span data-ttu-id="8ae19-234">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8ae19-234">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8ae19-235">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8ae19-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ae19-236"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ae19-236"><dt>Wininet.h</dt></span></span> </dl> |



 

