---
description: Описание кодов ошибок 6000-8199, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: Коды системных ошибок (6000-8199) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: d24a165798f0d4bf8a3ed534880cd3f9ad1f2b8b85d072e8a4d7aae8e6345508
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131664"
---
# <a name="system-error-codes-6000-8199"></a>Коды системных ошибок (6000-8199)

> [!NOTE]
> Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки. для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.

В следующем списке приведены [коды системных ошибок](system-error-codes.md) (ошибки 6000 – 8199). Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций. Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .

<dl> <dt>

<span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**Ошибка \_ шифрования \_ при ошибке**
</dt> <dd> <dl> <dt>

6000 (0x1770)
</dt> <dt>



Указанный файл не может быть зашифрован.


</dt> </dl> </dd> <dt>

<span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**\_сбой при расшифровке ошибки \_**
</dt> <dd> <dl> <dt>

6001 (0x1771)
</dt> <dt>



Не удалось расшифровать указанный файл.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**файл с ОШИБКАми \_ \_ зашифрован**
</dt> <dd> <dl> <dt>

6002 (0x1772)
</dt> <dt>



Указанный файл зашифрован, и пользователь не может его расшифровать.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**Ошибка \_ без \_ \_ политики восстановления**
</dt> <dd> <dl> <dt>

6003 (0x1773)
</dt> <dt>



Для этой системы не настроена допустимая политика восстановления шифрования.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**Ошибка \_ без \_ EFS**
</dt> <dd> <dl> <dt>

6004 (0x1774)
</dt> <dt>



Необходимый для этой системы драйвер шифрования не загружен.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**произошла ошибка \_ \_ EFS**
</dt> <dd> <dl> <dt>

6005 (0x1775)
</dt> <dt>



Файл был зашифрован с использованием другого драйвера шифрования, чем в настоящий момент загружен.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**Ошибка \_ без \_ \_ ключей пользователей**
</dt> <dd> <dl> <dt>

6006 (0x1776)
</dt> <dt>



Для пользователя не определены ключи EFS.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**\_файл ошибок \_ не \_ зашифрован**
</dt> <dd> <dl> <dt>

6007 (0x1777)
</dt> <dt>



Указанный файл не зашифрован.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**Ошибка \_ при \_ экспорте \_ формата**
</dt> <dd> <dl> <dt>

6008 (0x1778)
</dt> <dt>



Указанный файл не находится в определенном формате экспорта EFS.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**Ошибка \_ файл \_ только для чтения \_**
</dt> <dd> <dl> <dt>

6009 (0x1779)
</dt> <dt>



Указанный файл доступен только для чтения.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**Ошибка \_ dir. \_ EFS \_ запрещена**
</dt> <dd> <dl> <dt>

6010 (0x177A)
</dt> <dt>



Для этого каталога отключено шифрование.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**Ошибка \_ " \_ сервер EFS \_ не является \_ доверенным"**
</dt> <dd> <dl> <dt>

6011 (0x177B)
</dt> <dt>



Сервер не является доверенным для удаленной операции шифрования.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**Ошибка \_ неправильной \_ \_ политики восстановления**
</dt> <dd> <dl> <dt>

6012 (0x177C)
</dt> <dt>



Политика восстановления, настроенная для этой системы, содержит недопустимый сертификат восстановления.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**Ошибка \_ \_ \_ \_ слишком \_ большой размер BLOB-объекта алгоритма EFS**
</dt> <dd> <dl> <dt>

6013 (0x177D)
</dt> <dt>



Алгоритму шифрования, используемому в исходном файле, требуется больший буфер ключа, чем тот, который находится в целевом файле.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**\_том ошибок \_ не \_ поддерживает \_ EFS**
</dt> <dd> <dl> <dt>

6014 (0x177E)
</dt> <dt>



Раздел диска не поддерживает шифрование файлов.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**Ошибка \_ EFS \_ отключена**
</dt> <dd> <dl> <dt>

6015 (0x177F)
</dt> <dt>



Этот компьютер отключен для шифрования файлов.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**Ошибка \_ \_ \_ не поддерживает версию \_ EFS**
</dt> <dd> <dl> <dt>

6016 (0x1780)
</dt> <dt>



Для расшифровки этого зашифрованного файла требуется более новая система.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**Ошибка \_ CS \_ ENCRYPTION \_ Недопустимый \_ \_ ответ сервера**
</dt> <dd> <dl> <dt>

6017 (0x1781)
</dt> <dt>



Удаленный сервер отправил недопустимый ответ для открываемого файла с шифрованием на стороне клиента.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**Ошибка \_ CS \_ ENCRYPTION \_ неподдерживаемый \_ сервер**
</dt> <dd> <dl> <dt>

6018 (0x1782)
</dt> <dt>



Шифрование на стороне клиента не поддерживается удаленным сервером, хотя оно требует его поддержки.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**Ошибка \_ CS \_ Шифрование \_ существующего \_ зашифрованного \_ файла**
</dt> <dd> <dl> <dt>

6019 (0x1783)
</dt> <dt>



Файл зашифрован и должен быть открыт в режиме шифрования на стороне клиента.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**Ошибка \_ CS \_ Шифрование \_ нового \_ зашифрованного \_ файла**
</dt> <dd> <dl> <dt>

6020 (0x1784)
</dt> <dt>



Создается новый зашифрованный файл, и необходимо указать $EFS.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**Ошибка \_ CS \_ \_ File Encryption \_ не является \_ CSE**
</dt> <dd> <dl> <dt>

6021 (0x1785)
</dt> <dt>



Клиент SMB запросил CSE ФСКТЛ в файле, отличном от CSE.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**\_Политика шифрования \_ ошибок \_ запрещает \_ операцию**
</dt> <dd> <dl> <dt>

6022 (0x1786)
</dt> <dt>



Запрошенная операция заблокирована политикой. Для получения дополнительных сведений обратитесь к системному администратору.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**Ошибка \_ не \_ \_ найдены серверы \_ браузера**
</dt> <dd> <dl> <dt>

6118 (0x17E6)
</dt> <dt>



Список серверов для этой Рабочей группы в настоящее время недоступен.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**SCHED \_ E \_ Service \_ Not \_ LocalSystem**
</dt> <dd> <dl> <dt>

6200 (0x1838)
</dt> <dt>



Служба планировщик задач должна быть настроена для правильной работы в системной учетной записи. Отдельные задачи могут быть настроены для работы в других учетных записях.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**\_ \_ Недопустимый сектор журнала ошибок \_**
</dt> <dd> <dl> <dt>

6600 (0x19C8)
</dt> <dt>



Служба журнала обнаружила недопустимый сектор журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**\_ \_ \_ Недопустимый контроль четности для сектора журнала \_ ошибок**
</dt> <dd> <dl> <dt>

6601 (0x19C9)
</dt> <dt>



Служба журнала обнаружила сектор журнала с недопустимым контролем четности блоков.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**повторное \_ \_ сопоставление сектора журнала ошибок \_**
</dt> <dd> <dl> <dt>

6602 (0x19CA)
</dt> <dt>



Служба журнала обнаружила повторно сопоставленный сектор журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**\_неполный \_ блок журнала ошибок \_**
</dt> <dd> <dl> <dt>

6603 (0x19CB)
</dt> <dt>



Служба журнала обнаружила частичный или неполный блок журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**\_ \_ Недопустимый \_ диапазон журнала ошибок**
</dt> <dd> <dl> <dt>

