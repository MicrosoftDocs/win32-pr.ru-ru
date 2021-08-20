---
description: Описание кодов ошибок 1000-1299, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: Коды системных ошибок (1000-1299) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: dfda2e29a6b75acd683842509229f3bc52d7e8d3599855b01d8376f5a7daf2ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076338"
---
# <a name="system-error-codes-1000-1299"></a>Коды системных ошибок (1000-1299)

> [!NOTE]
> Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки. для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.

В следующем списке приведены [коды системных ошибок](system-error-codes.md) для ошибок 1000 – 1299. Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций. Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .

<dl> <dt>

<span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**\_переполнение стека ошибок \_**
</dt> <dd> <dl> <dt>

1001 (0x3E9)
</dt> <dt>



Слишком глубокая рекурсия. стек переполняется.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**Ошибка \_ недопустимого \_ сообщения**
</dt> <dd> <dl> <dt>

1002 (0x3EA)
</dt> <dt>



Окно не может работать с отправленным сообщением.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**Ошибка \_ не может быть \_ \_ завершена**
</dt> <dd> <dl> <dt>

1003 (0x3EB)
</dt> <dt>



Не удается завершить эту функцию.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**Ошибка \_ недопустимых \_ флагов**
</dt> <dd> <dl> <dt>

1004 (0x3EC)
</dt> <dt>



Недопустимые флаги.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**Ошибка \_ НЕраспознанного \_ тома**
</dt> <dd> <dl> <dt>

1005 (0x3ED)
</dt> <dt>



Том не содержит распознанную файловую систему. Убедитесь, что загружены все необходимые драйверы файловой системы и что том не поврежден.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**\_Недопустимый файл ошибок \_**
</dt> <dd> <dl> <dt>

1006 (0x3EE)
</dt> <dt>



Том для файла был изменен извне, поэтому открытый файл больше не является допустимым.


</dt> </dl> </dd> <dt>

<span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**Ошибка \_ полноэкранного \_ режима**
</dt> <dd> <dl> <dt>

1007 (0x3EF)
</dt> <dt>



Не удается выполнить запрошенную операцию в полноэкранном режиме.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**Ошибка \_ без \_ токена**
</dt> <dd> <dl> <dt>

1008 (0x3F0)
</dt> <dt>



Предпринята попытка ссылки на несуществующий токен.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADDB"></span><span id="error_baddb"></span>**Ошибка \_ баддб**
</dt> <dd> <dl> <dt>

1009 (0x3F1)
</dt> <dt>



База данных реестра конфигурации повреждена.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**Ошибка \_ бадкэй**
</dt> <dd> <dl> <dt>

1010 (0x3F2)
</dt> <dt>



Недопустимый раздел реестра конфигурации.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**Ошибка \_ кантопен**
</dt> <dd> <dl> <dt>

1011 (0x3F3)
</dt> <dt>



Не удалось открыть раздел реестра конфигурации.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**Ошибка \_ кантреад**
</dt> <dd> <dl> <dt>

1012 (размер 0x3f4)
</dt> <dt>



Не удалось прочитать раздел реестра конфигурации.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**Ошибка \_ кантврите**
</dt> <dd> <dl> <dt>

1013 (0x3F5)
</dt> <dt>



Не удалось записать раздел реестра конфигурации.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**\_реестр ошибок \_ восстановлен**
</dt> <dd> <dl> <dt>

1014 (0x3F6)
</dt> <dt>



Один из файлов в базе данных реестра был восстановлен с помощью журнала или альтернативной копии. Восстановление прошло успешно.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**\_реестр ошибок \_ поврежден**
</dt> <dd> <dl> <dt>

1015 (0x3F7)
</dt> <dt>



Реестр поврежден. Структура одного из файлов, содержащих данные реестра, повреждена, либо поврежден образ памяти системы, либо не удалось восстановить файл, так как альтернативная копия или журнал отсутствовали или повреждены.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**Ошибка \_ \_ при вводе-выводе реестра \_**
</dt> <dd> <dl> <dt>

1016 (0x3F8)
</dt> <dt>



Не удалось восстановить операцию ввода-вывода, инициированную реестром. Реестру не удалось прочесть, записать или очистить один из файлов, содержащих образ системы в реестре.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**Ошибка \_ не \_ \_ файл реестра**
</dt> <dd> <dl> <dt>

1017 (0x3F9)
</dt> <dt>



Система попыталась загрузить или восстановить файл в реестр, но указанный файл не находится в формате файла реестра.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**\_ключ ошибки \_ удален**
</dt> <dd> <dl> <dt>

1018 (0x3FA)
</dt> <dt>



Попытка выполнить недопустимую операцию для раздела реестра, помеченного для удаления.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**\_нет \_ пространства журнала \_**
</dt> <dd> <dl> <dt>

1019 (0x3FB)
</dt> <dt>



Системе не удалось выделить необходимый объем в журнале реестра.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**\_ключ ошибки \_ имеет \_ дочерние элементы**
</dt> <dd> <dl> <dt>

1020 (0x3FC)
</dt> <dt>



Невозможно создать символьную ссылку в разделе реестра, который уже содержит подразделы или значения.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**\_дочерний элемент error \_ должен \_ быть \_ временным**
</dt> <dd> <dl> <dt>

1021 (0x3FD)
</dt> <dt>



Невозможно создать стабильный подраздел с временным родительским ключом.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**уведомление об ОШИБКе \_ \_ Перечисление \_ dir**
</dt> <dd> <dl> <dt>

1022 (0x3FE)
</dt> <dt>



Выполняется запрос на уведомление об изменении, и данные не возвращаются в буфере вызывающего объекта. Теперь вызывающий объект должен перечислить файлы для поиска изменений.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**\_службы, зависящие от ошибок, \_ \_ выполняются**
</dt> <dd> <dl> <dt>

1051 (0x41B)
</dt> <dt>



Элемент управления "Отмена" был отправлен службе, от которой зависят другие работающие службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**Ошибка при \_ недопустимом \_ \_ управлении службой**
</dt> <dd> <dl> <dt>

1052 (0x41C)
</dt> <dt>



Запрошенный элемент управления не является допустимым для этой службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**\_ \_ время ожидания запроса службы ошибок \_**
</dt> <dd> <dl> <dt>

1053 (0x41D)
</dt> <dt>



