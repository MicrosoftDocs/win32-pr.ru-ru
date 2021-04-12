---
description: Эти атрибуты и модификаторы используются WinHttpQueryHeaders.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Флаги сведений о запросе (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9ffc8f4ba4a947fe6fb277617c99460c43ffb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081007"
---
# <a name="query-info-flags-winhttph"></a>Флаги сведений о запросе (WinHTTP. h)

Эти атрибуты и модификаторы используются [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).

Флаги атрибута используются [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) для указания извлекаемой информации. Большинство флагов атрибутов сопоставляются непосредственно с конкретным заголовком HTTP. Также есть некоторые специальные флаги, такие как \_ \_ необработанные \_ заголовки запросов WinHTTP, которые не связаны с определенным заголовком.

<dl> <dt>

<span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**\_принятие запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Возвращает допустимые типы носителей для ответа.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**\_запрос WinHTTP \_ Accept \_ CharSet**
</dt> <dd> <dl> <dt>



Возвращает допустимые наборы символов для ответа.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**\_ \_ Кодировка Accept запроса WinHTTP \_**
</dt> <dd> <dl> <dt>



Извлекает приемлемые значения кодирования содержимого для ответа.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**\_ \_ язык принятия запросов \_ WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает допустимые естественные языки для ответа.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**\_ \_ диапазоны приема запросов WinHTTP \_**
</dt> <dd> <dl> <dt>



Возвращает типы запросов диапазона, которые принимаются для ресурса.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**\_возраст запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает поле "возраст ответа-заголовок", которое содержит оценку отправителя периода времени, прошедшее с момента создания ответа на исходном сервере.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**\_Разрешить запросы \_ WinHTTP**
</dt> <dd> <dl> <dt>



Получает [*HTTP-команду*](glossary.md)s, поддерживаемую сервером.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**\_ \_ сведения о проверке подлинности запросов WinHTTP \_**
</dt> <dd> <dl> <dt>



Извлекает заголовок Authentication-Info.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**\_ \_ авторизация запросов WinHTTP**
</dt> <dd> <dl> <dt>



Получает учетные данные авторизации, используемые для запроса.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**\_ \_ Управление КЭШЕМ запросов \_ WinHTTP**
</dt> <dd> <dl> <dt>



Получает директивы управления кэшем.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**\_соединение с запросом WinHTTP \_**
</dt> <dd> <dl> <dt>



Извлекает все параметры, указанные для конкретного соединения, и не должны передаваться через прокси-серверы при последующих соединениях.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**\_ \_ база содержимого запросов \_ WinHTTP**
</dt> <dd> <dl> <dt>



Получает базовый универсальный код ресурса (URI) для разрешения относительных URL-адресов внутри сущности.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**\_ \_ Описание содержимого запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Является устаревшей. Поддерживается для совместимости с устаревшими приложениями.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**\_ \_ расстановка содержимого запроса WinHTTP \_**
</dt> <dd> <dl> <dt>



Является устаревшей. Поддерживается для совместимости с устаревшими приложениями.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**\_ \_ кодирование содержимого запросов \_ WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает дополнительный код, примененный ко всему ресурсу.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**\_ \_ идентификатор содержимого запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Получает идентификацию содержимого.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**\_ \_ язык содержимого запросов \_ WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает язык, на котором написано содержимое.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**\_ \_ длина содержимого запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Возвращает размер ресурса в байтах.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**\_ \_ расположение содержимого запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Возвращает расположение ресурса для сущности, заключенной в сообщение.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**\_ \_ MD5 содержимого запросов \_ WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает дайджест MD5 тела сущности для предоставления сквозной проверки целостности сообщения для тела сущности. Дополнительные сведения см. в [документе RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**\_ \_ диапазон содержимого запросов \_ WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает расположение в полном тексте сущности, куда следует вставить частичный текст сущности, и общий размер полного тела сущности.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**\_ \_ \_ Кодировка для обмена СОДЕРЖИМым запросов WinHTTP \_**
</dt> <dd> <dl> <dt>



Получает преобразование кодирования, применимое к сущности-тексту. Возможно, он уже применен, может потребоваться применение или, возможно, он применим.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**\_ \_ тип содержимого запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Получает тип содержимого ресурса, например текст или HTML.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**\_ \_ файл Cookie запроса WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает все файлы cookie, связанные с запросом.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**\_стоимость запросов \_ WinHTTP**
</dt> <dd> <dl> <dt>



Не поддерживается.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**\_Пользовательский запрос \_ WinHTTP**
</dt> <dd> <dl> <dt>



Приводит к тому, что [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) ищет имя заголовка, указанное в параметре *pwszName* , и сохраняет сведения о заголовке в *лпбуффер*. Приложение может использовать **параметр WinHTTP \_ \_ \_ \_ время ожидания ответа** для ограничения максимального времени, в течение которого запрос ожидает получения всех заголовков.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**\_Дата запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Получает дату и время порождения сообщения.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**запрос WINHTTP, \_ \_ производный \_ от**
</dt> <dd> <dl> <dt>



Не поддерживается.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**\_ETag запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает тег сущности для связанной сущности.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**\_ \_ Ожидание запроса WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает заголовок Expect, который указывает, должен ли клиентское приложение получать ответы на серии 100.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**\_ \_ срок действия запроса WinHTTP истек**
</dt> <dd> <dl> <dt>



Получает дату и время, после которого ресурс должен считаться устаревшим.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**\_запрос WinHTTP \_ переадресован**
</dt> <dd> <dl> <dt>



Является устаревшей. Поддерживается для совместимости с устаревшими приложениями.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**\_запрос WinHTTP \_ от**
</dt> <dd> <dl> <dt>



Получает адрес электронной почты пользователя, управляющего запрашивающим [*агентом пользователя*](glossary.md) , если указан заголовок From.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**\_узел запросов \_ WinHTTP**
</dt> <dd> <dl> <dt>



Возвращает Интернет хост и номер порта запрашиваемого ресурса.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**\_запрос WinHTTP \_ при \_ совпадении**
</dt> <dd> <dl> <dt>



Извлекает содержимое поля заголовка запроса If-Match.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**запрос WINHTTP, \_ \_ Если \_ изменен \_ с**
</dt> <dd> <dl> <dt>



Извлекает содержимое заголовка If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**запрос WINHTTP, \_ \_ Если \_ ничего не \_ Найдено**
</dt> <dd> <dl> <dt>



Извлекает содержимое поля заголовка запроса If-None-Match.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**запрос WINHTTP, \_ \_ Если \_ диапазон**
</dt> <dd> <dl> <dt>



Извлекает содержимое поля заголовка запроса If-Range. Этот заголовок позволяет клиентскому приложению проверять, не обновлялась ли сущность, связанная с частичной копией сущности в кэше клиентского приложения. Если сущность не была обновлена, отправьте части, которые отсутствуют в клиентском приложении. Если сущность была обновлена, отправьте всю обновленную сущность.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**запрос WINHTTP, \_ \_ если не \_ изменен \_ с**
</dt> <dd> <dl> <dt>



Извлекает содержимое поля "If-Unmodified-with" в заголовке запроса.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**\_ссылка на запрос WinHTTP \_**
</dt> <dd> <dl> <dt>



Является устаревшей. Поддерживается для совместимости с устаревшими приложениями.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**\_ \_ Дата последнего изменения запроса WinHTTP \_**
</dt> <dd> <dl> <dt>



Получает дату и время последнего изменения ресурса. Дата и время определяются сервером.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**\_Расположение запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Получает абсолютный URI, используемый в заголовке ответа расположения.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**\_ \_ Максимальное число запросов WinHTTP**
</dt> <dd> <dl> <dt>



Указывает максимальное значение \_ значения запроса WinHTTP \_ \* . Не флаг запроса.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**\_ \_ Максимальное число \_ пересылаемых запросов WinHTTP**
</dt> <dd> <dl> <dt>



Возвращает число прокси-серверов или шлюзов, которые могут перенаправлять запрос на следующий Входящий сервер.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**\_ \_ идентификатор сообщения запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Не поддерживается.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**\_ \_ версия MIME запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Получает версию протокола MIME, которая использовалась для создания сообщения.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**\_ \_ URI orig запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Является устаревшей. Поддерживается для совместимости с устаревшими приложениями.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**\_pragma запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Получает директивы для конкретной реализации, которые могут применяться к любому получателю в цепочке запросов и ответов.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**\_ \_ Аутентификация прокси-сервера запросов WinHTTP \_**
</dt> <dd> <dl> <dt>



Извлекает схему проверки подлинности и область, возвращенную прокси-сервером.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**\_ \_ авторизация прокси-сервера запросов WinHTTP \_**
</dt> <dd> <dl> <dt>



Извлекает заголовок, который используется для идентификации пользователя на прокси-сервере, требующем проверки подлинности. Этот заголовок может быть получен только до отправки запроса на сервер.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**\_ \_ Подключение прокси-сервера запросов WinHTTP \_**
</dt> <dd> <dl> <dt>



Извлекает заголовок Proxy-Connection.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**\_ \_ Поддержка прокси-сервера запросов WinHTTP \_**
</dt> <dd> <dl> <dt>



Извлекает заголовок Proxy-Support.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**\_открытый запрос \_ WinHTTP**
</dt> <dd> <dl> <dt>



Получает HTTP-команды, доступные на этом сервере.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**\_диапазон запросов \_ WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает диапазон байтов сущности.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**\_ \_ необработанные \_ заголовки запросов WinHTTP**
</dt> <dd> <dl> <dt>



Получает все заголовки, возвращенные сервером. Каждый заголовок завершается " \\ 0". Дополнительный " \\ 0" завершает список заголовков.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**\_запросы WinHTTP \_ необработанных \_ заголовков \_ CRLF**
</dt> <dd> <dl> <dt>



Получает все заголовки, возвращенные сервером. Каждый заголовок отделяется последовательностью возврата каретки/перевода строки (CR/LF).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**\_ \_ ссылка на запрос WinHTTP**
</dt> <dd> <dl> <dt>



Получает URI ресурса, в котором был получен запрошенный URI.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**\_Обновление запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Является устаревшей. Поддерживается для совместимости с устаревшими приложениями.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**\_ \_ метод запроса WinHTTP \_**
</dt> <dd> <dl> <dt>



Получает HTTP-команду, которая используется в запросе, обычно GET или POST.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**\_Повтор запроса WinHTTP \_ \_ после**
</dt> <dd> <dl> <dt>



Возвращает количество времени, в течение которого служба должна быть недоступна.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**\_сервер запросов \_ WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает сведения о программном обеспечении, используемом сервером источника для выполнения запроса.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**\_ \_ файл cookie набора запросов WinHTTP \_**
</dt> <dd> <dl> <dt>



Получает значение набора файлов cookie для запроса.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**\_ \_ код состояния запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Получает код состояния, возвращенный сервером. Список возможных значений см. в разделе [**коды состояния HTTP**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**\_ \_ текст состояния запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Получает дополнительный текст, возвращенный сервером в строке ответа.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**\_заголовок запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Является устаревшей. Поддерживается для совместимости с устаревшими приложениями.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**\_Шифрование запросов \_ WinHTTP \_**
</dt> <dd> <dl> <dt>



Возвращает тип преобразования, которое было применено к тексту сообщения, чтобы его можно было безопасно передать между отправителем и получателем.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**запрос WINHTTP, \_ \_ если не \_ изменился \_ с**
</dt> <dd> <dl> <dt>



Возвращает заголовок, за исключением "-Modified-с".


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**\_Обновление запросов \_ WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает дополнительные протоколы связи, поддерживаемые сервером.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**\_URI запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Получает некоторые или все URI, на которые может быть идентифицирован ресурс Request-URI.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**\_ \_ Агент пользователя запросов \_ WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает сведения об агенте пользователя, который выполнил запрос.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**\_запрос WinHTTP \_ различается**
</dt> <dd> <dl> <dt>



Извлекает заголовок, указывающий, что сущность была выбрана из ряда доступных представлений ответа с помощью согласования на сервере.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**\_версия запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Возвращает версию HTTP, которая содержится в строке состояния.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**\_запрос WinHTTP \_ через**
</dt> <dd> <dl> <dt>



Извлекает промежуточные протоколы и получателей между агентом пользователя и сервером по запросам, а также между сервером источника и клиентом в ответах.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**\_предупреждение запроса \_ WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает дополнительные сведения о состоянии ответа, который может не отражаться кодом состояния отклика.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP \_ запрос \_ www \_ Проверка подлинности**
</dt> <dd> <dl> <dt>



Извлекает схему проверки подлинности и область, возвращенные сервером.


</dt> </dl> </dd> </dl>

Флаги модификатора используются вместе с флагом атрибута для изменения запроса. Флаги модификатора либо изменяют формат возвращаемых данных, либо указывают, где функция [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) должна искать информацию.

<dl> <dt>

<span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**\_ \_ номер флага запроса WinHTTP \_**
</dt> <dd> <dl> <dt>



Возвращает данные в виде 32-разрядного числа для заголовков, значение которых является числом, например код состояния.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**\_заголовки запросов \_ флагов запросов \_ WinHTTP \_**
</dt> <dd> <dl> <dt>



Запросы заголовков запросов.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**\_флаг запроса \_ WinHTTP \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>



Возвращает значение заголовка в виде структуры [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , которое не требует от приложения анализа данных. Используйте для заголовков, значение которых является строкой даты и времени, например "Last-Modified-Time".


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>      |
| Минимальная версия сервера<br/> | Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>   |
| Header<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Версии WinHTTP](winhttp-versions.md)
</dt> </dl>

 

