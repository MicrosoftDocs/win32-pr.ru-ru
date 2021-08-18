---
description: значения ошибок, определенные в этом разделе, возвращаются функцией GetLastError при сбое одной из функций служб Microsoft Windows HTTP (WinHTTP).
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Сообщения об ошибках (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d83fa1859f071b0fc0e651235deea51626f55b8a45cdb2a3ea8736a57317741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744720"
---
# <a name="error-messages-winhttph"></a>Сообщения об ошибках (WinHTTP. h)

приведенные ниже значения ошибок возвращаются функцией [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) , если одна из функций служб Microsoft Windows HTTP (WinHTTP) завершается с ошибкой, а также возвращаются в младших 16 битах [**из объекта**](../com/structure-of-com-error-codes.md) [**WinHttpRequest**](winhttprequest.md) .

Значения ошибок, имена которых начинаются с "ERROR \_ WinHTTP \_ ", относятся к функциям WinHTTP. функции WinHTTP также возвращают Windows сообщения об ошибках, если это уместно.

<dl> <dt>

<span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**Ошибка \_ \_ службы автоматического \_ прокси-сервера WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12178
</dt> <dt>



Возвращается функцией [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) , если не удается найти прокси-сервер для указанного URL-адреса.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**Ошибка \_ \_ при автообнаружении WinHTTP \_**
</dt> <dd> <dl> <dt>

12180
</dt> <dt>



Возвращается функцией [**винхттпдетектаутопроксиконфигурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) , если службе WinHTTP не удалось обнаружить URL-адрес файла автоматической настройки прокси-сервера (PAC).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**Ошибка \_ WinHTTP \_ неверный \_ \_ Скрипт автоматического прокси \_**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Произошла ошибка при исполнении кода скрипта в файле автоматической настройки прокси-сервера (PAC).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**Ошибка \_ WinHTTP \_ не удается \_ вызвать \_ после \_ открытия**
</dt> <dd> <dl> <dt>

12103
</dt> <dt>



Возвращается объектом [**HttpRequest**](winhttprequest.md) , если не удается запросить указанный параметр после вызова метода [**Open**](iwinhttprequest-open.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**Ошибка \_ WinHTTP \_ не удается \_ вызвать \_ после \_ отправки**
</dt> <dd> <dl> <dt>

12102
</dt> <dt>



Возвращается объектом [**HttpRequest**](winhttprequest.md) , если не удается выполнить запрошенную операцию после вызова метода [**Send**](iwinhttprequest-send.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**Ошибка \_ WinHTTP \_ не может \_ вызвать \_ перед \_ открытием**
</dt> <dd> <dl> <dt>

12100
</dt> <dt>



Возвращается объектом [**HttpRequest**](winhttprequest.md) , если не удается выполнить запрошенную операцию до вызова метода [**Open**](iwinhttprequest-open.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**Ошибка \_ WinHTTP \_ не может \_ вызвать \_ перед \_ отправкой**
</dt> <dd> <dl> <dt>

12101
</dt> <dt>



Возвращается объектом [**HttpRequest**](winhttprequest.md) , если не удается выполнить запрошенную операцию до вызова метода [**Send**](iwinhttprequest-send.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**Ошибка \_ WinHTTP \_ не удается \_ подключиться**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Возвращается при сбое соединения с сервером.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**Ошибка \_ \_ \_ требуется сертификат проверки подлинности клиента WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Сервер требует проверки подлинности клиента SSL. Приложение получает список издателей сертификатов, вызывая [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) с параметром **WinHTTP Certificate \_ \_ Client \_ CERT \_ \_ List** . Дополнительные сведения см. в описании параметра **WinHTTP Certificate \_ \_ Client \_ CERT \_ Issuer \_** .

Если сервер запрашивает сертификат клиента, но не требует его, приложение может дополнительно вызвать [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) с параметром **\_ контекста WinHTTP параметр \_ \_ сертификата \_ клиента** . В этом случае в приложении указывается \_ \_ Контекстный макрос WinHTTP No Client Certificate \_ \_ в параметре *лпбуффер* объекта **винхттпсетоптион**. Дополнительные сведения см. в описании параметра службы **WinHTTP \_ параметр \_ \_ \_ контекста сертификата клиента** .

**Windows Server 2003 с пакетом обновления 1 и Windows XP с пакетом обновления 2 (SP2):** Эта ошибка не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**Ошибка \_ WinHTTP \_ \_ сертификат клиента \_ без \_ доступа \_ закрытый \_ ключ**
</dt> <dd> <dl> <dt>



У приложения нет необходимых привилегий для доступа к закрытому ключу, связанному с сертификатом клиента.

**Windows Server 2003 с пакетом обновления 1 и Windows XP с пакетом обновления 2 (SP2):** Эта ошибка не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**Ошибка \_ WinHTTP \_ \_ сертификат клиента \_ без \_ закрытого \_ ключа**
</dt> <dd> <dl> <dt>



Контекст для SSL-сертификата клиента не связан с закрытым ключом. Сертификат клиента мог быть импортирован на компьютер без закрытого ключа.

**Windows Server 2003 с пакетом обновления 1 и Windows XP с пакетом обновления 2 (SP2):** Эта ошибка не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**Ошибка \_ при \_ \_ \_ \_ переполнении размера заголовка фрагментированной кодировки WinHTTP \_**
</dt> <dd> <dl> <dt>

12183
</dt> <dt>



Возвращается функцией [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) при обнаружении условия переполнения в процессе синтаксического анализа фрагментированной кодировки.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**Ошибка \_ \_ \_ требуется сертификат проверки подлинности клиента WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



Возвращается функцией [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) , когда сервер запрашивает проверку подлинности клиента.

**Windows Server 2003 с пакетом обновления 1 и Windows XP с пакетом обновления 2 (SP2):** Эта ошибка не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**Ошибка \_ \_ подключения WinHTTP \_**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



Подключение к серверу было сброшено или прервано, или обнаружен несовместимый протокол SSL. Например, служба WinHTTP версии 5,1 не поддерживает SSL2, если только клиент явно не включит ее.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**\_заголовок ошибки \_ WinHTTP \_ уже \_ существует**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Устаревшие больше не используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**Ошибка \_ при \_ \_ превышении числа заголовков WinHTTP \_**
</dt> <dd> <dl> <dt>

12181
</dt> <dt>



Возвращается функцией [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) , если в ответе было больше заголовков, чем может получить WinHTTP.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена заголовок WinHTTP**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



Не удается найти запрошенный заголовок.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**Ошибка \_ \_ \_ переполнения размера заголовка WinHTTP \_**
</dt> <dd> <dl> <dt>

12182
</dt> <dt>



Возвращается функцией [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) , если размер полученных заголовков превышает предельное значение для маркера запроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**Ошибка \_ WinHTTP \_ неправильное \_ состояние обработчика \_**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



Не удается выполнить запрошенную операцию, так как указанный обработчик находится в неправильном состоянии.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**Ошибка \_ WinHTTP \_ неверный \_ тип обработчика \_**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



Для этой операции указан недопустимый тип обработчика.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**Ошибка \_ \_ внутренней \_ ошибки WinHTTP**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Произошла внутренняя ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**Ошибка \_ WinHTTP \_ Недопустимый \_ параметр**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Запрос к [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) или [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) указал недопустимое значение параметра.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**Ошибка \_ WinHTTP \_ Недопустимый \_ \_ запрос запроса**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



Устаревшие больше не используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**Ошибка \_ WinHTTP \_ Недопустимый \_ \_ ответ сервера**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



Не удается выполнить синтаксический анализ ответа сервера.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**Ошибка \_ WinHTTP \_ Недопустимый \_ URL-адрес**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



URL-адрес является недопустимым.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**Ошибка \_ \_ при попытке входа WinHTTP \_**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



Ошибка при попытке входа. При обнаружении этой ошибки обработчик запроса должен быть закрыт с помощью [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle). Перед повторной попыткой функции, вызвавшей эту ошибку, должен быть создан новый обработчик запроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**Ошибка \_ \_ имя WinHTTP \_ не \_ разрешено**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



Не удается разрешить имя сервера.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**Ошибка \_ WinHTTP \_ не \_ инициализирована**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



Устаревшие больше не используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**Ошибка \_ \_ операции WinHTTP \_ отменена**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



Операция была отменена, как правило, из-за того, что обработчик, на котором был запущен запрос, был закрыт до завершения операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**Ошибка \_ , \_ \_ не устанавливаемая параметром WinHTTP \_**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



Невозможно задать запрошенный параметр, выполняется только запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**Ошибка \_ WinHTTP \_ вне \_ \_ дескрипторов**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



Устаревшие больше не используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**Ошибка \_ \_ при перенаправлении WinHTTP \_**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



Перенаправление завершилось сбоем, так как либо изменилась схема, либо все попытки перенаправления завершились неудачей (по умолчанию пять попыток).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**Ошибка \_ \_ запроса повторной отправки WinHTTP \_**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



Сбой функции WinHTTP. Нужная функция может быть выполнена повторно с тем же маркером запроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**Ошибка \_ \_ \_ переполнения очистки ответа WinHTTP \_**
</dt> <dd> <dl> <dt>

12184
</dt> <dt>



Возвращается, когда входящий ответ превышает ограничение внутреннего размера WinHTTP.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**Ошибка \_ \_ при выполнении скрипта WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12177
</dt> <dt>



При выполнении скрипта произошла ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**Ошибка \_ WinHTTP \_ \_ \_ \_ Недопустимый CN Secure CERT**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



Возвращается, если различающееся имя сертификата не соответствует переданному значению (что эквивалентно ошибке " **\_ \_ CN \_ без \_ сопоставления" сертификата E** ).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**Ошибка \_ \_ \_ \_ Недопустимая дата безопасного сертификата WinHTTP \_**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



Указывает, что требуемый сертификат не находится в течение срока действия при проверке по текущему системному времени или отметке времени в подписанном файле, а также в том, что срок действия цепочки сертификатов не вкладывается правильно (аналогично **сертификату \_ электронной почты с \_ истекшим** периодом действия или валидитипериоднестинг ошибке **CERT \_ e \_** ).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**Ошибка \_ \_ \_ \_ \_ при попытке установить безопасный сертификат WinHTTP**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Указывает, что отзыв не может быть проверен, так как сервер отзыва был отключен (что эквивалентно **шифрованию \_ \_ отзыва \_ E**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**Ошибка \_ при \_ \_ отзыве безопасного сертификата WinHTTP \_**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Указывает, что сертификат был отозван (эквивалентно **шифрованию \_ E \_ REVOKE**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**Ошибка \_ при \_ \_ \_ неправильном \_ использовании безопасного сертификата WinHTTP**
</dt> <dd> <dl> <dt>

12179
</dt> <dt>



Указывает, что сертификат недействителен для запрошенного использования (аналогично **\_ \_ неправильному \_ использованию CERT E**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**Ошибка \_ при \_ \_ ошибке безопасного канала WinHTTP \_**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



Указывает, что при возникновении ошибки в защищенном канале (эквиваленты кодам ошибок, которые начинаются с "с \_ E \_ " и "сек \_ I", \_ перечисленные в файле заголовка Winerror. h).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**Ошибка \_ \_ безопасного \_ сбоя WinHTTP**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



В сертификате SSL (SSL), отправленном сервером, обнаружена одна или несколько ошибок. Чтобы определить тип обнаруженной ошибки, проверьте [**\_ состояние обратного вызова WinHTTP на \_ \_ \_**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) наличие уведомления о сбое в функции обратного вызова состояния. Дополнительные сведения см. в [**разделе \_ \_ обратный вызов состояния WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**Ошибка \_ WinHTTP \_ безопасный \_ Недопустимый \_ ЦС**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



Указывает, что цепочка сертификатов была обработана, но была прервана в корневом сертификате, который не является доверенным для поставщика доверия (эквивалентно **CERT \_ E \_ унтрустедрут**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**Ошибка \_ WinHTTP \_ безопасный \_ Недопустимый \_ сертификат**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



Указывает, что сертификат является недопустимым (аналогично таким ошибкам, как **\_ \_ роль CERT e**, **CERT \_ e \_ пасленконст**, **CERT \_ e \_ Critical**, **CERT \_ e \_**, **CERT \_ e \_ иссуерчаининг**, **CERT \_ e \_ неправильный формат** и **\_ \_ цепочка сертификатов e**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**Ошибка \_ при \_ завершении работы WinHTTP**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



Поддержка функции WinHTTP завершается или выгружается.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**Ошибка \_ при \_ истечении времени ожидания WinHTTP**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



Истекло время ожидания запроса.

эта ошибка может быть возвращена в результате истечения времени ожидания TCP/IP независимо от значений времени ожидания, заданных в Windows служб HTTP.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**Ошибка \_ WinHTTP \_ не \_ удалось \_ скачать \_ Скрипт**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



Не удается скачать файл PAC. Например, сервер, на который ссылается URL-адрес PAC, может быть недоступен, или сервер вернул ответ 404 не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**Ошибка \_ \_ необработанного \_ типа скрипта WinHTTP \_**
</dt> <dd> <dl> <dt>

12176
</dt> <dt>



Тип скрипта не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**Ошибка \_ WinHTTP \_ Нераспознанная \_ схема**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



В URL-адресе указана схема, отличная от "http:" или "https:".


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**Ошибка \_ не \_ хватает \_ памяти**
</dt> <dd> <dl> <dt>



Недостаточно памяти для завершения запрошенной операции.

**Заголовок:** Объявлено в файле Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**Ошибка \_ недостаточного \_ буфера**
</dt> <dd> <dl> <dt>



Размер (в байтах) буфера, предоставленного функции, недостаточно для того, чтобы он содержал возвращенные данные. Дополнительные сведения см. в разделе конкретная функция.

**Заголовок:** Объявлено в файле Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**Ошибка \_ недопустимого \_ маркера**
</dt> <dd> <dl> <dt>



Маркер, переданный в интерфейс прикладного программирования (API), был либо недействительным, либо закрытым.

**Заголовок:** Объявлено в файле Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**Ошибка \_ больше \_ нет \_ файлов**
</dt> <dd> <dl> <dt>



Больше файлов не найдено.

**Заголовок:** Объявлено в файле Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**Ошибка \_ больше \_ нет \_ элементов**
</dt> <dd> <dl> <dt>



Больше элементов не найдено.

**Заголовок:** Объявлено в файле Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**Ошибка \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>



Необходимый стек протокола не загружен, и приложение не может запустить WinSock.

**Заголовок:** Объявлено в файле Winerror. h


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

сведения о Windows XP и Windows 2000 см. в разделе [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHttp.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с SP3 \[ только для настольных приложений\]<br/>            |
| Минимальная версия сервера<br/> | Windows сервер 2003, Windows 2000 server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>         |
| Распространяемые компоненты<br/>          | WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.<br/> |
| Заголовок<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Версии WinHTTP](winhttp-versions.md)
</dt> </dl>

 