Служба не ответила на запрос запуска или контроля за отведенное время.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**\_Служба ошибок \_ нет \_ потока**
</dt> <dd> <dl> <dt>

1054 (0x41E)
</dt> <dt>



Не удалось создать поток для службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**\_ \_ база данных службы ошибок \_ заблокирована**
</dt> <dd> <dl> <dt>

1055 (0x41F)
</dt> <dt>



База данных службы заблокирована.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**\_Служба ошибок \_ уже \_ запущена**
</dt> <dd> <dl> <dt>

1056 (0x420)
</dt> <dt>



Экземпляр службы уже запущен.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**Ошибка \_ недопустимой \_ \_ учетной записи службы**
</dt> <dd> <dl> <dt>

1057 (0x421)
</dt> <dt>



Имя учетной записи недопустимо или не существует, или пароль недопустим для указанного имени учетной записи.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**\_Служба ошибок \_ отключена**
</dt> <dd> <dl> <dt>

1058 (0x422)
</dt> <dt>



Не удается запустить службу, так как она отключена или не имеет связанных с ней включенных устройств.


</dt> </dl> </dd> <dt>

<span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**Ошибка \_ циклической \_ зависимости**
</dt> <dd> <dl> <dt>

1059 (0x423)
</dt> <dt>



Указана циклическая зависимость службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**\_Служба ошибок \_ \_ не \_ существует**
</dt> <dd> <dl> <dt>

1060 (0x424)
</dt> <dt>



Указанная служба не существует в качестве установленной службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**\_Служба ошибок \_ не может \_ принять \_ CTRL**
</dt> <dd> <dl> <dt>

1061 (0x425)
</dt> <dt>



В данный момент служба не может принимать управляющие сообщения.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**\_Служба ошибок \_ \_ неактивна**
</dt> <dd> <dl> <dt>

1062 (0x426)
</dt> <dt>



Служба не запущена.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**Ошибка \_ при \_ \_ подключении к контроллеру службы \_**
</dt> <dd> <dl> <dt>

1063 (0x427)
</dt> <dt>



Процессу службы не удалось подключиться к контроллеру службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**Ошибка \_ исключения \_ в \_ службе**
</dt> <dd> <dl> <dt>

1064 (0x428)
</dt> <dt>



При обработке управляющего запроса возникло исключение в службе.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**\_база данных \_ ошибок \_ не \_ существует**
</dt> <dd> <dl> <dt>

1065 (0x429)
</dt> <dt>



Указанная база данных не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**Ошибка \_ , \_ специфическая для службы \_**
</dt> <dd> <dl> <dt>

1066 (0x42A)
</dt> <dt>



Служба вернула код ошибки, зависящий от службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**\_Обработка ошибок \_ прервана**
</dt> <dd> <dl> <dt>

1067 (0x42B)
</dt> <dt>



Процесс был неожиданно завершен.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**\_ \_ Сбой зависимости службы \_ ошибок**
</dt> <dd> <dl> <dt>

1068 (0x42C)
</dt> <dt>



Не удалось запустить службу или группу зависимостей.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**Ошибка \_ \_ при входе в службу ошибок \_**
</dt> <dd> <dl> <dt>

1069 (0x42D)
</dt> <dt>



Служба не запущена из-за ошибки входа в систему.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**Ошибка \_ при \_ запуске \_ службы**
</dt> <dd> <dl> <dt>

1070 (0x42E)
</dt> <dt>



После запуска служба зависла в состоянии ожидания запуска.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**Ошибка при \_ неправильной \_ \_ блокировке службы**
</dt> <dd> <dl> <dt>

1071 (0x42F)
</dt> <dt>



Указана недопустимая блокировка базы данных службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**\_Служба ошибок \_ помечена \_ для \_ удаления**
</dt> <dd> <dl> <dt>

1072 (0x430)
</dt> <dt>



Указанная служба помечена для удаления.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**\_Служба ошибок \_ существует**
</dt> <dd> <dl> <dt>

1073 (0x431)
</dt> <dt>



Указанная служба уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**Ошибка \_ уже \_ запущена \_ LKG**
</dt> <dd> <dl> <dt>

1074 (0x432)
</dt> <dt>



В настоящее время система работает с последней удачной конфигурацией.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**\_зависимость службы \_ ошибок \_ удалена**
</dt> <dd> <dl> <dt>

1075 (0x433)
</dt> <dt>



Служба зависимостей не существует или помечена для удаления.


</dt> </dl> </dd> <dt>

<span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**Ошибка \_ загрузки \_ уже \_ принята**
</dt> <dd> <dl> <dt>

1076 (0x434)
</dt> <dt>



Текущая загрузка уже принята для использования в качестве последнего известного набора элементов управления.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**\_Служба ошибок \_ никогда не \_ запустилась**
</dt> <dd> <dl> <dt>

1077 (0x435)
</dt> <dt>



С момента последней загрузки попытки запуска службы не были выполнены.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**Ошибка при \_ дублировании \_ \_ имени службы**
</dt> <dd> <dl> <dt>

1078 (0x436)
</dt> <dt>



Это имя уже используется как имя службы или отображаемое имя службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**Ошибка \_ другой \_ \_ учетной записи службы**
</dt> <dd> <dl> <dt>

1079 (0x437)
</dt> <dt>



Учетная запись, указанная для этой службы, отличается от учетной записи, указанной для других служб, работающих в том же процессе.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**Ошибка \_ не \_ может \_ обнаружить \_ сбой драйвера**
</dt> <dd> <dl> <dt>

1080 (0x438)
</dt> <dt>



Действия при сбое могут быть заданы только для служб Win32, а не для драйверов.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**Ошибка \_ не \_ может \_ обнаружить \_ Прерывание процесса**
</dt> <dd> <dl> <dt>

1081 (0x439)
</dt> <dt>



Эта служба выполняется в том же процессе, что и диспетчер управления службами. Поэтому диспетчер управления службами не может предпринимать никаких действий в случае непредвиденного завершения процесса этой службы.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**Ошибка \_ без \_ \_ программы восстановления**
</dt> <dd> <dl> <dt>

1082 (0x43A)
</dt> <dt>



Для этой службы не настроена программа восстановления.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**\_Служба ошибок \_ отсутствует \_ в \_ exe**
</dt> <dd> <dl> <dt>

1083 (0x43B)
</dt> <dt>



