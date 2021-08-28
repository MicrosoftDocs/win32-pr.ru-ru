---
title: Коды ошибок маршрутизации и удаленного доступа
description: Следующие коды ошибок маршрутизации и удаленного доступа (RRAS) определены в расеррор. h.
ms.assetid: 1fa41438-7c93-4e9c-851c-652fba23da4f
topic_type:
- apiref
api_name:
- Routing and Remote Access Error Codes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bd68c31ef2b92cce75059d5d86ee68dc65d1151
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624330"
---
# <a name="routing-and-remote-access-error-codes"></a>Коды ошибок маршрутизации и удаленного доступа

Следующие коды ошибок маршрутизации и удаленного доступа (RRAS) определены в расеррор. h. все коды ошибок поддерживаются в Windows 2000 или более поздних версиях Windows, если не указано иное.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Возвращаемый код и значение</th>
<th>Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="PENDING"></span><span id="pending"></span><dl> <dt><strong>Ожидается</strong></dt> <dt>600</dt> </dl></td>
<td>Операция находится в состоянии ожидания.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PORT_HANDLE"></span><span id="error_invalid_port_handle"></span><dl> <dt><strong>ERROR_INVALID_PORT_HANDLE</strong></dt> <dt>601</dt> </dl></td>
<td>Указан недопустимый маркер порта.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_ALREADY_OPEN"></span><span id="error_port_already_open"></span><dl> <dt><strong>ERROR_PORT_ALREADY_OPEN</strong></dt> <dt>602</dt> </dl></td>
<td>Указанный порт уже открыт.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BUFFER_TOO_SMALL"></span><span id="error_buffer_too_small"></span><dl> <dt><strong>ERROR_BUFFER_TOO_SMALL</strong></dt> <dt>603</dt> </dl></td>
<td>Указанный буфер слишком мал.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_INFO_SPECIFIED"></span><span id="error_wrong_info_specified"></span><dl> <dt><strong>ERROR_WRONG_INFO_SPECIFIED</strong></dt> <dt>604</dt> </dl></td>
<td>Указаны неправильные сведения о портах.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SET_PORT_INFO"></span><span id="error_cannot_set_port_info"></span><dl> <dt><strong>ERROR_CANNOT_SET_PORT_INFO</strong></dt> <dt>605</dt> </dl></td>
<td>Не удается задать указанные сведения о порте.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_CONNECTED"></span><span id="error_port_not_connected"></span><dl> <dt><strong>ERROR_PORT_NOT_CONNECTED</strong></dt> <dt>606</dt> </dl></td>
<td>Указанный порт не подключен.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EVENT_INVALID"></span><span id="error_event_invalid"></span><dl> <dt><strong>ERROR_EVENT_INVALID</strong></dt> <dt>607</dt> </dl></td>
<td>Обнаружено недопустимое событие.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_DOES_NOT_EXIST"></span><span id="error_device_does_not_exist"></span><dl> <dt><strong>ERROR_DEVICE_DOES_NOT_EXIST</strong></dt> <dt>608</dt> </dl></td>
<td>Указанное устройство не существует.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICETYPE_DOES_NOT_EXIST"></span><span id="error_devicetype_does_not_exist"></span><dl> <dt><strong>ERROR_DEVICETYPE_DOES_NOT_EXIST</strong></dt> <dt>609</dt> </dl></td>
<td>Указанный тип устройства не существует.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUFFER_INVALID"></span><span id="error_buffer_invalid"></span><dl> <dt><strong>ERROR_BUFFER_INVALID</strong></dt> <dt>610</dt> </dl></td>
<td>Указан недопустимый буфер.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTE_NOT_AVAILABLE"></span><span id="error_route_not_available"></span><dl> <dt><strong>ERROR_ROUTE_NOT_AVAILABLE</strong></dt> <dt>611</dt> </dl></td>
<td>Указан недоступный маршрут.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ROUTE_NOT_ALLOCATED"></span><span id="error_route_not_allocated"></span><dl> <dt><strong>ERROR_ROUTE_NOT_ALLOCATED</strong></dt> <dt>612</dt> </dl></td>
<td>Указанный маршрут не выделен.<br/></td>
</tr>
<tr class="even">
<td><span id="ERRERROR_INVALID_COMPRESSION_SPECIFIED"></span><span id="errerror_invalid_compression_specified"></span><dl> <dt><strong>ERRERROR_INVALID_COMPRESSION_SPECIFIED</strong></dt> <dt>613</dt> </dl></td>
<td>Указано недопустимое сжатие.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OUT_OF_BUFFERS"></span><span id="error_out_of_buffers"></span><dl> <dt><strong>ERROR_OUT_OF_BUFFERS</strong></dt> <dt>614</dt> </dl></td>
<td>Недостаточно доступных буферов.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_FOUND_"></span><span id="error_port_not_found_"></span><dl> <dt> <strong>ERROR_PORT_NOT_FOUND</strong> </dt> <dt>615</dt> </dl></td>
<td>Указанный порт не найден.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ASYNC_REQUEST_PENDING"></span><span id="error_async_request_pending"></span><dl> <dt><strong>ERROR_ASYNC_REQUEST_PENDING</strong></dt> <dt>616</dt> </dl></td>
<td>Ожидается асинхронный запрос.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_DISCONNECTING"></span><span id="error_already_disconnecting"></span><dl> <dt><strong>ERROR_ALREADY_DISCONNECTING</strong></dt> <dt>617</dt> </dl></td>
<td>Указанный порт или устройство уже отключены.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_OPEN"></span><span id="error_port_not_open"></span><dl> <dt><strong>ERROR_PORT_NOT_OPEN</strong></dt> <dt>618</dt> </dl></td>
<td>Указанный порт не открыт.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_DISCONNECTED"></span><span id="error_port_disconnected"></span><dl> <dt><strong>ERROR_PORT_DISCONNECTED</strong></dt> <dt>619</dt> </dl></td>
<td>Указанный порт отключен.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ENDPOINTS"></span><span id="error_no_endpoints"></span><dl> <dt><strong>ERROR_NO_ENDPOINTS</strong></dt> <dt>620</dt> </dl></td>
<td>Не удалось определить конечные точки.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_OPEN_PHONEBOOK"></span><span id="error_cannot_open_phonebook"></span><dl> <dt><strong>ERROR_CANNOT_OPEN_PHONEBOOK</strong></dt> <dt>621</dt> </dl></td>
<td>Не удается открыть указанный файл телефонной книги.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_PHONEBOOK"></span><span id="error_cannot_load_phonebook"></span><dl> <dt><strong>ERROR_CANNOT_LOAD_PHONEBOOK</strong></dt> <dt>622</dt> </dl></td>
<td>Не удается загрузить указанный файл телефонной книги.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_FIND_PHONEBOOK_ENTRY"></span><span id="error_cannot_find_phonebook_entry"></span><dl> <dt><strong>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</strong></dt> <dt>623</dt> </dl></td>
<td>Не удается найти указанную запись телефонной книги.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_WRITE_PHONEBOOK"></span><span id="error_cannot_write_phonebook"></span><dl> <dt><strong>ERROR_CANNOT_WRITE_PHONEBOOK</strong></dt> <dt>624</dt> </dl></td>
<td>Не удается выполнить запись в указанный файл телефонной книги.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CORRUPT_PHONEBOOK"></span><span id="error_corrupt_phonebook"></span><dl> <dt><strong>ERROR_CORRUPT_PHONEBOOK</strong></dt> <dt>625</dt> </dl></td>
<td>В указанной телефонной книге обнаружена недопустимая информация.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_STRING"></span><span id="error_cannot_load_string"></span><dl> <dt><strong>ERROR_CANNOT_LOAD_STRING</strong></dt> <dt>626</dt> </dl></td>
<td>Не удалось загрузить строку.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_KEY_NOT_FOUND"></span><span id="error_key_not_found"></span><dl> <dt><strong>ERROR_KEY_NOT_FOUND</strong></dt> <dt>627</dt> </dl></td>
<td>Не удается найти указанный ключ.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DISCONNECTION"></span><span id="error_disconnection"></span><dl> <dt><strong>ERROR_DISCONNECTION</strong></dt> <dt>628</dt> </dl></td>
<td>Указанный порт был отключен.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_DISCONNECTION"></span><span id="error_remote_disconnection"></span><dl> <dt><strong>ERROR_REMOTE_DISCONNECTION</strong></dt> <dt>629</dt> </dl></td>
<td>Указанный порт был отключен удаленным компьютером.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HARDWARE_FAILURE"></span><span id="error_hardware_failure"></span><dl> <dt><strong>ERROR_HARDWARE_FAILURE</strong></dt> <dt>630</dt> </dl></td>
<td>Указанный порт был отключен из-за сбоя оборудования.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_DISCONNECTION"></span><span id="error_user_disconnection"></span><dl> <dt><strong>ERROR_USER_DISCONNECTION</strong></dt> <dt>631</dt> </dl></td>
<td>Указанный порт отключен пользователем.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIZE"></span><span id="error_invalid_size"></span><dl> <dt><strong>ERROR_INVALID_SIZE</strong></dt> <dt>632</dt> </dl></td>
<td>Неверный размер структуры.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_AVAILABLE"></span><span id="error_port_not_available"></span><dl> <dt><strong>ERROR_PORT_NOT_AVAILABLE</strong></dt> <dt>633</dt> </dl></td>
<td>Указанный порт уже используется или не настроен для удаленного доступа.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_PROJECT_CLIENT"></span><span id="error_cannot_project_client"></span><dl> <dt><strong>ERROR_CANNOT_PROJECT_CLIENT</strong></dt> <dt>634</dt> </dl></td>
<td>Не удалось зарегистрировать компьютер в удаленной сети.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN"></span><span id="error_unknown"></span><dl> <dt><strong>ERROR_UNKNOWN</strong></dt> <dt>635</dt> </dl></td>
<td>Произошла неизвестная ошибка.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_DEVICE_ATTACHED"></span><span id="error_wrong_device_attached"></span><dl> <dt><strong>ERROR_WRONG_DEVICE_ATTACHED</strong></dt> <dt>636</dt> </dl></td>
<td>К указанному порту подключено неправильное устройство.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_STRING"></span><span id="error_bad_string"></span><dl> <dt><strong>ERROR_BAD_STRING</strong></dt> <dt>637</dt> </dl></td>
<td>Обнаружена строка, которую не удалось преобразовать.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REQUEST_TIMEOUT"></span><span id="error_request_timeout"></span><dl> <dt><strong>ERROR_REQUEST_TIMEOUT</strong></dt> <dt>638</dt> </dl></td>
<td>Истекло время ожидания запроса.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_GET_LANA"></span><span id="error_cannot_get_lana"></span><dl> <dt><strong>ERROR_CANNOT_GET_LANA</strong></dt> <dt>639</dt> </dl></td>
<td>Нет доступной асинхронной сети.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NETBIOS_ERROR"></span><span id="error_netbios_error"></span><dl> <dt><strong>ERROR_NETBIOS_ERROR</strong></dt> <dt>640</dt> </dl></td>
<td>Произошла ошибка при вовлечении NetBIOS.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_OUT_OF_RESOURCES"></span><span id="error_server_out_of_resources"></span><dl> <dt><strong>ERROR_SERVER_OUT_OF_RESOURCES</strong></dt> <dt>641</dt> </dl></td>
<td>сервер не может выделить ресурсы NetBIOS, необходимые для поддержки клиента.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NAME_EXISTS_ON_NET"></span><span id="error_name_exists_on_net"></span><dl> <dt><strong>ERROR_NAME_EXISTS_ON_NET</strong></dt> <dt>642</dt> </dl></td>
<td>Одно из NetBIOS-имен вашего компьютера уже зарегистрировано в удаленной сети.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_GENERAL_NET_FAILURE"></span><span id="error_server_general_net_failure"></span><dl> <dt><strong>ERROR_SERVER_GENERAL_NET_FAILURE</strong></dt> <dt>643</dt> </dl></td>
<td>Сбой сетевого адаптера на сервере.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_MSG_ALIAS_NOT_ADDED"></span><span id="warning_msg_alias_not_added"></span><dl> <dt><strong>WARNING_MSG_ALIAS_NOT_ADDED</strong></dt> <dt>644</dt> </dl></td>
<td>Всплывающие окна сетевых сообщений не появятся.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_INTERNAL"></span><span id="error_auth_internal"></span><dl> <dt><strong>ERROR_AUTH_INTERNAL</strong></dt> <dt>645</dt> </dl></td>
<td>Произошла внутренняя ошибка проверки подлинности.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RESTRICTED_LOGON_HOURS"></span><span id="error_restricted_logon_hours"></span><dl> <dt><strong>ERROR_RESTRICTED_LOGON_HOURS</strong></dt> <dt>646</dt> </dl></td>
<td>Для указанной учетной записи запрещено выполнять вход в это время суток.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCT_DISABLED"></span><span id="error_acct_disabled"></span><dl> <dt><strong>ERROR_ACCT_DISABLED</strong></dt> <dt>647</dt> </dl></td>
<td>Учетная запись отключена.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PASSWD_EXPIRED"></span><span id="error_passwd_expired"></span><dl> <dt><strong>ERROR_PASSWD_EXPIRED</strong></dt> <dt>648</dt> </dl></td>
<td>Срок действия указанного пароля истек.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_DIALIN_PERMISSION"></span><span id="error_no_dialin_permission"></span><dl> <dt><strong>ERROR_NO_DIALIN_PERMISSION</strong></dt> <dt>649</dt> </dl></td>
<td>Указанная учетная запись не имеет разрешений на удаленный доступ.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_NOT_RESPONDING"></span><span id="error_server_not_responding"></span><dl> <dt><strong>ERROR_SERVER_NOT_RESPONDING</strong></dt> <dt>650</dt> </dl></td>
<td>Сервер удаленного доступа не отвечает.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FROM_DEVICE"></span><span id="error_from_device"></span><dl> <dt><strong>ERROR_FROM_DEVICE</strong></dt> <dt>651</dt> </dl></td>
<td>Модем или другое устройство подключения сообщило об ошибке.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNRECOGNIZED_RESPONSE"></span><span id="error_unrecognized_response"></span><dl> <dt><strong>ERROR_UNRECOGNIZED_RESPONSE</strong></dt> <dt>652</dt> </dl></td>
<td>Устройство вернуло неопознанный ответ.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MACRO_NOT_FOUND"></span><span id="error_macro_not_found"></span><dl> <dt><strong>ERROR_MACRO_NOT_FOUND</strong></dt> <dt>653</dt> </dl></td>
<td>Макрос, требуемый для устройства, не найден на устройстве. Раздел INF-файла.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MACRO_NOT_DEFINED"></span><span id="error_macro_not_defined"></span><dl> <dt><strong>ERROR_MACRO_NOT_DEFINED</strong></dt> <dt>654</dt> </dl></td>
<td>Команда или ответ на устройстве. Раздел INF-файла ссылается на неопределенный макрос.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MESSAGE_MACRO_NOT_FOUND"></span><span id="error_message_macro_not_found"></span><dl> <dt><strong>ERROR_MESSAGE_MACRO_NOT_FOUND</strong></dt> <dt>655</dt> </dl></td>
<td><message>Макрос не найден на устройстве. Раздел INF-файла.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEFAULTOFF_MACRO_NOT_FOUND"></span><span id="error_defaultoff_macro_not_found"></span><dl> <dt><strong>ERROR_DEFAULTOFF_MACRO_NOT_FOUND</strong></dt> <dt>656</dt> </dl></td>
<td><defaultoff>Макрос на устройстве. Раздел INF-файла содержит неопределенный макрос.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FILE_COULD_NOT_BE_OPENED"></span><span id="error_file_could_not_be_opened"></span><dl> <dt><strong>ERROR_FILE_COULD_NOT_BE_OPENED</strong></dt> <dt>657</dt> </dl></td>
<td>Устройство. Не удалось открыть INF-файл.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICENAME_TOO_LONG"></span><span id="error_devicename_too_long"></span><dl> <dt><strong>ERROR_DEVICENAME_TOO_LONG</strong></dt> <dt>658</dt> </dl></td>
<td>Имя устройства на устройстве. Слишком длинный INF-файл .INI носителя. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICENAME_NOT_FOUND"></span><span id="error_devicename_not_found"></span><dl> <dt><strong>ERROR_DEVICENAME_NOT_FOUND</strong></dt> <dt>659</dt> </dl></td>
<td>Файл мультимедиа .INI ссылается на неизвестное имя устройства.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RESPONSES"></span><span id="error_no_responses"></span><dl> <dt><strong>ERROR_NO_RESPONSES</strong></dt> <dt>660</dt> </dl></td>
<td>Устройство. INF-файл не содержит ответов для команды.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_COMMAND_FOUND"></span><span id="error_no_command_found"></span><dl> <dt><strong>ERROR_NO_COMMAND_FOUND</strong></dt> <dt>661</dt> </dl></td>
<td>Устройство. В INF-файле отсутствует команда.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_KEY_SPECIFIED"></span><span id="error_wrong_key_specified"></span><dl> <dt><strong>ERROR_WRONG_KEY_SPECIFIED</strong></dt> <dt>662</dt> </dl></td>
<td>Попытка задать макрос, не указанный в списке устройств. Раздел INF-файла.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN_DEVICE_TYPE"></span><span id="error_unknown_device_type"></span><dl> <dt><strong>ERROR_UNKNOWN_DEVICE_TYPE</strong></dt> <dt>663</dt> </dl></td>
<td>Файл мультимедиа .INI ссылается на неизвестный тип устройства.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALLOCATING_MEMORY"></span><span id="error_allocating_memory"></span><dl> <dt><strong>ERROR_ALLOCATING_MEMORY</strong></dt> <dt>664</dt> </dl></td>
<td>Не удается выделить память.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_CONFIGURED"></span><span id="error_port_not_configured"></span><dl> <dt><strong>ERROR_PORT_NOT_CONFIGURED</strong></dt> <dt>665</dt> </dl></td>
<td>Порт не настроен для удаленного доступа.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_NOT_READY"></span><span id="error_device_not_ready"></span><dl> <dt><strong>ERROR_DEVICE_NOT_READY</strong></dt> <dt>666</dt> </dl></td>
<td>Ваш модем или другое устройство подключения не работает.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_INI_FILE"></span><span id="error_reading_ini_file"></span><dl> <dt><strong>ERROR_READING_INI_FILE</strong></dt> <dt>667</dt> </dl></td>
<td>Не удается прочитать файл .INI мультимедиа.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CONNECTION"></span><span id="error_no_connection"></span><dl> <dt><strong>ERROR_NO_CONNECTION</strong></dt> <dt>668</dt> </dl></td>
<td>Подключение отброшено.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_USAGE_IN_INI_FILE"></span><span id="error_bad_usage_in_ini_file"></span><dl> <dt><strong>ERROR_BAD_USAGE_IN_INI_FILE</strong></dt> <dt>669</dt> </dl></td>
<td>Недопустимый параметр использования в файле мультимедиа .ini.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SECTIONNAME"></span><span id="error_reading_sectionname"></span><dl> <dt><strong>ERROR_READING_SECTIONNAME</strong></dt> <dt>670</dt> </dl></td>
<td>Не удается прочитать имя раздела из файла мультимедиа .INI.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEVICETYPE"></span><span id="error_reading_devicetype"></span><dl> <dt><strong>ERROR_READING_DEVICETYPE</strong></dt> <dt>671</dt> </dl></td>
<td>Не удается прочитать тип устройства из файла .INI носителя.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_DEVICENAME"></span><span id="error_reading_devicename"></span><dl> <dt><strong>ERROR_READING_DEVICENAME</strong></dt> <dt>672</dt> </dl></td>
<td>Не удается прочитать имя устройства из файла .INI носителя.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_USAGE"></span><span id="error_reading_usage"></span><dl> <dt><strong>ERROR_READING_USAGE</strong></dt> <dt>673</dt> </dl></td>
<td>Не удается прочитать сведения об использовании из файла мультимедиа .INI.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_MAXCONNECTBPS"></span><span id="error_reading_maxconnectbps"></span><dl> <dt><strong>ERROR_READING_MAXCONNECTBPS</strong></dt> <dt>674</dt> </dl></td>
<td>Системе не удалось прочесть максимальную скорость подключения перевозчика из файла .INI носителя.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_MAXCARRIERBPS"></span><span id="error_reading_maxcarrierbps"></span><dl> <dt><strong>ERROR_READING_MAXCARRIERBPS</strong></dt> <dt>675</dt> </dl></td>
<td>Не удается прочитать сведения об использовании из файла мультимедиа .INI.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_LINE_BUSY"></span><span id="error_line_busy"></span><dl> <dt><strong>ERROR_LINE_BUSY</strong></dt> <dt>676</dt> </dl></td>
<td>Линия занята.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VOICE_ANSWER"></span><span id="error_voice_answer"></span><dl> <dt><strong>ERROR_VOICE_ANSWER</strong></dt> <dt>677</dt> </dl></td>
<td>Вместо модема ответил человек.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ANSWER"></span><span id="error_no_answer"></span><dl> <dt><strong>ERROR_NO_ANSWER</strong></dt> <dt>678</dt> </dl></td>
<td>Нет ответа.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_CARRIER"></span><span id="error_no_carrier"></span><dl> <dt><strong>ERROR_NO_CARRIER</strong></dt> <dt>679</dt> </dl></td>
<td>Не удается обнаружить сигнал несущей.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIALTONE"></span><span id="error_no_dialtone"></span><dl> <dt><strong>ERROR_NO_DIALTONE</strong></dt> <dt>680</dt> </dl></td>
<td>Нет гудка в линии.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IN_COMMAND"></span><span id="error_in_command"></span><dl> <dt><strong>ERROR_IN_COMMAND</strong></dt> <dt>681</dt> </dl></td>
<td>Модем (или другое устройство для подключения) сообщил об общей ошибке.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_SECTIONNAME"></span><span id="error_writing_sectionname"></span><dl> <dt><strong>ERROR_WRITING_SECTIONNAME</strong></dt> <dt>682</dt> </dl></td>
<td>Произошла ошибка при записи имени раздела.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_DEVICETYPE"></span><span id="error_writing_devicetype"></span><dl> <dt><strong>ERROR_WRITING_DEVICETYPE</strong></dt> <dt>683</dt> </dl></td>
<td>Произошла ошибка при записи типа устройства.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEVICENAME"></span><span id="error_writing_devicename"></span><dl> <dt><strong>ERROR_WRITING_DEVICENAME</strong></dt> <dt>684</dt> </dl></td>
<td>Произошла ошибка при записи имени устройства.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_MAXCONNECTBPS"></span><span id="error_writing_maxconnectbps"></span><dl> <dt><strong>ERROR_WRITING_MAXCONNECTBPS</strong></dt> <dt>685</dt> </dl></td>
<td>Произошла ошибка при записи максимальной скорости подключения.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_MAXCARRIERBPS"></span><span id="error_writing_maxcarrierbps"></span><dl> <dt><strong>ERROR_WRITING_MAXCARRIERBPS</strong></dt> <dt>686</dt> </dl></td>
<td>Произошла ошибка при записи максимальной частоты несущей частоты.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_USAGE"></span><span id="error_writing_usage"></span><dl> <dt><strong>ERROR_WRITING_USAGE</strong></dt> <dt>687</dt> </dl></td>
<td>Произошла ошибка при записи сведений об использовании.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEFAULTOFF"></span><span id="error_writing_defaultoff"></span><dl> <dt><strong>ERROR_WRITING_DEFAULTOFF</strong></dt> <dt>688</dt> </dl></td>
<td>Произошла ошибка при записи значения по умолчанию.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEFAULTOFF"></span><span id="error_reading_defaultoff"></span><dl> <dt><strong>ERROR_READING_DEFAULTOFF</strong></dt> <dt>689</dt> </dl></td>

