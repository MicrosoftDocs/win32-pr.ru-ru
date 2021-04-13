---
description: Эти константы и соответствующие значения указывают коды состояния HTTP, возвращаемые серверами в Интернете.
ms.assetid: 3de6a35d-41e9-4fce-ab92-e970c7c07e55
title: Коды состояния HTTP (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcf4103cdc382bd5ab0d582fe99212083e2780ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265189"
---
# <a name="http-status-codes-winhttph"></a><span data-ttu-id="fe01f-103">Коды состояния HTTP (WinHTTP. h)</span><span class="sxs-lookup"><span data-stu-id="fe01f-103">HTTP Status Codes (Winhttp.h)</span></span>

<span data-ttu-id="fe01f-104">Эти константы и соответствующие значения указывают коды состояния HTTP, возвращаемые серверами в Интернете.</span><span class="sxs-lookup"><span data-stu-id="fe01f-104">These constants and corresponding values indicate HTTP status codes returned by servers on the Internet.</span></span>

<dl> <dt>

<span data-ttu-id="fe01f-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**\_продолжение состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="fe01f-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-106">100</span><span class="sxs-lookup"><span data-stu-id="fe01f-106">100</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-107">Запрос можно продолжить.</span><span class="sxs-lookup"><span data-stu-id="fe01f-107">The request can be continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_ \_ протоколы переключения состояния HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fe01f-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP\_STATUS\_SWITCH\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-109">101</span><span class="sxs-lookup"><span data-stu-id="fe01f-109">101</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-110">Сервер переключил протоколы в заголовке обновления.</span><span class="sxs-lookup"><span data-stu-id="fe01f-110">The server has switched protocols in an upgrade header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**состояние HTTP " \_ \_ ОК"**</span><span class="sxs-lookup"><span data-stu-id="fe01f-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP\_STATUS\_OK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-112">200</span><span class="sxs-lookup"><span data-stu-id="fe01f-112">200</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-113">Запрос успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="fe01f-113">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**\_состояние HTTP \_ создано**</span><span class="sxs-lookup"><span data-stu-id="fe01f-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP\_STATUS\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-115">201</span><span class="sxs-lookup"><span data-stu-id="fe01f-115">201</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-116">Запрос был выполнен и привел к созданию нового ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe01f-116">The request has been fulfilled and resulted in the creation of a new resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_состояние HTTP \_ принято**</span><span class="sxs-lookup"><span data-stu-id="fe01f-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP\_STATUS\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-118">202</span><span class="sxs-lookup"><span data-stu-id="fe01f-118">202</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-119">Запрос принят на обработку, но обработка не завершена.</span><span class="sxs-lookup"><span data-stu-id="fe01f-119">The request has been accepted for processing, but the processing has not been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**\_ \_ частичное состояние HTTP**</span><span class="sxs-lookup"><span data-stu-id="fe01f-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP\_STATUS\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-121">203</span><span class="sxs-lookup"><span data-stu-id="fe01f-121">203</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-122">Возвращенные метаданные в заголовке сущности не являются определяющим набором, доступным на исходном сервере.</span><span class="sxs-lookup"><span data-stu-id="fe01f-122">The returned meta information in the entity-header is not the definitive set available from the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**\_состояние HTTP \_ без \_ содержимого**</span><span class="sxs-lookup"><span data-stu-id="fe01f-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP\_STATUS\_NO\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-124">204</span><span class="sxs-lookup"><span data-stu-id="fe01f-124">204</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-125">Сервер выполнил запрос, но нет новых данных для отправки обратно.</span><span class="sxs-lookup"><span data-stu-id="fe01f-125">The server has fulfilled the request, but there is no new information to send back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_ \_ содержимое сброса состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="fe01f-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP\_STATUS\_RESET\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-127">205</span><span class="sxs-lookup"><span data-stu-id="fe01f-127">205</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-128">Запрос завершен, и клиентская программа должна сбросить представление документа, вызвавшее отправку запроса, чтобы позволить пользователю легко инициировать другое Входное действие.</span><span class="sxs-lookup"><span data-stu-id="fe01f-128">The request has been completed, and the client program should reset the document view that caused the request to be sent to allow the user to easily initiate another input action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ частичное содержимое состояния HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fe01f-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP\_STATUS\_PARTIAL\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-130">206</span><span class="sxs-lookup"><span data-stu-id="fe01f-130">206</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-131">Сервер выполнил частичный запрос GET для ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe01f-131">The server has fulfilled the partial GET request for the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-132"><span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**\_состояние HTTP \_ . \_ Множественное \_ состояние WEBDAV**</span><span class="sxs-lookup"><span data-stu-id="fe01f-132"><span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**HTTP\_STATUS\_WEBDAV\_MULTI\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-133">207</span><span class="sxs-lookup"><span data-stu-id="fe01f-133">207</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-134">Во время выполнения операции WebDAV в Интернете это указывает на несколько кодов состояния для одного ответа.</span><span class="sxs-lookup"><span data-stu-id="fe01f-134">During a World Wide Web Distributed Authoring and Versioning (WebDAV) operation, this indicates multiple status codes for a single response.</span></span> <span data-ttu-id="fe01f-135">Текст ответа содержит язык XML (XML), описывающий коды состояния.</span><span class="sxs-lookup"><span data-stu-id="fe01f-135">The response body contains Extensible Markup Language (XML) that describes the status codes.</span></span> <span data-ttu-id="fe01f-136">Дополнительные сведения см. в разделе [расширения HTTP для распределенной разработки](../webdav/webdav-portal.md).</span><span class="sxs-lookup"><span data-stu-id="fe01f-136">For more information, see [HTTP Extensions for Distributed Authoring](../webdav/webdav-portal.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-137"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_неоднозначное состояние HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fe01f-137"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP\_STATUS\_AMBIGUOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-138">300</span><span class="sxs-lookup"><span data-stu-id="fe01f-138">300</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-139">Запрошенный ресурс доступен в одном или нескольких расположениях.</span><span class="sxs-lookup"><span data-stu-id="fe01f-139">The requested resource is available at one or more locations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-140"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_состояние HTTP \_ перемещено**</span><span class="sxs-lookup"><span data-stu-id="fe01f-140"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP\_STATUS\_MOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-141">301</span><span class="sxs-lookup"><span data-stu-id="fe01f-141">301</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-142">Запрошенному ресурсу был назначен новый постоянный универсальный код ресурса (URI), и все будущие ссылки на этот ресурс следует выполнять с помощью одного из возвращенных URI.</span><span class="sxs-lookup"><span data-stu-id="fe01f-142">The requested resource has been assigned to a new permanent Uniform Resource Identifier (URI), and any future references to this resource should be done using one of the returned URIs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-143"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**\_Перенаправление состояния HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fe01f-143"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP\_STATUS\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-144">302</span><span class="sxs-lookup"><span data-stu-id="fe01f-144">302</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-145">Запрошенный ресурс временно находится под другим URI.</span><span class="sxs-lookup"><span data-stu-id="fe01f-145">The requested resource resides temporarily under a different URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-146"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_ \_ метод ПЕРЕНАПРАВЛЕНИЯ HTTP-состояния \_**</span><span class="sxs-lookup"><span data-stu-id="fe01f-146"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP\_STATUS\_REDIRECT\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-147">303</span><span class="sxs-lookup"><span data-stu-id="fe01f-147">303</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-148">Ответ на запрос можно найти по другому URI, и его следует получить с помощью [*команды GET HTTP*](glossary.md) для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe01f-148">The response to the request can be found under a different URI and should be retrieved using a GET [*HTTP verb*](glossary.md) on that resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-149"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_состояние HTTP \_ не \_ изменено**</span><span class="sxs-lookup"><span data-stu-id="fe01f-149"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP\_STATUS\_NOT\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-150">304</span><span class="sxs-lookup"><span data-stu-id="fe01f-150">304</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-151">Запрошенный ресурс не был изменен.</span><span class="sxs-lookup"><span data-stu-id="fe01f-151">The requested resource has not been modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-152"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**\_ \_ использование \_ прокси-сервера состояния HTTP**</span><span class="sxs-lookup"><span data-stu-id="fe01f-152"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP\_STATUS\_USE\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-153">305</span><span class="sxs-lookup"><span data-stu-id="fe01f-153">305</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-154">Доступ к запрошенному ресурсу должен осуществляться через прокси-сервер, заданный в поле Location.</span><span class="sxs-lookup"><span data-stu-id="fe01f-154">The requested resource must be accessed through the proxy given by the location field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-155"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_команда сохранения состояния HTTP- \_ перенаправления \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fe01f-155"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP\_STATUS\_REDIRECT\_KEEP\_VERB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-156">307</span><span class="sxs-lookup"><span data-stu-id="fe01f-156">307</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-157">Перенаправленный запрос сохраняет ту же [*команду HTTP*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fe01f-157">The redirected request keeps the same [*HTTP verb*](glossary.md).</span></span> <span data-ttu-id="fe01f-158">Поведение HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="fe01f-158">HTTP/1.1 behavior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-159"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_ \_ неправильный запрос состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="fe01f-159"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP\_STATUS\_BAD\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-160">400</span><span class="sxs-lookup"><span data-stu-id="fe01f-160">400</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-161">Серверу не удалось обработать запрос из-за недопустимого синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="fe01f-161">The request could not be processed by the server due to invalid syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-162"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**состояние HTTP " \_ \_ отклонено"**</span><span class="sxs-lookup"><span data-stu-id="fe01f-162"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP\_STATUS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-163">401</span><span class="sxs-lookup"><span data-stu-id="fe01f-163">401</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-164">Запрошенный ресурс требует проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="fe01f-164">The requested resource requires user authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-165"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**\_ \_ Заявка на оплату состояния HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fe01f-165"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP\_STATUS\_PAYMENT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-166">402</span><span class="sxs-lookup"><span data-stu-id="fe01f-166">402</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-167">Не реализовано в протоколе HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe01f-167">Not implemented in the HTTP protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-168"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**\_состояние HTTP \_ запрещено**</span><span class="sxs-lookup"><span data-stu-id="fe01f-168"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP\_STATUS\_FORBIDDEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-169">403</span><span class="sxs-lookup"><span data-stu-id="fe01f-169">403</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-170">Сервер понял запрос, но не может выполнить его.</span><span class="sxs-lookup"><span data-stu-id="fe01f-170">The server understood the request, but cannot fulfill it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-171"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_состояние HTTP \_ не \_ Найдено**</span><span class="sxs-lookup"><span data-stu-id="fe01f-171"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP\_STATUS\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-172">404</span><span class="sxs-lookup"><span data-stu-id="fe01f-172">404</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-173">Сервер не нашел ничего, что соответствует запрошенному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="fe01f-173">The server has not found anything that matches the requested URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-174"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**\_ \_ неправильный метод состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="fe01f-174"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP\_STATUS\_BAD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-175">405</span><span class="sxs-lookup"><span data-stu-id="fe01f-175">405</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-176">Используемая [*команда HTTP*](glossary.md) не разрешена.</span><span class="sxs-lookup"><span data-stu-id="fe01f-176">The [*HTTP verb*](glossary.md) used is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-177"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**состояние HTTP " \_ \_ нет \_ допустимого"**</span><span class="sxs-lookup"><span data-stu-id="fe01f-177"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP\_STATUS\_NONE\_ACCEPTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-178">406</span><span class="sxs-lookup"><span data-stu-id="fe01f-178">406</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-179">Не найдены ответы, приемлемые для клиента.</span><span class="sxs-lookup"><span data-stu-id="fe01f-179">No responses acceptable to the client were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-180"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**\_состояние HTTP \_ \_ Проверка подлинности прокси \_**</span><span class="sxs-lookup"><span data-stu-id="fe01f-180"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP\_STATUS\_PROXY\_AUTH\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-181">407</span><span class="sxs-lookup"><span data-stu-id="fe01f-181">407</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-182">Требуется проверка подлинности прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="fe01f-182">Proxy authentication required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-183"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_ \_ время ожидания запроса состояния HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fe01f-183"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP\_STATUS\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-184">408</span><span class="sxs-lookup"><span data-stu-id="fe01f-184">408</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-185">Истекло время ожидания запроса сервером.</span><span class="sxs-lookup"><span data-stu-id="fe01f-185">The server timed out waiting for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-186"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_конфликт состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="fe01f-186"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP\_STATUS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-187">409</span><span class="sxs-lookup"><span data-stu-id="fe01f-187">409</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-188">Не удалось выполнить запрос из-за конфликта с текущим состоянием ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe01f-188">The request could not be completed due to a conflict with the current state of the resource.</span></span> <span data-ttu-id="fe01f-189">Пользователю следует повторить отправку с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="fe01f-189">The user should resubmit with more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-190"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**\_состояние HTTP \_ пропала**</span><span class="sxs-lookup"><span data-stu-id="fe01f-190"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP\_STATUS\_GONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-191">410</span><span class="sxs-lookup"><span data-stu-id="fe01f-191">410</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-192">Запрошенный ресурс больше не доступен на сервере, и адрес пересылки неизвестен.</span><span class="sxs-lookup"><span data-stu-id="fe01f-192">The requested resource is no longer available at the server, and no forwarding address is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-193"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_ \_ требуется длина состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="fe01f-193"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP\_STATUS\_LENGTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-194">411</span><span class="sxs-lookup"><span data-stu-id="fe01f-194">411</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-195">Сервер не может принять запрос без определенной длины содержимого.</span><span class="sxs-lookup"><span data-stu-id="fe01f-195">The server cannot accept the request without a defined content length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-196"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**\_Ошибка HTTP Status \_ преконд \_**</span><span class="sxs-lookup"><span data-stu-id="fe01f-196"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP\_STATUS\_PRECOND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-197">412</span><span class="sxs-lookup"><span data-stu-id="fe01f-197">412</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-198">Предусловие, заданное в одном или нескольких полях заголовка запроса, выдает значение false при проверке на сервере.</span><span class="sxs-lookup"><span data-stu-id="fe01f-198">The precondition given in one or more of the request header fields evaluated to false when it was tested on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-199"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_ \_ \_ слишком \_ большой запрос состояния HTTP**</span><span class="sxs-lookup"><span data-stu-id="fe01f-199"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP\_STATUS\_REQUEST\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-200">413</span><span class="sxs-lookup"><span data-stu-id="fe01f-200">413</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-201">Серверу не удается обработать запрос, так как сущность запроса больше, чем может обработать сервер.</span><span class="sxs-lookup"><span data-stu-id="fe01f-201">The server cannot process the request because the request entity is larger than the server is able to process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-202"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_ \_ \_ слишком \_ длинный URI состояния HTTP**</span><span class="sxs-lookup"><span data-stu-id="fe01f-202"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP\_STATUS\_URI\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-203">414</span><span class="sxs-lookup"><span data-stu-id="fe01f-203">414</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-204">Серверу не удается обработать запрос, так как URI запроса длиннее, чем может интерпретировать сервер.</span><span class="sxs-lookup"><span data-stu-id="fe01f-204">The server cannot service the request because the request URI is longer than the server can interpret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-205"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**\_ \_ неподдерживаемый носитель состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="fe01f-205"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP\_STATUS\_UNSUPPORTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-206">415</span><span class="sxs-lookup"><span data-stu-id="fe01f-206">415</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-207">Сервер не может обслуживать запрос, так как сущность запроса имеет формат, не поддерживаемый запрошенным ресурсом для запрошенного метода.</span><span class="sxs-lookup"><span data-stu-id="fe01f-207">The server cannot service the request because the entity of the request is in a format not supported by the requested resource for the requested method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-208"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**\_Повтор состояния HTTP \_ \_ с**</span><span class="sxs-lookup"><span data-stu-id="fe01f-208"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP\_STATUS\_RETRY\_WITH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-209">449</span><span class="sxs-lookup"><span data-stu-id="fe01f-209">449</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-210">После выполнения соответствующего действия запрос должен быть выполнен повторно.</span><span class="sxs-lookup"><span data-stu-id="fe01f-210">The request should be retried after doing the appropriate action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-211"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_ \_ Ошибка сервера состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="fe01f-211"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP\_STATUS\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-212">500</span><span class="sxs-lookup"><span data-stu-id="fe01f-212">500</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-213">Сервер обнаружил непредвиденное условие, препятствующее выполнению запроса.</span><span class="sxs-lookup"><span data-stu-id="fe01f-213">The server encountered an unexpected condition that prevented it from fulfilling the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-214"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_состояние HTTP \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="fe01f-214"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP\_STATUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-215">501</span><span class="sxs-lookup"><span data-stu-id="fe01f-215">501</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-216">Сервер не поддерживает функции, необходимые для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="fe01f-216">The server does not support the functionality required to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-217"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**\_ \_ неправильный шлюз состояния \_ http**</span><span class="sxs-lookup"><span data-stu-id="fe01f-217"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP\_STATUS\_BAD\_GATEWAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-218">502</span><span class="sxs-lookup"><span data-stu-id="fe01f-218">502</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-219">Сервер, выполняющий роль шлюза или прокси-сервера, получил недопустимый ответ от вышестоящего сервера, к которому он обращался при попытке выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="fe01f-219">The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-220"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**недоступный для \_ службы состояния HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fe01f-220"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP\_STATUS\_SERVICE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-221">503</span><span class="sxs-lookup"><span data-stu-id="fe01f-221">503</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-222">Служба временно перегружена.</span><span class="sxs-lookup"><span data-stu-id="fe01f-222">The service is temporarily overloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-223"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**\_ \_ время ожидания шлюза состояния HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="fe01f-223"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP\_STATUS\_GATEWAY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-224">504</span><span class="sxs-lookup"><span data-stu-id="fe01f-224">504</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-225">При выполнении запроса было превышено время ожидания шлюза.</span><span class="sxs-lookup"><span data-stu-id="fe01f-225">The request was timed out waiting for a gateway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01f-226"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_версия состояния \_ HTTP \_ не \_ SUP**</span><span class="sxs-lookup"><span data-stu-id="fe01f-226"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP\_STATUS\_VERSION\_NOT\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe01f-227">505</span><span class="sxs-lookup"><span data-stu-id="fe01f-227">505</span></span>
</dt> <dt>



<span data-ttu-id="fe01f-228">Сервер не поддерживает версию протокола HTTP, которая использовалась в сообщении запроса.</span><span class="sxs-lookup"><span data-stu-id="fe01f-228">The server does not support the HTTP protocol version that was used in the request message.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe01f-229">Требования</span><span class="sxs-lookup"><span data-stu-id="fe01f-229">Requirements</span></span>



| <span data-ttu-id="fe01f-230">Требование</span><span class="sxs-lookup"><span data-stu-id="fe01f-230">Requirement</span></span> | <span data-ttu-id="fe01f-231">Значение</span><span class="sxs-lookup"><span data-stu-id="fe01f-231">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fe01f-232">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe01f-232">Minimum supported client</span></span><br/> | <span data-ttu-id="fe01f-233">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fe01f-233">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="fe01f-234">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe01f-234">Minimum supported server</span></span><br/> | <span data-ttu-id="fe01f-235">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fe01f-235">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="fe01f-236">Header</span><span class="sxs-lookup"><span data-stu-id="fe01f-236">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe01f-237"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe01f-237"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe01f-238">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe01f-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe01f-239">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="fe01f-239">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