Исполняемая программа, для запуска которой настроена эта служба, не реализует службу.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**Ошибка \_ не \_ SAFEBOOT \_ службы**
</dt> <dd> <dl> <dt>

1084 (0x43C)
</dt> <dt>



эта служба не может быть запущена в режиме Сейф.


</dt> </dl> </dd> <dt>

<span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**Ошибка при \_ завершении \_ \_ носителя**
</dt> <dd> <dl> <dt>

1100 (0x44C)
</dt> <dt>



Достигнут физический конец ленты.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**\_ \_ обнаружена ошибка метка файла**
</dt> <dd> <dl> <dt>

1101 (0x44D)
</dt> <dt>



Доступ к ленте достиг метка файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**Ошибка \_ начала \_ \_ носителя**
</dt> <dd> <dl> <dt>

1102 (0x44E)
</dt> <dt>



Обнаружено начало ленты или раздела.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**\_ \_ обнаружена ошибка сетмарк**
</dt> <dd> <dl> <dt>

1103 (0x44F)
</dt> <dt>



Доступ к ленте достиг конца набора файлов.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**Ошибка \_ не \_ \_ обнаружено данных**
</dt> <dd> <dl> <dt>

1104 (0x450)
</dt> <dt>



На ленте больше нет данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**Ошибка \_ секции \_ ошибок**
</dt> <dd> <dl> <dt>

1105 (0x451)
</dt> <dt>



Не удалось секционировать ленту.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**Ошибка \_ недопустимой \_ \_ длины блока**
</dt> <dd> <dl> <dt>

1106 (0x452)
</dt> <dt>



При доступе к новой ленте многодискового раздела текущий размер блока неверен.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**устройство с ОШИБКАми \_ \_ не \_ секционировано**
</dt> <dd> <dl> <dt>

1107 (0x453)
</dt> <dt>



Не удалось найти сведения о разделах ленты при загрузке ленты.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**Ошибка \_ не \_ удалось \_ заблокировать \_ носитель**
</dt> <dd> <dl> <dt>

1108 (0x454)
</dt> <dt>



Не удалось заблокировать механизм извлечения мультимедиа.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**Ошибка \_ не \_ удалось \_ выгрузить \_ носитель**
</dt> <dd> <dl> <dt>

1109 (0x455)
</dt> <dt>



Не удалось выгрузить носитель.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**\_носитель ошибок \_ изменен**
</dt> <dd> <dl> <dt>

1110 (0x456)
</dt> <dt>



Носитель в устройстве мог измениться.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**\_сброс шины с ошибками \_**
</dt> <dd> <dl> <dt>

1111 (0x457)
</dt> <dt>



Шина ввода-вывода сброшена.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**Ошибка \_ без \_ носителя \_ в \_ устройстве**
</dt> <dd> <dl> <dt>

1112 (0x458)
</dt> <dt>



Нет носителя в устройстве.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**Ошибка \_ без \_ преобразования в Юникод \_**
</dt> <dd> <dl> <dt>

1113 (0x459)
</dt> <dt>



В целевой многобайтовой кодовой странице не существует сопоставления для символа Юникода.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**Ошибка \_ \_ при инициализации библиотеки DLL \_**
</dt> <dd> <dl> <dt>

1114 (0x45A)
</dt> <dt>



Не удалось выполнить подпрограммы инициализации библиотеки динамической компоновки (DLL).


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**\_выполняется завершение работы \_ с \_ ошибкой**
</dt> <dd> <dl> <dt>

1115 (0x45B)
</dt> <dt>



Выполняется завершение работы системы.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**Ошибка \_ \_ при завершении работы \_ \_**
</dt> <dd> <dl> <dt>

1116 (0x45C)
</dt> <dt>



Не удалось прервать завершение работы системы, так как не выполнялось завершение работы.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**\_устройство ввода-вывода с ошибками \_**
</dt> <dd> <dl> <dt>

1117 (0x45D)
</dt> <dt>



Выполнить запрос невозможно из-за ошибки устройства ввода-вывода.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**\_последовательная ошибка \_ без \_ устройства**
</dt> <dd> <dl> <dt>

1118 (0x45E)
</dt> <dt>



Не удалось инициализировать последовательные устройства. Последовательный драйвер будет выгружен.


</dt> </dl> </dd> <dt>

<span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**\_IRQ ошибок \_ занятости**
</dt> <dd> <dl> <dt>

1119 (0x45F)
</dt> <dt>



Не удалось открыть устройство, которое совместно использовало запрос на прерывание (IRQ) с другими устройствами. По крайней мере одно другое устройство, использующее этот IRQ, уже открыто.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**Ошибка при дополнительных операциях \_ \_ записи**
</dt> <dd> <dl> <dt>

1120 (0x460)
</dt> <dt>



Операция последовательного ввода-вывода была выполнена другой записью в последовательный порт. \_Счетчик последовательного XOFF-порта ioctl \_ \_ достиг нуля.)


</dt> </dl> </dd> <dt>

<span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**\_время ожидания счетчика ошибок \_**
</dt> <dd> <dl> <dt>

1121 (0x461)
</dt> <dt>



Операция последовательного ввода-вывода завершена из-за истечения времени ожидания. \_Счетчик последовательного XOFF-порта ioctl \_ \_ не получил доступ к нулю.)


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**Ошибка \_ \_ отметка идентификатора дискеты \_ \_ не \_ найдена**
</dt> <dd> <dl> <dt>

1122 (0x462)
</dt> <dt>



На гибком диске не найдена метка адреса идентификатора.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**Ошибка при \_ отформатировании \_ неправильного \_ цилиндра**
</dt> <dd> <dl> <dt>

1123 (0x463)
</dt> <dt>



Несоответствие между полем идентификатора сектора гибкого диска и адресом записи контроллера гибкого диска.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**Ошибка \_ флоппи-дисковода \_ неизвестная \_ Ошибка**
</dt> <dd> <dl> <dt>

1124 (0x464)
</dt> <dt>



В контроллере дисковода гибких дисков обнаружена ошибка, не распознанная драйвером гибкого диска.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**ошибочные \_ \_ неправильные \_ регистры диска**
</dt> <dd> <dl> <dt>

1125 (0x465)
</dt> <dt>



Контроллер гибкого диска вернул непоследовательные результаты в регистрах.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**Ошибка \_ при повторной \_ калибровке диска \_**
</dt> <dd> <dl> <dt>