</tr>
<tr class="odd">
<td><span id="ERROR_EMPTY_INI_FILE"></span><span id="error_empty_ini_file"></span><dl> <dt><strong>ERROR_EMPTY_INI_FILE</strong></dt> <dt>690</dt> </dl></td>
<td>Файл .INI носителя пуст.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTHENTICATION_FAILURE"></span><span id="error_authentication_failure"></span><dl> <dt><strong>ERROR_AUTHENTICATION_FAILURE</strong></dt> <dt>691</dt> </dl></td>
<td>Отказано в доступе, так как имя пользователя, пароль или оба значения недопустимы в домене.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_OR_DEVICE"></span><span id="error_port_or_device"></span><dl> <dt><strong>ERROR_PORT_OR_DEVICE</strong></dt> <dt>692</dt> </dl></td>
<td>В порте или подключенном устройстве произошла ошибка оборудования<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_BINARY_MACRO"></span><span id="error_not_binary_macro"></span><dl> <dt><strong>ERROR_NOT_BINARY_MACRO</strong></dt> <dt>693</dt> </dl></td>
<td>Макрос не является двоичным макросом.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DCB_NOT_FOUND"></span><span id="error_dcb_not_found"></span><dl> <dt><strong>ERROR_DCB_NOT_FOUND</strong></dt> <dt>694</dt> </dl></td>
<td>Не найдена DCB.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_STATE_MACHINES_NOT_STARTED"></span><span id="error_state_machines_not_started"></span><dl> <dt><strong>ERROR_STATE_MACHINES_NOT_STARTED</strong></dt> <dt>695</dt> </dl></td>
<td>Конечный автомат не запущен.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_STATE_MACHINES_ALREADY_STARTED"></span><span id="error_state_machines_already_started"></span><dl> <dt><strong>ERROR_STATE_MACHINES_ALREADY_STARTED</strong></dt> <dt>696</dt> </dl></td>
<td>Конечный автомат уже запущен.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PARTIAL_RESPONSE_LOOPING"></span><span id="error_partial_response_looping"></span><dl> <dt><strong>ERROR_PARTIAL_RESPONSE_LOOPING</strong></dt> <dt>697</dt> </dl></td>
<td>Циклическая зависимость от частичного ответа.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_RESPONSE_KEY"></span><span id="error_unknown_response_key"></span><dl> <dt><strong>ERROR_UNKNOWN_RESPONSE_KEY</strong></dt> <dt>698</dt> </dl></td>
<td>Имя ключа ответа на устройстве. Неверный формат INF-файла.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RECV_BUF_FULL"></span><span id="error_recv_buf_full"></span><dl> <dt><strong>ERROR_RECV_BUF_FULL</strong></dt> <dt>699</dt> </dl></td>
<td>Ответ устройства привел к переполнению буфера.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CMD_TOO_LONG"></span><span id="error_cmd_too_long"></span><dl> <dt><strong>ERROR_CMD_TOO_LONG</strong></dt> <dt>700</dt> </dl></td>
<td>Расширенная команда на устройстве. Слишком длинный INF-файл.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNSUPPORTED_BPS"></span><span id="error_unsupported_bps"></span><dl> <dt><strong>ERROR_UNSUPPORTED_BPS</strong></dt> <dt>701</dt> </dl></td>
<td>Устройство перешло на скорость подключения, которая не поддерживается драйвером COM.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNEXPECTED_RESPONSE"></span><span id="error_unexpected_response"></span><dl> <dt><strong>ERROR_UNEXPECTED_RESPONSE</strong></dt> <dt>702</dt> </dl></td>
<td>Получен ответ устройства, если не ожидалось ни одного.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERACTIVE_MODE"></span><span id="error_interactive_mode"></span><dl> <dt><strong>ERROR_INTERACTIVE_MODE</strong></dt> <dt>703</dt> </dl></td>
<td>Произошла ошибка, так как включен интерактивный режим.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAD_CALLBACK_NUMBER"></span><span id="error_bad_callback_number"></span><dl> <dt><strong>ERROR_BAD_CALLBACK_NUMBER</strong></dt> <dt>704</dt> </dl></td>
<td>Указан недопустимый номер обратного вызова.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_AUTH_STATE"></span><span id="error_invalid_auth_state"></span><dl> <dt><strong>ERROR_INVALID_AUTH_STATE</strong></dt> <dt>705</dt> </dl></td>
<td>Указано недопустимое состояние проверки подлинности.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_INITBPS"></span><span id="error_writing_initbps"></span><dl> <dt><strong>ERROR_WRITING_INITBPS</strong></dt> <dt>706</dt> </dl></td>
<td>Произошла ошибка при записи начальной скорости подключения.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_X25_DIAGNOSTIC"></span><span id="error_x25_diagnostic"></span><dl> <dt><strong>ERROR_X25_DIAGNOSTIC</strong></dt> <dt>707</dt> </dl></td>
<td>Получено диагностическое уведомление X. 25.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ACCT_EXPIRED"></span><span id="error_acct_expired"></span><dl> <dt><strong>ERROR_ACCT_EXPIRED</strong></dt> <dt>708</dt> </dl></td>
<td>Срок действия указанной учетной записи истек.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CHANGING_PASSWORD"></span><span id="error_changing_password"></span><dl> <dt><strong>ERROR_CHANGING_PASSWORD</strong></dt> <dt>709</dt> </dl></td>
<td>Произошла ошибка при попытке изменить пароль в домене.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OVERRUN"></span><span id="error_overrun"></span><dl> <dt><strong>ERROR_OVERRUN</strong></dt> <dt>710</dt> </dl></td>
<td>При обмене данными с вашим модемом обнаружены ошибки переполнения последовательного порта.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASMAN_CANNOT_INITIALIZE"></span><span id="error_rasman_cannot_initialize"></span><dl> <dt><strong>ERROR_RASMAN_CANNOT_INITIALIZE</strong></dt> <dt>711</dt> </dl></td>
<td>Сбой инициализации RasMan. Проверьте журнал событий.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BIPLEX_PORT_NOT_AVAILABLE"></span><span id="error_biplex_port_not_available"></span><dl> <dt><strong>ERROR_BIPLEX_PORT_NOT_AVAILABLE</strong></dt> <dt>712</dt> </dl></td>
<td>Двусторонний порт инициализируется. Подождите несколько секунд и перезвоните.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_ACTIVE_ISDN_LINES"></span><span id="error_no_active_isdn_lines"></span><dl> <dt><strong>ERROR_NO_ACTIVE_ISDN_LINES</strong></dt> <dt>713</dt> </dl></td>
<td>Нет доступных активных линий ISDN.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ISDN_CHANNELS_AVAILABLE"></span><span id="error_no_isdn_channels_available"></span><dl> <dt><strong>ERROR_NO_ISDN_CHANNELS_AVAILABLE</strong></dt> <dt>714</dt> </dl></td>
<td>Нет доступных каналов ISDN для выполнения вызова.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_TOO_MANY_LINE_ERRORS"></span><span id="error_too_many_line_errors"></span><dl> <dt><strong>ERROR_TOO_MANY_LINE_ERRORS</strong></dt> <dt>715</dt> </dl></td>
<td>Возникло слишком много ошибок из-за низкого качества телефонной линии.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IP_CONFIGURATION"></span><span id="error_ip_configuration"></span><dl> <dt><strong>ERROR_IP_CONFIGURATION</strong></dt> <dt>716</dt> </dl></td>
<td>IP-конфигурация удаленного доступа непригодна для использования.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_IP_ADDRESSES"></span><span id="error_no_ip_addresses"></span><dl> <dt><strong>ERROR_NO_IP_ADDRESSES</strong></dt> <dt>717</dt> </dl></td>
<td>В статическом пуле IP-адресов удаленного доступа нет доступных IP-адресов.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_TIMEOUT"></span><span id="error_ppp_timeout"></span><dl> <dt><strong>ERROR_PPP_TIMEOUT</strong></dt> <dt>718</dt> </dl></td>
<td>Истекло время ожидания PPP.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REMOTE_TERMINATED"></span><span id="error_ppp_remote_terminated"></span><dl> <dt><strong>ERROR_PPP_REMOTE_TERMINATED</strong></dt> <dt>719</dt> </dl></td>
<td>Соединение было прервано удаленным компьютером.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_PROTOCOLS_CONFIGURED"></span><span id="error_ppp_no_protocols_configured"></span><dl> <dt><strong>ERROR_PPP_NO_PROTOCOLS_CONFIGURED</strong></dt> <dt>720</dt> </dl></td>
<td>Протоколы управления PPP не настроены.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_NO_RESPONSE"></span><span id="error_ppp_no_response"></span><dl> <dt><strong>ERROR_PPP_NO_RESPONSE</strong></dt> <dt>721</dt> </dl></td>
<td>Удаленный узел PPP не отвечает.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_INVALID_PACKET"></span><span id="error_ppp_invalid_packet"></span><dl> <dt><strong>ERROR_PPP_INVALID_PACKET</strong></dt> <dt>722</dt> </dl></td>
<td>Недопустимый пакет PPP.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PHONE_NUMBER_TOO_LONG"></span><span id="error_phone_number_too_long"></span><dl> <dt><strong>ERROR_PHONE_NUMBER_TOO_LONG</strong></dt> <dt>723</dt> </dl></td>
<td>Номер телефона, включая префикс и суффикс, слишком длинный.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NO_DIALOUT_CONFIGURED"></span><span id="error_ipxcp_no_dialout_configured"></span><dl> <dt><strong>ERROR_IPXCP_NO_DIALOUT_CONFIGURED</strong></dt> <dt>724</dt> </dl></td>
<td>Протоколу IPX не удается выполнить вызов через модем (или другое устройство для подключения), так как этот компьютер не настроен для исходящего вызова (это маршрутизатор IPX).<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPXCP_NO_DIALIN_CONFIGURED"></span><span id="error_ipxcp_no_dialin_configured"></span><dl> <dt><strong>ERROR_IPXCP_NO_DIALIN_CONFIGURED</strong></dt> <dt>725</dt> </dl></td>
<td>Протоколу IPX не удается выполнить вызов через модем (или другое устройство для подключения), так как этот компьютер не настроен для набора номера (маршрутизатор IPX не установлен).<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE"></span><span id="error_ipxcp_dialout_already_active"></span><dl> <dt><strong>ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE</strong></dt> <dt>726</dt> </dl></td>
<td>Протокол IPX не может использоваться для удаленного доступа на нескольких портах за один раз.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCESSING_TCPCFGDLL"></span><span id="error_accessing_tcpcfgdll"></span><dl> <dt><strong>ERROR_ACCESSING_TCPCFGDLL</strong></dt> <dt>727</dt> </dl></td>
<td>Не удается получить доступ к TCPCFG.DLL.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_IP_RAS_ADAPTER"></span><span id="error_no_ip_ras_adapter"></span><dl> <dt><strong>ERROR_NO_IP_RAS_ADAPTER</strong></dt> <dt>728</dt> </dl></td>
<td>Не удается найти IP-адаптер, привязанный к удаленному доступу.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SLIP_REQUIRES_IP"></span><span id="error_slip_requires_ip"></span><dl> <dt><strong>ERROR_SLIP_REQUIRES_IP</strong></dt> <dt>729</dt> </dl></td>
<td>Нельзя использовать SLIP, если не установлен протокол IP.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PROJECTION_NOT_COMPLETE"></span><span id="error_projection_not_complete"></span><dl> <dt><strong>ERROR_PROJECTION_NOT_COMPLETE</strong></dt> <dt>730</dt> </dl></td>
<td>Регистрация компьютера не завершена.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_NOT_CONFIGURED"></span><span id="error_protocol_not_configured"></span><dl> <dt><strong>ERROR_PROTOCOL_NOT_CONFIGURED</strong></dt> <dt>731</dt> </dl></td>
<td>Указанный протокол не настроен.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NOT_CONVERGING"></span><span id="error_ppp_not_converging"></span><dl> <dt><strong>ERROR_PPP_NOT_CONVERGING</strong></dt> <dt>732</dt> </dl></td>
<td>Согласование PPP не сходится.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_CP_REJECTED"></span><span id="error_ppp_cp_rejected"></span><dl> <dt><strong>ERROR_PPP_CP_REJECTED</strong></dt> <dt>733</dt> </dl></td>
<td>Протокол управления PPP для указанного сетевого протокола недоступен на сервере.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_LCP_TERMINATED"></span><span id="error_ppp_lcp_terminated"></span><dl> <dt><strong>ERROR_PPP_LCP_TERMINATED</strong></dt> <dt>734</dt> </dl></td>
<td>Протокол управления связью PPP был завершен.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REQUIRED_ADDRESS_REJECTED"></span><span id="error_ppp_required_address_rejected"></span><dl> <dt><strong>ERROR_PPP_REQUIRED_ADDRESS_REJECTED</strong></dt> <dt>735</dt> </dl></td>
<td>Запрошенный адрес был отклонен сервером.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NCP_TERMINATED"></span><span id="error_ppp_ncp_terminated"></span><dl> <dt><strong>ERROR_PPP_NCP_TERMINATED</strong></dt> <dt>736</dt> </dl></td>
<td>Удаленный компьютер прервал протокол управления.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_LOOPBACK_DETECTED"></span><span id="error_ppp_loopback_detected"></span><dl> <dt><strong>ERROR_PPP_LOOPBACK_DETECTED</strong></dt> <dt>737</dt> </dl></td>
<td>Обнаружено замыкание на себя.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_ADDRESS_ASSIGNED"></span><span id="error_ppp_no_address_assigned"></span><dl> <dt><strong>ERROR_PPP_NO_ADDRESS_ASSIGNED</strong></dt> <dt>738</dt> </dl></td>
<td>Сервер не назначил адрес.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_USE_LOGON_CREDENTIALS"></span><span id="error_cannot_use_logon_credentials"></span><dl> <dt><strong>ERROR_CANNOT_USE_LOGON_CREDENTIALS</strong></dt> <dt>739</dt> </dl></td>
<td>удаленный сервер не может использовать зашифрованный пароль Windows NT.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TAPI_CONFIGURATION"></span><span id="error_tapi_configuration"></span><dl> <dt><strong>ERROR_TAPI_CONFIGURATION</strong></dt> <dt>740</dt> </dl></td>
<td>Не удалось инициализировать устройства TAPI, настроенные для удаленного доступа, или они установлены неправильно.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_LOCAL_ENCRYPTION"></span><span id="error_no_local_encryption"></span><dl> <dt><strong>ERROR_NO_LOCAL_ENCRYPTION</strong></dt> <dt>741</dt> </dl></td>
<td>Локальный компьютер не поддерживает шифрование.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_REMOTE_ENCRYPTION"></span><span id="error_no_remote_encryption"></span><dl> <dt><strong>ERROR_NO_REMOTE_ENCRYPTION</strong></dt> <dt>742</dt> </dl></td>
<td>Удаленный сервер не поддерживает шифрование.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_REQUIRES_ENCRYPTION"></span><span id="error_remote_requires_encryption"></span><dl> <dt><strong>ERROR_REMOTE_REQUIRES_ENCRYPTION</strong></dt> <dt>743</dt> </dl></td>
<td>Удаленный компьютер требует шифрования данных.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NET_NUMBER_CONFLICT"></span><span id="error_ipxcp_net_number_conflict"></span><dl> <dt><strong>ERROR_IPXCP_NET_NUMBER_CONFLICT</strong></dt> <dt>744</dt> </dl></td>
<td>Система не может использовать номер сети IPX, назначенный удаленным компьютером. Дополнительные сведения содержатся в журнале событий.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SMM"></span><span id="error_invalid_smm"></span><dl> <dt><strong>ERROR_INVALID_SMM</strong></dt> <dt>745</dt> </dl></td>
<td>Недопустимый модуль управления сеансами (SMM).<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_UNINITIALIZED"></span><span id="error_smm_uninitialized"></span><dl> <dt><strong>ERROR_SMM_UNINITIALIZED</strong></dt> <dt>746</dt> </dl></td>
<td>SMM не инициализирован.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_MAC_FOR_PORT"></span><span id="error_no_mac_for_port"></span><dl> <dt><strong>ERROR_NO_MAC_FOR_PORT</strong></dt> <dt>747</dt> </dl></td>
<td>Отсутствует MAC для порта.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_TIMEOUT"></span><span id="error_smm_timeout"></span><dl> <dt><strong>ERROR_SMM_TIMEOUT</strong></dt> <dt>748</dt> </dl></td>
<td>Истекло время ожидания SMM.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_PHONE_NUMBER"></span><span id="error_bad_phone_number"></span><dl> <dt><strong>ERROR_BAD_PHONE_NUMBER</strong></dt> <dt>749</dt> </dl></td>
<td>Указан недопустимый номер телефона.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_MODULE"></span><span id="error_wrong_module"></span><dl> <dt><strong>ERROR_WRONG_MODULE</strong></dt> <dt>750</dt> </dl></td>
<td>Указана неправильная SMM.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_CALLBACK_NUMBER"></span><span id="error_invalid_callback_number"></span><dl> <dt><strong>ERROR_INVALID_CALLBACK_NUMBER</strong></dt> <dt>751</dt> </dl></td>
<td>Номер обратного вызова содержит недопустимый символ. Допустимы только следующие 18 символов: от 0 до 9, T, P, W, (,),-, @ и пробел.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SCRIPT_SYNTAX"></span><span id="error_script_syntax"></span><dl> <dt><strong>ERROR_SCRIPT_SYNTAX</strong></dt> <dt>752</dt> </dl></td>
<td>При обработке скрипта обнаружена синтаксическая ошибка.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_HANGUP_FAILED"></span><span id="error_hangup_failed"></span><dl> <dt><strong>ERROR_HANGUP_FAILED</strong></dt> <dt>753</dt> </dl></td>
<td>Не удалось отключить подключение, так как оно было создано маршрутизатором с несколькими протоколами.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUNDLE_NOT_FOUND"></span><span id="error_bundle_not_found"></span><dl> <dt><strong>ERROR_BUNDLE_NOT_FOUND</strong></dt> <dt>754</dt> </dl></td>
<td>Системе не удалось найти многоканальный пакет.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DO_CUSTOMDIAL"></span><span id="error_cannot_do_customdial"></span><dl> <dt><strong>ERROR_CANNOT_DO_CUSTOMDIAL</strong></dt> <dt>755</dt> </dl></td>
<td>Система не может выполнить автоматический вызов, так как для этого соединения указан пользовательский номеронабиратель.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIAL_ALREADY_IN_PROGRESS"></span><span id="error_dial_already_in_progress"></span><dl> <dt><strong>ERROR_DIAL_ALREADY_IN_PROGRESS</strong></dt> <dt>756</dt> </dl></td>
<td>Это подключение уже набирается.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASAUTO_CANNOT_INITIALIZE"></span><span id="error_rasauto_cannot_initialize"></span><dl> <dt><strong>ERROR_RASAUTO_CANNOT_INITIALIZE</strong></dt> <dt>757</dt> </dl></td>
<td>Не удалось запустить службу RAS автоматически. Дополнительные сведения содержатся в журнале событий.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_ALREADY_SHARED"></span><span id="error_connection_already_shared"></span><dl> <dt><strong>ERROR_CONNECTION_ALREADY_SHARED</strong></dt> <dt>758</dt> </dl></td>
<td>В подключении уже включен общий доступ к подключению к Интернету (ICS).<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_CHANGE_FAILED"></span><span id="error_sharing_change_failed"></span><dl> <dt><strong>ERROR_SHARING_CHANGE_FAILED</strong></dt> <dt>759</dt> </dl></td>
<td>Произошла ошибка при изменении параметров общего доступа к подключению Интернета.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_ROUTER_INSTALL"></span><span id="error_sharing_router_install"></span><dl> <dt><strong>ERROR_SHARING_ROUTER_INSTALL</strong></dt> <dt>760</dt> </dl></td>
<td>При включении возможностей маршрутизации произошла ошибка.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARE_CONNECTION_FAILED"></span><span id="error_share_connection_failed"></span><dl> <dt><strong>ERROR_SHARE_CONNECTION_FAILED</strong></dt> <dt>761</dt> </dl></td>
<td>При включении общего доступа к подключению к Интернету произошла ошибка.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="7ERROR_SHARING_PRIVATE_INSTALL64"></span><span id="7error_sharing_private_install64"></span><dl> <dt><strong>7ERROR_SHARING_PRIVATE_INSTALL64</strong></dt> <dt>762</dt> </dl></td>
<td>При настройке локальной сети для совместного использования произошла ошибка.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SHARE_CONNECTION"></span><span id="error_cannot_share_connection"></span><dl> <dt><strong>ERROR_CANNOT_SHARE_CONNECTION</strong></dt> <dt>763</dt> </dl></td>
<td>Не удается включить общий доступ к подключению к Интернету. Существует несколько подключений локальной сети, Кроме подключения к общему подключению.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SMART_CARD_READER"></span><span id="error_no_smart_card_reader"></span><dl> <dt><strong>ERROR_NO_SMART_CARD_READER</strong></dt> <dt>764</dt> </dl></td>
<td>Модуль чтения смарт-карт не установлен.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_ADDRESS_EXISTS"></span><span id="error_sharing_address_exists"></span><dl> <dt><strong>ERROR_SHARING_ADDRESS_EXISTS</strong></dt> <dt>765</dt> </dl></td>
<td>Не удается включить общий доступ к подключению к Интернету. Для подключения к локальной сети уже настроен IP-адрес, необходимый для автоматической IP-адресации. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CERTIFICATE"></span><span id="error_no_certificate"></span><dl> <dt><strong>ERROR_NO_CERTIFICATE</strong></dt> <dt>766</dt> </dl></td>
<td>Не удалось найти сертификат. Для подключений, использующих протокол L2TP через IPSec, требуется установка сертификата компьютера, также называемого сертификатом компьютера. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_MULTIPLE_ADDRESSES"></span><span id="error_sharing_multiple_addresses"></span><dl> <dt><strong>ERROR_SHARING_MULTIPLE_ADDRESSES</strong></dt> <dt>767</dt> </dl></td>
<td>Не удается включить общий доступ к подключению к Интернету. Подключение локальной сети, выбранное в качестве частной сети, имеет несколько настроенных IP-адресов. Перед включением общего доступа к Интернету перенастройте подключение локальной сети с помощью одного IP-адреса. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FAILED_TO_ENCRYPT"></span><span id="error_failed_to_encrypt"></span><dl> <dt><strong>ERROR_FAILED_TO_ENCRYPT</strong></dt> <dt>768</dt> </dl></td>
<td>Попытка подключения не удалась из-за сбоя шифрования данных. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_ADDRESS_SPECIFIED"></span><span id="error_bad_address_specified"></span><dl> <dt><strong>ERROR_BAD_ADDRESS_SPECIFIED</strong></dt> <dt>769</dt> </dl></td>
<td>Указанное назначение недоступно. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_REJECT"></span><span id="error_connection_reject"></span><dl> <dt><strong>ERROR_CONNECTION_REJECT</strong></dt> <dt>770</dt> </dl></td>
<td>Удаленный компьютер отклонил попытки подключения. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONGESTION"></span><span id="error_congestion"></span><dl> <dt><strong>ERROR_CONGESTION</strong></dt> <dt>771</dt> </dl></td>
<td>Попытка подключения не удалась, так как сеть занята. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INCOMPATIBLE"></span><span id="error_incompatible"></span><dl> <dt><strong>ERROR_INCOMPATIBLE</strong></dt> <dt>772</dt> </dl></td>
<td>Сетевое оборудование удаленного компьютера несовместимо с типом запрошенного вызова. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NUMBERCHANGED"></span><span id="error_numberchanged"></span><dl> <dt><strong>ERROR_NUMBERCHANGED</strong></dt> <dt>773</dt> </dl></td>
<td>Попытка подключения не удалась, так как номер назначения изменился. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TEMPFAILURE"></span><span id="error_tempfailure"></span><dl> <dt><strong>ERROR_TEMPFAILURE</strong></dt> <dt>774</dt> </dl></td>
<td>Попытка подключения не удалась из-за временного сбоя. Повторите попытку подключения.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BLOCKED"></span><span id="error_blocked"></span><dl> <dt><strong>ERROR_BLOCKED</strong></dt> <dt>775</dt> </dl></td>
<td>Вызов был заблокирован удаленным компьютером. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DONOTDISTURB"></span><span id="error_donotdisturb"></span><dl> <dt><strong>ERROR_DONOTDISTURB</strong></dt> <dt>776</dt> </dl></td>
<td>Не удалось подключить вызов, так как удаленный компьютер вызвал функцию "не беспокоить". <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OUTOFORDER"></span><span id="error_outoforder"></span><dl> <dt><strong>ERROR_OUTOFORDER</strong></dt> <dt>777</dt> </dl></td>
<td>Попытка подключения не удалась из-за неупорядоченного модема или другого устройства подключения на удаленном компьютере. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNABLE_TO_AUTHENTICATE_SERVER"></span><span id="error_unable_to_authenticate_server"></span><dl> <dt><strong>ERROR_UNABLE_TO_AUTHENTICATE_SERVER</strong></dt> <dt>778</dt> </dl></td>
<td>Не удалось проверить удостоверение сервера. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SMART_CARD_REQUIRED"></span><span id="error_smart_card_required"></span><dl> <dt><strong>ERROR_SMART_CARD_REQUIRED</strong></dt> <dt>779</dt> </dl></td>
<td>Для исходящего вызова с помощью этого подключения необходимо использовать смарт-карту.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_FUNCTION_FOR_ENTRY"></span><span id="error_invalid_function_for_entry"></span><dl> <dt><strong>ERROR_INVALID_FUNCTION_FOR_ENTRY</strong></dt> <dt>780</dt> </dl></td>
<td>Предпринятая функция недопустима для этого соединения. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND"></span><span id="error_cert_for_encryption_not_found"></span><dl> <dt><strong>ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND</strong></dt> <dt>781</dt> </dl></td>
<td>Попытка шифрования не удалась, так как не найден допустимый сертификат.<br/>
<blockquote>
[!Note]<br />
не рекомендуется использовать в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_RRAS_CONFLICT"></span><span id="error_sharing_rras_conflict"></span><dl> <dt><strong>ERROR_SHARING_RRAS_CONFLICT</strong></dt> <dt>782</dt> </dl></td>
<td>Общий доступ к подключению (NAT) установлен в качестве протокола маршрутизации и должен быть удален перед включением общего доступа к подключению к Интернету.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_NO_PRIVATE_LAN"></span><span id="error_sharing_no_private_lan"></span><dl> <dt><strong>ERROR_SHARING_NO_PRIVATE_LAN</strong></dt> <dt>783</dt> </dl></td>
<td>Не удается включить общий доступ к подключению к Интернету. Подключение по локальной сети, выбранное в качестве частной, отсутствует или отключено от сети. Убедитесь, что адаптер локальной сети подключен, прежде чем включать общий доступ к подключению к Интернету. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIFF_USER_AT_LOGON"></span><span id="error_no_diff_user_at_logon"></span><dl> <dt><strong>ERROR_NO_DIFF_USER_AT_LOGON</strong></dt> <dt>784</dt> </dl></td>
<td>Нельзя использовать это подключение во время входа, так как оно настроено на использование имени пользователя, отличного от того, на котором установлена смарт-карта. Если вы хотите использовать это подключение во время входа, необходимо настроить его для использования имени пользователя на смарт-карте. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_REG_CERT_AT_LOGON"></span><span id="error_no_reg_cert_at_logon"></span><dl> <dt><strong>ERROR_NO_REG_CERT_AT_LOGON</strong></dt> <dt>785</dt> </dl></td>
<td>Нельзя использовать это подключение во время входа, так как оно не настроено для использования смарт-карты. Если вы хотите использовать его во время входа в систему, необходимо изменить свойства этого подключения так, чтобы оно использовало смарт-карту. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_CERT"></span><span id="error_oakley_no_cert"></span><dl> <dt><strong>ERROR_OAKLEY_NO_CERT</strong></dt> <dt>786</dt> </dl></td>
<td>Попытка L2TP-подключения не удалась, так как на компьютере нет действительного сертификата компьютера для проверки подлинности безопасности. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_AUTH_FAIL"></span><span id="error_oakley_auth_fail"></span><dl> <dt><strong>ERROR_OAKLEY_AUTH_FAIL</strong></dt> <dt>787</dt> </dl></td>
<td>Попытка L2TP-подключения не удалась, так как уровень безопасности не смог проверить подлинность удаленного компьютера. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_ATTRIB_FAIL"></span><span id="error_oakley_attrib_fail"></span><dl> <dt><strong>ERROR_OAKLEY_ATTRIB_FAIL</strong></dt> <dt>788</dt> </dl></td>
<td>Попытка подключения L2TP не удалась, так как уровень безопасности не смог согласовать совместимые параметры с удаленным компьютером. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_GENERAL_PROCESSING"></span><span id="error_oakley_general_processing"></span><dl> <dt><strong>ERROR_OAKLEY_GENERAL_PROCESSING</strong></dt> <dt>789</dt> </dl></td>
<td>Попытка L2TP-подключения не удалась, так как уровень безопасности обнаружил ошибку обработки во время первоначального согласования с удаленным компьютером. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_PEER_CERT"></span><span id="error_oakley_no_peer_cert"></span><dl> <dt><strong>ERROR_OAKLEY_NO_PEER_CERT</strong></dt> <dt>790</dt> </dl></td>
<td>Сбой попытки подключения L2TP из-за сбоя проверки сертификата на удаленном компьютере. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_NO_POLICY"></span><span id="error_oakley_no_policy"></span><dl> <dt><strong>ERROR_OAKLEY_NO_POLICY</strong></dt> <dt>791</dt> </dl></td>
<td>Попытка подключения L2TP не удалась, так как не найдена политика безопасности для подключения. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_TIMED_OUT"></span><span id="error_oakley_timed_out"></span><dl> <dt><strong>ERROR_OAKLEY_TIMED_OUT</strong></dt> <dt>792</dt> </dl></td>
<td>Попытка подключения L2TP не удалась, так как истекло время согласования безопасности. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_ERROR"></span><span id="error_oakley_error"></span><dl> <dt><strong>ERROR_OAKLEY_ERROR</strong></dt> <dt>793</dt> </dl></td>
<td>Попытка L2TP-подключения не удалась, поскольку произошла ошибка при согласовании безопасности. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_FRAMED_PROTOCOL"></span><span id="error_unknown_framed_protocol"></span><dl> <dt><strong>ERROR_UNKNOWN_FRAMED_PROTOCOL</strong></dt> <dt>794</dt> </dl></td>
<td>Атрибут РАДИУСа протокола Frame для этого пользователя не является PPP. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRONG_TUNNEL_TYPE"></span><span id="error_wrong_tunnel_type"></span><dl> <dt><strong>ERROR_WRONG_TUNNEL_TYPE</strong></dt> <dt>795</dt> </dl></td>
<td>недопустимый атрибут RADIUS типа Tunnel для этого пользователя. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_SERVICE_TYPE"></span><span id="error_unknown_service_type"></span><dl> <dt><strong>ERROR_UNKNOWN_SERVICE_TYPE</strong></dt> <dt>796</dt> </dl></td>
<td>Атрибут RADIUS типа службы для этого пользователя не является ни фреймом, ни обратным вызовом. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONNECTING_DEVICE_NOT_FOUND"></span><span id="error_connecting_device_not_found"></span><dl> <dt><strong>ERROR_CONNECTING_DEVICE_NOT_FOUND</strong></dt> <dt>797</dt> </dl></td>
<td>Не удалось установить подключение к удаленному компьютеру, так как модем не найден или занят. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_EAPTLS_CERTIFICATE"></span><span id="error_no_eaptls_certificate"></span><dl> <dt><strong>ERROR_NO_EAPTLS_CERTIFICATE</strong></dt> <dt>798</dt> </dl></td>
<td>Не удалось найти сертификат, который можно использовать с протоколом EAP. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_HOST_ADDRESS_CONFLICT"></span><span id="error_sharing_host_address_conflict"></span><dl> <dt><strong>ERROR_SHARING_HOST_ADDRESS_CONFLICT</strong></dt> <dt>799</dt> </dl></td>
<td>Общий доступ к подключению к Интернету (ICS) не может быть включен из-за конфликта IP-адресов в сети. Для ICS требуется, чтобы узел был настроен для использования <strong>192.168.0.1</strong>. Убедитесь, что никакой другой клиент в сети не настроен на использование <strong>192.168.0.1</strong>.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows XP и более поздних версиях Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Windows 7 и более поздних версий: узел должен быть настроен для использования <strong>192.168.137.1</strong>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTOMATIC_VPN_FAILED"></span><span id="error_automatic_vpn_failed"></span><dl> <dt><strong>ERROR_AUTOMATIC_VPN_FAILED</strong></dt> <dt>800</dt> </dl></td>
<td>Не удалось установить VPN-подключение. VPN-сервер может быть недоступен, или параметры безопасности для этого подключения могут быть неправильно настроены. <br/>
<blockquote>
[!Note]<br />
поддерживается в Windows XP и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VALIDATING_SERVER_CERT"></span><span id="error_validating_server_cert"></span><dl> <dt><strong>ERROR_VALIDATING_SERVER_CERT</strong></dt> <dt>801</dt> </dl></td>
<td>это подключение настроено для проверки подлинности сервера доступа, но Windows не может проверить цифровой сертификат, отправленный сервером.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows XP и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SCARD"></span><span id="error_reading_scard"></span><dl> <dt><strong>ERROR_READING_SCARD</strong></dt> <dt>802</dt> </dl></td>
<td>Указанная карта не распознана. Убедитесь, что карточка вставлена правильно и надежно подходит.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows XP с пакетом обновления 1 (SP1) и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_CONFIG"></span><span id="error_invalid_peap_cookie_config"></span><dl> <dt><strong>ERROR_INVALID_PEAP_COOKIE_CONFIG</strong></dt> <dt>803</dt> </dl></td>
<td>Конфигурация PEAP, хранящаяся в файле cookie сеанса, не соответствует текущей конфигурации сеанса.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows XP с пакетом обновления 1 (SP1) и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PEAP_COOKIE_USER"></span><span id="error_invalid_peap_cookie_user"></span><dl> <dt><strong>ERROR_INVALID_PEAP_COOKIE_USER</strong></dt> <dt>804</dt> </dl></td>
<td>Удостоверение PEAP, хранящееся в файле cookie сеанса, не соответствует текущему удостоверению.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows XP с пакетом обновления 1 (SP1) и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_MSCHAPV2_CONFIG"></span><span id="error_invalid_mschapv2_config"></span><dl> <dt><strong>ERROR_INVALID_MSCHAPV2_CONFIG</strong></dt> <dt>805</dt> </dl></td>
<td>Нельзя использовать это подключение во время входа, так как оно настроено для использования учетных данных пользователя, вошедшего в систему.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows XP с пакетом обновления 1 (SP1) и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_GRE_BLOCKED"></span><span id="error_vpn_gre_blocked"></span><dl> <dt><strong>ERROR_VPN_GRE_BLOCKED</strong></dt> <dt>806</dt> </dl></td>
<td>Подключение между компьютером и VPN-сервером запущено, но VPN-подключение не может быть завершено. Наиболее распространенной причиной этого является то, что хотя бы одно интернет-устройство (например, брандмауэр или маршрутизатор) между компьютером и VPN-сервером не настроено на разрешение пакетов протокола GRE.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_DISCONNECT"></span><span id="error_vpn_disconnect"></span><dl> <dt><strong>ERROR_VPN_DISCONNECT</strong></dt> <dt>807</dt> </dl></td>
<td>Сетевое подключение между компьютером и VPN-сервером было прервано. Это может быть вызвано проблемой в передаче данных через VPN и, как правило, результатом задержки в Интернете или просто тем, что VPN-сервер достиг емкости. Попробуйте повторно подключиться к VPN-серверу.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_REFUSED"></span><span id="error_vpn_refused"></span><dl> <dt><strong>ERROR_VPN_REFUSED</strong></dt> <dt>808</dt> </dl></td>
<td>Не удалось установить сетевое подключение между компьютером и VPN-сервером, так как удаленный сервер отклонил подключение. Обычно это вызвано несоответствием конфигурации сервера и параметров подключения.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_TIMEOUT"></span><span id="error_vpn_timeout"></span><dl> <dt><strong>ERROR_VPN_TIMEOUT</strong></dt> <dt>809</dt> </dl></td>
<td>Не удалось установить сетевое подключение между компьютером и VPN-сервером, так как удаленный сервер не отвечает. Это может быть вызвано тем, что одно из сетевых устройств (например, брандмауэры, NAT, маршрутизаторы) между компьютером и удаленным сервером не настроено для разрешения VPN-подключений.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_BAD_CERT"></span><span id="error_vpn_bad_cert"></span><dl> <dt><strong>ERROR_VPN_BAD_CERT</strong></dt> <dt>810</dt> </dl></td>
<td>Было запущено сетевое подключение между компьютером и VPN-сервером, но VPN-подключение не было завершено. Обычно это вызвано использованием неправильного или просроченного сертификата для проверки подлинности между клиентом и сервером.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_BAD_PSK"></span><span id="error_vpn_bad_psk"></span><dl> <dt><strong>ERROR_VPN_BAD_PSK</strong></dt> <dt>811</dt> </dl></td>
<td>Не удалось установить сетевое подключение между компьютером и VPN-сервером, так как удаленный сервер не отвечает. Обычно это вызвано проблемой с общим ключом между клиентом и сервером. Общий ключ используется для гарантии того, что вы указали, что вы являетесь в цикле связи IP-безопасности (IPSec).<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_POLICY"></span><span id="error_server_policy"></span><dl> <dt><strong>ERROR_SERVER_POLICY</strong></dt> <dt>812</dt> </dl></td>
<td>Подключение не выполнено из-за политики, заданной на вашем RAS/VPN сервере. В частности, метод проверки подлинности, используемый сервером для проверки имени пользователя и пароля, может не соответствовать методу проверки подлинности, настроенному в профиле подключения.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_ACTIVE"></span><span id="error_broadband_active"></span><dl> <dt><strong>ERROR_BROADBAND_ACTIVE</strong></dt> <dt>813</dt> </dl></td>
<td>Предпринята попытка установить второе широкополосное подключение, в то время как предыдущее высокоскоростное подключение уже установлено с помощью того же устройства или порта.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BROADBAND_NO_NIC"></span><span id="error_broadband_no_nic"></span><dl> <dt><strong>ERROR_BROADBAND_NO_NIC</strong></dt> <dt>814</dt> </dl></td>
<td>Не найдено базовое подключение Ethernet, необходимое для широкополосного подключения.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_TIMEOUT"></span><span id="error_broadband_timeout"></span><dl> <dt><strong>ERROR_BROADBAND_TIMEOUT</strong></dt> <dt>815</dt> </dl></td>
<td>Не удалось установить широкополосное сетевое подключение на компьютере, так как удаленный сервер не отвечает. Это может быть вызвано недопустимым значением поля Service Name для этого соединения.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FEATURE_DEPRECATED"></span><span id="error_feature_deprecated"></span><dl> <dt><strong>ERROR_FEATURE_DEPRECATED</strong></dt> <dt>816</dt> </dl></td>
<td>Функция или параметр, которые вы попытались включить, больше не поддерживаются службой удаленного доступа.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DELETE"></span><span id="error_cannot_delete"></span><dl> <dt><strong>ERROR_CANNOT_DELETE</strong></dt> <dt>817</dt> </dl></td>
<td>Невозможно удалить подключение, пока оно подключено.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_RESOURCE_CREATION_FAILED"></span><span id="error_rasqec_resource_creation_failed"></span><dl> <dt><strong>ERROR_RASQEC_RESOURCE_CREATION_FAILED</strong></dt> <dt>818</dt> </dl></td>
<td>Клиенту принудительной защиты доступа к сети (NAP) не удалось создать системные ресурсы для подключений удаленного доступа. Некоторые сетевые службы или ресурсы могут быть недоступны.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_ENABLED"></span><span id="error_rasqec_napagent_not_enabled"></span><dl> <dt><strong>ERROR_RASQEC_NAPAGENT_NOT_ENABLED</strong></dt> <dt>819</dt> </dl></td>
<td>Служба агента защиты доступа к сети (агент NAP) была отключена или не установлена на этом компьютере. Некоторые сетевые службы или ресурсы могут быть недоступны.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_CONNECTED"></span><span id="error_rasqec_napagent_not_connected"></span><dl> <dt><strong>ERROR_RASQEC_NAPAGENT_NOT_CONNECTED</strong></dt> <dt>820</dt> </dl></td>
<td>Клиенту принудительной защиты доступа к сети (NAP) не удалось зарегистрироваться в службе агента защиты доступа к сети (агент NAP). Некоторые сетевые службы или ресурсы могут быть недоступны.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_CONN_DOESNOTEXIST"></span><span id="error_rasqec_conn_doesnotexist"></span><dl> <dt><strong>ERROR_RASQEC_CONN_DOESNOTEXIST</strong></dt> <dt>821</dt> </dl></td>
<td>Клиенту принудительной защиты доступа к сети (NAP) не удалось обработать запрос, так как подключение удаленного доступа не существует.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_TIMEOUT"></span><span id="error_rasqec_timeout"></span><dl> <dt><strong>ERROR_RASQEC_TIMEOUT</strong></dt> <dt>822</dt> </dl></td>
<td>Клиент принудительной защиты доступа к сети (NAP) не ответил. Некоторые сетевые службы или ресурсы могут быть недоступны.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_CRYPTOBINDING_INVALID"></span><span id="error_peap_cryptobinding_invalid"></span><dl> <dt><strong>ERROR_PEAP_CRYPTOBINDING_INVALID</strong></dt> <dt>823</dt> </dl></td>
<td>Получен недопустимый Crypto-Binding тип-длина (TLV).<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED"></span><span id="error_peap_cryptobinding_notreceived"></span><dl> <dt><strong>ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED</strong></dt> <dt>824</dt> </dl></td>
<td>Crypto-Bindingный TLV не получен.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_VPNSTRATEGY"></span><span id="error_invalid_vpnstrategy"></span><dl> <dt><strong>ERROR_INVALID_VPNSTRATEGY</strong></dt> <dt>825</dt> </dl></td>
<td>Туннельный протокол "точка — точка" (PPTP) несовместим с IPv6. Измените тип виртуальной частной сети на протокол L2TP.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_cache_credentials_invalid"></span><dl> <dt><strong>ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>826</dt> </dl></td>
<td>Ошибка при проверке EAPTLS кэшированных учетных данных. Удаление кэшированных учетных данных.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPSEC_SERVICE_STOPPED"></span><span id="error_ipsec_service_stopped"></span><dl> <dt><strong>ERROR_IPSEC_SERVICE_STOPPED</strong></dt> <dt>827</dt> </dl></td>
<td>Не удается завершить подключение по протоколу L2TP и IPsec, так как служба модулей ключей IPSec для IKE и AuthIP и (или) служба модуля базовой фильтрации не запущена. Эти службы необходимы для установления подключения по протоколу L2TP/IPSec.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_TIMEOUT"></span><span id="error_idle_timeout"></span><dl> <dt><strong>ERROR_IDLE_TIMEOUT</strong></dt> <dt>828</dt> </dl></td>
<td>Соединение было прервано из-за истечения времени ожидания простоя.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_LINK_FAILURE"></span><span id="error_link_failure"></span><dl> <dt><strong>ERROR_LINK_FAILURE</strong></dt> <dt>829</dt> </dl></td>
<td>Модем (или другое устройство подключения) был отключен из-за сбоя связи.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_USER_LOGOFF"></span><span id="error_user_logoff"></span><dl> <dt><strong>ERROR_USER_LOGOFF</strong></dt> <dt>830</dt> </dl></td>
<td>Соединение было прервано, так как пользователь вышел из системы.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAST_USER_SWITCH"></span><span id="error_fast_user_switch"></span><dl> <dt><strong>ERROR_FAST_USER_SWITCH</strong></dt> <dt>831</dt> </dl></td>
<td>Соединение было прервано, так как произошло переключение пользователя.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HIBERNATION"></span><span id="error_hibernation"></span><dl> <dt><strong>ERROR_HIBERNATION</strong></dt> <dt>832</dt> </dl></td>
<td>Соединение было прервано из-за гибернации.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SYSTEM_SUSPENDED"></span><span id="error_system_suspended"></span><dl> <dt><strong>ERROR_SYSTEM_SUSPENDED</strong></dt> <dt>833</dt> </dl></td>
<td>Соединение было разорвано из-за приостановки системы.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASMAN_SERVICE_STOPPED"></span><span id="error_rasman_service_stopped"></span><dl> <dt><strong>ERROR_RASMAN_SERVICE_STOPPED</strong></dt> <dt>834</dt> </dl></td>
<td>Соединение прервано, так как диспетчер подключений удаленного доступа остановлен.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SERVER_CERT"></span><span id="error_invalid_server_cert"></span><dl> <dt><strong>ERROR_INVALID_SERVER_CERT</strong></dt> <dt>835</dt> </dl></td>
<td>Попытка L2TP-подключения не удалась, так как уровень безопасности не смог проверить подлинность удаленного компьютера. Это может быть вызвано тем, что одно или несколько полей сертификата, представленного удаленным сервером, не могут быть проверены как принадлежащие целевому назначению.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_NAP_CAPABLE"></span><span id="error_not_nap_capable"></span><dl> <dt><strong>ERROR_NOT_NAP_CAPABLE</strong></dt> <dt>836</dt> </dl></td>
<td>Компьютер не поддерживает защиту доступа к сети.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows Vista и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_TUNNELID"></span><span id="error_invalid_tunnelid"></span><dl> <dt><strong>ERROR_INVALID_TUNNELID</strong></dt> <dt>837</dt> </dl></td>
<td>недопустимый идентификатор Tunnel.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows 7 и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS"></span><span id="error_updateconnection_request_in_process"></span><dl> <dt><strong>ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS</strong></dt> <dt>838</dt> </dl></td>
<td>Выполняется другой запрос на обновление соединения. Служба RAS допускает только один запрос на обновление подключения за раз.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows 7 и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ENGINE_DISABLED"></span><span id="error_protocol_engine_disabled"></span><dl> <dt><strong>ERROR_PROTOCOL_ENGINE_DISABLED</strong></dt> <dt>839</dt> </dl></td>
<td>Согласование с помощью настроенного протокола отключено. Измените свойства соединения и выберите другой протокол для согласования и повторите попытку.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows 7 и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERNAL_ADDRESS_FAILURE"></span><span id="error_internal_address_failure"></span><dl> <dt><strong>ERROR_INTERNAL_ADDRESS_FAILURE</strong></dt> <dt>840</dt> </dl></td>
<td>Сбой согласования внутреннего адреса.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows 7 и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAILED_CP_REQUIRED"></span><span id="error_failed_cp_required"></span><dl> <dt><strong>ERROR_FAILED_CP_REQUIRED</strong></dt> <dt>841</dt> </dl></td>
<td>Клиент должен запросить внутренний адрес IPv4 или IPv6.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows 7 и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TS_UNACCEPTABLE"></span><span id="error_ts_unacceptable"></span><dl> <dt><strong>ERROR_TS_UNACCEPTABLE</strong></dt> <dt>842</dt> </dl></td>
<td>Сбой согласования селекторов трафика.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows 7 и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MOBIKE_DISABLED"></span><span id="error_mobike_disabled"></span><dl> <dt><strong>ERROR_MOBIKE_DISABLED</strong></dt> <dt>843</dt> </dl></td>
<td>Мобильное подключение отключено для этого подключения.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows 7 и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_INITIATE_MOBIKE_UPDATE"></span><span id="error_cannot_initiate_mobike_update"></span><dl> <dt><strong>ERROR_CANNOT_INITIATE_MOBIKE_UPDATE</strong></dt> <dt>844</dt> </dl></td>
<td>Подключение VPN по-прежнему подключается или повторно проходит проверку подлинности из-за изменения состояния карантина. Запускать мобильное обновление только в том случае, если состояние подключения — "Connected".<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows 7 и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV"></span><span id="error_peap_server_rejected_client_tlv"></span><dl> <dt><strong>ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV</strong></dt> <dt>845</dt> </dl></td>
<td>Сервер отклонил проверку подлинности клиента из-за непредвиденного значения TLV или несоответствия значений для TLV.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows 7 и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PREFERENCES"></span><span id="error_invalid_preferences"></span><dl> <dt><strong>ERROR_INVALID_PREFERENCES</strong></dt> <dt>846</dt> </dl></td>
<td>Параметры назначения VPN не выбраны пользователем или больше не являются допустимыми.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows 7 и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_scard_cache_credentials_invalid"></span><dl> <dt><strong>ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>847</dt> </dl></td>
<td>Кэшированные учетные данные смарт-карты недопустимы.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows 7 и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SSTP_COOKIE_SET_FAILURE"></span><span id="error_sstp_cookie_set_failure"></span><dl> <dt><strong>ERROR_SSTP_COOKIE_SET_FAILURE</strong></dt> <dt>848</dt> </dl></td>
<td>Сбой попытки подключения VPN из-за внутренней ошибки при добавлении файлов cookie в протокол SSTP. Подробные сведения см. в журнале системных событий.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES"></span><span id="error_invalid_peap_cookie_attributes"></span><dl> <dt><strong>ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES</strong></dt> <dt>849</dt> </dl></td>
<td>Атрибуты внутреннего метода PEAP, хранящиеся в файле cookie, являются недопустимыми.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_NOT_INSTALLED"></span><span id="error_eap_method_not_installed"></span><dl> <dt><strong>ERROR_EAP_METHOD_NOT_INSTALLED</strong></dt> <dt>850</dt> </dl></td>
<td>Тип протокола расширенной проверки подлинности, необходимый для проверки подлинности подключения удаленного доступа, не установлен на компьютере.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO"></span><span id="error_eap_method_does_not_support_sso"></span><dl> <dt><strong>ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO</strong></dt> <dt>851</dt> </dl></td>
<td>Тип протокола расширяемой проверки подлинности, настроенный для подключения удаленного доступа, не поддерживает единый вход.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="error_eap_method_operation_not_supported"></span><dl> <dt><strong>ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED</strong></dt> <dt>852</dt> </dl></td>
<td>Тип протокола расширяемой проверки подлинности, настроенный для подключения удаленного доступа, не поддерживает запрошенную операцию.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_INVALID"></span><span id="error_eap_user_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_INVALID</strong></dt> <dt>853</dt> </dl></td>
<td>Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как сертификат, проверяющий подлинность клиента на сервере, является недопустимым. Убедитесь, что сертификат, используемый для проверки подлинности, допустим.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_EXPIRED"></span><span id="error_eap_user_cert_expired"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_EXPIRED</strong></dt> <dt>854</dt> </dl></td>
<td>Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как истек срок действия сертификата, проверяющего подлинность клиента на сервере. Продлите сертификат.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_REVOKED"></span><span id="error_eap_user_cert_revoked"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_REVOKED</strong></dt> <dt>855</dt> </dl></td>
<td>Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как сертификат, проверяющий подлинность клиента на сервере, отозван. Используйте сертификат, который не был отозван.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_OTHER_ERROR"></span><span id="error_eap_user_cert_other_error"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_OTHER_ERROR</strong></dt> <dt>856</dt> </dl></td>
<td>Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности из-за ошибки в сертификате, который выполняет проверку подлинности клиента на сервере.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_INVALID"></span><span id="error_eap_server_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_INVALID</strong></dt> <dt>857</dt> </dl></td>
<td>Подключение удаленного доступа выполнено, но проверка подлинности не удалась, так как сертификат, используемый клиентом для проверки подлинности сервера, недопустим.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_EXPIRED"></span><span id="error_eap_server_cert_expired"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_EXPIRED</strong></dt> <dt>858</dt> </dl></td>
<td>Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как истек срок действия сертификата, используемого клиентом для проверки подлинности сервера.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_REVOKED"></span><span id="error_eap_server_cert_revoked"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_REVOKED</strong></dt> <dt>859</dt> </dl></td>
<td>Подключение удаленного доступа выполнено, но проверка подлинности не удалась, так как сертификат, используемый клиентом для проверки подлинности сервера, отозван.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_OTHER_ERROR"></span><span id="error_eap_server_cert_other_error"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_OTHER_ERROR</strong></dt> <dt>860</dt> </dl></td>
<td>Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности из-за ошибки в сертификате, используемом клиентом для проверки подлинности сервера.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_user_root_cert_not_found"></span><dl> <dt><strong>ERROR_EAP_USER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>861</dt> </dl></td>
<td>Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как доверенный корневой сертификат, проверяющий сертификат пользователя, не найден в хранилище сертификатов доверенных корневых центров сертификации.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_ROOT_CERT_INVALID"></span><span id="error_eap_user_root_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_USER_ROOT_CERT_INVALID</strong></dt> <dt>862</dt> </dl></td>
<td>Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как доверенный корневой сертификат, используемый для проверки сертификата пользователя, является недопустимым.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_EXPIRED"></span><span id="error_eap_user_root_cert_expired"></span><dl> <dt><strong>ERROR_EAP_USER_ROOT_CERT_EXPIRED</strong></dt> <dt>863</dt> </dl></td>
<td>Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как истек срок действия сертификата в хранилище сертификатов доверенных корневых центров сертификации, проверяющего сертификат пользователя. Продлите сертификат.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_server_root_cert_not_found"></span><dl> <dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>864</dt> </dl></td>
<td>Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как сертификат, проверяющий сертификат сервера, не найден в хранилище сертификатов доверенных корневых центров сертификации.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_INVALID"></span><span id="error_eap_server_root_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_SERVER_ROOT_CERT_INVALID</strong></dt> <dt>865</dt> </dl></td>
<td>Подключение удаленного доступа выполнено, но проверка подлинности не удалась, так как сертификат в хранилище сертификатов доверенных корневых центров сертификации, который проверяет сертификат сервера, недопустим.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="error_eap_server_root_cert_name_required"></span><dl> <dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED</strong></dt> <dt>866</dt> </dl></td>
<td>Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как для сертификата на сервере не указано имя сервера.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_IDENTITY_MISMATCH"></span><span id="error_peap_identity_mismatch"></span><dl> <dt><strong>ERROR_PEAP_IDENTITY_MISMATCH</strong></dt> <dt>867</dt> </dl></td>
<td>Внешнее удостоверение PEAP не совпадает с внутренним удостоверением при отключении конфиденциальности удостоверений.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DNSNAME_NOT_RESOLVABLE"></span><span id="error_dnsname_not_resolvable"></span><dl> <dt><strong>ERROR_DNSNAME_NOT_RESOLVABLE</strong></dt> <dt>868</dt> </dl></td>
<td>Удаленное соединение не было установлено, так как не удалось разрешить имя сервера удаленного доступа.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_PASSWD_INVALID"></span><span id="error_eaptls_passwd_invalid"></span><dl> <dt><strong>ERROR_EAPTLS_PASSWD_INVALID</strong></dt> <dt>869</dt> </dl></td>
<td>Для сертификата указан недопустимый пароль.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS"></span><span id="error_ikev2_psk_interface_already_exists"></span><dl> <dt><strong>ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>870</dt> </dl></td>
<td>Не удалось включить интерфейс, так как был создан более одного интерфейса с одним и тем же назначением с помощью метода проверки подлинности с общим ключом. Измените метод назначения или проверки подлинности и включите интерфейс.<br/></td>
</tr>
</tbody>
</table>



 