6604 (0x19CC)
</dt> <dt>



Служба журнала обнаружила попытки доступа к данным за пределами активного диапазона журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**\_ \_ исчерпаны блоки журнала ошибок \_**
</dt> <dd> <dl> <dt>

6605 (0x19CD)
</dt> <dt>



Буферы для пользователя службы журнала исчерпаны.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**\_ \_ \_ Недопустимый контекст \_ чтения журнала ошибок**
</dt> <dd> <dl> <dt>

6606 (0x19CE)
</dt> <dt>



Служба журнала обнаружила операцию чтения из области маршалирования с недопустимым контекстом чтения.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**\_ \_ Недопустимый ПЕРЕЗАПУСК журнала ошибок \_**
</dt> <dd> <dl> <dt>

6607 (0x19CF)
</dt> <dt>



Служба журнала обнаружила недопустимую область перезапуска журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**\_ \_ версия блока журнала \_ ошибок**
</dt> <dd> <dl> <dt>

6608 (0x19D0)
</dt> <dt>



Служба журнала обнаружила недопустимую версию блока журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**\_ \_ Недопустимый блок журнала ошибок \_**
</dt> <dd> <dl> <dt>

6609 (0x19D1)
</dt> <dt>



Служба журнала обнаружила недопустимый блок журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**\_ \_ \_ Недопустимый режим \_ чтения журнала ошибок**
</dt> <dd> <dl> <dt>

6610 (0x19D2)
</dt> <dt>



Служба журнала обнаружила попытку чтения журнала с недопустимым режимом чтения.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**\_журнал ошибок \_ без \_ перезагрузки**
</dt> <dd> <dl> <dt>

6611 (0x19D3)
</dt> <dt>



Служба журнала обнаружила поток журнала без области перезапуска.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**\_ \_ повреждение МЕТАДАННЫХ журнала \_ ошибок**
</dt> <dd> <dl> <dt>

6612 (0x19D4)
</dt> <dt>



Служба журнала обнаружила поврежденный файл метаданных.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**\_ \_ недопустимые метаданные журнала ошибок \_**
</dt> <dd> <dl> <dt>

6613 (0x19D5)
</dt> <dt>



Служба журнала обнаружила файл метаданных, который не удалось создать с помощью файловой системы журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**\_несоответствие \_ МЕТАДАННЫХ журнала ошибок \_**
</dt> <dd> <dl> <dt>

6614 (0x19D6)
</dt> <dt>



Служба журнала обнаружила файл метаданных с непоследовательными данными.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**\_ \_ недопустимое резервирование журнала ошибок \_**
</dt> <dd> <dl> <dt>

6615 (0x19D7)
</dt> <dt>



Служба журнала обнаружила попытку ошибочного выделения или удаления пространства резервирования.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**журнал ошибок "не \_ \_ удается \_ Удалить"**
</dt> <dd> <dl> <dt>

6616 (0x19D8)
</dt> <dt>



Службе журнала не удается удалить файл журнала или контейнер файловой системы.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**\_ \_ \_ Превышено ограничение \_ контейнера журнала ошибок**
</dt> <dd> <dl> <dt>

6617 (0x19D9)
</dt> <dt>



Служба журналов достигла максимально допустимого контейнера, выделенного файлу журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**Журнал \_ ошибок \_ \_ , начало \_ журнала**
</dt> <dd> <dl> <dt>

6618 (0x19DA)
</dt> <dt>



Служба журнала попыталась выполнить чтение или запись в обратном направлении после начала журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**\_Политика журнала \_ ошибок \_ уже \_ установлена**
</dt> <dd> <dl> <dt>

6619 (0x19DB)
</dt> <dt>



Не удалось установить политику журнала, так как уже существует политика того же типа.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**\_Политика журнала \_ ошибок \_ не \_ установлена**
</dt> <dd> <dl> <dt>

6620 (0x19DC)
</dt> <dt>



Рассматриваемая политика журнала не была установлена во время запроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**\_ \_ Недопустимая политика журнала ошибок \_**
</dt> <dd> <dl> <dt>

6621 (0x19DD)
</dt> <dt>



В журнале установлен недопустимый набор политик.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**\_ \_ конфликт политик журнала \_ ошибок**
</dt> <dd> <dl> <dt>

6622 (0x19DE)
</dt> <dt>



Не удалось завершить операцию из-за политики для рассматриваемого журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**\_ \_ закрепленный \_ \_ ЗАКЛЮЧИТЕЛЬный фрагмент журнала ошибок**
</dt> <dd> <dl> <dt>

6623 (0x19DF)
</dt> <dt>



Не удается освободить пространство журнала, так как журнал закреплен с помощью заключительного фрагмента архива.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**\_ \_ несуществующая запись журнала ошибок \_**
</dt> <dd> <dl> <dt>

6624 (0x19E0)
</dt> <dt>



Запись журнала не является записью в файле журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**\_ \_ \_ недопустимые зарезервированные записи журнала ошибок \_**
</dt> <dd> <dl> <dt>

6625 (0x19E1)
</dt> <dt>



Количество зарезервированных записей журнала или недопустимая Коррекция количества зарезервированных записей журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**\_ \_ \_ недопустимое зарезервированное пространство журнала ошибок \_**
</dt> <dd> <dl> <dt>

6626 (0x19E2)
</dt> <dt>



Зарезервированное пространство журнала или корректировка пространства журнала недействительны.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**\_ \_ Недопустимый конец журнала ошибок \_**
</dt> <dd> <dl> <dt>

6627 (0x19E3)
</dt> <dt>



Новый или существующий архивный хвост или база активного журнала недействительна.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**\_журнал ошибок \_ полон**
</dt> <dd> <dl> <dt>

6628 (0x19E4)
</dt> <dt>



Место в журнале исчерпано.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**Ошибка \_ \_ не удалось \_ изменить размер \_ журнала**
</dt> <dd> <dl> <dt>

6629 (0x19E5)
</dt> <dt>



Не удалось установить запрошенный размер журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**\_немультиплексированный журнал ошибок \_**
</dt> <dd> <dl> <dt>

6630 (0x19E6)
</dt> <dt>



Журнал мультиплексен, прямая запись в физический журнал запрещена.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**\_ \_ Выделенный Журнал ошибок**
</dt> <dd> <dl> <dt>

6631 (0x19E7)
</dt> <dt>



Не удалось выполнить операцию, так как журнал является выделенным журналом.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**\_ \_ \_ не \_ выполняется архивация \_ журнала ошибок**
</dt> <dd> <dl> <dt>

6632 (0x19E8)
</dt> <dt>



Для операции требуется контекст архива.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**\_ \_ выполняется архивация \_ журнала \_ ошибок**
</dt> <dd> <dl> <dt>

6633 (0x19E9)
</dt> <dt>



Выполняется архивация журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**журнал ошибок " \_ \_ эфемерный"**
</dt> <dd> <dl> <dt>

6634 (0x19EA)
</dt> <dt>



Для операции требуется невременный журнал, но журнал является эфемерным.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**\_ \_ \_ недостаточно контейнеров для журнала \_ ошибок**
</dt> <dd> <dl> <dt>

6635 (0x19EB)
</dt> <dt>



В журнале должно быть по крайней мере два контейнера, прежде чем они могут быть считаны или записаны в.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**\_Клиент журнала \_ ошибок \_ уже \_ зарегистрирован**
</dt> <dd> <dl> <dt>

