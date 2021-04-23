---
title: Константы HTTP_LOG_FIELD_ (HTTP. h)
description: Определите поля в журнале W3C и в журналах ошибок.
ms.assetid: 44307d5a-f413-4ee9-9f9c-586c824d5493
topic_type:
- apiref
api_name:
- HTTP_LOG_FIELD_DATE
- HTTP_LOG_FIELD_TIME
- HTTP_LOG_FIELD_CLIENT_IP
- HTTP_LOG_FIELD_USER_NAME
- HTTP_LOG_FIELD_SITE_NAME
- HTTP_LOG_FIELD_COMPUTER_NAME
- HTTP_LOG_FIELD_SERVER_IP
- HTTP_LOG_FIELD_METHOD
- HTTP_LOG_FIELD_URI_STEM
- HTTP_LOG_FIELD_URI_QUERY
- HTTP_LOG_FIELD_STATUS
- HTTP_LOG_FIELD_WIN32_STATUS
- HTTP_LOG_FIELD_BYTES_SENT
- HTTP_LOG_FIELD_BYTES_RECV
- HTTP_LOG_FIELD_TIME_TAKEN
- HTTP_LOG_FIELD_SERVER_PORT
- HTTP_LOG_FIELD_USER_AGENT
- HTTP_LOG_FIELD_COOKIE
- HTTP_LOG_FIELD_REFERER
- HTTP_LOG_FIELD_VERSION
- HTTP_LOG_FIELD_HOST
- HTTP_LOG_FIELD_SUB_STATUS
- HTTP_LOG_FIELD_CLIENT_PORT
- HTTP_LOG_FIELD_URI
- HTTP_LOG_FIELD_SITE_ID
- HTTP_LOG_FIELD_REASON
- HTTP_LOG_FIELD_QUEUE_NAME
- HTTP_LOG_FIELD_STREAMID
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9ab05a9126cb5ffb81b65a460e6a9d671c268bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661866"
---
# <a name="http_log_field_-constants"></a><span data-ttu-id="a237f-103">\_ \_ Константы поля журнала HTTP \_</span><span class="sxs-lookup"><span data-stu-id="a237f-103">HTTP\_LOG\_FIELD\_ Constants</span></span>

<span data-ttu-id="a237f-104">Константы **\_ \_ поля \_ журнала HTTP** определяют поля в журнале W3C и в журналах ошибок.</span><span class="sxs-lookup"><span data-stu-id="a237f-104">The **HTTP\_LOG\_FIELD\_** constants define the fields in the W3C log and the error logs.</span></span>