Следующие коды ошибок маршрутизации и удаленного доступа (RRAS) определены в мпреррор. h. все коды ошибок поддерживаются в Windows 2000 или более поздних версиях Windows, если не указано иное.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Возвращаемый код и значение</th>
<th>Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ERROR_ROUTER_STOPPED"></span><span id="error_router_stopped"></span><dl> <dt><strong>ERROR_ROUTER_STOPPED</strong></dt> <dt>900</dt> </dl></td>
<td>Маршрутизатор не работает.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_CONNECTED"></span><span id="error_already_connected"></span><dl> <dt><strong>ERROR_ALREADY_CONNECTED</strong></dt> <dt>901</dt> </dl></td>
<td>Интерфейс уже подключен.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_PROTOCOL_ID"></span><span id="error_unknown_protocol_id"></span><dl> <dt><strong>ERROR_UNKNOWN_PROTOCOL_ID</strong></dt> <dt>902</dt> </dl></td>
<td>Указанный идентификатор протокола неизвестен маршрутизатору.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DDM_NOT_RUNNING"></span><span id="error_ddm_not_running"></span><dl> <dt><strong>ERROR_DDM_NOT_RUNNING</strong></dt> <dt>903</dt> </dl></td>
<td>Диспетчер интерфейсов вызова по требованию (DDM) не работает.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_ALREADY_EXISTS"></span><span id="error_interface_already_exists"></span><dl> <dt><strong>ERROR_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>904</dt> </dl></td>
<td>Интерфейс с таким именем уже зарегистрирован на маршрутизаторе.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_SUCH_INTERFACE"></span><span id="error_no_such_interface"></span><dl> <dt><strong>ERROR_NO_SUCH_INTERFACE</strong></dt> <dt>905</dt> </dl></td>
<td>Интерфейс с таким именем не зарегистрирован на маршрутизаторе.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_NOT_CONNECTED"></span><span id="error_interface_not_connected"></span><dl> <dt><strong>ERROR_INTERFACE_NOT_CONNECTED</strong></dt> <dt>906</dt> </dl></td>
<td>Интерфейс не подключен.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_STOP_PENDING"></span><span id="error_protocol_stop_pending"></span><dl> <dt><strong>ERROR_PROTOCOL_STOP_PENDING</strong></dt> <dt>907</dt> </dl></td>
<td>Указанный протокол останавливается.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONNECTED"></span><span id="error_interface_connected"></span><dl> <dt><strong>ERROR_INTERFACE_CONNECTED</strong></dt> <dt>908</dt> </dl></td>
<td>Интерфейс подключен, и поэтому не может быть удален.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_INTERFACE_CREDENTIALS_SET"></span><span id="error_no_interface_credentials_set"></span><dl> <dt><strong>ERROR_NO_INTERFACE_CREDENTIALS_SET</strong></dt> <dt>909</dt> </dl></td>
<td>Не были заданы учетные данные интерфейса.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALREADY_CONNECTING"></span><span id="error_already_connecting"></span><dl> <dt><strong>ERROR_ALREADY_CONNECTING</strong></dt> <dt>910</dt> </dl></td>
<td>Этот интерфейс уже находится в процессе подключения.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UPDATE_IN_PROGRESS"></span><span id="error_update_in_progress"></span><dl> <dt><strong>ERROR_UPDATE_IN_PROGRESS</strong></dt> <dt>911</dt> </dl></td>
<td>Обновление сведений о маршрутизации для этого интерфейса уже выполняется.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONFIGURATION"></span><span id="error_interface_configuration"></span><dl> <dt><strong>ERROR_INTERFACE_CONFIGURATION</strong></dt> <dt>912</dt> </dl></td>
<td>Недопустимая конфигурации интерфейса. Уже существует другой интерфейс, подключенный к тому же интерфейсу на удаленном маршрутизаторе.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_CLIENT_PORT"></span><span id="error_not_client_port"></span><dl> <dt><strong>ERROR_NOT_CLIENT_PORT</strong></dt> <dt>913</dt> </dl></td>
<td>Клиент удаленного доступа попытался подключиться через порт, зарезервированный только для маршрутизаторов.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_ROUTER_PORT"></span><span id="error_not_router_port"></span><dl> <dt><strong>ERROR_NOT_ROUTER_PORT</strong></dt> <dt>914</dt> </dl></td>
<td>Маршрутизатор вызова по требованию попытался подключиться через порт, зарезервированный только для клиентов удаленного доступа.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CLIENT_INTERFACE_ALREADY_EXISTS"></span><span id="error_client_interface_already_exists"></span><dl> <dt><strong>ERROR_CLIENT_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>915</dt> </dl></td>
<td>Клиентский интерфейс с таким именем уже существует и в настоящее время подключен.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_DISABLED"></span><span id="error_interface_disabled"></span><dl> <dt><strong>ERROR_INTERFACE_DISABLED</strong></dt> <dt>916</dt> </dl></td>
<td>Интерфейс находится в отключенном состоянии.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_PROTOCOL_REJECTED"></span><span id="error_auth_protocol_rejected"></span><dl> <dt><strong>ERROR_AUTH_PROTOCOL_REJECTED</strong></dt> <dt>917</dt> </dl></td>
<td>Протокол проверки подлинности был отклонен удаленным одноранговым узлом.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_AUTH_PROTOCOL_AVAILABLE"></span><span id="error_no_auth_protocol_available"></span><dl> <dt><strong>ERROR_NO_AUTH_PROTOCOL_AVAILABLE</strong></dt> <dt>918</dt> </dl></td>
<td>Нет доступных протоколов проверки подлинности для использования.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEER_REFUSED_AUTH"></span><span id="error_peer_refused_auth"></span><dl> <dt><strong>ERROR_PEER_REFUSED_AUTH</strong></dt> <dt>919</dt> </dl></td>
<td>Не удалось установить подключение, так как протокол проверки подлинности, используемый сервером RAS/VPN для проверки имени пользователя и пароля, не удалось сопоставить с параметрами в профиле подключения.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_NO_DIALIN_PERMISSION"></span><span id="error_remote_no_dialin_permission"></span><dl> <dt><strong>ERROR_REMOTE_NO_DIALIN_PERMISSION</strong></dt> <dt>920</dt> </dl></td>
<td>Удаленная учетная запись не имеет разрешения на удаленный доступ.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_PASSWD_EXPIRED"></span><span id="error_remote_passwd_expired"></span><dl> <dt><strong>ERROR_REMOTE_PASSWD_EXPIRED</strong></dt> <dt>921</dt> </dl></td>
<td>Срок действия удаленной учетной записи истек.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_ACCT_DISABLED"></span><span id="error_remote_acct_disabled"></span><dl> <dt><strong>ERROR_REMOTE_ACCT_DISABLED</strong></dt> <dt>922</dt> </dl></td>
<td>Удаленная учетная запись отключена.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_RESTRICTED_LOGON_HOURS"></span><span id="error_remote_restricted_logon_hours"></span><dl> <dt><strong>ERROR_REMOTE_RESTRICTED_LOGON_HOURS</strong></dt> <dt>923</dt> </dl></td>
<td>Для удаленной учетной записи не разрешено выполнять вход в это время суток.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_AUTHENTICATION_FAILURE"></span><span id="error_remote_authentication_failure"></span><dl> <dt><strong>ERROR_REMOTE_AUTHENTICATION_FAILURE</strong></dt> <dt>924</dt> </dl></td>
<td>Отказано в доступе к удаленному одноранговому узлу, так как имя пользователя, пароль или оба значения недопустимы в домене.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_HAS_NO_DEVICES"></span><span id="error_interface_has_no_devices"></span><dl> <dt><strong>ERROR_INTERFACE_HAS_NO_DEVICES</strong></dt> <dt>925</dt> </dl></td>
<td>Нет доступных портов с поддержкой маршрутизации для использования этим интерфейсом вызова по требованию.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_DISCONNECTED"></span><span id="error_idle_disconnected"></span><dl> <dt><strong>ERROR_IDLE_DISCONNECTED</strong></dt> <dt>926</dt> </dl></td>
<td>Порт был отключен из-за неактивности.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_UNREACHABLE"></span><span id="error_interface_unreachable"></span><dl> <dt><strong>ERROR_INTERFACE_UNREACHABLE</strong></dt> <dt>927</dt> </dl></td>
<td>В данный момент интерфейс недоступен.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVICE_IS_PAUSED"></span><span id="error_service_is_paused"></span><dl> <dt><strong>ERROR_SERVICE_IS_PAUSED</strong></dt> <dt>928</dt> </dl></td>
<td>Служба вызова по требованию находится в приостановленном состоянии.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_DISCONNECTED"></span><span id="error_interface_disconnected"></span><dl> <dt><strong>ERROR_INTERFACE_DISCONNECTED</strong></dt> <dt>929</dt> </dl></td>
<td>Интерфейс отключен администратором.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_SERVER_TIMEOUT"></span><span id="error_auth_server_timeout"></span><dl> <dt><strong>ERROR_AUTH_SERVER_TIMEOUT</strong></dt> <dt>930</dt> </dl></td>
<td>Сервер проверки подлинности не ответил на запросы проверки подлинности в течение отведенного времени.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_LIMIT_REACHED"></span><span id="error_port_limit_reached"></span><dl> <dt><strong>ERROR_PORT_LIMIT_REACHED</strong></dt> <dt>931</dt> </dl></td>
<td>Достигнуто максимально допустимое число портов для использования в многокомпонентном соединении.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_SESSION_TIMEOUT"></span><span id="error_ppp_session_timeout"></span><dl> <dt><strong>ERROR_PPP_SESSION_TIMEOUT</strong></dt> <dt>932</dt> </dl></td>
<td>Достигнуто предельное время подключения для пользователя.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_LAN_INTERFACE_LIMIT"></span><span id="error_max_lan_interface_limit"></span><dl> <dt><strong>ERROR_MAX_LAN_INTERFACE_LIMIT</strong></dt> <dt>933</dt> </dl></td>
<td>Достигнуто максимальное число поддерживаемых интерфейсов локальной сети.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MAX_WAN_INTERFACE_LIMIT"></span><span id="error_max_wan_interface_limit"></span><dl> <dt><strong>ERROR_MAX_WAN_INTERFACE_LIMIT</strong></dt> <dt>934</dt> </dl></td>
<td>Достигнуто предельное число поддерживаемых интерфейсов вызова по требованию.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_CLIENT_INTERFACE_LIMIT"></span><span id="error_max_client_interface_limit"></span><dl> <dt><strong>ERROR_MAX_CLIENT_INTERFACE_LIMIT</strong></dt> <dt>935</dt> </dl></td>
<td>Достигнуто максимальное число поддерживаемых клиентов удаленного доступа.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAP_DISCONNECTED"></span><span id="error_bap_disconnected"></span><dl> <dt><strong>ERROR_BAP_DISCONNECTED</strong></dt> <dt>936</dt> </dl></td>
<td>Порт был отключен из-за политики протокола распределения пропускной способности (BAP).<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_LIMIT"></span><span id="error_user_limit"></span><dl> <dt><strong>ERROR_USER_LIMIT</strong></dt> <dt>937</dt> </dl></td>
<td>Поскольку используется другое подключение типа, входящее подключение не может принять ваш запрос на подключение.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RADIUS_SERVERS"></span><span id="error_no_radius_servers"></span><dl> <dt><strong>ERROR_NO_RADIUS_SERVERS</strong></dt> <dt>938</dt> </dl></td>
<td>В сети не было найдено ни одного RADIUS-сервера.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_RADIUS_RESPONSE"></span><span id="error_invalid_radius_response"></span><dl> <dt><strong>ERROR_INVALID_RADIUS_RESPONSE</strong></dt> <dt>939</dt> </dl></td>
<td>От сервера проверки подлинности RADIUS получен недопустимый ответ. Убедитесь, что секретный пароль с учетом регистра для сервера RADIUS установлен правильно.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALIN_HOURS_RESTRICTION"></span><span id="error_dialin_hours_restriction"></span><dl> <dt><strong>ERROR_DIALIN_HOURS_RESTRICTION</strong></dt> <dt>940</dt> </dl></td>
<td>У вас нет разрешения на подключение в данный момент.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALLOWED_PORT_TYPE_RESTRICTION"></span><span id="error_allowed_port_type_restriction"></span><dl> <dt><strong>ERROR_ALLOWED_PORT_TYPE_RESTRICTION</strong></dt> <dt>941</dt> </dl></td>
<td>У вас нет разрешения на подключение с использованием текущего типа устройства.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_PROTOCOL_RESTRICTION"></span><span id="error_auth_protocol_restriction"></span><dl> <dt><strong>ERROR_AUTH_PROTOCOL_RESTRICTION</strong></dt> <dt>942</dt> </dl></td>
<td>Не удалось установить подключение, так как метод проверки подлинности, используемый в профиле подключения, не разрешен для использования политикой доступа, настроенной на сервере RAS/VPN. В частности, это может быть вызвано различиями в конфигурации метода проверки подлинности, выбранного на сервере RAS/VPN, и политики доступа, настроенной для нее.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAP_REQUIRED"></span><span id="error_bap_required"></span><dl> <dt><strong>ERROR_BAP_REQUIRED</strong></dt> <dt>943</dt> </dl></td>
<td>Для этого пользователя требуется BAP.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALOUT_HOURS_RESTRICTION"></span><span id="error_dialout_hours_restriction"></span><dl> <dt><strong>ERROR_DIALOUT_HOURS_RESTRICTION</strong></dt> <dt>944</dt> </dl></td>
<td>В данный момент интерфейс не может подключаться.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTER_CONFIG_INCOMPATIBLE"></span><span id="error_router_config_incompatible"></span><dl> <dt><strong>ERROR_ROUTER_CONFIG_INCOMPATIBLE</strong></dt> <dt>945</dt> </dl></td>
<td>Сохраненная конфигурация маршрутизатора несовместима с текущим маршрутизатором.<br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_NO_MD5_MIGRATION"></span><span id="warning_no_md5_migration"></span><dl> <dt><strong>WARNING_NO_MD5_MIGRATION</strong></dt> <dt>946</dt> </dl></td>
<td>Удаленный доступ обнаружил устаревшие учетные записи пользователей в формате, которые не будут автоматически перенесены.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ALREADY_INSTALLED"></span><span id="error_protocol_already_installed"></span><dl> <dt><strong>ERROR_PROTOCOL_ALREADY_INSTALLED</strong></dt> <dt>948</dt> </dl></td>
<td>Транспорт уже установлен с маршрутизатором.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIGNATURE_LENGTH"></span><span id="error_invalid_signature_length"></span><dl> <dt><strong>ERROR_INVALID_SIGNATURE_LENGTH</strong></dt> <dt>949</dt> </dl></td>
<td>Недопустимая длина подписи, полученная в пакете от сервера RADIUS.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows XP и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SIGNATURE"></span><span id="error_invalid_signature"></span><dl> <dt><strong>ERROR_INVALID_SIGNATURE</strong></dt> <dt>950</dt> </dl></td>
<td>Недопустимая подпись, полученная в пакете от сервера RADIUS.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows XP и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SIGNATURE"></span><span id="error_no_signature"></span><dl> <dt><strong>ERROR_NO_SIGNATURE</strong></dt> <dt>951</dt> </dl></td>
<td>Не получал подпись и Еапмессаже от сервера RADIUS.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows XP и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET_LENGTH_OR_ID"></span><span id="error_invalid_packet_length_or_id"></span><dl> <dt><strong>ERROR_INVALID_PACKET_LENGTH_OR_ID</strong></dt> <dt>952</dt> </dl></td>
<td>Недопустимая длина или идентификатор, полученный в пакете от сервера RADIUS.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows XP и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_ATTRIBUTE_LENGTH"></span><span id="error_invalid_attribute_length"></span><dl> <dt><strong>ERROR_INVALID_ATTRIBUTE_LENGTH</strong></dt> <dt>953</dt> </dl></td>
<td>Недопустимая длина, полученная в пакете с атрибутом от сервера RADIUS.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows XP и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET"></span><span id="error_invalid_packet"></span><dl> <dt><strong>ERROR_INVALID_PACKET</strong></dt> <dt>954</dt> </dl></td>
<td>Недопустимый пакет, полученный от сервера RADIUS.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows XP и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTHENTICATOR_MISMATCH"></span><span id="error_authenticator_mismatch"></span><dl> <dt><strong>ERROR_AUTHENTICATOR_MISMATCH</strong></dt> <dt>955</dt> </dl></td>
<td>Authenticator не совпадает в пакете от RADIUS-сервера.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows XP и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTEACCESS_NOT_CONFIGURED"></span><span id="error_remoteaccess_not_configured"></span><dl> <dt><strong>ERROR_REMOTEACCESS_NOT_CONFIGURED</strong></dt> <dt>956</dt> </dl></td>
<td>Сервер маршрутизации и удаленного доступа либо не настроен, либо не работает.<br/>
<blockquote>
[!Note]<br />
поддерживается в Windows 7 и более поздних версиях Windows.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



 

 





