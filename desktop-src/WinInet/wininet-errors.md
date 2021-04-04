---
title: Сообщения об ошибках (WinInet. h)
description: Функции WinINet возвращают коды ошибок там, где это уместно. Следующие ошибки относятся к функциям WinINet.
ms.assetid: 338bf65f-ebe5-4434-8407-9ab2a4c8d381
topic_type:
- apiref
api_name:
- ERROR_FTP_DROPPED
- ERROR_FTP_NO_PASSIVE_MODE
- ERROR_FTP_TRANSFER_IN_PROGRESS
- ERROR_GOPHER_ATTRIBUTE_NOT_FOUND
- ERROR_GOPHER_DATA_ERROR
- ERROR_GOPHER_END_OF_DATA
- ERROR_GOPHER_INCORRECT_LOCATOR_TYPE
- ERROR_GOPHER_INVALID_LOCATOR
- ERROR_GOPHER_NOT_FILE
- ERROR_GOPHER_NOT_GOPHER_PLUS
- ERROR_GOPHER_PROTOCOL_ERROR
- ERROR_GOPHER_UNKNOWN_LOCATOR
- ERROR_HTTP_COOKIE_DECLINED
- ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION
- ERROR_HTTP_DOWNLEVEL_SERVER
- ERROR_HTTP_HEADER_ALREADY_EXISTS
- ERROR_HTTP_HEADER_NOT_FOUND
- ERROR_HTTP_INVALID_HEADER
- ERROR_HTTP_INVALID_QUERY_REQUEST
- ERROR_HTTP_INVALID_SERVER_RESPONSE
- ERROR_HTTP_NOT_REDIRECTED
- ERROR_HTTP_REDIRECT_FAILED
- ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION
- ERROR_INTERNET_ASYNC_THREAD_FAILED
- ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT
- ERROR_INTERNET_BAD_OPTION_LENGTH
- ERROR_INTERNET_BAD_REGISTRY_PARAMETER
- ERROR_INTERNET_CANNOT_CONNECT
- ERROR_INTERNET_CHG_POST_IS_NON_SECURE
- ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED
- ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP
- ERROR_INTERNET_CONNECTION_ABORTED
- ERROR_INTERNET_CONNECTION_RESET
- ERROR_INTERNET_DECODING_FAILED
- ERROR_INTERNET_DIALOG_PENDING
- ERROR_INTERNET_DISCONNECTED
- ERROR_INTERNET_EXTENDED_ERROR
- ERROR_INTERNET_FAILED_DUETOSECURITYCHECK
- ERROR_INTERNET_FORCE_RETRY
- ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED
- ERROR_INTERNET_HANDLE_EXISTS
- ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR
- ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR
- ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR
- ERROR_INTERNET_INCORRECT_FORMAT
- ERROR_INTERNET_INCORRECT_HANDLE_STATE
- ERROR_INTERNET_INCORRECT_HANDLE_TYPE
- ERROR_INTERNET_INCORRECT_PASSWORD
- ERROR_INTERNET_INCORRECT_USER_NAME
- ERROR_INTERNET_INSERT_CDROM
- ERROR_INTERNET_INTERNAL_ERROR
- ERROR_INTERNET_INVALID_CA
- ERROR_INTERNET_INVALID_OPERATION
- ERROR_INTERNET_INVALID_OPTION
- ERROR_INTERNET_INVALID_PROXY_REQUEST
- ERROR_INTERNET_INVALID_URL
- ERROR_INTERNET_ITEM_NOT_FOUND
- ERROR_INTERNET_LOGIN_FAILURE
- ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY
- ERROR_INTERNET_MIXED_SECURITY
- ERROR_INTERNET_NAME_NOT_RESOLVED
- ERROR_INTERNET_NEED_MSN_SSPI_PKG
- ERROR_INTERNET_NEED_UI
- ERROR_INTERNET_NO_CALLBACK
- ERROR_INTERNET_NO_CONTEXT
- ERROR_INTERNET_NO_DIRECT_ACCESS
- ERROR_INTERNET_NOT_INITIALIZED
- ERROR_INTERNET_NOT_PROXY_REQUEST
- ERROR_INTERNET_OPERATION_CANCELLED
- ERROR_INTERNET_OPTION_NOT_SETTABLE
- ERROR_INTERNET_OUT_OF_HANDLES
- ERROR_INTERNET_POST_IS_NON_SECURE
- ERROR_INTERNET_PROTOCOL_NOT_FOUND
- ERROR_INTERNET_PROXY_SERVER_UNREACHABLE
- ERROR_INTERNET_REDIRECT_SCHEME_CHANGE
- ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND
- ERROR_INTERNET_REQUEST_PENDING
- ERROR_INTERNET_RETRY_DIALOG
- ERROR_INTERNET_SEC_CERT_CN_INVALID
- ERROR_INTERNET_SEC_CERT_DATE_INVALID
- ERROR_INTERNET_SEC_CERT_ERRORS
- ERROR_INTERNET_SEC_CERT_NO_REV
- ERROR_INTERNET_SEC_CERT_REV_FAILED
- ERROR_INTERNET_SEC_CERT_REVOKED
- ERROR_INTERNET_SEC_INVALID_CERT
- ERROR_INTERNET_SECURITY_CHANNEL_ERROR
- ERROR_INTERNET_SERVER_UNREACHABLE
- ERROR_INTERNET_SHUTDOWN
- ERROR_INTERNET_TCPIP_NOT_INSTALLED
- ERROR_INTERNET_TIMEOUT
- ERROR_INTERNET_UNABLE_TO_CACHE_FILE
- ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT
- ERROR_INTERNET_UNRECOGNIZED_SCHEME
- ERROR_INVALID_HANDLE
- ERROR_MORE_DATA
- ERROR_NO_MORE_FILES
- ERROR_NO_MORE_ITEMS
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcaba7f0404ad002d2a94ac8291c95b0f7440
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137751"
---
# <a name="error-messages-winineth"></a>Сообщения об ошибках (WinInet. h)