<span data-ttu-id="a237f-105">Эти константы используются в структуре [**\_ \_ сведений о ведении журнала HTTP**](/windows/desktop/api/Http/ns-http-http_logging_info) .</span><span class="sxs-lookup"><span data-stu-id="a237f-105">These constants are used in the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="a237f-106"><span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**\_ \_ Дата поля журнала \_ http**</span><span class="sxs-lookup"><span data-stu-id="a237f-106"><span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**HTTP\_LOG\_FIELD\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-107">Дата, когда произошло действие.</span><span class="sxs-lookup"><span data-stu-id="a237f-107">The date on which the activity occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-108"><span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**\_время для \_ поля \_ журнала HTTP**</span><span class="sxs-lookup"><span data-stu-id="a237f-108"><span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**HTTP\_LOG\_FIELD\_TIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-109">Время, в течение которого произошло действие, в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="a237f-109">The time, in coordinated universal time (UTC), at which the activity occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-110"><span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**\_ \_ \_ \_ IP-адрес клиента для поля журнала HTTP**</span><span class="sxs-lookup"><span data-stu-id="a237f-110"><span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**HTTP\_LOG\_FIELD\_CLIENT\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-111">IP-адрес отправившего запрос клиента.</span><span class="sxs-lookup"><span data-stu-id="a237f-111">The IP address of the client that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-112"><span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**\_ \_ имя пользователя для поля журнала \_ HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a237f-112"><span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**HTTP\_LOG\_FIELD\_USER\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-113">Имя пользователя, прошедшего проверку подлинности, который получил доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="a237f-113">The name of the authenticated user who accessed your server.</span></span> <span data-ttu-id="a237f-114">Анонимные пользователи обозначаются дефисом.</span><span class="sxs-lookup"><span data-stu-id="a237f-114">Anonymous users are indicated by a hyphen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-115"><span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**\_ \_ имя сайта для поля журнала \_ HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a237f-115"><span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**HTTP\_LOG\_FIELD\_SITE\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-116">Имя сайта, на котором была создана запись файла журнала.</span><span class="sxs-lookup"><span data-stu-id="a237f-116">The name of the site on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-117"><span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**Протокол HTTP \_ \_ \_ \_ имя компьютера для поля журнала**</span><span class="sxs-lookup"><span data-stu-id="a237f-117"><span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span> **HTTP\_LOG\_FIELD\_COMPUTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-118">Имя компьютера, на котором была создана запись файла журнала.</span><span class="sxs-lookup"><span data-stu-id="a237f-118">The name of the computer on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-119"><span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**\_ \_ \_ \_ IP-адрес сервера для поля журнала HTTP**</span><span class="sxs-lookup"><span data-stu-id="a237f-119"><span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**HTTP\_LOG\_FIELD\_SERVER\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-120">IP-адрес сервера, на котором была создана запись файла журнала.</span><span class="sxs-lookup"><span data-stu-id="a237f-120">The IP address of the server on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-121"><span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**\_ \_ метод поля журнала \_ http**</span><span class="sxs-lookup"><span data-stu-id="a237f-121"><span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**HTTP\_LOG\_FIELD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-122">Запрошенное действие, например метод Get.</span><span class="sxs-lookup"><span data-stu-id="a237f-122">The requested action, for example, a get method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-123"><span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**Протокол HTTP \_ \_ \_ \_ ресурс URI поля журнала**</span><span class="sxs-lookup"><span data-stu-id="a237f-123"><span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span> **HTTP\_LOG\_FIELD\_URI\_STEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-124">Целевой объект действия, например Default.htm.</span><span class="sxs-lookup"><span data-stu-id="a237f-124">The target of the action, for example, Default.htm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-125"><span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**\_ \_ запрос URI для поля журнала \_ HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a237f-125"><span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**HTTP\_LOG\_FIELD\_URI\_QUERY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-126">Запрос, если таковой имеется, который клиент пытался выполнить.</span><span class="sxs-lookup"><span data-stu-id="a237f-126">The query, if any, that the client was trying to perform.</span></span> <span data-ttu-id="a237f-127">Запрос универсального кода ресурса (URI) требуется только для динамических страниц.</span><span class="sxs-lookup"><span data-stu-id="a237f-127">A Universal Resource Identifier (URI) query is necessary only for dynamic pages.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-128"><span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**\_ \_ состояние поля журнала \_ http**</span><span class="sxs-lookup"><span data-stu-id="a237f-128"><span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**HTTP\_LOG\_FIELD\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-129">Код состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="a237f-129">The HTTP status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-130"><span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**\_Поле журнала \_ HTTP \_ \_ состояние Win32**</span><span class="sxs-lookup"><span data-stu-id="a237f-130"><span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**HTTP\_LOG\_FIELD\_WIN32\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-131">Код состояния Windows.</span><span class="sxs-lookup"><span data-stu-id="a237f-131">The Windows status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-132"><span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**\_ \_ \_ Отправлено байт для поля журнала \_ http**</span><span class="sxs-lookup"><span data-stu-id="a237f-132"><span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**HTTP\_LOG\_FIELD\_BYTES\_SENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-133">Число в байтах, отправленное сервером.</span><span class="sxs-lookup"><span data-stu-id="a237f-133">The number, in bytes, sent by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-134"><span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**\_байтов для \_ поля журнала HTTP \_ \_ recv**</span><span class="sxs-lookup"><span data-stu-id="a237f-134"><span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**HTTP\_LOG\_FIELD\_BYTES\_RECV**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-135">Число в байтах, полученное сервером.</span><span class="sxs-lookup"><span data-stu-id="a237f-135">The number, in bytes, received by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-136"><span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**\_ \_ \_ затраченное время для поля журнала \_ http**</span><span class="sxs-lookup"><span data-stu-id="a237f-136"><span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**HTTP\_LOG\_FIELD\_TIME\_TAKEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-137">Время (в миллисекундах) действия.</span><span class="sxs-lookup"><span data-stu-id="a237f-137">The time, in milliseconds, of the action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-138"><span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**\_ \_ \_ порт сервера полей журнала \_ http**</span><span class="sxs-lookup"><span data-stu-id="a237f-138"><span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**HTTP\_LOG\_FIELD\_SERVER\_PORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-139">Номер порта сервера, настроенного для службы.</span><span class="sxs-lookup"><span data-stu-id="a237f-139">The server port number that is configured for the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-140"><span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**Протокол HTTP \_ \_ \_ \_ Агент пользователя поля журнала**</span><span class="sxs-lookup"><span data-stu-id="a237f-140"><span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span> **HTTP\_LOG\_FIELD\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-141">Приложение, используемое клиентом.</span><span class="sxs-lookup"><span data-stu-id="a237f-141">The application that the client used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-142"><span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**\_ \_ файл cookie поля журнала HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a237f-142"><span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**HTTP\_LOG\_FIELD\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-143">Содержимое отправленного или полученного файла cookie, если таковое имеется.</span><span class="sxs-lookup"><span data-stu-id="a237f-143">The content of the cookie sent or received, if any.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-144"><span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**\_ \_ ссылка на поле журнала HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a237f-144"><span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**HTTP\_LOG\_FIELD\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-145">Сайт, который последний раз посещал пользователь.</span><span class="sxs-lookup"><span data-stu-id="a237f-145">The site that the user last visited.</span></span> <span data-ttu-id="a237f-146">Этот сайт предоставил ссылку на текущий сайт.</span><span class="sxs-lookup"><span data-stu-id="a237f-146">This site provided a link to the current site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-147"><span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**\_ \_ версия поля журнала \_ http**</span><span class="sxs-lookup"><span data-stu-id="a237f-147"><span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**HTTP\_LOG\_FIELD\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-148">Версия протокола HTTP, используемая клиентом.</span><span class="sxs-lookup"><span data-stu-id="a237f-148">The HTTP protocol version that the client used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-149"><span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**\_ \_ узел поля журнала \_ http**</span><span class="sxs-lookup"><span data-stu-id="a237f-149"><span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**HTTP\_LOG\_FIELD\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-150">Имя заголовка узла, если оно есть.</span><span class="sxs-lookup"><span data-stu-id="a237f-150">The host header name, if any.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-151"><span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**\_подсостояние \_ поля \_ журнала \_ http**</span><span class="sxs-lookup"><span data-stu-id="a237f-151"><span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**HTTP\_LOG\_FIELD\_SUB\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-152">Код ошибки подсостояния.</span><span class="sxs-lookup"><span data-stu-id="a237f-152">The substatus error code.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="a237f-153">Для ведения журнала ошибок HTTP используются следующие константы.</span><span class="sxs-lookup"><span data-stu-id="a237f-153">The following constants are used for HTTP error logging.</span></span>