1126 (0x466)
</dt> <dt>



При доступе к жесткому диску операция повторной калибровки завершилась сбоем даже после повторных попыток.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**Ошибка \_ \_ при выполнении операции с диском \_**
</dt> <dd> <dl> <dt>

1127 (0x467)
</dt> <dt>



При доступе к жесткому диску операция с диском завершилась сбоем даже после повторных попыток.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**Ошибка \_ \_ при сбросе диска \_**
</dt> <dd> <dl> <dt>

1128 (0x468)
</dt> <dt>



При доступе к жесткому диску требуется сброс контроллера диска, но даже сбой.


</dt> </dl> </dd> <dt>

<span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**Ошибка \_ ЕОМ \_ Overflow**
</dt> <dd> <dl> <dt>

1129 (0x469)
</dt> <dt>



Обнаружен физический конец ленты.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**Ошибка \_ \_ недостаточно \_ памяти сервера \_**
</dt> <dd> <dl> <dt>

1130 (0x46A)
</dt> <dt>



"Недостаточно памяти сервера для обработки команды".


</dt> </dl> </dd> <dt>

<span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**\_возможна ошибка \_ взаимоблокировки**
</dt> <dd> <dl> <dt>

1131 (0x46B)
</dt> <dt>



Обнаружена потенциальная ситуация взаимоблокировки.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**\_Выравнивание по сопоставлению ошибок \_**
</dt> <dd> <dl> <dt>

1132 (0x46C)
</dt> <dt>



Указанный базовый адрес или смещение файла не имеют правильного выравнивания.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**Ошибка \_ при \_ установке \_ запрета на состояние электропитания \_**
</dt> <dd> <dl> <dt>

1140 (0x474)
</dt> <dt>



Попытка изменить системное состояние питания была заблокирована другим приложением или драйвером.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**Ошибка \_ \_ при установке \_ состояния электропитания \_**
</dt> <dd> <dl> <dt>

1141 (0x475)
</dt> <dt>



BIOS системы не удалось изменить состояние электропитания системы.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**Ошибка \_ слишком \_ много \_ ссылок**
</dt> <dd> <dl> <dt>

1142 (0x476)
</dt> <dt>



Была предпринята попытка создать больше ссылок на файл, чем поддерживает файловая система.


</dt> </dl> </dd> <dt>

<span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**Ошибка \_ старой \_ \_ версии Win**
</dt> <dd> <dl> <dt>

1150 (0x47E)
</dt> <dt>



Для указанной программы требуется более новая версия Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**Ошибка в приложении, не \_ \_ соответствующем \_ ОС**
</dt> <dd> <dl> <dt>

1151 (0x47F)
</dt> <dt>



Указанная программа не является программой Windows или MS–DOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**Ошибка \_ приложения с одним \_ экземпляром \_**
</dt> <dd> <dl> <dt>

1152 (0x480)
</dt> <dt>



Невозможно запустить более одного экземпляра указанной программы.


</dt> </dl> </dd> <dt>

<span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**Ошибка \_ \_ приложения рмоде**
</dt> <dd> <dl> <dt>

1153 (0x481)
</dt> <dt>



Указанная программа была написана для более ранней версии Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**Ошибка \_ недопустимой \_ библиотеки DLL**
</dt> <dd> <dl> <dt>

1154 (0x482)
</dt> <dt>



Один из файлов библиотеки, необходимых для запуска этого приложения, поврежден.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**Ошибка \_ без \_ связи**
</dt> <dd> <dl> <dt>

1155 (0x483)
</dt> <dt>



С указанным файлом для этой операции не связано ни одно приложение.


</dt> </dl> </dd> <dt>

<span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**Ошибка \_ DDE — \_ сбой**
</dt> <dd> <dl> <dt>

1156 (0x484)
</dt> <dt>



Произошла ошибка при отправке команды приложению.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**\_Библиотека DLL ошибок \_ не \_ найдена**
</dt> <dd> <dl> <dt>

1157 (0x485)
</dt> <dt>



Не удается найти один из файлов библиотеки, необходимых для запуска этого приложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ОШИБКИ \_ больше \_ нет \_ \_ дескрипторов пользователей**
</dt> <dd> <dl> <dt>

1158 (0x486)
</dt> <dt>



Текущий процесс использовал все свои системные квоты дескрипторов объектов диспетчера окон.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**\_ \_ только синхронное сообщение об ошибке \_**
</dt> <dd> <dl> <dt>

1159 (0x487)
</dt> <dt>



Сообщение может использоваться только с синхронными операциями.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**\_элемент источника \_ ошибки \_ пуст**
</dt> <dd> <dl> <dt>

1160 (0x488)
</dt> <dt>



Указанный исходный элемент не имеет носителя.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**\_элемент назначения \_ ошибки \_ полон**
</dt> <dd> <dl> <dt>

1161 (0x489)
</dt> <dt>



Указанный элемент назначения уже содержит носитель.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**Ошибка \_ недопустимого \_ \_ адреса элемента**
</dt> <dd> <dl> <dt>

1162 (0x48A)
</dt> <dt>



Указанный элемент не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**\_журнал ошибок \_ отсутствует \_**
</dt> <dd> <dl> <dt>

1163 (0x48B)
</dt> <dt>



Указанный элемент является частью отсутствующего журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**Ошибка \_ при \_ повторной инициализации \_ устройства**
</dt> <dd> <dl> <dt>

1164 (0x48C)
</dt> <dt>



Указанное устройство требует повторной инициализации из-за ошибок оборудования.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**устройство с ошибкой \_ \_ требует \_ очистки**
</dt> <dd> <dl> <dt>

1165 (0x48D)
</dt> <dt>



Устройство обозначало необходимость очистки перед дальнейшими операциями.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**\_ \_ открыта дверца устройства с ошибкой \_**
</dt> <dd> <dl> <dt>

1166 (0x48E)
</dt> <dt>



Устройство сообщило, что его дверца открыта.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**устройство с ошибкой \_ \_ не \_ подключено**
</dt> <dd> <dl> <dt>

1167 (0x48F)
</dt> <dt>



Устройство не подключено.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**Ошибка \_ не \_ найдена**
</dt> <dd> <dl> <dt>

1168 (0x490)
</dt> <dt>



Элемент не найден.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**Ошибка \_ без \_ соответствия**
</dt> <dd> <dl> <dt>