Функции WinINet возвращают коды ошибок там, где это уместно. Следующие ошибки относятся к функциям WinINet.

<dl> <dt>

<span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**Ошибка \_ при \_ удалении FTP**
</dt> <dd> <dl> <dt>

12111
</dt> <dt>



Операция FTP не была завершена из-за прерывания сеанса.


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**Ошибка \_ FTP \_ без \_ пассивного \_ режима**
</dt> <dd> <dl> <dt>

12112
</dt> <dt>



Пассивный режим недоступен на сервере.


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**Ошибка \_ \_ \_ при выполнении FTP-перемещения \_**
</dt> <dd> <dl> <dt>

12110
</dt> <dt>



Невозможно выполнить запрошенную операцию над обработчиком сеанса FTP, так как операция уже выполняется.


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена атрибут Gopher**
</dt> <dd> <dl> <dt>

12137
</dt> <dt>



Не удалось найти запрошенный атрибут.

> [!Note]  
> Windows XP и Windows Server 2003 R2 и более ранних версий.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**Ошибка \_ в \_ данных \_ Gopher**
</dt> <dd> <dl> <dt>

12132
</dt> <dt>



При получении данных от сервера gopher обнаружена ошибка.

> [!Note]  
> Windows XP и Windows Server 2003 R2 и более ранних версий.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**Ошибка \_ \_ в конце \_ \_ данных Gopher**
</dt> <dd> <dl> <dt>

12133
</dt> <dt>



Достигнут конец данных.

> [!Note]  
> Windows XP и Windows Server 2003 R2 и более ранних версий.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**Ошибка \_ Gopher \_ неверный \_ \_ тип указателя**
</dt> <dd> <dl> <dt>

12135
</dt> <dt>



Недопустимый тип указателя для данной операции.

> [!Note]  
> Windows XP и Windows Server 2003 R2 и более ранних версий.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**Ошибка \_ Gopher, \_ Недопустимый \_ указатель**
</dt> <dd> <dl> <dt>

12134
</dt> <dt>



Указан недопустимый указатель.

> [!Note]  
> Windows XP и Windows Server 2003 R2 и более ранних версий.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**Ошибка \_ Gopher \_ не \_ файл**
</dt> <dd> <dl> <dt>

12131
</dt> <dt>



Запрос должен быть выполнен для указателя файла.

> [!Note]  
> Windows XP и Windows Server 2003 R2 и более ранних версий.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**Ошибка \_ Gopher \_ , \_ а не Gopher \_**
</dt> <dd> <dl> <dt>

12136
</dt> <dt>



