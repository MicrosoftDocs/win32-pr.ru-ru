---
title: Флаги сведений о запросе (WinInet. h)
description: Следующие списки содержат атрибуты и модификаторы, используемые Хттпкуеринфо и Куеринфо.
ms.assetid: b1613193-ae03-411e-bf05-de42f471cd8c
topic_type:
- apiref
api_name:
- HTTP_QUERY_ACCEPT
- HTTP_QUERY_ACCEPT_CHARSET
- HTTP_QUERY_ACCEPT_ENCODING
- HTTP_QUERY_ACCEPT_LANGUAGE
- HTTP_QUERY_ACCEPT_RANGES
- HTTP_QUERY_AGE
- HTTP_QUERY_ALLOW
- HTTP_QUERY_AUTHORIZATION
- HTTP_QUERY_CACHE_CONTROL
- HTTP_QUERY_CONNECTION
- HTTP_QUERY_CONTENT_BASE
- HTTP_QUERY_CONTENT_DESCRIPTION
- HTTP_QUERY_CONTENT_DISPOSITION
- HTTP_QUERY_CONTENT_ENCODING
- HTTP_QUERY_CONTENT_ID
- HTTP_QUERY_CONTENT_LANGUAGE
- HTTP_QUERY_CONTENT_LENGTH
- HTTP_QUERY_CONTENT_LOCATION
- HTTP_QUERY_CONTENT_MD5
- HTTP_QUERY_CONTENT_RANGE
- HTTP_QUERY_CONTENT_TRANSFER_ENCODING
- HTTP_QUERY_CONTENT_TYPE
- HTTP_QUERY_COOKIE
- HTTP_QUERY_COST
- HTTP_QUERY_CUSTOM
- HTTP_QUERY_DATE
- HTTP_QUERY_DERIVED_FROM
- HTTP_QUERY_ECHO_HEADERS
- HTTP_QUERY_ECHO_HEADERS_CRLF
- HTTP_QUERY_ECHO_REPLY
- HTTP_QUERY_ECHO_REQUEST
- HTTP_QUERY_ETAG
- HTTP_QUERY_EXPECT
- HTTP_QUERY_EXPIRES
- HTTP_QUERY_FORWARDED
- HTTP_QUERY_FROM
- HTTP_QUERY_HOST
- HTTP_QUERY_IF_MATCH
- HTTP_QUERY_IF_MODIFIED_SINCE
- HTTP_QUERY_IF_NONE_MATCH
- HTTP_QUERY_IF_RANGE
- HTTP_QUERY_IF_UNMODIFIED_SINCE
- HTTP_QUERY_LAST_MODIFIED
- HTTP_QUERY_LINK
- HTTP_QUERY_LOCATION
- HTTP_QUERY_MAX
- HTTP_QUERY_MAX_FORWARDS
- HTTP_QUERY_MESSAGE_ID
- HTTP_QUERY_MIME_VERSION
- HTTP_QUERY_ORIG_URI
- HTTP_QUERY_PRAGMA
- HTTP_QUERY_PROXY_AUTHENTICATE
- HTTP_QUERY_PROXY_AUTHORIZATION
- HTTP_QUERY_PROXY_CONNECTION
- HTTP_QUERY_PUBLIC
- HTTP_QUERY_RANGE
- HTTP_QUERY_RAW_HEADERS
- HTTP_QUERY_RAW_HEADERS_CRLF
- HTTP_QUERY_REFERER
- HTTP_QUERY_REFRESH
- HTTP_QUERY_REQUEST_METHOD
- HTTP_QUERY_RETRY_AFTER
- HTTP_QUERY_SERVER
- HTTP_QUERY_SET_COOKIE
- HTTP_QUERY_STATUS_CODE
- HTTP_QUERY_STATUS_TEXT
- HTTP_QUERY_TITLE
- HTTP_QUERY_TRANSFER_ENCODING
- HTTP_QUERY_UNLESS_MODIFIED_SINCE
- HTTP_QUERY_UPGRADE
- HTTP_QUERY_URI
- HTTP_QUERY_USER_AGENT
- HTTP_QUERY_VARY
- HTTP_QUERY_VERSION
- HTTP_QUERY_VIA
- HTTP_QUERY_WARNING
- HTTP_QUERY_WWW_AUTHENTICATE
- HTTP_QUERY_X_CONTENT_TYPE_OPTIONS
- HTTP_QUERY_P3P
- HTTP_QUERY_X_P2P_PEERDIST
- HTTP_QUERY_TRANSLATE
- HTTP_QUERY_X_UA_COMPATIBLE
- HTTP_QUERY_DEFAULT_STYLE
- HTTP_QUERY_X_FRAME_OPTIONS
- HTTP_QUERY_X_XSS_PROTECTION
- HTTP_QUERY_FLAG_COALESCE
- HTTP_QUERY_FLAG_NUMBER
- HTTP_QUERY_FLAG_REQUEST_HEADERS
- HTTP_QUERY_FLAG_SYSTEMTIME
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f3a6166c59e158d041e730d2198f6e1b066a8b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691966"
---
# <a name="query-info-flags-winineth"></a><span data-ttu-id="2c3b8-103">Флаги сведений о запросе (WinInet. h)</span><span class="sxs-lookup"><span data-stu-id="2c3b8-103">Query Info Flags (Wininet.h)</span></span>

