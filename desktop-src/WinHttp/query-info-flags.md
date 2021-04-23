---
description: Эти атрибуты и модификаторы используются WinHttpQueryHeaders.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Флаги сведений о запросе (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32ba15c258a37627cdbdd79f13859761fd671385
ms.sourcegitcommit: df0933ad2b42f07031f4340330712c11cf712ff0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107385892"
---
# <a name="query-info-flags-winhttph"></a><span data-ttu-id="707b0-103">Флаги сведений о запросе (WinHTTP. h)</span><span class="sxs-lookup"><span data-stu-id="707b0-103">Query Info Flags (Winhttp.h)</span></span>

<span data-ttu-id="707b0-104">Эти атрибуты и модификаторы используются [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="707b0-104">These attributes and modifiers are used by [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

<span data-ttu-id="707b0-105">Флаги атрибута используются [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) для указания извлекаемой информации.</span><span class="sxs-lookup"><span data-stu-id="707b0-105">The attribute flags are used by [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) to indicate what information to retrieve.</span></span> <span data-ttu-id="707b0-106">Большинство флагов атрибутов сопоставляются непосредственно с конкретным заголовком HTTP.</span><span class="sxs-lookup"><span data-stu-id="707b0-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="707b0-107">Также есть некоторые специальные флаги, такие как \_ \_ необработанные \_ заголовки запросов WinHTTP, которые не связаны с определенным заголовком.</span><span class="sxs-lookup"><span data-stu-id="707b0-107">There are also some special flags, such as WINHTTP\_QUERY\_RAW\_HEADERS, that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="707b0-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**\_принятие запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-109">Возвращает допустимые типы носителей для ответа.</span><span class="sxs-lookup"><span data-stu-id="707b0-109">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**\_запрос WinHTTP \_ Accept \_ CharSet**</span><span class="sxs-lookup"><span data-stu-id="707b0-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-111">Возвращает допустимые наборы символов для ответа.</span><span class="sxs-lookup"><span data-stu-id="707b0-111">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**\_ \_ Кодировка Accept запроса WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WINHTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-113">Извлекает приемлемые значения кодирования содержимого для ответа.</span><span class="sxs-lookup"><span data-stu-id="707b0-113">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**\_ \_ язык принятия запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-115">Извлекает допустимые естественные языки для ответа.</span><span class="sxs-lookup"><span data-stu-id="707b0-115">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**\_ \_ диапазоны приема запросов WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**WINHTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-117">Возвращает типы запросов диапазона, которые принимаются для ресурса.</span><span class="sxs-lookup"><span data-stu-id="707b0-117">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**\_возраст запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**WINHTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-119">Извлекает поле "возраст ответа-заголовок", которое содержит оценку отправителя периода времени, прошедшее с момента создания ответа на исходном сервере.</span><span class="sxs-lookup"><span data-stu-id="707b0-119">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**\_Разрешить запросы \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-121">Получает [**HTTP-команды**](glossary.md) , поддерживаемые сервером.</span><span class="sxs-lookup"><span data-stu-id="707b0-121">Receives the [**HTTP verbs**](glossary.md) supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**\_ \_ сведения о проверке подлинности запросов WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**WINHTTP\_QUERY\_AUTHENTICATION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-123">Извлекает заголовок Authentication-Info.</span><span class="sxs-lookup"><span data-stu-id="707b0-123">Retrieves the Authentication-Info header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**\_ \_ авторизация запросов WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**WINHTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-125">Получает учетные данные авторизации, используемые для запроса.</span><span class="sxs-lookup"><span data-stu-id="707b0-125">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**\_ \_ Управление КЭШЕМ запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**WINHTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-127">Получает директивы управления кэшем.</span><span class="sxs-lookup"><span data-stu-id="707b0-127">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**\_соединение с запросом WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**WINHTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-129">Извлекает все параметры, указанные для конкретного соединения, и не должны передаваться через прокси-серверы при последующих соединениях.</span><span class="sxs-lookup"><span data-stu-id="707b0-129">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**\_ \_ база содержимого запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**WINHTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-131">Получает базовый универсальный код ресурса (URI) для разрешения относительных URL-адресов внутри сущности.</span><span class="sxs-lookup"><span data-stu-id="707b0-131">Retrieves the base Uniform Resource Identifier (URI) to resolve relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**\_ \_ Описание содержимого запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**WINHTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-133">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="707b0-133">Obsolete.</span></span> <span data-ttu-id="707b0-134">Поддерживается для совместимости с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="707b0-134">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**\_ \_ расстановка содержимого запроса WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**WINHTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-136">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="707b0-136">Obsolete.</span></span> <span data-ttu-id="707b0-137">Поддерживается для совместимости с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="707b0-137">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**\_ \_ кодирование содержимого запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-139">Извлекает дополнительный код, примененный ко всему ресурсу.</span><span class="sxs-lookup"><span data-stu-id="707b0-139">Retrieves additional content coding that has been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**\_ \_ идентификатор содержимого запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**WINHTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-141">Получает идентификацию содержимого.</span><span class="sxs-lookup"><span data-stu-id="707b0-141">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**\_ \_ язык содержимого запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**WINHTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-143">Извлекает язык, на котором написано содержимое.</span><span class="sxs-lookup"><span data-stu-id="707b0-143">Retrieves the language that the content is written in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**\_ \_ длина содержимого запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**WINHTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-145">Возвращает размер ресурса в байтах.</span><span class="sxs-lookup"><span data-stu-id="707b0-145">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**\_ \_ расположение содержимого запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**WINHTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-147">Возвращает расположение ресурса для сущности, заключенной в сообщение.</span><span class="sxs-lookup"><span data-stu-id="707b0-147">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**\_ \_ MD5 содержимого запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-149">Извлекает дайджест MD5 тела сущности для предоставления сквозной проверки целостности сообщения для тела сущности.</span><span class="sxs-lookup"><span data-stu-id="707b0-149">Retrieves an MD5 digest of the entity body for the purpose of providing an end-to-end message integrity check for the entity body.</span></span> <span data-ttu-id="707b0-150">Дополнительные сведения см. в [документе RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span><span class="sxs-lookup"><span data-stu-id="707b0-150">For more information, see [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**\_ \_ диапазон содержимого запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**WINHTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-152">Извлекает расположение в полном тексте сущности, куда следует вставить частичный текст сущности, и общий размер полного тела сущности.</span><span class="sxs-lookup"><span data-stu-id="707b0-152">Retrieves the location in the full entity body where the partial entity body should be inserted and the total size of the full entity body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**\_ \_ \_ Кодировка для обмена СОДЕРЖИМым запросов WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-154">Получает преобразование кодирования, применимое к сущности-тексту.</span><span class="sxs-lookup"><span data-stu-id="707b0-154">Retrieves an encoding transformation applicable to an entity-body.</span></span> <span data-ttu-id="707b0-155">Возможно, он уже применен, может потребоваться применение или, возможно, он применим.</span><span class="sxs-lookup"><span data-stu-id="707b0-155">It may already have been applied, may need to be applied, or may be optionally applicable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**\_ \_ тип содержимого запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**WINHTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-157">Получает тип содержимого ресурса, например текст или HTML.</span><span class="sxs-lookup"><span data-stu-id="707b0-157">Receives the content type of the resource, such as text or html.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**\_ \_ файл Cookie запроса WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**WINHTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-159">Извлекает все файлы cookie, связанные с запросом.</span><span class="sxs-lookup"><span data-stu-id="707b0-159">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**\_стоимость запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**WINHTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-161">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="707b0-161">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**\_Пользовательский запрос \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-163">Приводит к тому, что [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) ищет имя заголовка, указанное в параметре *pwszName* , и сохраняет сведения о заголовке в *лпбуффер*.</span><span class="sxs-lookup"><span data-stu-id="707b0-163">Causes [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) to search for the header name specified in the *pwszName* parameter and store the header information in *lpBuffer*.</span></span> <span data-ttu-id="707b0-164">Приложение может использовать **параметр WinHTTP \_ \_ \_ \_ время ожидания ответа** для ограничения максимального времени, в течение которого запрос ожидает получения всех заголовков.</span><span class="sxs-lookup"><span data-stu-id="707b0-164">An application can use **WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT** to limit the maximum time this query waits for all headers to be received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**\_Дата запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**WINHTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-166">Получает дату и время порождения сообщения.</span><span class="sxs-lookup"><span data-stu-id="707b0-166">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**запрос WINHTTP, \_ \_ производный \_ от**</span><span class="sxs-lookup"><span data-stu-id="707b0-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**WINHTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-168">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="707b0-168">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**\_ETag запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WINHTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-170">Извлекает тег сущности для связанной сущности.</span><span class="sxs-lookup"><span data-stu-id="707b0-170">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**\_ \_ Ожидание запроса WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-172">Извлекает заголовок Expect, который указывает, должен ли клиентское приложение получать ответы на серии 100.</span><span class="sxs-lookup"><span data-stu-id="707b0-172">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**\_ \_ срок действия запроса WinHTTP истек**</span><span class="sxs-lookup"><span data-stu-id="707b0-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**WINHTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-174">Получает дату и время, после которого ресурс должен считаться устаревшим.</span><span class="sxs-lookup"><span data-stu-id="707b0-174">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**\_запрос WinHTTP \_ переадресован**</span><span class="sxs-lookup"><span data-stu-id="707b0-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**WINHTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-176">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="707b0-176">Obsolete.</span></span> <span data-ttu-id="707b0-177">Поддерживается для совместимости с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="707b0-177">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**\_запрос WinHTTP \_ от**</span><span class="sxs-lookup"><span data-stu-id="707b0-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WINHTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-179">Получает адрес электронной почты пользователя, управляющего запрашивающим [*агентом пользователя*](glossary.md) , если указан заголовок From.</span><span class="sxs-lookup"><span data-stu-id="707b0-179">Retrieves the e-mail address for the user who controls the requesting [*user agent*](glossary.md) if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**\_узел запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**WINHTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-181">Возвращает Интернет хост и номер порта запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="707b0-181">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**\_запрос WinHTTP \_ при \_ совпадении**</span><span class="sxs-lookup"><span data-stu-id="707b0-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-183">Извлекает содержимое поля заголовка запроса If-Match.</span><span class="sxs-lookup"><span data-stu-id="707b0-183">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**запрос WINHTTP, \_ \_ Если \_ изменен \_ с**</span><span class="sxs-lookup"><span data-stu-id="707b0-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**WINHTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-185">Извлекает содержимое заголовка If-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="707b0-185">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**запрос WINHTTP, \_ \_ Если \_ ничего не \_ Найдено**</span><span class="sxs-lookup"><span data-stu-id="707b0-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**WINHTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-187">Извлекает содержимое поля заголовка запроса If-None-Match.</span><span class="sxs-lookup"><span data-stu-id="707b0-187">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**запрос WINHTTP, \_ \_ Если \_ диапазон**</span><span class="sxs-lookup"><span data-stu-id="707b0-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WINHTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-189">Извлекает содержимое поля заголовка запроса If-Range.</span><span class="sxs-lookup"><span data-stu-id="707b0-189">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="707b0-190">Этот заголовок позволяет клиентскому приложению проверять, не обновлялась ли сущность, связанная с частичной копией сущности в кэше клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="707b0-190">This header allows the client application to check if the entity related to a partial copy of the entity in the client application's cache has not been updated.</span></span> <span data-ttu-id="707b0-191">Если сущность не была обновлена, отправьте части, которые отсутствуют в клиентском приложении.</span><span class="sxs-lookup"><span data-stu-id="707b0-191">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="707b0-192">Если сущность была обновлена, отправьте всю обновленную сущность.</span><span class="sxs-lookup"><span data-stu-id="707b0-192">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**запрос WINHTTP, \_ \_ если не \_ изменен \_ с**</span><span class="sxs-lookup"><span data-stu-id="707b0-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**WINHTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-194">Извлекает содержимое поля "If-Unmodified-with" в заголовке запроса.</span><span class="sxs-lookup"><span data-stu-id="707b0-194">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**\_ссылка на запрос WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**WINHTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-196">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="707b0-196">Obsolete.</span></span> <span data-ttu-id="707b0-197">Поддерживается для совместимости с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="707b0-197">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**\_ \_ Дата последнего изменения запроса WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**WINHTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-199">Получает дату и время последнего изменения ресурса.</span><span class="sxs-lookup"><span data-stu-id="707b0-199">Receives the date and time at which the resource was last modified.</span></span> <span data-ttu-id="707b0-200">Дата и время определяются сервером.</span><span class="sxs-lookup"><span data-stu-id="707b0-200">The date and time are determined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**\_Расположение запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**WINHTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-202">Получает абсолютный URI, используемый в заголовке ответа расположения.</span><span class="sxs-lookup"><span data-stu-id="707b0-202">Retrieves the absolute URI used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**\_ \_ Максимальное число запросов WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-204">Указывает максимальное значение \_ значения запроса WinHTTP \_ \* .</span><span class="sxs-lookup"><span data-stu-id="707b0-204">Indicates the maximum value of a WINHTTP\_QUERY\_\* value.</span></span> <span data-ttu-id="707b0-205">Не флаг запроса.</span><span class="sxs-lookup"><span data-stu-id="707b0-205">Not a query flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**\_ \_ Максимальное число \_ пересылаемых запросов WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**WINHTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-207">Возвращает число прокси-серверов или шлюзов, которые могут перенаправлять запрос на следующий Входящий сервер.</span><span class="sxs-lookup"><span data-stu-id="707b0-207">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**\_ \_ идентификатор сообщения запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**WINHTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-209">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="707b0-209">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**\_ \_ версия MIME запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**WINHTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-211">Получает версию протокола MIME, которая использовалась для создания сообщения.</span><span class="sxs-lookup"><span data-stu-id="707b0-211">Receives the version of the Multipurpose Internet Mail Extensions (MIME) protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**\_ \_ URI orig запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**WINHTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-213">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="707b0-213">Obsolete.</span></span> <span data-ttu-id="707b0-214">Поддерживается для совместимости с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="707b0-214">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**\_pragma запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WINHTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-216">Получает директивы для конкретной реализации, которые могут применяться к любому получателю в цепочке запросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="707b0-216">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**\_ \_ Аутентификация прокси-сервера запросов WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**WINHTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-218">Извлекает схему проверки подлинности и область, возвращенную прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="707b0-218">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**\_ \_ авторизация прокси-сервера запросов WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**WINHTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-220">Извлекает заголовок, который используется для идентификации пользователя на прокси-сервере, требующем проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="707b0-220">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="707b0-221">Этот заголовок может быть получен только до отправки запроса на сервер.</span><span class="sxs-lookup"><span data-stu-id="707b0-221">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**\_ \_ Подключение прокси-сервера запросов WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**WINHTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-223">Извлекает заголовок Proxy-Connection.</span><span class="sxs-lookup"><span data-stu-id="707b0-223">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**\_ \_ Поддержка прокси-сервера запросов WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**WINHTTP\_QUERY\_PROXY\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-225">Извлекает заголовок Proxy-Support.</span><span class="sxs-lookup"><span data-stu-id="707b0-225">Retrieves the Proxy-Support header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**\_открытый запрос \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WINHTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-227">Получает HTTP-команды, доступные на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="707b0-227">Receives HTTP verbs available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**\_диапазон запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**WINHTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-229">Извлекает диапазон байтов сущности.</span><span class="sxs-lookup"><span data-stu-id="707b0-229">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**\_ \_ необработанные \_ заголовки запросов WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**WINHTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-231">Получает все заголовки, возвращенные сервером.</span><span class="sxs-lookup"><span data-stu-id="707b0-231">Receives all the headers returned by the server.</span></span> <span data-ttu-id="707b0-232">Каждый заголовок завершается " \\ 0".</span><span class="sxs-lookup"><span data-stu-id="707b0-232">Each header is terminated by "\\0".</span></span> <span data-ttu-id="707b0-233">Дополнительный " \\ 0" завершает список заголовков.</span><span class="sxs-lookup"><span data-stu-id="707b0-233">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**\_запросы WinHTTP \_ необработанных \_ заголовков \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="707b0-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**WINHTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-235">Получает все заголовки, возвращенные сервером.</span><span class="sxs-lookup"><span data-stu-id="707b0-235">Receives all the headers returned by the server.</span></span> <span data-ttu-id="707b0-236">Каждый заголовок отделяется последовательностью возврата каретки/перевода строки (CR/LF).</span><span class="sxs-lookup"><span data-stu-id="707b0-236">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**\_ \_ ссылка на запрос WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**WINHTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-238">Получает URI ресурса, в котором был получен запрошенный URI.</span><span class="sxs-lookup"><span data-stu-id="707b0-238">Receives the URI of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**\_Обновление запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**WINHTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-240">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="707b0-240">Obsolete.</span></span> <span data-ttu-id="707b0-241">Поддерживается для совместимости с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="707b0-241">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**\_ \_ метод запроса WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**WINHTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-243">Получает HTTP-команду, которая используется в запросе, обычно GET или POST.</span><span class="sxs-lookup"><span data-stu-id="707b0-243">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**\_Повтор запроса WinHTTP \_ \_ после**</span><span class="sxs-lookup"><span data-stu-id="707b0-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WINHTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-245">Возвращает количество времени, в течение которого служба должна быть недоступна.</span><span class="sxs-lookup"><span data-stu-id="707b0-245">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**\_сервер запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**WINHTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-247">Извлекает сведения о программном обеспечении, используемом сервером источника для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="707b0-247">Retrieves information about the software used by the originating server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**\_ \_ файл cookie набора запросов WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**WINHTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-249">Получает значение набора файлов cookie для запроса.</span><span class="sxs-lookup"><span data-stu-id="707b0-249">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**\_ \_ код состояния запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**WINHTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-251">Получает код состояния, возвращенный сервером.</span><span class="sxs-lookup"><span data-stu-id="707b0-251">Receives the status code returned by the server.</span></span> <span data-ttu-id="707b0-252">Список возможных значений см. в разделе [**коды состояния HTTP**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="707b0-252">For a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**\_ \_ текст состояния запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**WINHTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-254">Получает дополнительный текст, возвращенный сервером в строке ответа.</span><span class="sxs-lookup"><span data-stu-id="707b0-254">Receives additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**\_заголовок запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**WINHTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-256">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="707b0-256">Obsolete.</span></span> <span data-ttu-id="707b0-257">Поддерживается для совместимости с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="707b0-257">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**\_Шифрование запросов \_ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**WINHTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-259">Возвращает тип преобразования, которое было применено к тексту сообщения, чтобы его можно было безопасно передать между отправителем и получателем.</span><span class="sxs-lookup"><span data-stu-id="707b0-259">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**запрос WINHTTP, \_ \_ если не \_ изменился \_ с**</span><span class="sxs-lookup"><span data-stu-id="707b0-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**WINHTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-261">Возвращает заголовок, за исключением "-Modified-с".</span><span class="sxs-lookup"><span data-stu-id="707b0-261">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**\_Обновление запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**WINHTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-263">Извлекает дополнительные протоколы связи, поддерживаемые сервером.</span><span class="sxs-lookup"><span data-stu-id="707b0-263">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**\_URI запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**WINHTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-265">Получает некоторые или все URI, на которые может быть идентифицирован ресурс Request-URI.</span><span class="sxs-lookup"><span data-stu-id="707b0-265">Receives some or all of the URI by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**\_ \_ Агент пользователя запросов \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**WINHTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-267">Извлекает сведения об агенте пользователя, который выполнил запрос.</span><span class="sxs-lookup"><span data-stu-id="707b0-267">Retrieves information about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**\_запрос WinHTTP \_ различается**</span><span class="sxs-lookup"><span data-stu-id="707b0-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WINHTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-269">Извлекает заголовок, указывающий, что сущность была выбрана из ряда доступных представлений ответа с помощью согласования на сервере.</span><span class="sxs-lookup"><span data-stu-id="707b0-269">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**\_версия запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**WINHTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-271">Возвращает версию HTTP, которая содержится в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="707b0-271">Retrieves the HTTP version that is present in the status line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**\_запрос WinHTTP \_ через**</span><span class="sxs-lookup"><span data-stu-id="707b0-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**WINHTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-273">Извлекает промежуточные протоколы и получателей между агентом пользователя и сервером по запросам, а также между сервером источника и клиентом в ответах.</span><span class="sxs-lookup"><span data-stu-id="707b0-273">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**\_предупреждение запроса \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="707b0-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**WINHTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-275">Извлекает дополнительные сведения о состоянии ответа, который может не отражаться кодом состояния отклика.</span><span class="sxs-lookup"><span data-stu-id="707b0-275">Retrieves additional information about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP \_ запрос \_ www \_ Проверка подлинности**</span><span class="sxs-lookup"><span data-stu-id="707b0-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-277">Извлекает схему проверки подлинности и область, возвращенные сервером.</span><span class="sxs-lookup"><span data-stu-id="707b0-277">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="707b0-278">Флаги модификатора используются вместе с флагом атрибута для изменения запроса.</span><span class="sxs-lookup"><span data-stu-id="707b0-278">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="707b0-279">Флаги модификатора либо изменяют формат возвращаемых данных, либо указывают, где функция [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) должна искать информацию.</span><span class="sxs-lookup"><span data-stu-id="707b0-279">Modifier flags either modify the format of the data returned or indicate where the [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) function should search for the information.</span></span>

<dl> <dt>

<span data-ttu-id="707b0-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**\_ \_ номер флага запроса WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**WINHTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-281">Возвращает данные в виде 32-разрядного числа для заголовков, значение которых является числом, например код состояния.</span><span class="sxs-lookup"><span data-stu-id="707b0-281">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**\_заголовки запросов \_ флагов запросов \_ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="707b0-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**WINHTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-283">Запросы заголовков запросов.</span><span class="sxs-lookup"><span data-stu-id="707b0-283">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="707b0-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**\_флаг запроса \_ WinHTTP \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="707b0-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**WINHTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="707b0-285">Возвращает значение заголовка в виде структуры [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) , которое не требует от приложения анализа данных.</span><span class="sxs-lookup"><span data-stu-id="707b0-285">Returns the header value as a [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="707b0-286">Используйте для заголовков, значение которых является строкой даты и времени, например "Last-Modified-Time".</span><span class="sxs-lookup"><span data-stu-id="707b0-286">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="707b0-287">Требования</span><span class="sxs-lookup"><span data-stu-id="707b0-287">Requirements</span></span>

| <span data-ttu-id="707b0-288">Требование</span><span class="sxs-lookup"><span data-stu-id="707b0-288">Requirement</span></span> | <span data-ttu-id="707b0-289">Значение</span><span class="sxs-lookup"><span data-stu-id="707b0-289">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="707b0-290">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="707b0-290">Minimum supported client</span></span> | <span data-ttu-id="707b0-291">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="707b0-291">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>      |
| <span data-ttu-id="707b0-292">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="707b0-292">Minimum supported server</span></span> | <span data-ttu-id="707b0-293">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="707b0-293">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>   |
| <span data-ttu-id="707b0-294">Заголовок</span><span class="sxs-lookup"><span data-stu-id="707b0-294">Header</span></span>                   | <dl> <span data-ttu-id="707b0-295"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="707b0-295"><dt>Winhttp.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="707b0-296">См. также</span><span class="sxs-lookup"><span data-stu-id="707b0-296">See also</span></span>

* [<span data-ttu-id="707b0-297">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="707b0-297">WinHTTP Versions</span></span>](winhttp-versions.md)