1169 (0x491)
</dt> <dt>



Для указанного ключа в индексе не найдено совпадений.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**\_ \_ не \_ удалось найти набор ошибок**
</dt> <dd> <dl> <dt>

1170 (0x492)
</dt> <dt>



Указанный набор свойств не существует в объекте.


</dt> </dl> </dd> <dt>

<span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**\_точка ошибки \_ не \_ найдена**
</dt> <dd> <dl> <dt>

1171 (0x493)
</dt> <dt>



Точка, передаваемая в Жетмаусемовепоинтс, отсутствует в буфере.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**Ошибка \_ без \_ \_ службы отслеживания**
</dt> <dd> <dl> <dt>

1172 (0x494)
</dt> <dt>



Служба отслеживания (Рабочая станция) не запущена.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**Ошибка \_ без \_ \_ идентификатора тома**
</dt> <dd> <dl> <dt>

1173 (0x495)
</dt> <dt>



Не удалось найти идентификатор тома.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**Ошибка \_ не \_ удалось \_ удалить \_ замененные**
</dt> <dd> <dl> <dt>

1175 (0x497)
</dt> <dt>



Не удалось удалить файл для замены.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**Ошибка \_ не \_ удалось \_ Переместить \_ замену**
</dt> <dd> <dl> <dt>

1176 (0x498)
</dt> <dt>



Не удалось переместить заменяющий файл в заменяемый файл. Файл, который необходимо заменить, сохранил свое исходное имя.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**Ошибка \_ не \_ удалось \_ Переместить \_ замену \_ 2**
</dt> <dd> <dl> <dt>

1177 (0x499)
</dt> <dt>



Не удалось переместить заменяющий файл в заменяемый файл. Файл, который требуется заменить, был переименован с использованием имени резервной копии.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**\_ \_ выполняется удаление журнала \_ ошибок \_**
</dt> <dd> <dl> <dt>

1178 (0x49A)
</dt> <dt>



Удаляется журнал изменений тома.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**\_журнал ошибок \_ \_ неактивен**
</dt> <dd> <dl> <dt>

1179 (0x49B)
</dt> <dt>



Журнал изменений тома неактивен.


</dt> </dl> </dd> <dt>

<span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**обнаружен ОШИБОЧный \_ \_ файл \_**
</dt> <dd> <dl> <dt>

1180 (0x49C)
</dt> <dt>



Файл найден, но он может быть неправильным.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**\_запись журнала \_ ошибок \_ удалена**
</dt> <dd> <dl> <dt>

1181 (0x49D)
</dt> <dt>



Запись журнала была удалена из журнала.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**Ошибка \_ завершения \_ работы \_ запланирована**
</dt> <dd> <dl> <dt>

1190 (0x4A6)
</dt> <dt>



Завершение работы системы уже запланировано.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**Ошибка \_ при завершении работы \_ пользователей, \_ вошедших \_ в систему**
</dt> <dd> <dl> <dt>

1191 (0x4A7)
</dt> <dt>



Не удается запустить завершение работы системы, так как на компьютере вошли другие пользователи.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**Ошибка \_ неправильного \_ устройства**
</dt> <dd> <dl> <dt>

1200 (0x4B0)
</dt> <dt>



Указано недопустимое имя устройства.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**Ошибка \_ \_ несвободного подключения**
</dt> <dd> <dl> <dt>

1201 (0x4B1)
</dt> <dt>



Устройство в настоящее время не подключено, но это запоминаемое подключение.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**устройство с ОШИБКАми \_ \_ уже \_ сохранено**
</dt> <dd> <dl> <dt>

1202 (0x4B2)
</dt> <dt>



Локальное имя устройства имеет запоминаемое подключение к другому сетевому ресурсу.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**Ошибка \_ без \_ сетевого \_ или \_ неверного \_ пути**
</dt> <dd> <dl> <dt>

1203 (0x4B3)
</dt> <dt>



Сетевой путь был либо неправильно введен, не существует, либо поставщик сети в настоящее время недоступен. Попробуйте ввести путь заново или обратитесь к администратору сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**Ошибка \_ неверного \_ поставщика**
</dt> <dd> <dl> <dt>

1204 (0x4B4)
</dt> <dt>



Указано недопустимое имя поставщика сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**Ошибка \_ не может \_ открыть \_ профиль**
</dt> <dd> <dl> <dt>

1205 (0x4B5)
</dt> <dt>



Не удалось открыть профиль сетевого подключения.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ОШИБКА с \_ неправильным \_ профилем**
</dt> <dd> <dl> <dt>

1206 (0x4B6)
</dt> <dt>



Профиль сетевого подключения поврежден.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**Ошибка \_ не является \_ контейнером**
</dt> <dd> <dl> <dt>

1207 (0x4B7)
</dt> <dt>



Невозможно перечислить неконтейнер.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**Ошибка \_ расширенной \_ ошибки**
</dt> <dd> <dl> <dt>

1208 (0x4B8)
</dt> <dt>



Произошла Расширенная ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**Ошибка \_ недопустимого \_ GROUPNAME**
</dt> <dd> <dl> <dt>

1209 (0x4B9)
</dt> <dt>



Формат указанного имени группы недопустим.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**Ошибка \_ недопустимое \_ имя компьютера**
</dt> <dd> <dl> <dt>

1210 (0x4BA)
</dt> <dt>



Недопустимый формат указанного имени компьютера.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**Ошибка \_ Недопустимая \_ EVENTNAME**
</dt> <dd> <dl> <dt>

1211 (0x4BB)
</dt> <dt>



Недопустимый формат указанного имени события.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**Ошибка \_ недопустимое \_ имя домена**
</dt> <dd> <dl> <dt>

1212 (0x4BC)
</dt> <dt>



Недопустимый формат указанного доменного имени.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**Ошибка \_ недопустимого \_ ServiceName**
</dt> <dd> <dl> <dt>

1213 (0x4BD)
</dt> <dt>



Формат указанного имени службы недопустим.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**Ошибка \_ недопустимого \_ NETNAME**
</dt> <dd> <dl> <dt>

1214 (0x4BE)
</dt> <dt>



Недопустимый формат указанного сетевого имени.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**Ошибка \_ недопустимое \_ SHARENAME**
</dt> <dd> <dl> <dt>

1215 (0x4BF)
</dt> <dt>