6636 (0x19EC)
</dt> <dt>



Клиент журнала уже зарегистрирован в потоке.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**\_Клиент журнала \_ ошибок \_ не \_ зарегистрирован**
</dt> <dd> <dl> <dt>

6637 (0x19ED)
</dt> <dt>



Клиент журнала не зарегистрирован в потоке.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**\_ \_ \_ выполняется полный обработчик \_ \_ журнала ошибок**
</dt> <dd> <dl> <dt>

6638 (0x19EE)
</dt> <dt>



Уже выполнен запрос на обработку условия переполнения журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**\_ \_ \_ сбой чтения контейнера журнала \_ ошибок**
</dt> <dd> <dl> <dt>

6639 (0x19EF)
</dt> <dt>



Служба журнала обнаружила ошибку при попытке чтения из контейнера журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**\_ \_ \_ сбой записи контейнера журнала \_ ошибок**
</dt> <dd> <dl> <dt>

6640 (0x19F0)
</dt> <dt>



Служба журнала обнаружила ошибку при попытке записи в контейнер журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**\_ \_ \_ не удалось открыть контейнер журнала ошибок \_**
</dt> <dd> <dl> <dt>

6641 (0x19F1)
</dt> <dt>



Служба журнала обнаружила ошибку при попыток открыть контейнер журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**\_ \_ \_ недопустимое состояние контейнера журнала ошибок \_**
</dt> <dd> <dl> <dt>

6642 (0x19F2)
</dt> <dt>



Служба журнала обнаружила недопустимое состояние контейнера при выполнении запрошенного действия.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**\_ \_ недопустимое состояние журнала ошибок \_**
</dt> <dd> <dl> <dt>

6643 (0x19F3)
</dt> <dt>



Служба журнала находится в неправильном состоянии для выполнения запрошенного действия.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**\_ \_ закрепленный журнал ошибок**
</dt> <dd> <dl> <dt>

6644 (0x19F4)
</dt> <dt>



Не удается освободить место в журнале, так как журнал закреплен.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**\_ \_ \_ сбой при записи метаданных журнала ошибок \_**
</dt> <dd> <dl> <dt>

6645 (0x19F5)
</dt> <dt>



Сбой при записи метаданных журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**журнал ошибок — \_ \_ несовместимость \_ безопасности**
</dt> <dd> <dl> <dt>

6646 (0x19F6)
</dt> <dt>



Безопасность журнала и его контейнеров не согласуется.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**Ошибка \_ \_ при присоединении \_ записи журнала ошибок \_**
</dt> <dd> <dl> <dt>

6647 (0x19F7)
</dt> <dt>



Записи были добавлены в журнал или были внесены изменения в резервирование, но журнал не может быть сброшен.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**\_ \_ зафиксированное \_ РЕЗЕРВИРОВАНие журнала ошибок**
</dt> <dd> <dl> <dt>

6648 (0x19F8)
</dt> <dt>



Журнал закреплен из-за резервирования, использующего большую часть пространства журнала. Освободите зарезервированные записи, чтобы освободить место.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**Ошибка \_ недопустимой \_ транзакции**
</dt> <dd> <dl> <dt>

6700 (0x1A2C)
</dt> <dt>



Недопустимый маркер транзакции, связанный с этой операцией.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**\_неактивная Ошибка транзакции \_ \_**
</dt> <dd> <dl> <dt>

6701 (0x1A2D)
</dt> <dt>



Запрошенная операция была выполнена в контексте транзакции, которая больше не активна.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**\_ \_ Недопустимый запрос ошибки транзакции \_ \_**
</dt> <dd> <dl> <dt>

6702 (0x1A2E)
</dt> <dt>



Запрошенная операция недопустима для объекта транзакции в его текущем состоянии.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**ОШИБОЧная \_ транзакция \_ не \_ запрошена**
</dt> <dd> <dl> <dt>

6703 (0x1A2F)
</dt> <dt>



Вызывающий объект вызвал API ответа, но ответ не ожидается, так как TM не выдавала соответствующий запрос вызывающему объекту.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**транзакция с ошибкой \_ \_ уже \_ прервана**
</dt> <dd> <dl> <dt>

6704 (0x1A30)
</dt> <dt>



Выполнение запрошенной операции слишком поздно, так как транзакция уже прервана.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**транзакция с ошибкой \_ \_ уже \_ зафиксирована**
</dt> <dd> <dl> <dt>

6705 (0x1A31)
</dt> <dt>



Выполнение запрошенной операции слишком поздно, так как транзакция уже была зафиксирована.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**Ошибка \_ \_ при инициализации \_ TM**
</dt> <dd> <dl> <dt>

6706 (0x1A32)
</dt> <dt>



Не удалось успешно инициализировать диспетчер транзакций. Транзакционные операции не поддерживаются.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ОШИБКИ \_ RESOURCEMANAGER \_ только для чтения \_**
</dt> <dd> <dl> <dt>

6707 (0x1A33)
</dt> <dt>



Указанный ResourceManager не внес изменений или обновлений в ресурс в этой транзакции.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**ОШИБОЧная \_ транзакция \_ не \_ присоединена**
</dt> <dd> <dl> <dt>

6708 (0x1A34)
</dt> <dt>



Диспетчер ресурсов попытался подготовить транзакцию, которая не была успешно присоединена.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**Существует некоторая транзакция с ошибкой \_ \_ \_**
</dt> <dd> <dl> <dt>

6709 (0x1A35)
</dt> <dt>



Объект транзакции уже имеет старший зачисление, и вызывающая сторона попыталась выполнить операцию, которая создала новый старший. Разрешается только один старший связующий элемент.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**Ошибка \_ \_ протокол CRM \_ уже \_ существует**
</dt> <dd> <dl> <dt>

6710 (0x1A36)
</dt> <dt>



Диспетчер ресурсов попытался зарегистрировать уже существующий протокол.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**Ошибка \_ \_ при распространении \_ транзакции**
</dt> <dd> <dl> <dt>

6711 (0x1A37)
</dt> <dt>



Сбой при попытке распространения транзакции.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена протокол CRM**
</dt> <dd> <dl> <dt>

6712 (0x1A38)
</dt> <dt>



Запрошенный протокол распространения не зарегистрирован в качестве CRM.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**\_Недопустимый Сбой транзакции \_ Маршалловы в \_ \_ буфере**
</dt> <dd> <dl> <dt>

6713 (0x1A39)
</dt> <dt>



Буфер, переданный в Пуштрансактион или Пуллтрансактион, имеет недопустимый формат.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**Ошибка \_ \_ \_ \_ недопустимой текущей транзакции**
</dt> <dd> <dl> <dt>

6714 (0x1A3A)
</dt> <dt>



Текущий контекст транзакции, связанный с потоком, не является допустимым маркером для объекта транзакции.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**\_ \_ не \_ удалось найти ТРАНЗАКЦИю с ошибками**
</dt> <dd> <dl> <dt>

6715 (0x1A3B)
</dt> <dt>



Не удалось открыть указанный объект транзакции, так как он не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**\_ \_ не \_ удалось найти RESOURCEMANAGER "ошибка"**
</dt> <dd> <dl> <dt>

6716 (0x1A3C)
</dt> <dt>



Не удалось открыть указанный объект ResourceManager, так как он не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**\_ \_ не удалось найти зачисление ошибок \_**
</dt> <dd> <dl> <dt>

