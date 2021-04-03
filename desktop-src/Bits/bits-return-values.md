---
title: Значения, возвращаемые BITS
description: Файл Битсмсг. h содержит следующие константы возвращаемого значения.
ms.assetid: 8df5022a-b161-4558-9d60-efdbdf1754d6
keywords:
- БИТЫ ошибок
- БИТЫ ошибок, коды
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9086de1d55bbdc9695876bd06368ab28dbbb161
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987756"
---
# <a name="bits-return-values"></a>Значения, возвращаемые BITS

Файл Битсмсг. h содержит следующие константы возвращаемого значения. Константы представляют возвращаемые значения, создаваемые BITS, и возвращаемые значения HTTP, которые захватывают биты. Все остальные возвращаемые значения — это COM, RPC или преобразованные возвращаемые значения Windows (BITS использует значение [HRESULT из макроса \_ \_ Win32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) для преобразования возвращаемых значений Windows в значения HRESULT).

Обратите внимание, что файл Битсмсг. h содержит дополнительные возвращаемые значения, не указанные ниже.

<dl> <dt>

<span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>\_ \_ Частично \_ завершено: BG (0x00200017)
</dt> <dd>

Переданное подмножество файлов задания успешно передано до вызова метода [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Были удалены те, которые не были завершены.

</dd> <dt>

<span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG \_ S \_ не \_ удается \_ удалить \_ файлы (0x0020001A)
</dt> <dd>

Не удалось удалить все временные файлы, связанные с заданием.

</dd> <dt>

<span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG \_ S \_ переопределяется \_ \_ политикой (0x00200055)
</dt> <dd>

Настройка конфигурации успешно сохранена, но предпочтение не будет использоваться, так как настроенный параметр групповая политика переопределяет настройки.

</dd> <dt>

<span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG \_ E \_ не \_ найдено (0x80200001)
</dt> <dd>

Запрошенное задание не найдено.

</dd> <dt>

<span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>\_ \_ Недопустимое состояние BG E \_ (0x80200002)
</dt> <dd>

Запрошенное действие запрещено в текущем состоянии задания.

</dd> <dt>

<span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ Empty (0x80200003)
</dt> <dd>

Задание должно содержать один или несколько файлов, прежде чем можно будет возобновить задание.

</dd> <dt>

<span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>\_Файл BG \_ E \_ \_ недоступен (0x80200004)
</dt> <dd>

Сведения о файле недоступны, так как ошибка не связана с локальным или удаленным файлом.

</dd> <dt>

<span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>\_Протокол BG \_ E \_ \_ недоступен (0x80200005)
</dt> <dd>

Сведения о протоколе недоступны, так как ошибка не связана с указанным Протоколом перемещения.

</dd> <dt>

<span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>\_ \_ Место назначения BG E \_ заблокировано (0x8020000D)
</dt> <dd>

Целевой том файловой системы, указанный в имени локального файла, заблокирован.

</dd> <dt>

<span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>\_ \_ Изменение тома BG E \_ (0x8020000E)
</dt> <dd>

Изменился целевой том, указанный в имени локального файла. Например, исходная дискета заменена на другой гибкий диск.

</dd> <dt>

<span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>\_ \_ Недоступная информация об ошибке BG E \_ \_ (0x8020000F)
</dt> <dd>

Сведения об ошибках доступны, только если состояние задания — \_ \_ Ошибка состояния задания BG \_ . Сведения об ошибке недоступны после того, как служба BITS начнет передачу данных задания или завершает работу клиента.

</dd> <dt>

<span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>\_Сеть BG \_ E \_ отключена (0x80200010)
</dt> <dd>

Сетевой адаптер неактивен или отключен. Все задания помещаются в \_ \_ \_ состояние промежуточной ошибки состояния задания BG \_ .

</dd> <dt>

<span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG \_ E \_ отсутствует \_ \_ Размер файла (0x80200011)
</dt> <dd>

Сервер не возвратил размер файла. Служба BITS передает только статическое содержимое и требует, чтобы HTTP-сервер возвращал заголовок Content-Length. Запрос на перемещение завершается неудачей, если URL-адрес указывает на динамическое содержимое.

</dd> <dt>

<span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>\_ \_ Недостаточная \_ Поддержка HTTP BG E \_ (0x80200012)
</dt> <dd>

Сервер не поддерживает протокол HTTP/1.1.

</dd> <dt>

<span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>\_ \_ Недостаточная \_ Поддержка диапазона BG E \_ (0x80200013)
</dt> <dd>

Сервер не поддерживает заголовок Content-Range. Как правило, эта ошибка возникает при попытке загрузить динамическое содержимое. Эту ошибку также можно получить, если промежуточный прокси-сервер удаляет заголовок Content-Range или Content-Length.

</dd> <dt>

<span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>\_ \_ Удаленное \_ \_ неподдерживаемое "BG E" (0x80200014)
</dt> <dd>

Удаленное использование BITS не поддерживается. Дополнительные сведения см. в разделе [Пользователи и сетевые подключения](users-and-network-connections.md).

</dd> <dt>

<span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG \_ — \_ новое \_ \_ сопоставление различий \_ (0x80200015)
</dt> <dd>

Сопоставление сетевых дисков для локального файла отличается от сопоставления для текущего владельца, чем для предыдущего владельца.

</dd> <dt>

<span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E \_ новый \_ владелец \_ нет \_ \_ доступа к файлам (0x80200016)
</dt> <dd>

У нового владельца недостаточно разрешений для временных файлов заданий.

</dd> <dt>

<span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>\_ \_ Слишком большой список прокси-серверов BG E \_ \_ \_ (0x80200018)
</dt> <dd>

Список прокси-серверов HTTP слишком длинный. Размер списка не должен превышать 32 КБ.

</dd> <dt>

<span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>\_ \_ Слишком большой список обхода прокси-сервера BG E \_ \_ \_ \_ (0x80200019)
</dt> <dd>

Список обхода прокси-сервера HTTP слишком длинный. Размер списка не должен превышать 32 КБ.

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>\_ \_ Слишком \_ много файлов BG E \_ (0x8020001C)
</dt> <dd>

В задание отправки нельзя добавить более одного файла.

</dd> <dt>

<span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>\_ \_ Изменение ЛОКАЛЬНОГО файла BG E \_ \_ (0x8020001D)
</dt> <dd>

Содержимое локального файла изменилось после начала процесса перемещения. Содержимое локального файла не может измениться после начала процесса передачи для задания отправки или отправки-ответа.

</dd> <dt>

<span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>\_ \_ Слишком большой BG E \_ (0x80200020)
</dt> <dd>

Размер файла отправки превышает максимально допустимый размер отправки, указанный на сервере.

</dd> <dt>

<span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>\_ \_ \_ Слишком длинная строка BG E \_ (0x80200021)
</dt> <dd>

Указана слишком длинная строка.

</dd> <dt>

<span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>\_Несоответствие \_ протокола клиентского сервера BG E \_ \_ \_ (0x80200022)
</dt> <dd>

Клиенту и серверу не удалось согласовать протокол, используемый для задания отправки.

</dd> <dt>

<span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>\_Сервер BG E с \_ \_ \_ включенным выполнением (0x80200023)
</dt> <dd>

В виртуальном каталоге IIS, связанном с заданием, включены разрешения на выполнение скриптов или выполнения. Чтобы передать файлы в виртуальный каталог, отключите разрешения скрипта и выполнения для виртуального каталога.

</dd> <dt>

<span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>\_ \_ Слишком большое имя пользователя BG E \_ \_ (0x80200025)
</dt> <dd>

Длина имени пользователя не может превышать 300 символов.

</dd> <dt>

<span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>\_ \_ Слишком большой пароль BG E \_ \_ (0x80200026)
</dt> <dd>

Длина пароля не может превышать 65535 символов.

</dd> <dt>

<span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>\_ \_ Недопустимый \_ целевой объект проверки подлинности BG E \_ (0x80200027)
</dt> <dd>

Указан недопустимый целевой объект проверки подлинности.

</dd> <dt>

<span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>\_ \_ Недопустимый \_ Схема проверки подлинности BG E \_ (0x80200028)
</dt> <dd>

Указана недопустимая схема проверки подлинности.

</dd> <dt>

<span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG \_ E \_ : недопустимый \_ диапазон (0x8020002B)
</dt> <dd>

Указанный диапазон байтов недопустим. Диапазон байтов должен существовать в указанном удаленном файле.

</dd> <dt>

<span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>\_Перекрывающиеся \_ \_ диапазоны BG E (0x8020002C)
</dt> <dd>

Список диапазонов байтов содержит перекрывающиеся или дублирующиеся диапазоны, которые не поддерживаются.

</dd> <dt>

<span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E \_ заблокировано \_ \_ политикой (0x8020003E)
</dt> <dd>

Параметры групповая политика не позволяют выполнять фоновые задания в данный момент. Дополнительные сведения см. в описании политики [максинтернетбандвидс](group-policies.md) .

</dd> <dt>

<span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG \_ E \_ недопустимые \_ \_ сведения о прокси (0x8020003F)
</dt> <dd>

Ошибка времени выполнения, указывающая на список прокси-серверов или список обхода прокси-сервера, указанный с помощью метода [**использованием метода ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) , недопустим.

</dd> <dt>

<span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG \_ E \_ недопустимые \_ учетные данные (0x80200040)
</dt> <dd>

Недопустимый формат предоставленных учетных данных безопасности.

</dd> <dt>

<span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>\_ \_ Удалена запись BG E \_ (0x80200042)
</dt> <dd>

Запись кэша удалена. Попытка обновить ее была прервана.

</dd> <dt>

<span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>\_ \_ Ошибка UPnP BG E \_ (0x80200045)
</dt> <dd>

Произошла ошибка универсального самонастраивающийся (UPnP). Проверьте устройство шлюза Интернета.

</dd> <dt>

<span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>\_ \_ Недоступен одноранговый кэшированный BG E \_ (0x80200047)
</dt> <dd>

Одноранговое кэширование отключено.

</dd> <dt>

<span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ бусикачерекорд (0x80200048)
</dt> <dd>

Запись кэша используется и не может быть изменена или удалена. Повторите попытку через несколько секунд.

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>\_ \_ Превышено \_ Максимальное количество \_ заданий \_ на \_ пользователя: BG (0x80200049)
</dt> <dd>

Число заданий для пользователя превысило предел для задания на пользователя, заданный параметром групповая политика Maxjobspermachine.

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>\_ \_ \_ Максимальное количество \_ заданий \_ в одном \_ компьютере (0x80200050): BG
</dt> <dd>

Число заданий на компьютере превысило предел для заданий на компьютер, заданный параметром групповая политика MaxJobsPerMachine.

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>\_ \_ Слишком \_ много \_ файлов \_ в \_ задании BG (0x80200051)
</dt> <dd>

Число файлов для задания превысило ограничение на количество файлов заданий, заданное параметром групповая политика MaxFilesPerJob.

</dd> <dt>

<span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>\_ \_ Слишком \_ много \_ диапазонов \_ в \_ файле (0x80200052) BG E
</dt> <dd>

Число диапазонов для файла превысило предел для диапазона файлов, заданный параметром групповая политика MaxRangesPerFile.

</dd> <dt>

<span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>\_ \_ Сбой проверки BG E \_ (0x80200053)
</dt> <dd>

Приложение запросило данные с веб-сайта, но ответ был недопустимым. Для получения дополнительных сведений используйте Просмотр событий для просмотра журнала приложений \\ Microsoft \\ Windows \\ BITS — \\ Журнал операций клиента.

</dd> <dt>

<span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>\_ \_ Максдовнлоад \_ тайм-аута BG E (0x80200054)
</dt> <dd>

Время ожидания BITS при скачивании задания. Загрузка не была завершена в течение максимального времени загрузки, заданного для задания или параметра групповая политика Максдовнлоадтиме.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 400 (0x80190190)
</dt> <dd>

Серверу не удалось обработать запрос на перемещение из-за недопустимого синтаксиса имени удаленного файла.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 401 (0x80190191)
</dt> <dd>

У пользователя нет разрешения на доступ к удаленному файлу. Запрошенный ресурс требует проверки подлинности пользователя.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 404 (0x80190194)
</dt> <dd>

Запрошенный URL-адрес не существует на сервере.

В IIS 7 Эта ошибка может означать, что

-   Отправка BITS не включена в виртуальном каталоге (vdir) на сервере.
-   , Что размер передачи превышает максимальный предел загрузки (Дополнительные сведения см. в описании свойства расширения IIS [**битсмаксимумуплоадсизе**](bits-iis-extension-properties.md) ).

</dd> <dt>

<span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 407 (0x80190197)
</dt> <dd>

У пользователя нет разрешения на доступ к прокси-серверу. Прокси-сервер требует проверки подлинности пользователя.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 414 (0x8019019E)
</dt> <dd>

Серверу не удается обработать запрос на перемещение. Длина универсального кода ресурса (URI) в имени удаленного файла превышает длину, которую может интерпретировать сервер.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 501 (0x801901F5)
</dt> <dd>

Сервер не поддерживает функции, необходимые для выполнения запроса. В IIS 6 Эта ошибка означает, что отправка BITS не включена в виртуальном каталоге (vdir) на сервере.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 503 (0x801901F7)
</dt> <dd>

Служба временно перегружена и не может обработать запрос. Возобновите задание позже.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 504 (0x801901F8)
</dt> <dd>

Истекло время ожидания запроса на перемещение при ожидании шлюза. Возобновите задание позже.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 505 (0x801901F9)
</dt> <dd>

Сервер не поддерживает версию протокола HTTP, указанную в имени удаленного файла.

</dd> </dl>

Файл заголовка Битсмсг. h содержит дополнительные возвращаемые значения HTTP, не указанные выше, которые используются службой BITS для внутренних целей. Дополнительные сведения об этих и других возвращаемых значениях HTTP см. в спецификации RFC 2616, приведенной в статье о задачах веб-проектирования в [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) .

 

 