Недопустимый формат указанного имени общего ресурса.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**Ошибка \_ недопустимого \_ пассворднаме**
</dt> <dd> <dl> <dt>

1216 (0x4C0)
</dt> <dt>



Недопустимый формат указанного пароля.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**Ошибка \_ недопустимого \_ мессаженаме**
</dt> <dd> <dl> <dt>

1217 (0x4C1)
</dt> <dt>



Недопустимый формат указанного имени сообщения.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**Ошибка \_ недопустимого \_ мессажедест**
</dt> <dd> <dl> <dt>

1218 (0x4C2)
</dt> <dt>



Недопустимый формат указанного назначения сообщения.


</dt> </dl> </dd> <dt>

<span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**\_ \_ конфликт учетных данных сеанса с ошибками \_**
</dt> <dd> <dl> <dt>

1219 (0x4C3)
</dt> <dt>



Несколько подключений к серверу или общему ресурсу одного и того же пользователя не разрешено использовать несколько имен пользователей. Отключите все предыдущие подключения к серверу или общему ресурсу и повторите попытку.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**\_ \_ \_ превышен предел удаленного сеанса \_**
</dt> <dd> <dl> <dt>

1220 (0x4C4)
</dt> <dt>



Была предпринята попытка установить сеанс на сетевом сервере, но уже установлено слишком много сеансов для этого сервера.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**Ошибка \_ DUP \_ имя_домена**
</dt> <dd> <dl> <dt>

1221 (0x4C5)
</dt> <dt>



Имя рабочей группы или домена уже используется другим компьютером в сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**Ошибка \_ нет \_ сети**
</dt> <dd> <dl> <dt>

1222 (0x4C6)
</dt> <dt>



Сеть отсутствует или не запущена.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**Ошибка \_ отменена**
</dt> <dd> <dl> <dt>

1223 (0x4C7)
</dt> <dt>



Операция отменена пользователем.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**Ошибка \_ \_ сопоставленного пользователем \_ файла**
</dt> <dd> <dl> <dt>

1224 (0x4C8)
</dt> <dt>



Невозможно выполнить запрошенную операцию над файлом с открытым сопоставленным пользователем разделом.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**Ошибка при \_ подключении \_**
</dt> <dd> <dl> <dt>

1225 (0x4C9)
</dt> <dt>



Удаленный компьютер отклонил сетевое подключение.


</dt> </dl> </dd> <dt>

<span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**Ошибка при \_ мягком \_ отключении**
</dt> <dd> <dl> <dt>

1226 (0x4CA)
</dt> <dt>



Сетевое подключение было корректно закрыто.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**\_адрес ошибки \_ уже \_ связан**
</dt> <dd> <dl> <dt>

1227 (0x4CB)
</dt> <dt>



С конечной точкой сетевого транспорта уже связан адрес.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**\_адрес ошибки \_ не \_ связан**
</dt> <dd> <dl> <dt>

1228 (0x4CC)
</dt> <dt>



С конечной точкой сети еще не связан адрес.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**\_недопустимое подключение к ошибке \_**
</dt> <dd> <dl> <dt>

1229 (0x4CD)
</dt> <dt>



Предпринята попытка выполнить операцию для несуществующего сетевого подключения.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**\_Подключение к ошибке \_ активно**
</dt> <dd> <dl> <dt>

1230 (0x4CE)
</dt> <dt>



Попытка выполнить недопустимую операцию для активного сетевого подключения.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**Ошибка " \_ сеть \_ недоступна"**
</dt> <dd> <dl> <dt>

1231 (0x4CF)
</dt> <dt>



Не удается получить доступ к сетевому расположению. сведения об устранении неполадок в сети см. в разделе справка Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**\_узел ошибок \_ недоступен**
</dt> <dd> <dl> <dt>

1232 (0x4D0)
</dt> <dt>



Не удается получить доступ к сетевому расположению. сведения об устранении неполадок в сети см. в разделе справка Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**\_протокол ошибки \_ недоступен**
</dt> <dd> <dl> <dt>

1233 (0x4D1)
</dt> <dt>



Не удается получить доступ к сетевому расположению. сведения об устранении неполадок в сети см. в разделе справка Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**\_порт ошибки \_ недоступен**
</dt> <dd> <dl> <dt>

1234 (0x4D2)
</dt> <dt>



В конечной точке сети назначения в удаленной системе не работает ни одна служба.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**запрос на ошибку \_ \_ прерван**
</dt> <dd> <dl> <dt>

1235 (0x4D3)
</dt> <dt>



Запрос был прерван.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**\_Подключение к ошибке \_ прервано**
</dt> <dd> <dl> <dt>

1236 (0x4D4)
</dt> <dt>



Сетевое подключение прервано локальной системой.


</dt> </dl> </dd> <dt>

<span id="ERROR_RETRY"></span><span id="error_retry"></span>**Ошибка \_ повтора**
</dt> <dd> <dl> <dt>

1237 (0x4D5)
</dt> <dt>



Не удалось завершить операцию. Необходимо выполнить повторную попытку.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**\_ \_ ограничение числа подключений об ошибках \_**
</dt> <dd> <dl> <dt>

1238 (0x4D6)
</dt> <dt>



Не удалось установить соединение с сервером, так как достигнуто предельное число одновременных подключений для этой учетной записи.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**\_ограничение времени входа в систему \_ \_**
</dt> <dd> <dl> <dt>

1239 (0x4D7)
</dt> <dt>



Попытка входа в систему в течение неавторизованного времени для этой учетной записи.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**Ошибка \_ при \_ вкста \_ ограничения имени входа**
</dt> <dd> <dl> <dt>

1240 (0x4D8)
</dt> <dt>



Учетная запись не имеет права на вход с этой станции.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**Ошибка при \_ неправильном \_ адресе**
</dt> <dd> <dl> <dt>

1241 (0x4D9)
</dt> <dt>



Не удалось использовать сетевой адрес для запрошенной операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**Ошибка \_ уже \_ зарегистрирована**
</dt> <dd> <dl> <dt>

1242 (0x4DA)
</dt> <dt>



Служба уже зарегистрирована.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**\_Служба ошибок \_ не \_ найдена**
</dt> <dd> <dl> <dt>

1243 (0x4DB)
</dt> <dt>



Указанная служба не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**Ошибка \_ не \_ прошла проверку подлинности**
</dt> <dd> <dl> <dt>