<dl> <dt>

<span data-ttu-id="a237f-154"><span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**\_ \_ порт клиента для поля журнала \_ HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a237f-154"><span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**HTTP\_LOG\_FIELD\_CLIENT\_PORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-155">Номер порта клиента, с которого получен запрос.</span><span class="sxs-lookup"><span data-stu-id="a237f-155">The client port number from which the request is received.</span></span> <span data-ttu-id="a237f-156">Это поле журнала используется только для ведения журнала ошибок.</span><span class="sxs-lookup"><span data-stu-id="a237f-156">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-157"><span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**\_ \_ URI поля журнала \_ http**</span><span class="sxs-lookup"><span data-stu-id="a237f-157"><span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**HTTP\_LOG\_FIELD\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-158">URI, полученный в запросе, включая часть запроса.</span><span class="sxs-lookup"><span data-stu-id="a237f-158">The URI received in the request including the query portion.</span></span> <span data-ttu-id="a237f-159">Это поле журнала используется только для ведения журнала ошибок.</span><span class="sxs-lookup"><span data-stu-id="a237f-159">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-160"><span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**\_ \_ идентификатор сайта для поля журнала \_ HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a237f-160"><span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**HTTP\_LOG\_FIELD\_SITE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-161">Зависящий от приложения числовой идентификатор группы URL-адресов, в которой направляется запрос.</span><span class="sxs-lookup"><span data-stu-id="a237f-161">The application-specific numeric ID of the URL Group on which the request is routed.</span></span> <span data-ttu-id="a237f-162">Это поле журнала используется только для ведения журнала ошибок.</span><span class="sxs-lookup"><span data-stu-id="a237f-162">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-163"><span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**\_Причина для \_ поля \_ журнала HTTP**</span><span class="sxs-lookup"><span data-stu-id="a237f-163"><span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**HTTP\_LOG\_FIELD\_REASON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-164">Причина ошибки.</span><span class="sxs-lookup"><span data-stu-id="a237f-164">The error reason phrase.</span></span> <span data-ttu-id="a237f-165">Это поле журнала используется только для ведения журнала ошибок.</span><span class="sxs-lookup"><span data-stu-id="a237f-165">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-166"><span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**\_ \_ имя очереди для поля журнала \_ HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a237f-166"><span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**HTTP\_LOG\_FIELD\_QUEUE\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-167">Имя очереди запросов, в которую отправляется запрос.</span><span class="sxs-lookup"><span data-stu-id="a237f-167">The name of the request queue to which the request is dispatched.</span></span> <span data-ttu-id="a237f-168">Это поле журнала используется только для ведения журнала ошибок.</span><span class="sxs-lookup"><span data-stu-id="a237f-168">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a237f-169"><span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**\_ \_ STREAMID поля журнала \_ http**</span><span class="sxs-lookup"><span data-stu-id="a237f-169"><span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**HTTP\_LOG\_FIELD\_STREAMID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a237f-170">Идентификатор потока.</span><span class="sxs-lookup"><span data-stu-id="a237f-170">The stream id.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a237f-171">Требования</span><span class="sxs-lookup"><span data-stu-id="a237f-171">Requirements</span></span>