Запрошенная операция может быть выполнена только для сервера gopher + или с указателем, указывающим на операцию Gopher +.

> [!Note]  
> Windows XP и Windows Server 2003 R2 и более ранних версий.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**Ошибка \_ \_ протокола Gopher \_**
</dt> <dd> <dl> <dt>

12130
</dt> <dt>



При синтаксическом анализе данных, возвращенных с сервера gopher, обнаружена ошибка.

> [!Note]  
> Windows XP и Windows Server 2003 R2 и более ранних версий.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**Ошибка \_ Gopher \_ неизвестный \_ указатель**
</dt> <dd> <dl> <dt>

12138
</dt> <dt>



Неизвестный тип указателя.

> [!Note]  
> Windows XP и Windows Server 2003 R2 и более ранних версий.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**Ошибка \_ cookie HTTP- \_ файла \_ отклонено**
</dt> <dd> <dl> <dt>

12162
</dt> <dt>



Файл cookie HTTP отклонен сервером.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**Ошибка \_ HTTP \_ cookie \_ требует \_ подтверждения**
</dt> <dd> <dl> <dt>

12161
</dt> <dt>



Для HTTP-файла cookie требуется подтверждение.

> [!Note]  
> Windows Vista и Windows Server 2008 и более ранние версии.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**Ошибка \_ HTTP- \_ сервера нижнего уровня \_**
</dt> <dd> <dl> <dt>

12151
</dt> <dt>



Сервер не вернул заголовки.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**\_заголовок ошибки \_ HTTP \_ уже \_ существует**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Не удалось добавить заголовок, поскольку он уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**\_заголовок ошибки \_ HTTP \_ не \_ найден**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



Не удалось найти запрошенный заголовок.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**Ошибка \_ - \_ Недопустимый \_ заголовок HTTP**
</dt> <dd> <dl> <dt>

12153
</dt> <dt>



Указанный заголовок недопустим.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**Ошибка \_ - \_ Недопустимый \_ \_ запрос HTTP**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



Запрос, сделанный в [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) , является недопустимым.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**Ошибка \_ HTTP — \_ Недопустимый \_ \_ ответ сервера**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



Не удалось проанализировать ответ сервера.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**Ошибка \_ HTTP \_ не \_ перенаправлена**
</dt> <dd> <dl> <dt>

12160
</dt> <dt>



Не удалось перенаправить HTTP-запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**Ошибка \_ \_ при перенаправлении HTTP \_**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



Перенаправление завершилось сбоем, так как схема изменилась (например, HTTP на FTP) или все попытки перенаправления завершились неудачей (по умолчанию пять попыток).


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**Ошибка \_ при \_ перенаправлении HTTP, запрос на перенаправление \_ \_**
</dt> <dd> <dl> <dt>

12168
</dt> <dt>



Перенаправление требует подтверждения пользователя.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**Ошибка \_ \_ \_ при выполнении асинхронного потока в Интернете \_**
</dt> <dd> <dl> <dt>

12047
</dt> <dt>



Приложению не удалось запустить асинхронный поток.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**Ошибка \_ Интернет \_ \_ \_ - \_ скрипта автоматического прокси**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Произошла ошибка в скрипте автоматической настройки прокси-сервера.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**Ошибка в \_ Интернете, \_ неправильная \_ \_ Длина параметра**
</dt> <dd> <dl> <dt>

12010
</dt> <dt>



Длина параметра, указанного в [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) или [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) , неверна для указанного типа параметра.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**Ошибка \_ Internet \_ Bad \_ \_ параметр реестра**
</dt> <dd> <dl> <dt>

12022
</dt> <dt>



Требуемое значение реестра найдено, но имеет неверный тип или имеет недопустимое значение.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**Ошибка \_ \_ \_ подключения к Интернету**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Сбой при подключении к серверу.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**Ошибка \_ Internet \_ чг \_ POST \_ не \_ является \_ безопасной**
</dt> <dd> <dl> <dt>

12042
</dt> <dt>



Приложение выполняет публикацию и пытается изменить несколько строк текста на небезопасном сервере.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**Ошибка \_ \_ \_ требуется сертификат проверки подлинности клиента Интернета \_ \_**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



Сервер запрашивает проверку подлинности клиента.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**Ошибка \_ при \_ \_ настройке проверки подлинности клиента Интернета \_ \_**
</dt> <dd> <dl> <dt>

