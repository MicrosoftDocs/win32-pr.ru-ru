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
# <a name="query-info-flags-winineth"></a>Флаги сведений о запросе (WinInet. h)

Следующие списки содержат атрибуты и модификаторы, используемые [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) и [**куеринфо**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).

Флаги атрибутов используются [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (или [**куеринфо**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) для указания извлекаемых данных. Большинство флагов атрибутов сопоставляются непосредственно с конкретным заголовком HTTP. Также есть некоторые специальные флаги, такие как [ \_ \_ необработанные \_ заголовки HTTP-запросов](/windows), которые не связаны с определенным заголовком.

<dl> <dt>

<span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**принятие HTTP- \_ запроса \_**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Возвращает допустимые типы носителей для ответа.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**\_запрос HTTP \_ Accept \_ CharSet**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Возвращает допустимые наборы символов для ответа.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**\_ \_ Кодировка приема HTTP-запроса \_**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Извлекает приемлемые значения кодирования содержимого для ответа.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**\_ \_ язык приема HTTP-запросов \_**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Извлекает допустимые естественные языки для ответа.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**\_ \_ диапазоны приема HTTP-запросов \_**
</dt> <dd> <dl> <dt>

42
</dt> <dt>



Возвращает типы запросов диапазона, которые принимаются для ресурса.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**\_ \_ срок действия HTTP-запроса**
</dt> <dd> <dl> <dt>

48
</dt> <dt>



Извлекает поле "возраст ответа-заголовок", которое содержит оценку отправителя периода времени, прошедшее с момента создания ответа на сервере-источнике.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**разрешить HTTP- \_ запрос \_**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Получает HTTP-команды, поддерживаемые сервером.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**\_авторизация HTTP-запросов \_**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Получает учетные данные авторизации, используемые для запроса.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**\_ \_ Управление кэшем HTTP-запросов \_**
</dt> <dd> <dl> <dt>

49
</dt> <dt>



Получает директивы управления кэшем.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**подключение HTTP- \_ запросов \_**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Извлекает все параметры, указанные для конкретного соединения, и не должны передаваться через прокси-серверы при последующих соединениях.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**\_ \_ база содержимого HTTP-запроса \_**
</dt> <dd> <dl> <dt>

50
</dt> <dt>



Извлекает базовый URI (универсальный идентификатор ресурса) для разрешения относительных URL-адресов в сущности.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**\_ \_ Описание содержимого HTTP-запроса \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Является устаревшей. Поддерживается только для совместимости с устаревшими приложениями.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**\_ \_ расположение содержимого HTTP-запроса \_**
</dt> <dd> <dl> <dt>

47
</dt> <dt>



Является устаревшей. Поддерживается только для совместимости с устаревшими приложениями.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**\_ \_ Кодировка содержимого HTTP-запросов \_**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Извлекает все дополнительные кодеки содержимого, которые были применены ко всему ресурсу.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**\_ \_ идентификатор содержимого HTTP-запроса \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Получает идентификацию содержимого.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**\_ \_ язык содержимого HTTP-запросов \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Извлекает язык, в котором находится содержимое.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**\_ \_ длина содержимого HTTP-запроса \_**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Возвращает размер ресурса в байтах.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**\_ \_ расположение содержимого HTTP-запроса \_**
</dt> <dd> <dl> <dt>

51
</dt> <dt>



Возвращает расположение ресурса для сущности, заключенной в сообщение.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**\_ \_ MD5 содержимого HTTP-запросов \_**
</dt> <dd> <dl> <dt>

52
</dt> <dt>



Извлекает дайджест MD5 из тела сущности для предоставления сквозной проверки целостности сообщений (MIC) для объекта-тела. Дополнительные сведения см. в разделе RFC1864, поле заголовка Content-MD5 в [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**\_ \_ диапазон содержимого HTTP-запроса \_**
</dt> <dd> <dl> <dt>

53
</dt> <dt>



Извлекает расположение в полном тексте сущности, где следует вставить частичную сущность-текст, и общий размер полного тела сущности.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**\_ \_ \_ Кодировка обмена содержимым HTTP-запросов \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Получает дополнительный код содержимого, примененный к ресурсу.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**\_ \_ тип содержимого HTTP-запроса \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Получает тип содержимого ресурса (например, text/html).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**\_ \_ файл cookie HTTP-запроса**
</dt> <dd> <dl> <dt>

44
</dt> <dt>



Извлекает все файлы cookie, связанные с запросом.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**Стоимость HTTP- \_ запроса \_**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Больше не поддерживается.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**пользовательский HTTP- \_ запрос \_**
</dt> <dd> <dl> <dt>

65535
</dt> <dt>



Приводит к тому, что [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) ищет имя заголовка, указанное в *лпвбуффер* , и сохраняет данные заголовка в *лпвбуффер*.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**\_Дата запроса \_ http**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Получает дату и время порождения сообщения.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**HTTP- \_ запрос, \_ производный \_ от**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Больше не поддерживается.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**\_ \_ заголовки эхо-запросов HTTP \_**
</dt> <dd> <dl> <dt>

73
</dt> <dt>



В настоящий момент не реализовано.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**\_заголовки эхо-запросов HTTP \_ \_ \_ CRLF**
</dt> <dd> <dl> <dt>

74
</dt> <dt>



В настоящий момент не реализовано.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**ответ HTTP- \_ запроса \_ echo \_**
</dt> <dd> <dl> <dt>

72
</dt> <dt>



В настоящий момент не реализовано.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**запрос HTTP- \_ запроса \_ echo \_**
</dt> <dd> <dl> <dt>

71
</dt> <dt>



В настоящий момент не реализовано.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**ETag HTTP- \_ запроса \_**
</dt> <dd> <dl> <dt>

54
</dt> <dt>



Извлекает тег сущности для связанной сущности.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**\_Ожидание HTTP-запроса \_**
</dt> <dd> <dl> <dt>

68
</dt> <dt>



Извлекает заголовок Expect, который указывает, должен ли клиентское приложение получать ответы на серии 100.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**\_срок действия HTTP-запроса \_ истек**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Получает дату и время, после которого ресурс должен считаться устаревшим.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**HTTP- \_ запрос \_ переадресован**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Является устаревшей. Поддерживается только для совместимости с устаревшими приложениями.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**HTTP- \_ запрос \_ из**
</dt> <dd> <dl> <dt>

31
</dt> <dt>



Получает адрес электронной почты пользователя, управляющего запрашивающим агентом пользователя, если указан заголовок From.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**узел HTTP- \_ запросов \_**
</dt> <dd> <dl> <dt>

55
</dt> <dt>



Возвращает Интернет хост и номер порта запрашиваемого ресурса.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**HTTP- \_ запрос \_ при \_ совпадении**
</dt> <dd> <dl> <dt>

56
</dt> <dt>



Извлекает содержимое поля заголовка запроса If-Match.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**HTTP- \_ запрос, \_ \_ измененный \_ с момента**
</dt> <dd> <dl> <dt>

32
</dt> <dt>



Извлекает содержимое заголовка If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**HTTP- \_ запрос, \_ Если ничего не \_ \_ Найдено**
</dt> <dd> <dl> <dt>

57
</dt> <dt>



Извлекает содержимое поля заголовка запроса If-None-Match.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP- \_ запрос, \_ Если \_ диапазон**
</dt> <dd> <dl> <dt>

58
</dt> <dt>



Извлекает содержимое поля заголовка запроса If-Range. Этот заголовок позволяет клиентскому приложению проверять, что сущность, связанная с частичной копией сущности в кэше клиентского приложения, не обновлена. Если сущность не была обновлена, отправьте части, которые отсутствуют в клиентском приложении. Если сущность была обновлена, отправьте всю обновленную сущность.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**HTTP-запрос, если он не \_ \_ \_ изменен \_ с**
</dt> <dd> <dl> <dt>

59
</dt> <dt>



Извлекает содержимое поля "If-Unmodified-with" в заголовке запроса.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_ \_ Дата последнего \_ изменения HTTP-запроса**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Получает дату и время, когда сервер считает, что ресурс был изменен последним.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**Ссылка HTTP- \_ запроса \_**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Является устаревшей. Поддерживается только для совместимости с устаревшими приложениями.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**расположение HTTP- \_ запроса \_**
</dt> <dd> <dl> <dt>

33
</dt> <dt>



Возвращает абсолютный универсальный идентификатор ресурса (URI), используемый в заголовке Response-Header.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**\_ \_ Максимальное число HTTP-запросов**
</dt> <dd> <dl> <dt>

78
</dt> <dt>



Не флаг запроса. Указывает максимальное значение HTTP- \_ запроса \_ \* .


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**\_ \_ Максимальное число \_ пересылаемых запросов HTTP**
</dt> <dd> <dl> <dt>

60
</dt> <dt>



Возвращает число прокси-серверов или шлюзов, которые могут перенаправлять запрос на следующий Входящий сервер.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**\_ \_ идентификатор сообщения HTTP-запроса \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Больше не поддерживается.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**\_ \_ версия MIME HTTP-запроса \_**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Получает версию протокола MIME, которая использовалась для создания сообщения.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**\_ \_ \_ универсальный код ресурса HTTP-запроса orig**
</dt> <dd> <dl> <dt>

34
</dt> <dt>



Является устаревшей. Поддерживается только для совместимости с устаревшими приложениями.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**PRAGMA HTTP- \_ запроса \_**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Получает директивы для конкретной реализации, которые могут применяться к любому получателю в цепочке запросов и ответов.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**\_ \_ \_ Проверка подлинности прокси HTTP-запроса**
</dt> <dd> <dl> <dt>

41
</dt> <dt>



Извлекает схему проверки подлинности и область, возвращенную прокси-сервером.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**\_ \_ авторизация прокси-сервера запросов HTTP \_**
</dt> <dd> <dl> <dt>

61
</dt> <dt>



Извлекает заголовок, который используется для идентификации пользователя на прокси-сервере, требующем проверки подлинности. Этот заголовок может быть получен только до отправки запроса на сервер.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**\_ \_ соединение прокси-сервера запросов HTTP \_**
</dt> <dd> <dl> <dt>

69
</dt> <dt>



Извлекает заголовок Proxy-Connection.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**общедоступный HTTP- \_ запрос \_**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Получает методы, доступные на этом сервере.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**диапазон HTTP- \_ запросов \_**
</dt> <dd> <dl> <dt>

62
</dt> <dt>



Извлекает диапазон байтов сущности.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**\_ \_ заголовки необработанных HTTP-запросов \_**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Получает все заголовки, возвращенные сервером. Каждый заголовок завершается " \\ 0". Дополнительный " \\ 0" завершает список заголовков.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**заголовки HTTP- \_ запросов \_ \_ \_ CRLF**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Получает все заголовки, возвращенные сервером. Каждый заголовок отделяется последовательностью возврата каретки/перевода строки (CR/LF).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**Ссылка HTTP- \_ запроса \_**
</dt> <dd> <dl> <dt>

35
</dt> <dt>



Получает универсальный код ресурса (URI) ресурса, в котором был получен запрошенный URI.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**Обновление HTTP- \_ запроса \_**
</dt> <dd> <dl> <dt>

46
</dt> <dt>



Является устаревшей. Поддерживается только для совместимости с устаревшими приложениями.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**\_ \_ метод запроса HTTP-запроса \_**
</dt> <dd> <dl> <dt>

45
</dt> <dt>



Получает HTTP-команду, которая используется в запросе, обычно GET или POST.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**Повтор HTTP- \_ запроса \_ \_ после**
</dt> <dd> <dl> <dt>

36
</dt> <dt>



Возвращает количество времени, в течение которого служба должна быть недоступна.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**сервер HTTP- \_ запросов \_**
</dt> <dd> <dl> <dt>

37
</dt> <dt>



Извлекает данные о программном обеспечении, используемом сервером источника для выполнения запроса.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**\_ \_ файл cookie для набора HTTP-запросов \_**
</dt> <dd> <dl> <dt>

43
</dt> <dt>



Получает значение набора файлов cookie для запроса.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**\_ \_ код состояния HTTP-запроса \_**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Получает код состояния, возвращенный сервером. Дополнительные сведения и список возможных значений см. в разделе [**коды состояния HTTP**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**\_ \_ текст состояния HTTP-запроса \_**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Получает дополнительный текст, возвращенный сервером в строке ответа.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**заголовок HTTP- \_ запроса \_**
</dt> <dd> <dl> <dt>

38
</dt> <dt>



Является устаревшей. Поддерживается только для совместимости с устаревшими приложениями.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**кодирование HTTP- \_ запросов \_ \_**
</dt> <dd> <dl> <dt>

63
</dt> <dt>



Возвращает тип преобразования, которое было применено к тексту сообщения, чтобы его можно было безопасно передать между отправителем и получателем.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**HTTP- \_ запрос, \_ если не \_ изменился \_ с**
</dt> <dd> <dl> <dt>

70
</dt> <dt>



Возвращает заголовок, за исключением "-Modified-с".


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**Обновление HTTP- \_ запроса \_**
</dt> <dd> <dl> <dt>

64
</dt> <dt>



Извлекает дополнительные протоколы связи, поддерживаемые сервером.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**URI HTTP- \_ запроса \_**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Получает некоторые или все универсальные идентификаторы ресурсов (URI), на которые может быть идентифицирован ресурс Request-URI.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**\_ \_ Агент пользователя HTTP-запросов \_**
</dt> <dd> <dl> <dt>

39
</dt> <dt>



Извлекает данные о агенте пользователя, который выполнил запрос.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**\_запрос HTTP \_ vary**
</dt> <dd> <dl> <dt>

65
</dt> <dt>



Извлекает заголовок, указывающий, что сущность была выбрана из ряда доступных представлений ответа с помощью согласования на сервере.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**Версия HTTP- \_ запроса \_**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Получает последний код ответа, возвращенный сервером.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**HTTP- \_ запрос \_ через**
</dt> <dd> <dl> <dt>

66
</dt> <dt>



Извлекает промежуточные протоколы и получателей между агентом пользователя и сервером по запросам, а также между сервером источника и клиентом в ответах.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**предупреждение HTTP- \_ запроса \_**
</dt> <dd> <dl> <dt>

67
</dt> <dt>



Извлекает дополнительные данные о состоянии ответа, который может не отражаться кодом состояния отклика.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**\_ \_ \_ Проверка подлинности веб-запросов HTTP**
</dt> <dd> <dl> <dt>

40
</dt> <dt>



Извлекает схему проверки подлинности и область, возвращенные сервером.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**\_ \_ \_ \_ Параметры типа содержимого HTTP-запроса X \_**
</dt> <dd> <dl> <dt>

79
</dt> <dt>



Извлекает значение заголовка X-Content-Type-Options.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**\_Запрос HTTP \_ P3P**
</dt> <dd> <dl> <dt>

80
</dt> <dt>



Извлекает значение заголовка P3P.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP- \_ запрос \_ X \_ P2P \_ , то**
</dt> <dd> <dl> <dt>

81
</dt> <dt>



Извлекает значение заголовка X-P2P-,


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**Преобразование HTTP- \_ запросов \_**
</dt> <dd> <dl> <dt>

82
</dt> <dt>



Получает значение заголовка преобразования.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP- \_ запрос \_ X UA, \_ \_ совместимый**
</dt> <dd> <dl> <dt>

83
</dt> <dt>



Извлекает значение заголовка, совместимое с X-UA-Compatible.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**стиль HTTP- \_ запроса \_ по умолчанию \_**
</dt> <dd> <dl> <dt>

84
</dt> <dt>



Возвращает значение заголовка Default-Style.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**Параметры кадра HTTP- \_ запроса \_ X \_ \_**
</dt> <dd> <dl> <dt>

85
</dt> <dt>



Извлекает значение заголовка X-Frame-Options.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP \_ - \_ запрос \_ X \_ Защита XSS**
</dt> <dd> <dl> <dt>

86
</dt> <dt>



Извлекает значение заголовка X-XSS-Protection.


</dt> </dl> </dd> </dl>

Флаги модификатора используются вместе с флагом атрибута для изменения запроса. Флаги модификатора либо изменяют формат возвращаемых данных, либо указывают, где [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (или [**куеринфо**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) должны искать данные.

<dl> <dt>

<span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**\_ \_ объединение ФЛАГОВ HTTP-запросов \_**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Не реализован.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**\_ \_ номер флага http-запроса \_**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Возвращает данные в виде 32-разрядного числа для заголовков, значение которых является числом, например код состояния.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**\_заголовки запросов \_ ФЛАГОВ HTTP-запросов \_ \_**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Запросы заголовков запросов.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**Флаг HTTP- \_ запроса \_ \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Возвращает значение заголовка в виде структуры [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , которое не требует от приложения анализа данных. Используйте для заголовков, значение которых является строкой даты и времени, например "Last-Modified-Time".


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



 