1244 (0x4DC)
</dt> <dt>



Запрошенная операция не была выполнена, так как пользователь не прошел проверку подлинности.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**Ошибка \_ не \_ зарегистрирована \_**
</dt> <dd> <dl> <dt>

1245 (0x4DD)
</dt> <dt>



Запрошенная операция не была выполнена, так как пользователь не выполнил вход в сеть. Указанная служба не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**Ошибка \_ продолжения**
</dt> <dd> <dl> <dt>

1246 (0x4DE)
</dt> <dt>



Продолжите работу с выполняемой работой.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**Ошибка \_ уже \_ инициализирована**
</dt> <dd> <dl> <dt>

1247 (0x4DF)
</dt> <dt>



Предпринята попытка выполнить операцию инициализации, когда инициализация уже завершена.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**Ошибка \_ больше \_ \_ устройств**
</dt> <dd> <dl> <dt>

1248 (0x4E0)
</dt> <dt>



Больше нет локальных устройств.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**Ошибка \_ нет \_ такого \_ сайта**
</dt> <dd> <dl> <dt>

1249 (0x4E1)
</dt> <dt>



Указанный сайт не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**Ошибка \_ \_ контроллер домена \_**
</dt> <dd> <dl> <dt>

1250 (0x4E2)
</dt> <dt>



Контроллер домена с указанным именем уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**Ошибка \_ только \_ при \_ наличии подключения**
</dt> <dd> <dl> <dt>

1251 (0x4E3)
</dt> <dt>



Эта операция поддерживается только при подключении к серверу.


</dt> </dl> </dd> <dt>

<span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**Ошибка \_ переопределения \_ неизмененных изменений**
</dt> <dd> <dl> <dt>

1252 (0x4E4)
</dt> <dt>



Платформа групповой политики должна вызывать расширение, даже если изменения отсутствуют.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**Ошибка \_ неверного \_ \_ профиля пользователя**
</dt> <dd> <dl> <dt>

1253 (0x4E5)
</dt> <dt>



Указанный пользователь не имеет допустимого профиля.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**Ошибка \_ не \_ поддерживается \_ в \_ SBS**
</dt> <dd> <dl> <dt>

1254 (0x4E6)
</dt> <dt>



эта операция не поддерживается на компьютере с Windows server 2003 для Small Business Server.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**Ошибка \_ \_ завершения работы \_ сервера \_**
</dt> <dd> <dl> <dt>

1255 (0x4E7)
</dt> <dt>



Компьютер сервера завершает работу.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**Ошибка \_ размещения узла \_**
</dt> <dd> <dl> <dt>

1256 (0x4E8)
</dt> <dt>



Удаленная система недоступна. сведения об устранении неполадок в сети см. в разделе справка Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**Ошибка \_ без \_ учетной записи \_ безопасности**
</dt> <dd> <dl> <dt>

1257 (0x4E9)
</dt> <dt>



Указанный идентификатор безопасности не относится к домену учетной записи.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**Ошибка \_ не \_ является \_ идентификатором безопасности домена**
</dt> <dd> <dl> <dt>

1258 (0x4EA)
</dt> <dt>



Указанный идентификатор безопасности не содержит компонент домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**Ошибка \_ APPHELP \_ блок**
</dt> <dd> <dl> <dt>

1259 (0x4EB)
</dt> <dt>



AppHelp диалоговое окно отменено, поэтому запускать приложение не удается.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**\_доступ к ошибкам \_ отключен \_ \_ политикой**
</dt> <dd> <dl> <dt>

1260 (0x4EC)
</dt> <dt>



Эта программа заблокирована групповой политикой. Для получения дополнительных сведений обратитесь к системному администратору.


</dt> </dl> </dd> <dt>

<span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**Ошибка \_ при \_ использовании NAT для регистрации ошибок \_**
</dt> <dd> <dl> <dt>

1261 (0x4ED)
</dt> <dt>



Программа пытается использовать недопустимое значение регистра. Обычно это вызвано неинициализированной регистрацией. Эта ошибка относится только к Itanium.


</dt> </dl> </dd> <dt>

<span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**Ошибка \_ кскшаре \_ offline**
</dt> <dd> <dl> <dt>

1262 (0x4EE)
</dt> <dt>



Общая папка в данный момент отключена или не существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**Ошибка \_ PKINIT \_**
</dt> <dd> <dl> <dt>

1263 (0x4EF)
</dt> <dt>



В протоколе Kerberos произошла ошибка при проверке сертификата KDC во время входа в смарт-карту. Дополнительные сведения см. в журнале системных событий.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**Ошибка \_ подсистемы смарт-карты \_ \_ при ошибке**
</dt> <dd> <dl> <dt>

1264 (0x4F0)
</dt> <dt>



В протоколе Kerberos произошла ошибка при попытке использовать подсистему смарт-карты.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**\_обнаружено понижение ошибки \_**
</dt> <dd> <dl> <dt>

1265 (0x4F1)
</dt> <dt>



Системе не удается связаться с контроллером домена для обслуживания запроса проверки подлинности. Повторите попытку позже.


</dt> </dl> </dd> <dt>

<span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**Ошибка \_ \_ блокировки компьютера**
</dt> <dd> <dl> <dt>

1271 (0x4F7)
</dt> <dt>



Компьютер заблокирован и не может завершить работу без параметра Force.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**\_обратный вызов ошибки \_ указал \_ недопустимые \_ данные**
</dt> <dd> <dl> <dt>

1273 (0x4F9)
</dt> <dt>



Определяемый приложением обратный вызов предоставил недопустимые данные при вызове.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**\_ \_ требуется обновление переднего плана для синхронизации ошибок \_ \_**
</dt> <dd> <dl> <dt>

1274 (0x4FA)
</dt> <dt>



Платформа групповой политики должна вызывать расширение в синхронном обновлении политики переднего плана.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**\_драйвер ошибки \_ заблокирован**
</dt> <dd> <dl> <dt>

1275 (0x4FB)
</dt> <dt>



Загрузка этого драйвера заблокирована.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**Ошибка \_ при \_ импорте недействительной \_ \_ \_ библиотеки DLL**
</dt> <dd> <dl> <dt>

1276 (0x4FC)
</dt> <dt>