| <span data-ttu-id="a237f-172">Требование</span><span class="sxs-lookup"><span data-stu-id="a237f-172">Requirement</span></span> | <span data-ttu-id="a237f-173">Значение</span><span class="sxs-lookup"><span data-stu-id="a237f-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a237f-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a237f-174">Minimum supported client</span></span><br/> | <span data-ttu-id="a237f-175">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a237f-175">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a237f-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a237f-176">Minimum supported server</span></span><br/> | <span data-ttu-id="a237f-177">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a237f-177">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a237f-178">Header</span><span class="sxs-lookup"><span data-stu-id="a237f-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="a237f-179"><dt>HTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="a237f-179"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a237f-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a237f-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a237f-181">Константы API сервера HTTP версии 2,0</span><span class="sxs-lookup"><span data-stu-id="a237f-181">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="a237f-182">**\_сведения о ведении журнала HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a237f-182">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[<span data-ttu-id="a237f-183">**хттпсетурлграуппроперти**</span><span class="sxs-lookup"><span data-stu-id="a237f-183">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="a237f-184">**хттпсетсерверсессионпроперти**</span><span class="sxs-lookup"><span data-stu-id="a237f-184">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="a237f-185">**хттпкуерюрлграуппроперти**</span><span class="sxs-lookup"><span data-stu-id="a237f-185">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="a237f-186">**хттпкуерисерверсессионпроперти**</span><span class="sxs-lookup"><span data-stu-id="a237f-186">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