6717 (0x1A3D)
</dt> <dt>



Не удалось открыть указанный объект зачислений, поскольку он не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**Ошибка \_ диспетчеров транзакций \_ не \_ найдена**
</dt> <dd> <dl> <dt>

6718 (0x1A3E)
</dt> <dt>



Не удалось открыть указанный объект диспетчер транзакций, так как он не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**Ошибка \_ диспетчеров транзакций \_ не в \_ сети**
</dt> <dd> <dl> <dt>

6719 (0x1A3F)
</dt> <dt>



Не удалось создать или открыть указанный объект, так как связанный с ним диспетчер транзакций не находится в режиме "в сети". Диспетчер транзакций должен быть полностью подключен к сети путем вызова Рековертрансактионманажер для восстановления до конца своего файла журнала, прежде чем можно будет открыть объекты в его транзакциях или пространствах имен ResourceManager. Кроме того, ошибки при записи в файл журнала могут привести к тому, что диспетчер транзакций перейдет в режим «вне сети».


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**Ошибка \_ при \_ \_ конфликте имен при восстановлении транзакций \_**
</dt> <dd> <dl> <dt>

6720 (0x1A40)
</dt> <dt>



Указанному диспетчеру транзакций не удалось создать объекты, содержащиеся в его файле журнала, в пространстве имен OB. Поэтому диспетчеру транзакций не удалось выполнить восстановление.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**Ошибка \_ \_ не является \_ корневой транзакцией**
</dt> <dd> <dl> <dt>

6721 (0x1A41)
</dt> <dt>



Не удалось завершить вызов для создания старшего прикрепления для этого объекта транзакции, так как объект транзакции, указанный для прикрепления, является подчиненной ветвью транзакции. Только корень транзакции можно прикрепить в качестве руководителя.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**\_ \_ срок действия объекта транзакции с ошибкой \_ истек**
</dt> <dd> <dl> <dt>

6722 (0x1A42)
</dt> <dt>



Так как связанный диспетчер транзакций или диспетчер ресурсов был закрыт, этот маркер больше не действителен.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**ОШИБОЧный \_ ответ на транзакцию \_ \_ не \_ прикреплен**
</dt> <dd> <dl> <dt>

6723 (0x1A43)
</dt> <dt>



Указанная операция не может быть выполнена для этого старшего прикрепления, так как зачисление не было создано с соответствующим ответом завершения в Нотификатионмаск.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**\_ \_ \_ слишком \_ длинная запись транзакции с ошибкой**
</dt> <dd> <dl> <dt>

6724 (0x1A44)
</dt> <dt>



Не удалось выполнить указанную операцию, так как запись, которая была записана в журнал, слишком длинная. Это может произойти из-за двух условий: слишком много зачислений в этой транзакции или объединенный Рековеринформатион, регистрируемый от имени этих зачислений, слишком длинный.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**Ошибка \_ неявной \_ транзакции \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

6725 (0x1A45)
</dt> <dt>



Неявная транзакция не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**\_ \_ нарушение целостности транзакции при ошибке \_**
</dt> <dd> <dl> <dt>

6726 (0x1A46)
</dt> <dt>



Диспетчеру транзакций ядра пришлось прервать или забыть транзакцию, так как она блокировала ход выполнения.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**Ошибка \_ при \_ несоответствии удостоверения в диспетчере транзакций \_**
</dt> <dd> <dl> <dt>

6727 (0x1A47)
</dt> <dt>



Переданное удостоверение диспетчером транзакций не соответствует записанному в файле журнала диспетчером транзакций.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**Ошибка \_ RM \_ не может \_ быть \_ заморожена \_ для \_ моментального снимка**
</dt> <dd> <dl> <dt>

6728 (0x1A48)
</dt> <dt>



Невозможно продолжить операцию создания моментального снимка, так как диспетчер ресурсов транзакций не может зафиксироваться в текущем состоянии. Повторите попытку.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**\_ \_ должна \_ WRITETHROUGHся транзакция с ошибкой**
</dt> <dd> <dl> <dt>

6729 (0x1A49)
</dt> <dt>



Не удается прикрепить транзакцию к указанному Енлистментмаск, так как транзакция уже завершила этап предварительной подготовки. Чтобы гарантировать правильность, ResourceManager необходимо переключиться в режим сквозной записи и прекратить кэширование данных в рамках этой транзакции. Прикрепление только к последующим этапам транзакций может выполняться с ошибкой.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**Ошибка \_ \_ \_ нестаршая транзакция**
</dt> <dd> <dl> <dt>

6730 (0x1A4A)
</dt> <dt>



Транзакция не имеет старшего прикрепления.


</dt> </dl> </dd> <dt>

<span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**\_возможна ошибка эвристического \_ повреждения \_**
</dt> <dd> <dl> <dt>

6731 (0x1A4B)
</dt> <dt>



Попытка зафиксировать транзакцию завершена, но возможно, что часть дерева транзакций не была успешно зафиксирована из-за эвристики. Поэтому возможно, что некоторые данные, измененные в транзакции, не зафиксированы, что приводит к несогласованности транзакций. По возможности проверьте согласованность связанных данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**Ошибка при \_ \_ КОНФЛИКТе транзакций**
</dt> <dd> <dl> <dt>

6800 (0x1A90)
</dt> <dt>



Функция попыталась использовать имя, зарезервированное для использования другой транзакцией.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**Ошибка \_ RM \_ не \_ активна**
</dt> <dd> <dl> <dt>

6801 (0x1A91)
</dt> <dt>



Поддержка транзакций в указанном диспетчере ресурсов не запущена или была завершена из-за ошибки.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**\_метаданные ошибки \_ RM \_ повреждены**
</dt> <dd> <dl> <dt>

6802 (0x1A92)
</dt> <dt>



Метаданные RM повреждены. RM не будет работать.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**\_Каталог ошибок \_ не \_ RM**
</dt> <dd> <dl> <dt>

6803 (0x1A93)
</dt> <dt>



Указанный каталог не содержит Resource Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**Неподдерживаемые транзакции с ОШИБКАми \_ \_ \_**
</dt> <dd> <dl> <dt>

6805 (0x1A95)
</dt> <dt>



Удаленный сервер или общая папка не поддерживает транзакционные файловые операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**\_ \_ \_ Недопустимый размер журнала \_ ошибок**
</dt> <dd> <dl> <dt>

6806 (0x1A96)
</dt> <dt>



Запрошенный размер журнала недопустим.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**\_объект Error \_ \_ больше не \_ существует**
</dt> <dd> <dl> <dt>

6807 (0x1A97)
</dt> <dt>



Объект (файл, поток, ссылка), соответствующий этому маркеру, был удален откатом точки сохранения транзакции.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**\_ \_ \_ не найдена мини – версия потока \_ ошибок**
</dt> <dd> <dl> <dt>

6808 (0x1A98)
</dt> <dt>



Указанная мини для файла не найдена для этого файла транзакций, открытых в настоящий момент.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**\_ \_ Недопустимая мини – версия потока ошибок \_ \_**
</dt> <dd> <dl> <dt>

6809 (0x1A99)
</dt> <dt>



Указанная мини – версия файла найдена, но стала недействительной. Наиболее вероятной причиной является откат точки сохранения транзакции.


</dt> </dl> </dd> <dt>