<span data-ttu-id="2c3b8-104">Следующие списки содержат атрибуты и модификаторы, используемые [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) и [**куеринфо**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2c3b8-104">The following lists contain the attributes and modifiers used by [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) and [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).</span></span>

<span data-ttu-id="2c3b8-105">Флаги атрибутов используются [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (или [**куеринфо**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) для указания извлекаемых данных.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-105">The attribute flags are used by [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (or [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) to indicate what data to retrieve.</span></span> <span data-ttu-id="2c3b8-106">Большинство флагов атрибутов сопоставляются непосредственно с конкретным заголовком HTTP.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="2c3b8-107">Также есть некоторые специальные флаги, такие как [ \_ \_ необработанные \_ заголовки HTTP-запросов](/windows), которые не связаны с определенным заголовком.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-107">There are also some special flags, such as [HTTP\_QUERY\_RAW\_HEADERS](/windows), that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="2c3b8-108"><span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**принятие HTTP- \_ запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-108"><span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**HTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-109">24</span><span class="sxs-lookup"><span data-stu-id="2c3b8-109">24</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-110">Возвращает допустимые типы носителей для ответа.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-110">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-111"><span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**\_запрос HTTP \_ Accept \_ CharSet**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-111"><span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**HTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-112">25</span><span class="sxs-lookup"><span data-stu-id="2c3b8-112">25</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-113">Возвращает допустимые наборы символов для ответа.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-113">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-114"><span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**\_ \_ Кодировка приема HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-114"><span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**HTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-115">26</span><span class="sxs-lookup"><span data-stu-id="2c3b8-115">26</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-116">Извлекает приемлемые значения кодирования содержимого для ответа.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-116">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-117"><span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**\_ \_ язык приема HTTP-запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-117"><span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**HTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-118">27</span><span class="sxs-lookup"><span data-stu-id="2c3b8-118">27</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-119">Извлекает допустимые естественные языки для ответа.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-119">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-120"><span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**\_ \_ диапазоны приема HTTP-запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-120"><span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**HTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-121">42</span><span class="sxs-lookup"><span data-stu-id="2c3b8-121">42</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-122">Возвращает типы запросов диапазона, которые принимаются для ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-122">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-123"><span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**\_ \_ срок действия HTTP-запроса**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-123"><span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**HTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-124">48</span><span class="sxs-lookup"><span data-stu-id="2c3b8-124">48</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-125">Извлекает поле "возраст ответа-заголовок", которое содержит оценку отправителя периода времени, прошедшее с момента создания ответа на сервере-источнике.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-125">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the origin server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-126"><span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**разрешить HTTP- \_ запрос \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-126"><span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**HTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-127">7</span><span class="sxs-lookup"><span data-stu-id="2c3b8-127">7</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-128">Получает HTTP-команды, поддерживаемые сервером.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-128">Receives the HTTP verbs supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-129"><span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**\_авторизация HTTP-запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-129"><span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**HTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-130">28</span><span class="sxs-lookup"><span data-stu-id="2c3b8-130">28</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-131">Получает учетные данные авторизации, используемые для запроса.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-131">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-132"><span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**\_ \_ Управление кэшем HTTP-запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-132"><span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**HTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-133">49</span><span class="sxs-lookup"><span data-stu-id="2c3b8-133">49</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-134">Получает директивы управления кэшем.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-134">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-135"><span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**подключение HTTP- \_ запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-135"><span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**HTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-136">23</span><span class="sxs-lookup"><span data-stu-id="2c3b8-136">23</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-137">Извлекает все параметры, указанные для конкретного соединения, и не должны передаваться через прокси-серверы при последующих соединениях.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-137">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-138"><span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**\_ \_ база содержимого HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-138"><span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**HTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-139">50</span><span class="sxs-lookup"><span data-stu-id="2c3b8-139">50</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-140">Извлекает базовый URI (универсальный идентификатор ресурса) для разрешения относительных URL-адресов в сущности.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-140">Retrieves the base URI (Uniform Resource Identifier) for resolving relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-141"><span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**\_ \_ Описание содержимого HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-141"><span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**HTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-142">4</span><span class="sxs-lookup"><span data-stu-id="2c3b8-142">4</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-143">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-143">Obsolete.</span></span> <span data-ttu-id="2c3b8-144">Поддерживается только для совместимости с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-144">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-145"><span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**\_ \_ расположение содержимого HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-145"><span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**HTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-146">47</span><span class="sxs-lookup"><span data-stu-id="2c3b8-146">47</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-147">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-147">Obsolete.</span></span> <span data-ttu-id="2c3b8-148">Поддерживается только для совместимости с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-148">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-149"><span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**\_ \_ Кодировка содержимого HTTP-запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-149"><span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**HTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-150">29</span><span class="sxs-lookup"><span data-stu-id="2c3b8-150">29</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-151">Извлекает все дополнительные кодеки содержимого, которые были применены ко всему ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-151">Retrieves any additional content codings that have been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-152"><span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**\_ \_ идентификатор содержимого HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-152"><span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**HTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-153">3</span><span class="sxs-lookup"><span data-stu-id="2c3b8-153">3</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-154">Получает идентификацию содержимого.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-154">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-155"><span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**\_ \_ язык содержимого HTTP-запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-155"><span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**HTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-156">6</span><span class="sxs-lookup"><span data-stu-id="2c3b8-156">6</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-157">Извлекает язык, в котором находится содержимое.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-157">Retrieves the language that the content is in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-158"><span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**\_ \_ длина содержимого HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-158"><span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**HTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-159">5</span><span class="sxs-lookup"><span data-stu-id="2c3b8-159">5</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-160">Возвращает размер ресурса в байтах.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-160">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-161"><span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**\_ \_ расположение содержимого HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-161"><span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**HTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-162">51</span><span class="sxs-lookup"><span data-stu-id="2c3b8-162">51</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-163">Возвращает расположение ресурса для сущности, заключенной в сообщение.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-163">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-164"><span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**\_ \_ MD5 содержимого HTTP-запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-164"><span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**HTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-165">52</span><span class="sxs-lookup"><span data-stu-id="2c3b8-165">52</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-166">Извлекает дайджест MD5 из тела сущности для предоставления сквозной проверки целостности сообщений (MIC) для объекта-тела.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-166">Retrieves an MD5 digest of the entity-body for the purpose of providing an end-to-end message integrity check (MIC) for the entity-body.</span></span> <span data-ttu-id="2c3b8-167">Дополнительные сведения см. в разделе RFC1864, поле заголовка Content-MD5 в [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .</span><span class="sxs-lookup"><span data-stu-id="2c3b8-167">For more information, see RFC1864, The Content-MD5 Header Field, at [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-168"><span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**\_ \_ диапазон содержимого HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-168"><span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**HTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-169">53</span><span class="sxs-lookup"><span data-stu-id="2c3b8-169">53</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-170">Извлекает расположение в полном тексте сущности, где следует вставить частичную сущность-текст, и общий размер полного тела сущности.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-170">Retrieves the location in the full entity-body where the partial entity-body should be inserted and the total size of the full entity-body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-171"><span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**\_ \_ \_ Кодировка обмена содержимым HTTP-запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-171"><span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**HTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-172">2</span><span class="sxs-lookup"><span data-stu-id="2c3b8-172">2</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-173">Получает дополнительный код содержимого, примененный к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-173">Receives the additional content coding that has been applied to the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-174"><span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**\_ \_ тип содержимого HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-174"><span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**HTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-175">1</span><span class="sxs-lookup"><span data-stu-id="2c3b8-175">1</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-176">Получает тип содержимого ресурса (например, text/html).</span><span class="sxs-lookup"><span data-stu-id="2c3b8-176">Receives the content type of the resource (such as text/html).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-177"><span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**\_ \_ файл cookie HTTP-запроса**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-177"><span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**HTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-178">44</span><span class="sxs-lookup"><span data-stu-id="2c3b8-178">44</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-179">Извлекает все файлы cookie, связанные с запросом.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-179">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-180"><span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**Стоимость HTTP- \_ запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-180"><span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**HTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-181">15</span><span class="sxs-lookup"><span data-stu-id="2c3b8-181">15</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-182">Больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-182">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-183"><span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**пользовательский HTTP- \_ запрос \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-183"><span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**HTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-184">65535</span><span class="sxs-lookup"><span data-stu-id="2c3b8-184">65535</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-185">Приводит к тому, что [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) ищет имя заголовка, указанное в *лпвбуффер* , и сохраняет данные заголовка в *лпвбуффер*.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-185">Causes [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) to search for the header name specified in *lpvBuffer* and store the header data in *lpvBuffer*.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-186"><span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**\_Дата запроса \_ http**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-186"><span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**HTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-187">9</span><span class="sxs-lookup"><span data-stu-id="2c3b8-187">9</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-188">Получает дату и время порождения сообщения.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-188">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-189"><span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**HTTP- \_ запрос, \_ производный \_ от**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-189"><span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**HTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-190">14</span><span class="sxs-lookup"><span data-stu-id="2c3b8-190">14</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-191">Больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-191">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-192"><span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**\_ \_ заголовки эхо-запросов HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-192"><span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**HTTP\_QUERY\_ECHO\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-193">73</span><span class="sxs-lookup"><span data-stu-id="2c3b8-193">73</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-194">В настоящий момент не реализовано.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-194">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-195"><span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**\_заголовки эхо-запросов HTTP \_ \_ \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-195"><span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**HTTP\_QUERY\_ECHO\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-196">74</span><span class="sxs-lookup"><span data-stu-id="2c3b8-196">74</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-197">В настоящий момент не реализовано.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-197">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-198"><span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**ответ HTTP- \_ запроса \_ echo \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-198"><span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**HTTP\_QUERY\_ECHO\_REPLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-199">72</span><span class="sxs-lookup"><span data-stu-id="2c3b8-199">72</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-200">В настоящий момент не реализовано.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-200">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-201"><span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**запрос HTTP- \_ запроса \_ echo \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-201"><span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**HTTP\_QUERY\_ECHO\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-202">71</span><span class="sxs-lookup"><span data-stu-id="2c3b8-202">71</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-203">В настоящий момент не реализовано.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-203">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-204"><span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**ETag HTTP- \_ запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-204"><span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**HTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-205">54</span><span class="sxs-lookup"><span data-stu-id="2c3b8-205">54</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-206">Извлекает тег сущности для связанной сущности.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-206">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-207"><span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**\_Ожидание HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-207"><span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**HTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-208">68</span><span class="sxs-lookup"><span data-stu-id="2c3b8-208">68</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-209">Извлекает заголовок Expect, который указывает, должен ли клиентское приложение получать ответы на серии 100.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-209">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-210"><span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**\_срок действия HTTP-запроса \_ истек**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-210"><span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**HTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-211">10</span><span class="sxs-lookup"><span data-stu-id="2c3b8-211">10</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-212">Получает дату и время, после которого ресурс должен считаться устаревшим.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-212">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-213"><span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**HTTP- \_ запрос \_ переадресован**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-213"><span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**HTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-214">30</span><span class="sxs-lookup"><span data-stu-id="2c3b8-214">30</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-215">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-215">Obsolete.</span></span> <span data-ttu-id="2c3b8-216">Поддерживается только для совместимости с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-216">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-217"><span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**HTTP- \_ запрос \_ из**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-217"><span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**HTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-218">31</span><span class="sxs-lookup"><span data-stu-id="2c3b8-218">31</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-219">Получает адрес электронной почты пользователя, управляющего запрашивающим агентом пользователя, если указан заголовок From.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-219">Retrieves the email address for the human user who controls the requesting user agent if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-220"><span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**узел HTTP- \_ запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-220"><span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**HTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-221">55</span><span class="sxs-lookup"><span data-stu-id="2c3b8-221">55</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-222">Возвращает Интернет хост и номер порта запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-222">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-223"><span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**HTTP- \_ запрос \_ при \_ совпадении**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-223"><span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**HTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-224">56</span><span class="sxs-lookup"><span data-stu-id="2c3b8-224">56</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-225">Извлекает содержимое поля заголовка запроса If-Match.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-225">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-226"><span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**HTTP- \_ запрос, \_ \_ измененный \_ с момента**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-226"><span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**HTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-227">32</span><span class="sxs-lookup"><span data-stu-id="2c3b8-227">32</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-228">Извлекает содержимое заголовка If-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-228">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-229"><span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**HTTP- \_ запрос, \_ Если ничего не \_ \_ Найдено**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-229"><span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**HTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-230">57</span><span class="sxs-lookup"><span data-stu-id="2c3b8-230">57</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-231">Извлекает содержимое поля заголовка запроса If-None-Match.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-231">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-232"><span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP- \_ запрос, \_ Если \_ диапазон**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-232"><span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-233">58</span><span class="sxs-lookup"><span data-stu-id="2c3b8-233">58</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-234">Извлекает содержимое поля заголовка запроса If-Range.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-234">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="2c3b8-235">Этот заголовок позволяет клиентскому приложению проверять, что сущность, связанная с частичной копией сущности в кэше клиентского приложения, не обновлена.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-235">This header enables the client application to verify that the entity related to a partial copy of the entity in the client application cache has not been updated.</span></span> <span data-ttu-id="2c3b8-236">Если сущность не была обновлена, отправьте части, которые отсутствуют в клиентском приложении.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-236">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="2c3b8-237">Если сущность была обновлена, отправьте всю обновленную сущность.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-237">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-238"><span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**HTTP-запрос, если он не \_ \_ \_ изменен \_ с**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-238"><span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**HTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-239">59</span><span class="sxs-lookup"><span data-stu-id="2c3b8-239">59</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-240">Извлекает содержимое поля "If-Unmodified-with" в заголовке запроса.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-240">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-241"><span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_ \_ Дата последнего \_ изменения HTTP-запроса**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-241"><span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**HTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-242">11</span><span class="sxs-lookup"><span data-stu-id="2c3b8-242">11</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-243">Получает дату и время, когда сервер считает, что ресурс был изменен последним.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-243">Receives the date and time at which the server believes the resource was last modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-244"><span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**Ссылка HTTP- \_ запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-244"><span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**HTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-245">16</span><span class="sxs-lookup"><span data-stu-id="2c3b8-245">16</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-246">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-246">Obsolete.</span></span> <span data-ttu-id="2c3b8-247">Поддерживается только для совместимости с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-247">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-248"><span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**расположение HTTP- \_ запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-248"><span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**HTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-249">33</span><span class="sxs-lookup"><span data-stu-id="2c3b8-249">33</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-250">Возвращает абсолютный универсальный идентификатор ресурса (URI), используемый в заголовке Response-Header.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-250">Retrieves the absolute Uniform Resource Identifier (URI) used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-251"><span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**\_ \_ Максимальное число HTTP-запросов**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-251"><span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**HTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-252">78</span><span class="sxs-lookup"><span data-stu-id="2c3b8-252">78</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-253">Не флаг запроса.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-253">Not a query flag.</span></span> <span data-ttu-id="2c3b8-254">Указывает максимальное значение HTTP- \_ запроса \_ \* .</span><span class="sxs-lookup"><span data-stu-id="2c3b8-254">Indicates the maximum value of an HTTP\_QUERY\_\* value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-255"><span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**\_ \_ Максимальное число \_ пересылаемых запросов HTTP**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-255"><span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**HTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-256">60</span><span class="sxs-lookup"><span data-stu-id="2c3b8-256">60</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-257">Возвращает число прокси-серверов или шлюзов, которые могут перенаправлять запрос на следующий Входящий сервер.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-257">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-258"><span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**\_ \_ идентификатор сообщения HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-258"><span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**HTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-259">12</span><span class="sxs-lookup"><span data-stu-id="2c3b8-259">12</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-260">Больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-260">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-261"><span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**\_ \_ версия MIME HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-261"><span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**HTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-262">0</span><span class="sxs-lookup"><span data-stu-id="2c3b8-262">0</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-263">Получает версию протокола MIME, которая использовалась для создания сообщения.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-263">Receives the version of the MIME protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-264"><span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**\_ \_ \_ универсальный код ресурса HTTP-запроса orig**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-264"><span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**HTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-265">34</span><span class="sxs-lookup"><span data-stu-id="2c3b8-265">34</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-266">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-266">Obsolete.</span></span> <span data-ttu-id="2c3b8-267">Поддерживается только для совместимости с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-267">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-268"><span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**PRAGMA HTTP- \_ запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-268"><span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**HTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-269">17</span><span class="sxs-lookup"><span data-stu-id="2c3b8-269">17</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-270">Получает директивы для конкретной реализации, которые могут применяться к любому получателю в цепочке запросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-270">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-271"><span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**\_ \_ \_ Проверка подлинности прокси HTTP-запроса**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-271"><span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**HTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-272">41</span><span class="sxs-lookup"><span data-stu-id="2c3b8-272">41</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-273">Извлекает схему проверки подлинности и область, возвращенную прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-273">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-274"><span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**\_ \_ авторизация прокси-сервера запросов HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-274"><span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**HTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-275">61</span><span class="sxs-lookup"><span data-stu-id="2c3b8-275">61</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-276">Извлекает заголовок, который используется для идентификации пользователя на прокси-сервере, требующем проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-276">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="2c3b8-277">Этот заголовок может быть получен только до отправки запроса на сервер.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-277">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-278"><span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**\_ \_ соединение прокси-сервера запросов HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-278"><span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**HTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-279">69</span><span class="sxs-lookup"><span data-stu-id="2c3b8-279">69</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-280">Извлекает заголовок Proxy-Connection.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-280">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-281"><span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**общедоступный HTTP- \_ запрос \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-281"><span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**HTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-282">8</span><span class="sxs-lookup"><span data-stu-id="2c3b8-282">8</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-283">Получает методы, доступные на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-283">Receives methods available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-284"><span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**диапазон HTTP- \_ запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-284"><span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**HTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-285">62</span><span class="sxs-lookup"><span data-stu-id="2c3b8-285">62</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-286">Извлекает диапазон байтов сущности.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-286">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-287"><span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**\_ \_ заголовки необработанных HTTP-запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-287"><span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**HTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-288">21</span><span class="sxs-lookup"><span data-stu-id="2c3b8-288">21</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-289">Получает все заголовки, возвращенные сервером.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-289">Receives all the headers returned by the server.</span></span> <span data-ttu-id="2c3b8-290">Каждый заголовок завершается " \\ 0".</span><span class="sxs-lookup"><span data-stu-id="2c3b8-290">Each header is terminated by "\\0".</span></span> <span data-ttu-id="2c3b8-291">Дополнительный " \\ 0" завершает список заголовков.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-291">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-292"><span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**заголовки HTTP- \_ запросов \_ \_ \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-292"><span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**HTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-293">22</span><span class="sxs-lookup"><span data-stu-id="2c3b8-293">22</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-294">Получает все заголовки, возвращенные сервером.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-294">Receives all the headers returned by the server.</span></span> <span data-ttu-id="2c3b8-295">Каждый заголовок отделяется последовательностью возврата каретки/перевода строки (CR/LF).</span><span class="sxs-lookup"><span data-stu-id="2c3b8-295">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-296"><span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**Ссылка HTTP- \_ запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-296"><span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**HTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-297">35</span><span class="sxs-lookup"><span data-stu-id="2c3b8-297">35</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-298">Получает универсальный код ресурса (URI) ресурса, в котором был получен запрошенный URI.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-298">Receives the Uniform Resource Identifier (URI) of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-299"><span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**Обновление HTTP- \_ запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-299"><span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**HTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-300">46</span><span class="sxs-lookup"><span data-stu-id="2c3b8-300">46</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-301">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-301">Obsolete.</span></span> <span data-ttu-id="2c3b8-302">Поддерживается только для совместимости с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-302">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-303"><span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**\_ \_ метод запроса HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-303"><span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**HTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-304">45</span><span class="sxs-lookup"><span data-stu-id="2c3b8-304">45</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-305">Получает HTTP-команду, которая используется в запросе, обычно GET или POST.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-305">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-306"><span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**Повтор HTTP- \_ запроса \_ \_ после**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-306"><span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**HTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-307">36</span><span class="sxs-lookup"><span data-stu-id="2c3b8-307">36</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-308">Возвращает количество времени, в течение которого служба должна быть недоступна.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-308">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-309"><span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**сервер HTTP- \_ запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-309"><span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**HTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-310">37</span><span class="sxs-lookup"><span data-stu-id="2c3b8-310">37</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-311">Извлекает данные о программном обеспечении, используемом сервером источника для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-311">Retrieves data about the software used by the origin server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-312"><span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**\_ \_ файл cookie для набора HTTP-запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-312"><span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**HTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-313">43</span><span class="sxs-lookup"><span data-stu-id="2c3b8-313">43</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-314">Получает значение набора файлов cookie для запроса.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-314">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-315"><span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**\_ \_ код состояния HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-315"><span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**HTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-316">19</span><span class="sxs-lookup"><span data-stu-id="2c3b8-316">19</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-317">Получает код состояния, возвращенный сервером.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-317">Receives the status code returned by the server.</span></span> <span data-ttu-id="2c3b8-318">Дополнительные сведения и список возможных значений см. в разделе [**коды состояния HTTP**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2c3b8-318">For more information and a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-319"><span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**\_ \_ текст состояния HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-319"><span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**HTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-320">20</span><span class="sxs-lookup"><span data-stu-id="2c3b8-320">20</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-321">Получает дополнительный текст, возвращенный сервером в строке ответа.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-321">Receives any additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-322"><span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**заголовок HTTP- \_ запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-322"><span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**HTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-323">38</span><span class="sxs-lookup"><span data-stu-id="2c3b8-323">38</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-324">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-324">Obsolete.</span></span> <span data-ttu-id="2c3b8-325">Поддерживается только для совместимости с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-325">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-326"><span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**кодирование HTTP- \_ запросов \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-326"><span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**HTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-327">63</span><span class="sxs-lookup"><span data-stu-id="2c3b8-327">63</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-328">Возвращает тип преобразования, которое было применено к тексту сообщения, чтобы его можно было безопасно передать между отправителем и получателем.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-328">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-329"><span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**HTTP- \_ запрос, \_ если не \_ изменился \_ с**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-329"><span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**HTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-330">70</span><span class="sxs-lookup"><span data-stu-id="2c3b8-330">70</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-331">Возвращает заголовок, за исключением "-Modified-с".</span><span class="sxs-lookup"><span data-stu-id="2c3b8-331">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-332"><span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**Обновление HTTP- \_ запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-332"><span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**HTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-333">64</span><span class="sxs-lookup"><span data-stu-id="2c3b8-333">64</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-334">Извлекает дополнительные протоколы связи, поддерживаемые сервером.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-334">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-335"><span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**URI HTTP- \_ запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-335"><span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**HTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-336">13</span><span class="sxs-lookup"><span data-stu-id="2c3b8-336">13</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-337">Получает некоторые или все универсальные идентификаторы ресурсов (URI), на которые может быть идентифицирован ресурс Request-URI.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-337">Receives some or all of the Uniform Resource Identifiers (URIs) by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-338"><span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**\_ \_ Агент пользователя HTTP-запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-338"><span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**HTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-339">39</span><span class="sxs-lookup"><span data-stu-id="2c3b8-339">39</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-340">Извлекает данные о агенте пользователя, который выполнил запрос.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-340">Retrieves data about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-341"><span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**\_запрос HTTP \_ vary**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-341"><span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**HTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-342">65</span><span class="sxs-lookup"><span data-stu-id="2c3b8-342">65</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-343">Извлекает заголовок, указывающий, что сущность была выбрана из ряда доступных представлений ответа с помощью согласования на сервере.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-343">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-344"><span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**Версия HTTP- \_ запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-344"><span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**HTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-345">18</span><span class="sxs-lookup"><span data-stu-id="2c3b8-345">18</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-346">Получает последний код ответа, возвращенный сервером.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-346">Receives the last response code returned by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-347"><span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**HTTP- \_ запрос \_ через**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-347"><span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**HTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-348">66</span><span class="sxs-lookup"><span data-stu-id="2c3b8-348">66</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-349">Извлекает промежуточные протоколы и получателей между агентом пользователя и сервером по запросам, а также между сервером источника и клиентом в ответах.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-349">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-350"><span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**предупреждение HTTP- \_ запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-350"><span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**HTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-351">67</span><span class="sxs-lookup"><span data-stu-id="2c3b8-351">67</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-352">Извлекает дополнительные данные о состоянии ответа, который может не отражаться кодом состояния отклика.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-352">Retrieves additional data about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-353"><span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**\_ \_ \_ Проверка подлинности веб-запросов HTTP**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-353"><span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-354">40</span><span class="sxs-lookup"><span data-stu-id="2c3b8-354">40</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-355">Извлекает схему проверки подлинности и область, возвращенные сервером.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-355">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-356"><span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**\_ \_ \_ \_ Параметры типа содержимого HTTP-запроса X \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-356"><span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**HTTP\_QUERY\_X\_CONTENT\_TYPE\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-357">79</span><span class="sxs-lookup"><span data-stu-id="2c3b8-357">79</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-358">Извлекает значение заголовка X-Content-Type-Options.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-358">Retrieves the X-Content-Type-Options header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-359"><span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**\_Запрос HTTP \_ P3P**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-359"><span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**HTTP\_QUERY\_P3P**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-360">80</span><span class="sxs-lookup"><span data-stu-id="2c3b8-360">80</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-361">Извлекает значение заголовка P3P.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-361">Retrieves the P3P header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-362"><span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP- \_ запрос \_ X \_ P2P \_ , то**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-362"><span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP\_QUERY\_X\_P2P\_PEERDIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-363">81</span><span class="sxs-lookup"><span data-stu-id="2c3b8-363">81</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-364">Извлекает значение заголовка X-P2P-,</span><span class="sxs-lookup"><span data-stu-id="2c3b8-364">Retrieves the X-P2P-PeerDist header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-365"><span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**Преобразование HTTP- \_ запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-365"><span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**HTTP\_QUERY\_TRANSLATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-366">82</span><span class="sxs-lookup"><span data-stu-id="2c3b8-366">82</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-367">Получает значение заголовка преобразования.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-367">Retrieves the translate header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-368"><span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP- \_ запрос \_ X UA, \_ \_ совместимый**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-368"><span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP\_QUERY\_X\_UA\_COMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-369">83</span><span class="sxs-lookup"><span data-stu-id="2c3b8-369">83</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-370">Извлекает значение заголовка, совместимое с X-UA-Compatible.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-370">Retrieves the X-UA-Compatible header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-371"><span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**стиль HTTP- \_ запроса \_ по умолчанию \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-371"><span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**HTTP\_QUERY\_DEFAULT\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-372">84</span><span class="sxs-lookup"><span data-stu-id="2c3b8-372">84</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-373">Возвращает значение заголовка Default-Style.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-373">Retrieves the Default-Style header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-374"><span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**Параметры кадра HTTP- \_ запроса \_ X \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-374"><span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**HTTP\_QUERY\_X\_FRAME\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-375">85</span><span class="sxs-lookup"><span data-stu-id="2c3b8-375">85</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-376">Извлекает значение заголовка X-Frame-Options.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-376">Retrieves the X-Frame-Options header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-377"><span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP \_ - \_ запрос \_ X \_ Защита XSS**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-377"><span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP\_QUERY\_X\_XSS\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-378">86</span><span class="sxs-lookup"><span data-stu-id="2c3b8-378">86</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-379">Извлекает значение заголовка X-XSS-Protection.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-379">Retrieves the X-XSS-Protection header value.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="2c3b8-380">Флаги модификатора используются вместе с флагом атрибута для изменения запроса.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-380">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="2c3b8-381">Флаги модификатора либо изменяют формат возвращаемых данных, либо указывают, где [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (или [**куеринфо**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) должны искать данные.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-381">Modifier flags either modify the format of the data returned or indicate where [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (or [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) should search for the data.</span></span>

<dl> <dt>

<span data-ttu-id="2c3b8-382"><span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**\_ \_ объединение ФЛАГОВ HTTP-запросов \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-382"><span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**HTTP\_QUERY\_FLAG\_COALESCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-383">0x10000000</span><span class="sxs-lookup"><span data-stu-id="2c3b8-383">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-384">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-384">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-385"><span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**\_ \_ номер флага http-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-385"><span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**HTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-386">0x20000000</span><span class="sxs-lookup"><span data-stu-id="2c3b8-386">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-387">Возвращает данные в виде 32-разрядного числа для заголовков, значение которых является числом, например код состояния.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-387">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-388"><span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**\_заголовки запросов \_ ФЛАГОВ HTTP-запросов \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-388"><span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**HTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-389">0x80000000</span><span class="sxs-lookup"><span data-stu-id="2c3b8-389">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-390">Запросы заголовков запросов.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-390">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c3b8-391"><span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**Флаг HTTP- \_ запроса \_ \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="2c3b8-391"><span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**HTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c3b8-392">0x40000000</span><span class="sxs-lookup"><span data-stu-id="2c3b8-392">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="2c3b8-393">Возвращает значение заголовка в виде структуры [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , которое не требует от приложения анализа данных.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-393">Returns the header value as a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="2c3b8-394">Используйте для заголовков, значение которых является строкой даты и времени, например "Last-Modified-Time".</span><span class="sxs-lookup"><span data-stu-id="2c3b8-394">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c3b8-395">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c3b8-395">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2c3b8-396">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-396">WinINet does not support server implementations.</span></span> <span data-ttu-id="2c3b8-397">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="2c3b8-397">In addition, it should not be used from a service.</span></span> <span data-ttu-id="2c3b8-398">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="2c3b8-398">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2c3b8-399">Требования</span><span class="sxs-lookup"><span data-stu-id="2c3b8-399">Requirements</span></span>



| <span data-ttu-id="2c3b8-400">Требование</span><span class="sxs-lookup"><span data-stu-id="2c3b8-400">Requirement</span></span> | <span data-ttu-id="2c3b8-401">Значение</span><span class="sxs-lookup"><span data-stu-id="2c3b8-401">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2c3b8-402">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c3b8-402">Minimum supported client</span></span><br/> | <span data-ttu-id="2c3b8-403">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c3b8-403">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2c3b8-404">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c3b8-404">Minimum supported server</span></span><br/> | <span data-ttu-id="2c3b8-405">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c3b8-405">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2c3b8-406">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2c3b8-406">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c3b8-407"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c3b8-407"><dt>Wininet.h</dt></span></span> </dl> |



 