Библиотека динамической компоновки (DLL) ссылается на модуль, который не является ни библиотекой DLL, ни исполняемым образом процесса.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**Ошибка \_ доступа к \_ колонке "отключено" \_**
</dt> <dd> <dl> <dt>

1277 (0x4FD)
</dt> <dt>



Windows не удается открыть эту программу, так как она отключена.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**Ошибка \_ доступа к \_ запрещенным \_ ИЗМЕНЕНИЯм в колонке \_**
</dt> <dd> <dl> <dt>

1278 (0x4FE)
</dt> <dt>



Windows не может открыть эту программу, так как система принудительного применения лицензий была незаконно изменена или повреждена.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**Ошибка \_ восстановления \_ при сбое**
</dt> <dd> <dl> <dt>

1279 (0x4FF)
</dt> <dt>



Не удалось восстановить транзакцию.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**Ошибка \_ уже \_ Fiber**
</dt> <dd> <dl> <dt>

1280 (0x500)
</dt> <dt>



Текущий поток уже преобразован в волокно.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**Ошибка \_ уже является \_ потоком**
</dt> <dd> <dl> <dt>

1281 (0x501)
</dt> <dt>



Текущий поток уже преобразован из волокон.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**\_ \_ переполнение буфера СТЕКа ошибок \_**
</dt> <dd> <dl> <dt>

1282 (0x502)
</dt> <dt>



Система обнаружила переполнение буфера на основе стека в этом приложении. Такое переполнение потенциально может позволить злоумышленнику получить контроль над этим приложением.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**\_ \_ превышена квота параметра ошибки \_**
</dt> <dd> <dl> <dt>

1283 (0x503)
</dt> <dt>



Данные в одном из параметров больше, чем может работать функция.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**\_ОТЛАДЧИК ошибок \_ неактивен**
</dt> <dd> <dl> <dt>

1284 (0x504)
</dt> <dt>



Попытка выполнить операцию с объектом Debug завершилась сбоем, так как объект находится в процессе удаления.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**Ошибка \_ \_ при загрузке с задержкой \_**
</dt> <dd> <dl> <dt>

1285 (0x505)
</dt> <dt>



Сбой при задержке загрузки .dll или получении адреса функции в .dll с отложенной загрузкой.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**Ошибка \_ не \_ разрешена для VDM**
</dt> <dd> <dl> <dt>

1286 (0x506)
</dt> <dt>



%1 является 16-разрядным приложением. У вас нет разрешений на выполнение 16-разрядных приложений. Проверьте свои разрешения у системного администратора.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**Ошибка \_ НЕопознанной \_ ошибки**
</dt> <dd> <dl> <dt>

1287 (0x507)
</dt> <dt>



Недостаточно сведений для выяснения причины сбоя.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**Ошибка \_ недопустимого \_ \_ параметра крунтиме**
</dt> <dd> <dl> <dt>

1288 (0x508)
</dt> <dt>



Неверное значение параметра, переданного в функцию среды выполнения C.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**Ошибка \_ за пределами \_ ВДЛ**
</dt> <dd> <dl> <dt>

1289 (0x509)
</dt> <dt>



Операция была выполнена за пределами допустимой длины данных файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**Ошибка \_ несовместимый \_ \_ тип SID \_ службы**
</dt> <dd> <dl> <dt>

1290 (0x50A)
</dt> <dt>



Не удалось запустить службу, так как одна или несколько служб в одном процессе имеют несовместимый параметр типа идентификатора безопасности службы. Служба с ограниченным типом SID может сосуществовать только в том же процессе с другими службами с ограниченным типом SID. Если для этой службы был только что настроен тип идентификатора безопасности службы, то для запуска этой службы необходимо перезапустить процесс размещения.

в Windows Server 2003 и Windows XP неограниченная служба не может сосуществовать в одном процессе с другими службами. Чтобы запустить эту службу, служба с типом SID неограниченного доступа должна быть перемещена в принадлежащий процесс.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**\_процесс драйвера \_ ошибки \_ завершен**
</dt> <dd> <dl> <dt>

1291 (0x50B)
</dt> <dt>



Процесс, в котором размещается драйвер для этого устройства, был завершен.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**\_ограничение реализации \_ ошибок**
</dt> <dd> <dl> <dt>

1292 (0x50C)
</dt> <dt>



Операция попыталась превысить предел, определенный реализацией.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**процесс с ОШИБКАми \_ \_ \_ защищен**
</dt> <dd> <dl> <dt>

1293 (0x50D)
</dt> <dt>



Целевой процесс или процесс, содержащий целевой поток, является защищенным процессом.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**\_Служба ошибок \_ уведомлять \_ клиента \_ задержкой**
</dt> <dd> <dl> <dt>

1294 (0x50E)
</dt> <dt>



Клиент уведомлений службы задержкой слишком далеко позади текущего состояния служб на компьютере.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**\_ \_ превышена квота диска \_**
</dt> <dd> <dl> <dt>

1295 (0x50F)
</dt> <dt>



Операция запрошенного файла завершилась сбоем из-за превышения квоты хранилища. Чтобы освободить место на диске, переместите файлы в другое расположение или удалите ненужные файлы. Для получения дополнительных сведений обратитесь к системному администратору.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**\_содержимое ошибки \_ заблокировано**
</dt> <dd> <dl> <dt>

1296 (0x510)
</dt> <dt>



Не удалось выполнить запрошенную операцию с файлом, так как политика хранилища блокирует этот тип файла. Для получения дополнительных сведений обратитесь к системному администратору.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**Ошибка \_ несовместимой \_ \_ привилегии службы**
</dt> <dd> <dl> <dt>

1297 (0x511)
</dt> <dt>



Привилегия, необходимая службе для правильной работы, не существует в конфигурации учетной записи службы. для просмотра конфигурации службы и конфигурации учетной записи можно использовать оснастку консоли управления (mmc) "службы" и оснастку локальной безопасности Параметры mmc (secpol. msc).


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**Ошибка \_ при \_ зависании приложения**
</dt> <dd> <dl> <dt>

1298 (0x512)
</dt> <dt>



Поток, вовлеченный в эту операцию, не отвечает.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**Ошибка \_ недопустимой \_ Метки**
</dt> <dd> <dl> <dt>

1299 (0x513)
</dt> <dt>



Указывает, что определенный идентификатор безопасности не может быть назначен в качестве метки объекта.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды системных ошибок](system-error-codes.md)
</dt> </dl>

 

 