<span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**Ошибка \_ мини, \_ недоступная \_ из \_ указанной \_ транзакции**
</dt> <dd> <dl> <dt>

6810 (0x1A9A)
</dt> <dt>



Мини-версия может быть открыта только в контексте транзакции, создавшей ее.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ОШИБКА не \_ удается \_ Открыть мини – версию \_ \_ с \_ \_ намерением изменения**
</dt> <dd> <dl> <dt>

6811 (0x1A9B)
</dt> <dt>



Невозможно открыть мини-версию с доступом на изменение.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ОШИБКА не \_ удается \_ создать \_ Дополнительные \_ потоковые \_ миниверсионс**
</dt> <dd> <dl> <dt>

6812 (0x1A9C)
</dt> <dt>



Невозможно создать дополнительные миниверсионс для этого потока.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии версии удаленного файла \_**
</dt> <dd> <dl> <dt>

6814 (0x1A9E)
</dt> <dt>



Удаленный сервер отправил несоответствующий номер версии или FID для файла, открытого с помощью транзакций.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**\_обработчик ошибок \_ \_ больше не \_ действителен**
</dt> <dd> <dl> <dt>

6815 (0x1A9F)
</dt> <dt>



Этот маркер был аннулирован транзакцией. Наиболее вероятная причина — наличие сопоставления памяти для файла или открытого обработчика после завершения или отката транзакции до точки сохранения.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**Ошибка \_ без \_ \_ метаданных TxF**
</dt> <dd> <dl> <dt>

6816 (0x1AA0)
</dt> <dt>



В файле нет метаданных транзакций.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**\_ \_ обнаружено повреждение журнала ошибок \_**
</dt> <dd> <dl> <dt>

6817 (0x1AA1)
</dt> <dt>



Данные журнала повреждены.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**Ошибка \_ не \_ удается \_ восстановить \_ с \_ открытым маркером**
</dt> <dd> <dl> <dt>

6818 (0x1AA2)
</dt> <dt>



Невозможно восстановить файл, так как на нем еще открыт обработчик.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**Ошибка \_ RM \_ отключена**
</dt> <dd> <dl> <dt>

6819 (0x1AA3)
</dt> <dt>



Результат транзакции недоступен, так как диспетчер ресурсов, ответственный за него, был отключен.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**\_зачисление ошибок \_ не является \_ старшим**
</dt> <dd> <dl> <dt>

6820 (0x1AA4)
</dt> <dt>



Запрос был отклонен, так как зачисление в вопросе не является старшим прикреплением.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**восстановление после ошибок \_ \_ не \_ требуется**
</dt> <dd> <dl> <dt>

6821 (0x1AA5)
</dt> <dt>



Транзакционный диспетчер ресурсов уже согласован. Восстановление не требуется.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**Ошибка \_ RM \_ уже \_ запущена**
</dt> <dd> <dl> <dt>

6822 (0x1AA6)
</dt> <dt>



Диспетчер ресурсов транзакций уже запущен.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**\_ \_ неустойчивое удостоверение файла ошибок \_ \_**
</dt> <dd> <dl> <dt>

6823 (0x1AA7)
</dt> <dt>



Файл нельзя открыть транзакционно, так как его удостоверение зависит от результата неразрешенной транзакции.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ОШИБКА не \_ удается \_ ПРЕрвать \_ транзакционную \_ зависимость**
</dt> <dd> <dl> <dt>

6824 (0x1AA8)
</dt> <dt>



Невозможно выполнить операцию, поскольку другая транзакция зависит от того факта, что это свойство не изменится.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ОШИБКА не \_ удается \_ перекрестно \_ \_ границы RM**
</dt> <dd> <dl> <dt>

6825 (0x1AA9)
</dt> <dt>



Операция будет затрагивать один файл с двумя диспетчерами ресурсов транзакций и, следовательно, не будет разрешен.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**Ошибка \_ TxF \_ dir \_ не \_ пуста**
</dt> <dd> <dl> <dt>

6826 (0x1AAA)
</dt> <dt>



Для выполнения этой операции каталог $Txf должен быть пустым.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**\_нет проблем с НЕсомнительными \_ транзакциями \_**
</dt> <dd> <dl> <dt>

6827 (0x1AAB)
</dt> <dt>



Операция оставляет диспетчер ресурсов транзакций в несогласованном состоянии и, следовательно, не разрешается.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**Ошибка \_ TM \_ volatile**
</dt> <dd> <dl> <dt>

6828 (0x1AAC)
</dt> <dt>



Не удалось выполнить операцию, так как диспетчер транзакций не имеет журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**\_ \_ срок действия таймера отката ошибки \_ истек**
</dt> <dd> <dl> <dt>

6829 (0x1AAD)
</dt> <dt>



Не удалось запланировать откат, так как ранее запланированный откат уже выполнен или поставлен в очередь на выполнение.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**Ошибка \_ при \_ \_ повреждении атрибута TxF**
</dt> <dd> <dl> <dt>

6830 (0x1AAE)
</dt> <dt>



Атрибут метаданных транзакций для файла или каталога поврежден и недоступен для чтения.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**Ошибка \_ EFS \_ не \_ разрешена \_ в \_ транзакции**
</dt> <dd> <dl> <dt>

6831 (0x1AAF)
</dt> <dt>



Не удалось выполнить операцию шифрования, так как транзакция активна.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**Ошибка при \_ открытии транзакции \_ \_ \_ запрещено**
</dt> <dd> <dl> <dt>

6832 (0x1AB0)
</dt> <dt>



Этот объект не может быть открыт в транзакции.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**\_ \_ сбой при росте журнала ошибок \_**
</dt> <dd> <dl> <dt>

6833 (0x1AB1)
</dt> <dt>



Сбой при создании пространства в журнале диспетчера ресурсов транзакций. Состояние сбоя записано в журнал событий.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**Ошибка при \_ \_ сопоставлении \_ неподдерживаемой удаленной транзакции сопоставления \_**
</dt> <dd> <dl> <dt>

6834 (0x1AB2)
</dt> <dt>



Сопоставление памяти (создание сопоставленного раздела) удаленный файл в транзакции не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**Ошибка \_ \_ \_ уже имеется метаданные \_ TxF**
</dt> <dd> <dl> <dt>

6835 (0x1AB3)
</dt> <dt>



Метаданные транзакции уже существуют в этом файле и не могут быть заменены.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**\_ \_ \_ \_ не заданы обратные вызовы области транзакций с ошибками \_**
</dt> <dd> <dl> <dt>

6836 (0x1AB4)
</dt> <dt>



Не удалось указать область транзакции, так как обработчик области не был инициализирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**\_ \_ требуется \_ специальное продвижение для транзакции с ошибками**
</dt> <dd> <dl> <dt>

6837 (0x1AB5)
</dt> <dt>



Требуется продвижение, чтобы разрешить диспетчеру ресурсов прикрепить, но для транзакции было задано значение "запретить".


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**Ошибка \_ не может \_ выполнить \_ файл \_ в \_ транзакции**
</dt> <dd> <dl> <dt>

6838 (0x1AB6)
</dt> <dt>



Этот файл открыт для изменения в неразрешенной транзакции и может быть открыт для выполнения только транзакционным агентом чтения.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**ОШИБОЧные \_ транзакции \_ не \_ заморожены**
</dt> <dd> <dl> <dt>

6839 (0x1AB7)
</dt> <dt>