12046
</dt> <dt>



На этом компьютере не настроена авторизация клиента.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**Ошибка \_ \_ прерванного подключения к Интернету \_**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



Подключение к серверу прервано.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**Ошибка \_ \_ сброса подключения к Интернету \_**
</dt> <dd> <dl> <dt>

12031
</dt> <dt>



Подключение к серверу было сброшено.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**Ошибка \_ \_ при декодировании в Интернете \_**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



WinINet не смог выполнить декодирование содержимого в ответе. Дополнительные сведения см. в разделе о [**кодировании содержимого**](content-encoding.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**Ошибка \_ \_ ожидания диалогового окна Интернета \_**
</dt> <dd> <dl> <dt>

12049
</dt> <dt>



В ходе выполнения другого потока появится диалоговое окно Password (пароль).


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**Ошибка \_ подключения к Интернету \_**
</dt> <dd> <dl> <dt>

12163
</dt> <dt>



Потеряно подключение к Интернету.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**Ошибка \_ \_ расширенной \_ ошибки Интернета**
</dt> <dd> <dl> <dt>

12003
</dt> <dt>



С сервера возвращена Расширенная ошибка. Обычно это строка или буфер, содержащий подробное сообщение об ошибке. Вызовите [**интернетжетластреспонсеинфо**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) , чтобы получить текст ошибки.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**Ошибка \_ \_ при сбое в Интернете \_ дуетосекуритичекк**
</dt> <dd> <dl> <dt>

12171
</dt> <dt>



Сбой функции из-за проверки безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**Ошибка \_ при \_ попытке принудительного подключения к Интернету \_**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



Функции необходимо повторить запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**Ошибка \_ при \_ \_ попытке входа в Интернет Fortezza \_**
</dt> <dd> <dl> <dt>

12054
</dt> <dt>



Запрошенный ресурс требует проверки подлинности Fortezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**Ошибка \_ в \_ наличии обработчика Интернета \_**
</dt> <dd> <dl> <dt>

12036
</dt> <dt>



Не удалось выполнить запрос, так как маркер уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**Ошибка \_ Интернет \_ -HTTP \_ для \_ HTTPS \_ в \_ редир**
</dt> <dd> <dl> <dt>

12039
</dt> <dt>



Приложение переходит с подключения не SSL к SSL-соединению из-за перенаправления.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**Ошибка \_ Интернет \_ \_ -отправки HTTP HTTPS \_ \_ редир**
</dt> <dd> <dl> <dt>

12052
</dt> <dt>



Данные, отправляемые в SSL-соединение, перенаправляются на подключение, не поддерживающее SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**Ошибка \_ Интернет \_ \_ -HTTPS для \_ HTTP \_ в \_ редир**
</dt> <dd> <dl> <dt>

12040
</dt> <dt>



Приложение перемещается из SSL в подключение без SSL из-за перенаправления.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**Ошибка в \_ Интернете, \_ неправильный \_ Формат**
</dt> <dd> <dl> <dt>

12027
</dt> <dt>



Недопустимый формат запроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**Ошибка \_ при \_ неправильном \_ состоянии обработчика Интернета \_**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



Не удается выполнить запрошенную операцию, так как указанный обработчик находится в неправильном состоянии.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**Ошибка \_ при \_ неправильном \_ типе обработчика Интернета \_**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



Для этой операции указан недопустимый тип обработчика.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**Ошибка в \_ Интернете \_ неверный \_ пароль**
</dt> <dd> <dl> <dt>

12014
</dt> <dt>



Не удалось выполнить запрос на подключение и вход на FTP-сервер, так как указанный пароль неверен.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**Ошибка в \_ Интернете \_ неправильное \_ \_ имя пользователя**
</dt> <dd> <dl> <dt>

12013
</dt> <dt>



Не удалось выполнить запрос на подключение и вход на FTP-сервер, так как указано неверное имя пользователя.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**Ошибка \_ при \_ вставке \_ компакт CDROM в Интернет**
</dt> <dd> <dl> <dt>

12053
</dt> <dt>



Для запроса требуется вставить компакт-диск на устройство чтения компакт-дисков, чтобы указать требуемый ресурс.

> [!Note]  
> Windows Vista и Windows Server 2008 и более ранние версии.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**Ошибка \_ при \_ внутренней \_ ошибке Интернета**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Произошла внутренняя ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**Ошибка в \_ Интернете, \_ Недопустимый \_ ЦС**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



Функция не знакома с центром сертификации, создавшим сертификат сервера.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**Ошибка \_ при \_ выполнении недопустимой операции в Интернете \_**
</dt> <dd> <dl> <dt>

12016
</dt> <dt>



Запрошенная операция недопустима.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**\_ \_ Недопустимый \_ параметр "ошибка в Интернете"**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Запрос к [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) или [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) указал недопустимое значение параметра.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**Ошибка \_ \_ \_ запроса прокси-сервера в Интернете \_**
</dt> <dd> <dl> <dt>

12033
</dt> <dt>



Недопустимый запрос к прокси-серверу.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**Ошибка \_ \_ \_ URL-адреса, недопустимого в Интернете**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



Недопустимый URL-адрес.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена веб – элемент**
</dt> <dd> <dl> <dt>

12028
</dt> <dt>



Не удалось найти запрошенный элемент.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**Ошибка \_ \_ при входе в Интернет \_**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



Не удалось выполнить запрос на подключение к серверу FTP и его вход.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**Ошибка \_ при входе в Интернет. \_ \_ \_ Отображение \_ \_ тела сущности**
</dt> <dd> <dl> <dt>

12174
</dt> <dt>



С веб-сайта возвращен заголовок дайджеста MS-Logoff. Этот заголовок специально указывает пакету дайджеста очистить учетные данные для связанной области. Эта ошибка будет возвращена только в случае, если параметр "ошибка подключения к ошибке при входе в сеть" имеет значение " [ \_ \_ \_ \_ \_ отображать \_ \_ тело сущности](option-flags.md) ". в противном случае возвращается **Ошибка \_ \_ \_ входа в Интернет** .


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**Ошибка \_ \_ смешанной \_ безопасности в Интернете**
</dt> <dd> <dl> <dt>

12041
</dt> <dt>



Содержимое не полностью защищено. Возможно, часть просматриваемого содержимого поступила с незащищенных серверов.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**Ошибка \_ " \_ имя Интернета \_ не \_ разрешено"**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



Не удалось разрешить имя сервера.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**Ошибка \_ Интернета — \_ требуется \_ MSN \_ SSPI \_ pkg**
</dt> <dd> <dl> <dt>

12173
</dt> <dt>



В настоящий момент не реализовано.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**Ошибка \_ в \_ \_ пользовательском интерфейсе для Интернета**
</dt> <dd> <dl> <dt>

12034
</dt> <dt>



Запрошен пользовательский интерфейс или другая операция блокировки.

> [!Note]  
> Windows Vista и Windows Server 2008 и более ранние версии.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**Ошибка \_ \_ \_ обратного вызова в Интернете**
</dt> <dd> <dl> <dt>

12025
</dt> <dt>



Не удалось выполнить асинхронный запрос, поскольку не задана функция обратного вызова.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**Ошибка \_ Интернета \_ без \_ контекста**
</dt> <dd> <dl> <dt>

12024
</dt> <dt>



Не удалось выполнить асинхронный запрос, так как было указано нулевое значение контекста.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**Ошибка \_ " \_ нет \_ прямого \_ доступа к Интернету"**
</dt> <dd> <dl> <dt>

12023
</dt> <dt>



В настоящее время невозможно выполнить прямой доступ к сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**Ошибка " \_ сеть \_ не \_ инициализирована"**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



Инициализация API WinINet не выполнена. Указывает, что функция более высокого уровня, например [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena), еще не была вызвана.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**Ошибка \_ \_ \_ запроса прокси-сервера в Интернете \_**
</dt> <dd> <dl> <dt>

12020
</dt> <dt>



Запрос не может быть выполнен через прокси-сервер.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**Ошибка \_ при \_ отмене операции в Интернете \_**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



Операция была отменена, как правило, из-за того, что обработчик, на котором был запущен запрос, был закрыт до завершения операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**\_ \_ параметр "Ошибка Интернета не может быть установлен" \_ \_**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



Невозможно задать запрошенный параметр, выполняется только запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**Ошибка \_ Интернета \_ вне \_ \_ дескрипторов**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



В данный момент больше не удалось создать дескрипторы.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**сообщение об ошибке " \_ Интернет \_ -Публикация не \_ \_ \_ защищена"**
</dt> <dd> <dl> <dt>

12043
</dt> <dt>



Приложение передает данные на сервер, который не является безопасным.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена протокол Интернета**
</dt> <dd> <dl> <dt>

12008
</dt> <dt>



Не удалось найти запрошенный протокол.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**Ошибка \_ \_ \_ недоступности прокси-сервера Интернета \_**
</dt> <dd> <dl> <dt>

12165
</dt> <dt>



Указанный прокси-сервер недоступен.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**Ошибка \_ при \_ \_ изменении схемы перенаправления Интернета \_**
</dt> <dd> <dl> <dt>

12048
</dt> <dt>



Функции не удалось выполнить перенаправление, поскольку схема изменилась (например, с HTTP на FTP).


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**Ошибка \_ \_ \_ \_ не \_ найдена значение реестра Интернета**
</dt> <dd> <dl> <dt>

12021
</dt> <dt>



Не удалось найти требуемое значение реестра.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**Ошибка \_ \_ запроса \_ в Интернет**
</dt> <dd> <dl> <dt>

12026
</dt> <dt>



Не удалось выполнить требуемую операцию, так как ожидается один или несколько запросов.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**Ошибка \_ \_ диалогового окна повторного подключения к Интернету \_**
</dt> <dd> <dl> <dt>

12050
</dt> <dt>



Необходимо повторить попытку в диалоговом окне.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**Ошибка \_ \_ \_ \_ недопустимое общее имя сертификата Internet sec \_**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



Неверное общее имя SSL-сертификата (поле имени узла), например, если вы указали www.server.com, а общее имя сертификата — www.different.com.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**Ошибка \_ при \_ обращении к Интернету с \_ \_ \_ недопустимым сертификатом**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



Дата SSL-сертификата, полученная с сервера, является неправильной. Срок действия сертификата истек.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**ошибки при ошибках \_ сертификатов Интернета ( \_ сек) \_ \_**
</dt> <dd> <dl> <dt>

12055
</dt> <dt>



SSL-сертификат содержит ошибки.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**Ошибка \_ \_ номер сертификата Internet sec, \_ \_ без \_ редакции**
</dt> <dd> <dl> <dt>

12056
</dt> <dt>



SSL-сертификат не был отозван.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**Ошибка \_ \_ при версии \_ сертификата Internet sec \_ \_**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Сбой отзыва SSL-сертификата.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**Ошибка \_ при \_ \_ \_ отзыве сертификата в Интернете (Internet sec)**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



SSL-сертификат был отозван.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**Ошибка \_ Интернет \_ с \_ недопустимым \_ сертификатом**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



Недопустимый SSL-сертификат.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**Ошибка \_ \_ канала безопасности \_ Интернета \_**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



Произошла внутренняя ошибка приложения при загрузке библиотек SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**Ошибка \_ " \_ сервер в Интернете \_ недоступен"**
</dt> <dd> <dl> <dt>

12164
</dt> <dt>



Указанный веб-сайт или сервер недоступен.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**Ошибка \_ \_ отключения Интернета**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



Поддержка WinINet завершается или выгружается.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**Ошибка \_ Internet \_ tcpip \_ не \_ установлена**
</dt> <dd> <dl> <dt>

12159
</dt> <dt>



Необходимый стек протокола не загружен, и приложение не может запустить WinSock.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**Ошибка \_ \_ времени ожидания в Интернете**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



Истекло время ожидания запроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**Ошибка \_ Интернет \_ не \_ удалось \_ кэшировать \_ файл**
</dt> <dd> <dl> <dt>

12158
</dt> <dt>



Функции не удалось кэшировать файл.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**Ошибка \_ Интернет \_ не \_ может \_ загрузить \_ Скрипт**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



Не удалось скачать скрипт конфигурации автоматического прокси-сервера. \_Флаг запроса в Интернете \_ должен быть \_ установлен в кэш \_ .


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**Ошибка \_ \_ нераспознанной \_ схемы Интернета**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



Не удалось распознать схему URL-адресов или она не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**Ошибка \_ недопустимого \_ маркера**
</dt> <dd> <dl> <dt>



Маркер, переданный в API, был либо недействительным, либо закрытым.

**Заголовок:** Объявлено в файле Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**Ошибка \_ дополнительных \_ данных**
</dt> <dd> <dl> <dt>



More data is available.

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



 