Запрос на разморозку замороженных транзакций был проигнорирован, так как транзакции ранее не были заморожены.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**\_ \_ выполняется замораживание транзакций \_ с \_ ошибками**
</dt> <dd> <dl> <dt>

6840 (0x1AB8)
</dt> <dt>



Транзакции нельзя зафиксировать, так как уже выполняется заморозка.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**Ошибка \_ не является \_ томом моментальных снимков \_**
</dt> <dd> <dl> <dt>

6841 (0x1AB9)
</dt> <dt>



Целевой том не является томом моментальных снимков. Эта операция допустима только для тома, подключенного в качестве моментального снимка.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**не обнаружена \_ \_ точка сохранения \_ с \_ открытыми \_ файлами**
</dt> <dd> <dl> <dt>

6842 (0x1ABA)
</dt> <dt>



Не удалось выполнить операцию точки сохранения, так как файлы открыты в транзакции. Это не разрешено.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**\_ \_ Восстановление потерянных данных об ошибках \_**
</dt> <dd> <dl> <dt>

6843 (0x1ABB)
</dt> <dt>



Windows обнаружил повреждение в файле, и этот файл был восстановлен. Возможно, произошла потери данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**\_ \_ \_ \_ в транзакции не РАЗРЕШЕНо разреженных ошибок \_**
</dt> <dd> <dl> <dt>

6844 (0x1ABC)
</dt> <dt>



Не удалось выполнить операцию разрежения, так как в файле активна транзакция.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**Ошибка \_ с \_ \_ несоответствием удостоверений TM**
</dt> <dd> <dl> <dt>

6845 (0x1ABD)
</dt> <dt>



Не удалось вызвать для создания объекта диспетчер транзакций, так как удостоверение TM, хранящееся в файле журнала, не совпадает с удостоверением TM, переданным в качестве аргумента.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**Ошибка в \_ разделе с плавающей ошибкой \_**
</dt> <dd> <dl> <dt>

6846 (0x1ABE)
</dt> <dt>



Предпринята попытка ввода-вывода для объекта раздела, который был перемещен в результате завершения транзакции. Нет допустимых данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**Ошибка \_ не может \_ принять \_ транзакционную \_ работу**
</dt> <dd> <dl> <dt>

6847 (0x1ABF)
</dt> <dt>



Диспетчер ресурсов транзакций в настоящее время не может принять транзакционную работу из-за временной ситуации, такой как нехватка ресурсов.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**Ошибка \_ не может \_ прерывать \_ транзакции**
</dt> <dd> <dl> <dt>

6848 (0x1AC0)
</dt> <dt>



Диспетчер ресурсов транзакций имел слишком много транактионсных невыполненных запросов, которые не удалось прервать. Работа диспетчера ресурсов транзакций завершена.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ОШИБКИ \_ поврежденных \_ кластеров**
</dt> <dd> <dl> <dt>

6849 (0x1AC1)
</dt> <dt>



Не удалось выполнить операцию из-за поврежденных кластеров на диске.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**\_Сжатие ошибок \_ не \_ разрешено \_ в \_ транзакции**
</dt> <dd> <dl> <dt>

6850 (0x1AC2)
</dt> <dt>



Не удалось выполнить операцию сжатия, так как в файле активна транзакция.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**Ошибка \_ \_ "грязный том"**
</dt> <dd> <dl> <dt>

6851 (0x1AC3)
</dt> <dt>



Не удалось выполнить операцию, так как том изменен. Запустите Chkdsk и повторите попытку.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**Ошибка \_ \_ \_ при отслеживании ссылок \_ в \_ транзакции**
</dt> <dd> <dl> <dt>

6852 (0x1AC4)
</dt> <dt>



Не удалось выполнить операцию отслеживания ссылок, так как транзакция активна.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**\_операция \_ с ошибкой не \_ поддерживается \_ в \_ транзакции**
</dt> <dd> <dl> <dt>

6853 (0x1AC5)
</dt> <dt>



Эта операция не может быть выполнена в транзакции.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**\_маркер с истекшим сроком действия \_**
</dt> <dd> <dl> <dt>

6854 (0x1AC6)
</dt> <dt>



Этот маркер больше не связан с его транзакцией. Возможно, он был открыт в транзакционном диспетчере ресурсов, который затем был принудительно перезапущен. Закройте этот обработчик и откройте новый.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**ОШИБОЧная \_ транзакция \_ не \_ прикреплена**
</dt> <dd> <dl> <dt>

6855 (0x1AC7)
</dt> <dt>



Не удалось выполнить указанную операцию, так как диспетчер ресурсов не прикреплен к транзакции.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**Ошибка \_ CTX \_ \_ \_ недопустимое имя винстатион**
</dt> <dd> <dl> <dt>

7001 (0x1B59)
</dt> <dt>



Указано недопустимое имя сеанса.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**Ошибка \_ CTX \_ недопустимых \_ PD**
</dt> <dd> <dl> <dt>

7002 (0x1B5A)
</dt> <dt>



Указан недопустимый драйвер протокола.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**Ошибка \_ CTX \_ PD \_ не \_ Найдено**
</dt> <dd> <dl> <dt>

7003 (0x1B5B)
</dt> <dt>



Указанный драйвер протокола не найден в системном пути.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**Ошибка \_ CTX \_ WD \_ не \_ найден**
</dt> <dd> <dl> <dt>

7004 (0x1B5C)
</dt> <dt>



Указанный драйвер подключения терминала не найден в системном пути.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**Ошибка \_ CTX. \_ не удается \_ создать \_ запись в журнале событий \_**
</dt> <dd> <dl> <dt>

7005 (0x1B5D)
</dt> <dt>



Не удалось создать раздел реестра для ведения журнала событий для этого сеанса.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**Ошибка \_ CTX \_ \_ конфликт имен \_ служб**
</dt> <dd> <dl> <dt>

7006 (0x1B5E)
</dt> <dt>



Служба с таким именем уже существует в системе.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**Ошибка \_ CTX \_ \_ Ожидание закрытия**
</dt> <dd> <dl> <dt>

7007 (0x1B5F)
</dt> <dt>



В сеансе ожидается операция закрытия.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**Ошибка \_ CTX \_ No \_ аутбуф**
</dt> <dd> <dl> <dt>

7008 (0x1B60)
</dt> <dt>



Свободные буферы вывода недоступны.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**Ошибка \_ CTX \_ . \_ \_ не \_ найден INF-файл модема**
</dt> <dd> <dl> <dt>

7009 (0x1B61)
</dt> <dt>



МОДЕМ. INF-файл не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**Ошибка \_ CTX \_ Недопустимая \_ модемнаме**
</dt> <dd> <dl> <dt>

7010 (0x1B62)
</dt> <dt>



Имя модема не найдено в файле MODEM. INF.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**Ошибка \_ при \_ \_ отклике модема CTX \_**
</dt> <dd> <dl> <dt>

7011 (0x1B63)
</dt> <dt>



Модем не принял отправленную ему команду. Убедитесь, что имя настроенного модема соответствует подключенному модему.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**Ошибка \_ CTX \_ \_ время ожидания ответа модема \_**
</dt> <dd> <dl> <dt>

7012 (0x1B64)
</dt> <dt>



Модем не ответил на отправленную ему команду. Убедитесь, что модем правильно подключен и включен.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**Ошибка \_ CTX \_ ответа модема \_ \_ нет \_ несущей**
</dt> <dd> <dl> <dt>

7013 (0x1B65)
</dt> <dt>



Произошла ошибка обнаружения несущей или она была удалена из-за отключения.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**Ошибка \_ , \_ CTX \_ ответ модема \_ No \_ диалтоне**
</dt> <dd> <dl> <dt>

7014 (0x1B66)
</dt> <dt>



Гудок не обнаружен в течение необходимого времени. Убедитесь, что телефонный кабель правильно подключен и работает.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**Ошибка \_ ctx, что \_ ответ модема \_ \_ занят**
</dt> <dd> <dl> <dt>

7015 (0x1B67)
</dt> <dt>



Сигнал занятости обнаружен на удаленном веб-сайте при обратном вызове.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**Ошибка \_ CTX \_ ответа модема \_ \_**
</dt> <dd> <dl> <dt>

7016 (0x1B68)
</dt> <dt>



Речь обнаружено на удаленном веб-сайте при обратном вызове.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**Ошибка \_ CTX \_ TD \_**
</dt> <dd> <dl> <dt>

7017 (0x1B69)
</dt> <dt>



Ошибка драйвера транспорта.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**Ошибка \_ CTX \_ винстатион \_ не \_ найдена**
</dt> <dd> <dl> <dt>

7022 (0x1B6E)
</dt> <dt>



Не удается найти указанный сеанс.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**Ошибка \_ CTX \_ винстатион \_ уже \_ существует**
</dt> <dd> <dl> <dt>

7023 (0x1B6F)
</dt> <dt>



Указанное имя сеанса уже используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**Ошибка \_ CTX \_ винстатион \_ Busy**
</dt> <dd> <dl> <dt>

7024 (0x1B70)
</dt> <dt>



Задача, которую вы пытаетесь выполнить, не может быть завершена, так как службы удаленных рабочих столов в данный момент занят. Повторите попытку через несколько минут. Другие пользователи по-прежнему должны иметь возможность войти в систему.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**Ошибка \_ CTXного \_ \_ \_ видеорежима**
</dt> <dd> <dl> <dt>

7025 (0x1B71)
</dt> <dt>



Предпринята попытка подключения к сеансу, видео режим которого не поддерживается текущим клиентом.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**Ошибка \_ CTX \_ графика \_**
</dt> <dd> <dl> <dt>

7035 (0x1B7B)
</dt> <dt>



Приложение попыталось включить графический режим DOS. Графический режим DOS не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**Ошибка \_ CTX \_ входа \_ отключена**
</dt> <dd> <dl> <dt>

7037 (0x1B7D)
</dt> <dt>



Права на интерактивный вход отключены. Обратитесь за помощью к администратору.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**Ошибка \_ CTX \_ не \_ консоль**
</dt> <dd> <dl> <dt>

7038 (0x1B7E)
</dt> <dt>



Запрошенную операцию можно выполнить только в системной консоли. Чаще всего это вызвано драйвером или системной библиотекой DLL, для которой необходим прямой доступ к консоли.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**Ошибка \_ CTX \_ \_ \_ время ожидания запроса клиента**
</dt> <dd> <dl> <dt>

7040 (0x1B80)
</dt> <dt>



Клиенту не удалось ответить на сообщение подключения к серверу.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**Ошибка \_ при \_ \_ отключении консоли CTX**
</dt> <dd> <dl> <dt>

7041 (0x1B81)
</dt> <dt>



Отключение сеанса консоли не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**Ошибка \_ CTX \_ \_ Подключение консоли**
</dt> <dd> <dl> <dt>

7042 (0x1B82)
</dt> <dt>



Повторное подключение отключенного сеанса к консоли не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**Ошибка \_ CTX \_ теневой копии \_**
</dt> <dd> <dl> <dt>

7044 (0x1B84)
</dt> <dt>



Запрос на удаленное управление другим сеансом был отклонен.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**Ошибка \_ CTX \_ \_ отказа в доступе винстатион \_**
</dt> <dd> <dl> <dt>

7045 (0x1B85)
</dt> <dt>



Отказано в доступе к запрошенному сеансу.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**Ошибка \_ CTX \_ Недопустимый \_ WD**
</dt> <dd> <dl> <dt>

7049 (0x1B89)
</dt> <dt>



Указан недопустимый драйвер подключения терминала.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**Ошибка \_ CTX \_ теневой копии \_**
</dt> <dd> <dl> <dt>

7050 (0x1B8A)
</dt> <dt>



Не удается управлять запрошенным сеансом удаленно. Это может быть вызвано тем, что сеанс отключен или в данный момент пользователь не вошел в систему.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**Ошибка \_ CTX \_ теневой копии \_ отключена**
</dt> <dd> <dl> <dt>

7051 (0x1B8B)
</dt> <dt>



Запрошенный сеанс не настроен на разрешение удаленного управления.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**Ошибка \_ \_ \_ \_ при использовании клиентской лицензии CTX \_**
</dt> <dd> <dl> <dt>

7052 (0x1B8C)
</dt> <dt>



Запрос на подключение к этому серверу терминалов отклонен. Номер клиентской лицензии сервера терминалов сейчас используется другим пользователем. Обратитесь к системному администратору, чтобы получить уникальный номер лицензии.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**Ошибка \_ CTX \_ клиентской \_ лицензии \_ не \_ задана**
</dt> <dd> <dl> <dt>

7053 (0x1B8D)
</dt> <dt>



Запрос на подключение к этому серверу терминалов отклонен. Номер клиентской лицензии сервера терминалов не был введен для этой копии клиента сервера терминалов. Обратитесь к системному администратору.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**Ошибка \_ CTX \_ Лицензия \_ \_ недоступна**
</dt> <dd> <dl> <dt>

7054 (0x1B8E)
</dt> <dt>



Число подключений к этому компьютеру ограничено, и все подключения сейчас используются. Попробуйте подключиться позже или обратитесь к системному администратору.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**Ошибка \_ CTX \_ Лицензия \_ клиента \_ недействительна**
</dt> <dd> <dl> <dt>

7055 (0x1B8F)
</dt> <dt>



Используемый клиент не имеет лицензии на использование этой системы. Запрос на вход запрещен.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**Ошибка \_ CTX \_ \_ срок действия лицензии истек**
</dt> <dd> <dl> <dt>

7056 (0x1B90)
</dt> <dt>



Срок действия системной лицензии истек. Запрос на вход запрещен.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**Ошибка \_ CTX \_ теневой копии \_ не \_ запущена**
</dt> <dd> <dl> <dt>

7057 (0x1B91)
</dt> <dt>



Не удалось завершить удаленное управление, так как указанный сеанс в настоящее время не управляется удаленно.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**Ошибка \_ CTX \_ теневой копии \_ , завершенной \_ \_ \_ изменением режима**
</dt> <dd> <dl> <dt>

7058 (0x1B92)
</dt> <dt>



Удаленное управление консолью прервано, так как был изменен режим экрана. Изменение режима просмотра в сеансе удаленного управления не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**\_Превышено число активаций ошибок \_ \_**
</dt> <dd> <dl> <dt>

7059 (0x1B93)
</dt> <dt>



Активация уже была сброшена максимально допустимое количество раз для этой установки. Таймер активации не будет сброшен.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**Ошибка \_ CTX \_ винстатионс \_ Disabled**
</dt> <dd> <dl> <dt>

7060 (0x1B94)
</dt> <dt>



Удаленные имена входа в настоящее время отключены.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**Ошибка \_ CTX \_ . \_ требуется уровень шифрования \_**
</dt> <dd> <dl> <dt>

7061 (0x1B95)
</dt> <dt>



У вас нет нужного уровня шифрования для доступа к этому сеансу.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**Ошибка \_ \_ \_ при использовании сеанса \_ CTX**
</dt> <dd> <dl> <dt>

7062 (0x1B96)
</dt> <dt>



Пользователь% s \\ \\ % s в данный момент вошел в систему на этом компьютере. Только текущий пользователь или администратор может войти на этот компьютер.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**Ошибка \_ CTX \_ без \_ принудительного \_ выхода**
</dt> <dd> <dl> <dt>

7063 (0x1B97)
</dt> <dt>



Пользователь% s \\ \\ % s уже вошел в консоль этого компьютера. У вас нет разрешения на вход в систему в данный момент. Чтобы устранить эту проблему, обратитесь в% s \\ \\ % s и выйдите из системы.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**Ошибка \_ при \_ ограничении учетной записи CTX \_**
</dt> <dd> <dl> <dt>

7064 (0x1B98)
</dt> <dt>



Не удалось войти в систему из-за ограничений учетной записи.


</dt> </dl> </dd> <dt>

<span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**Ошибка \_ \_ протокола RDP \_**
</dt> <dd> <dl> <dt>

7065 (0x1B99)
</dt> <dt>



Компонент протокола RDP %2 обнаружил ошибку в потоке протокола и отключил клиент.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**Ошибка \_ CTX \_ CDM \_ Connect**
</dt> <dd> <dl> <dt>

7066 (0x1B9A)
</dt> <dt>



Служба сопоставления клиентских дисков подключена к терминальному подключению.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**Ошибка \_ CTX \_ CDM \_ Disconnect**
</dt> <dd> <dl> <dt>

7067 (0x1B9B)
</dt> <dt>



Служба сопоставления клиентских дисков отключена на терминальном подключении.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**Ошибка \_ CTX \_ \_ уровня безопасности \_**
</dt> <dd> <dl> <dt>

7068 (0x1B9C)
</dt> <dt>



Уровень безопасности сервера терминалов обнаружил ошибку в потоке протокола и отключил клиента.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ОШИБКИ \_ \_ несовместимых \_ сеансов TS**
</dt> <dd> <dl> <dt>

7069 (0x1B9D)
</dt> <dt>



Целевой сеанс несовместим с текущим сеансом.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**Ошибка \_ \_ подсистемы видеоподсистемы TS \_ \_**
</dt> <dd> <dl> <dt>

7070 (0x1B9E)
</dt> <dt>



Windows не удается подключиться к сеансу из-за проблемы в Windows видеоподсистеме. Повторите попытку подключения позже или обратитесь за помощью к администратору сервера.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**\_ \_ неправильная \_ последовательность API \_ для FRS Err**
</dt> <dd> <dl> <dt>

8001 (0x1F41)
</dt> <dt>



API службы репликации файлов был вызван неправильно.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**\_служба FRS Err \_ starting \_ Service**
</dt> <dd> <dl> <dt>

8002 (0x1F42)
</dt> <dt>



Не удается запустить службу репликации файлов.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**\_служба FRS Err \_ останавливает \_ службу**
</dt> <dd> <dl> <dt>

8003 (0x1F43)
</dt> <dt>



Не удается остановить службу репликации файлов.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**\_ \_ внутренний API FRS \_ Err**
</dt> <dd> <dl> <dt>

8004 (0x1F44)
</dt> <dt>



API службы репликации файлов прервал запрос. В журнале событий могут быть дополнительные сведения.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**\_Внутренняя ошибка \_ FRS**
</dt> <dd> <dl> <dt>

8005 (0x1F45)
</dt> <dt>



Служба репликации файлов завершила запрос. В журнале событий могут быть дополнительные сведения.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**\_канал связи \_ службы FRS Err \_**
</dt> <dd> <dl> <dt>

8006 (0x1F46)
</dt> <dt>



Не удается связаться со службой репликации файлов. В журнале событий могут быть дополнительные сведения.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**Ошибка FRS при \_ \_ нехватке \_ Priv**
</dt> <dd> <dl> <dt>

8007 (0x1F47)
</dt> <dt>



Служба репликации файлов не может удовлетворить запрос, так как у пользователя недостаточно привилегий. В журнале событий могут быть дополнительные сведения.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**\_ \_ Проверка подлинности FRS Err**
</dt> <dd> <dl> <dt>

8008 (0x1F48)
</dt> <dt>



Службе репликации файлов не удается удовлетворить запрос, так как проверка подлинности RPC недоступна. В журнале событий могут быть дополнительные сведения.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**\_ \_ недостаточный родительский элемент FRS Err \_ \_**
</dt> <dd> <dl> <dt>

8009 (0x1F49)
</dt> <dt>



Службе репликации файлов не удается удовлетворить запрос, так как у пользователя недостаточно привилегий на контроллере домена. В журнале событий могут быть дополнительные сведения.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**\_ \_ родительская \_ Проверка подлинности FRS Err**
</dt> <dd> <dl> <dt>

8010 (0x1F4A)
</dt> <dt>



Службе репликации файлов не удается удовлетворить запрос, так как проверка подлинности RPC недоступна на контроллере домена. В журнале событий могут быть дополнительные сведения.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**\_ \_ дочерний элемент FRS Err \_ с \_ родительским \_ каналом**
</dt> <dd> <dl> <dt>

8011 (0x1F4B)
</dt> <dt>



Службе репликации файлов не удается связаться со службой репликации файлов на контроллере домена. В журнале событий могут быть дополнительные сведения.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS \_ Err \_ Parent \_ to \_ Дочерний \_ канал связи**
</dt> <dd> <dl> <dt>

8012 (0x1F4C)
</dt> <dt>



Службе репликации файлов на контроллере домена не удается связаться со службой репликации файлов на этом компьютере. В журнале событий могут быть дополнительные сведения.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**\_ \_ Заполнение SYSVOL Err FRS \_**
</dt> <dd> <dl> <dt>

8013 (0x1F4D)
</dt> <dt>



Службе репликации файлов не удается заполнить системный том из-за внутренней ошибки. В журнале событий могут быть дополнительные сведения.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**\_ \_ \_ время ожидания заполнения SYSVOL Err \_ FRS**
</dt> <dd> <dl> <dt>

8014 (0x1F4E)
</dt> <dt>



Службе репликации файлов не удается заполнить системный том из-за внутреннего времени ожидания. В журнале событий могут быть дополнительные сведения.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**Служба \_ FRS \_ Err \_ SYSVOL \_ занята**
</dt> <dd> <dl> <dt>

8015 (0x1F4F)
</dt> <dt>



Службе репликации файлов не удается обработать запрос. Системный том занят с помощью предыдущего запроса.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**Репликация \_ SYSVOL Err FRS \_ \_**
</dt> <dd> <dl> <dt>

8016 (0x1F50)
</dt> <dt>



Службе репликации файлов не удается отключить репликацию системного тома из-за внутренней ошибки. В журнале событий могут быть дополнительные сведения.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**\_ \_ Недопустимый \_ параметр службы FRS Err \_**
</dt> <dd> <dl> <dt>

8017 (0x1F51)
</dt> <dt>



Служба репликации файлов обнаружила недопустимый параметр.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды системных ошибок](system-error-codes.md)
</dt> </dl>

 

 




