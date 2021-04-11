---
description: Описание кодов ошибок 500-999, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: 8d8b427b-b761-4023-a834-a6eff96d6ba1
title: Коды системных ошибок (500-999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 02b35374fcb68f9b416948d5e39b2182f573b60f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262704"
---
# <a name="system-error-codes-500-999"></a>Коды системных ошибок (500-999)

> [!NOTE]
> Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки. Для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.

В следующем списке приведены [коды системных ошибок](system-error-codes.md) (ошибки 500 – 999). Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций. Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .

<dl> <dt>

<span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**Ошибка \_ при \_ загрузке профиля пользователя \_**
</dt> <dd> <dl> <dt>

500 (0x1F4)
</dt> <dt>



Не удается загрузить профиль пользователя.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**\_арифметическое \_ переполнение при ошибке**
</dt> <dd> <dl> <dt>

534 (0x216)
</dt> <dt>



Арифметический результат превысил 32 бит.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**\_канал ошибки \_ подключен**
</dt> <dd> <dl> <dt>

535 (0x217)
</dt> <dt>



Существует процесс на другом конце канала.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**Ошибка \_ при \_ прослушивании канала**
</dt> <dd> <dl> <dt>

536 (0x218)
</dt> <dt>



Ожидание открытия процессом другого конца канала.


</dt> </dl> </dd> <dt>

<span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**Ошибка \_ средства проверки ошибок \_**
</dt> <dd> <dl> <dt>

537 (0x219)
</dt> <dt>



Средство проверки приложений обнаружило ошибку в текущем процессе.


</dt> </dl> </dd> <dt>

<span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**Ошибка \_ абиос \_ , ошибка**
</dt> <dd> <dl> <dt>

538 (0x21A)
</dt> <dt>



Произошла ошибка в подсистеме АБИОС.


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**Ошибка \_ WX86, \_ предупреждение**
</dt> <dd> <dl> <dt>

539 (0x21B)
</dt> <dt>



В подсистеме WX86 возникло предупреждение.


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**Ошибка \_ WX86 \_ , ошибка**
</dt> <dd> <dl> <dt>

540 (0x21C)
</dt> <dt>



Произошла ошибка в подсистеме WX86.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**\_таймер ошибок \_ не \_ отменен**
</dt> <dd> <dl> <dt>

541 (0x21D)
</dt> <dt>



Предпринята попытка отмены или установки таймера, имеющего связанный объект APC, а поток субъекта не является потоком, который изначально установил таймер с помощью связанной подпрограммы APC.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**Ошибка \_ очистки**
</dt> <dd> <dl> <dt>

542 (0x21E)
</dt> <dt>



Код исключения очистки.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ошибочный \_ \_ стек ошибок**
</dt> <dd> <dl> <dt>

543 (0x21F)
</dt> <dt>



Во время операции очистки обнаружен недопустимый или несогласованный стек.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**Ошибка \_ недопустимого \_ \_ целевого объекта очистки**
</dt> <dd> <dl> <dt>

544 (0x220)
</dt> <dt>



При выполнении операции завершения обнаружен недопустимый целевой объект очистки.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**Ошибка \_ недопустимых \_ \_ атрибутов порта**
</dt> <dd> <dl> <dt>

545 (0x221)
</dt> <dt>



Указаны недопустимые атрибуты объекта для Нткреатепорт или для Нтконнектпорт указаны недопустимые атрибуты порта


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**\_ \_ \_ слишком \_ ДЛИННое сообщение порта ошибки**
</dt> <dd> <dl> <dt>

546 (0x222)
</dt> <dt>



Длина сообщения, переданного в Нтрекуестпорт или Нтрекуестваитреплипорт, превышает максимально допустимое для порта сообщение.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**Ошибка \_ недопустимой \_ квоты \_ ниже**
</dt> <dd> <dl> <dt>

547 (0x223)
</dt> <dt>



Предпринята попытка снижения предельной квоты ниже текущего использования.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**устройство с ошибкой \_ \_ уже \_ подключено**
</dt> <dd> <dl> <dt>

548 (0x224)
</dt> <dt>



Предпринята попытка присоединения к устройству, которое уже подключено к другому устройству.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**Ошибка при неправильном \_ \_ выравнивании инструкции**
</dt> <dd> <dl> <dt>

549 (0x225)
</dt> <dt>



Предпринята попытка выполнить инструкцию по несогласованному адресу, а система узла не поддерживает ссылки на несогласованные инструкции.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**\_ \_ не ЗАПУЩЕНо ПРОФИЛИРОВАНие ошибок \_**
</dt> <dd> <dl> <dt>

550 (0x226)
</dt> <dt>



Профилирование не запущено.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**\_ \_ не ОСТАНОВЛЕНо ПРОФИЛИРОВАНие ошибок \_**
</dt> <dd> <dl> <dt>

551 (0x227)
</dt> <dt>



Профилирование не остановлено.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**\_не удалось \_ \_ интерпретировать ошибку**
</dt> <dd> <dl> <dt>

552 (0x228)
</dt> <dt>



Переданный список ACL не содержал минимально необходимой информации.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**Ошибка \_ профилирования \_ в \_ ограничении**
</dt> <dd> <dl> <dt>

553 (0x229)
</dt> <dt>



Число активных объектов профилирования достигло максимума и больше не может быть запущено.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ОШИБКА не \_ удается \_ дождаться**
</dt> <dd> <dl> <dt>

554 (0x22A)
</dt> <dt>



Используется, чтобы указать, что операция не может продолжаться без блокировки операций ввода-вывода.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ОШИБКА не \_ удается \_ завершить \_ самостоятельно**
</dt> <dd> <dl> <dt>

555 (0x22B)
</dt> <dt>



Указывает, что поток попытался завершить себя по умолчанию (с именем Нттерминатесреад со **значением NULL**) и последним потоком в текущем процессе.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**\_непредвиденная ошибка при \_ создании ошибки mm \_ \_**
</dt> <dd> <dl> <dt>

556 (0x22C)
</dt> <dt>



Если возвращается ошибка MM, которая не определена в стандартном фильтре Фсртл, она преобразуется в одну из следующих ошибок, которые гарантированно будут в фильтре. В этом случае данные теряются, но фильтр правильно обрабатывает исключение.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**Ошибка \_ непредвиденной \_ \_ ошибки в карте mm \_**
</dt> <dd> <dl> <dt>

557 (0x22D)
</dt> <dt>



Если возвращается ошибка MM, которая не определена в стандартном фильтре Фсртл, она преобразуется в одну из следующих ошибок, которые гарантированно будут в фильтре. В этом случае данные теряются, но фильтр правильно обрабатывает исключение.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**\_непредвиденная ошибка при \_ расширении ошибки mm \_ \_**
</dt> <dd> <dl> <dt>

558 (0x22E)
</dt> <dt>



Если возвращается ошибка MM, которая не определена в стандартном фильтре Фсртл, она преобразуется в одну из следующих ошибок, которые гарантированно будут в фильтре. В этом случае данные теряются, но фильтр правильно обрабатывает исключение.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**Ошибка \_ неправильной \_ \_ таблицы функции**
</dt> <dd> <dl> <dt>

559 (0x22F)
</dt> <dt>



При выполнении операции завершения обнаружена неверно сформированная Таблица функций.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**Ошибка \_ при \_ \_ преобразовании GUID**
</dt> <dd> <dl> <dt>

560 (0X230)
</dt> <dt>



Указывает, что была предпринята попытка присвоить защиту файлу или каталогу файловой системы, а один из идентификаторов безопасности из этого дескриптора не может быть преобразован в идентификатор GUID, который может храниться в файловой системе. Это вызывает сбой попытки защиты, что может привести к сбою при попытке создания файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**Ошибка \_ недопустимого \_ размера локальной таблицы \_**
</dt> <dd> <dl> <dt>

561 (0x231)
</dt> <dt>



Указывает, что была предпринята попытка расширить список описателей локальной таблицы, задав ее размер или размер которой не является четным числом селекторов.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**Ошибка \_ недопустимого \_ смещения локальной таблицы \_**
</dt> <dd> <dl> <dt>

563 (0x233)
</dt> <dt>



Указывает, что начальное значение сведений о локальной списке описателей не является целым числом, кратным размеру селектора.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**Ошибка \_ недопустимого \_ \_ дескриптора локальной таблицы**
</dt> <dd> <dl> <dt>

564 (0x234)
</dt> <dt>



Указывает, что при попытке настройки описателей локальной таблицы пользователь указал недопустимый дескриптор.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**Ошибка \_ слишком \_ много \_ потоков**
</dt> <dd> <dl> <dt>

565 (0x235)
</dt> <dt>



Указывает, что процесс имеет слишком много потоков для выполнения запрошенного действия. Например, назначение основного маркера может быть выполнено только в том случае, если процесс имеет ноль или один поток.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**поток ошибок, \_ \_ не \_ \_ обрабатываемый процессом**
</dt> <dd> <dl> <dt>

566 (0x236)
</dt> <dt>



Предпринята попытка обработать поток в рамках определенного процесса, но указанный поток не находится в указанном процессе.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**\_ \_ превышена квота файла подкачки \_**
</dt> <dd> <dl> <dt>

567 (0x237)
</dt> <dt>



Превышена квота файла подкачки.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**Ошибка \_ при \_ \_ конфликте сервера входа**
</dt> <dd> <dl> <dt>

568 (0x238)
</dt> <dt>



Не удается запустить службу Netlogon, так как другая служба Netlogon, работающая в домене, конфликтует с указанной ролью.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**\_требуется синхронизация с ошибками \_**
</dt> <dd> <dl> <dt>

569 (0x239)
</dt> <dt>



База данных SAM на сервере Windows Server значительно не синхронизирована с копией на контроллере домена. Требуется полная синхронизация.


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**Ошибка \_ net \_ Open \_ не удалось**
</dt> <dd> <dl> <dt>

570 (0x23A)
</dt> <dt>



Сбой API NtCreateFile. Эта ошибка никогда не должна возвращаться в приложение. это заполнитель для перенаправителя диспетчера LAN Windows, который будет использоваться в внутренних подпрограммых сопоставления ошибок.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**Ошибка \_ \_ при выполнении права ввода-вывода \_**
</dt> <dd> <dl> <dt>

571 (0x23B)
</dt> <dt>



{Привилегия не пройдена} Не удалось изменить разрешения ввода-вывода для процесса.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**Управление ОШИБКАми \_ \_ C \_ выходом**
</dt> <dd> <dl> <dt>

572 (0x23C)
</dt> <dt>



{Выход из приложения по CTRL + C} Приложение прервано в результате нажатия клавиш CTRL + C.


</dt> </dl> </dd> <dt>

<span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**Ошибка при \_ отсутствии \_ системфиле**
</dt> <dd> <dl> <dt>

573 (0x23D)
</dt> <dt>



{Отсутствует системный файл} Необходимый системный файл% HS поврежден или отсутствует.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**Ошибка \_ НЕобработанного \_ исключения**
</dt> <dd> <dl> <dt>

574 (0x23E)
</dt> <dt>



{Ошибка приложения} Исключение% s (0x% 08lx) произошло в приложении в расположении 0x% 08LX.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**Ошибка \_ \_ инициализации приложения \_ при ошибке**
</dt> <dd> <dl> <dt>

575 (0x23F)
</dt> <dt>



{Ошибка приложения} Не удалось правильно запустить приложение (0x% LX). Нажмите кнопку ОК, чтобы закрыть приложение.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**\_сбой создания файла подкачки ошибок \_ \_**
</dt> <dd> <dl> <dt>

576 (0x240)
</dt> <dt>



{Не удается создать файл подкачки} Не удалось создать файл подкачки% HS (% LX). Запрошенный размер% ld.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**Ошибка \_ недопустимого \_ \_ хэша изображения**
</dt> <dd> <dl> <dt>

577 (0x241)
</dt> <dt>



Windows не удается проверить цифровую подпись для этого файла. При недавнем изменении оборудования или программного обеспечения может быть установлен файл, который подписан неправильно или поврежден или может быть вредоносным программным обеспечением из неизвестного источника.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**Ошибка \_ без \_ файла подкачки**
</dt> <dd> <dl> <dt>

578 (0x242)
</dt> <dt>



{Не указан файл подкачки} В конфигурации системы не указан файл подкачки.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**Ошибка \_ недопустимого \_ \_ контекста float**
</dt> <dd> <dl> <dt>

579 (0x243)
</dt> <dt>



ОБ Приложение реального режима выпустило инструкцию с плавающей запятой и оборудование с плавающей запятой отсутствует.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**Ошибка \_ без \_ \_ пары событий**
</dt> <dd> <dl> <dt>

580 (0x244)
</dt> <dt>



Операция синхронизации пары событий была выполнена с помощью объекта пары событий клиент/сервер конкретного потока, но с потоком не связан ни один объект пары событий.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**Ошибка \_ \_ настройки доменного \_ сочетания \_ ошибок**
</dt> <dd> <dl> <dt>

581 (0x245)
</dt> <dt>



Неверная конфигурация Windows Server.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**Ошибка \_ недопустимого \_ символа**
</dt> <dd> <dl> <dt>

582 (0x246)
</dt> <dt>



Обнаружен недопустимый знак. Для многобайтовой кодировки это включает старший байт без завершающего байта. Для набора символов Юникода это включает символы 0xFFFF и 0xFFFE.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**Ошибка \_ НЕопределенного \_ символа**
</dt> <dd> <dl> <dt>

583 (0x247)
</dt> <dt>



Символ Юникода не определен в наборе символов Юникода, установленном в системе.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**Ошибка в \_ томе гибких дисков \_**
</dt> <dd> <dl> <dt>

584 (0x248)
</dt> <dt>



Невозможно создать файл подкачки на дискете.


</dt> </dl> </dd> <dt>

<span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**Ошибка \_ BIOS \_ при \_ \_ подключении \_ прерывания**
</dt> <dd> <dl> <dt>

585 (0x249)
</dt> <dt>



BIOS системы не удалось подключить системное прерывание к устройству или шине, к которой подключено устройство.


</dt> </dl> </dd> <dt>

<span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**Ошибка \_ контроллера резервного копирования \_**
</dt> <dd> <dl> <dt>

586 (0x24A)
</dt> <dt>



Эта операция разрешена только для основного контроллера домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**\_Превышено ограничение мутанта ошибок \_ \_**
</dt> <dd> <dl> <dt>

587 (0x24B)
</dt> <dt>



Предпринята попытка получить мутант, чтобы было превышено его максимальное число.


</dt> </dl> </dd> <dt>

<span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**\_ \_ требуется драйвер FS \_**
</dt> <dd> <dl> <dt>

588 (0x24C)
</dt> <dt>



Доступ к тому, для которого требуется драйвер файловой системы, еще не был загружен.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**Ошибка \_ не \_ может \_ загрузить \_ файл реестра**
</dt> <dd> <dl> <dt>

589 (0x24D)
</dt> <dt>



{Ошибка в файле реестра} Реестр не может загрузить куст (файл):% HS или его журнал или альтернативный вариант. Он поврежден, отсутствует или недоступен для записи.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**Ошибка \_ \_ при присоединении отладки \_**
</dt> <dd> <dl> <dt>

590 (0x24E)
</dt> <dt>



{Непредвиденный сбой в [**дебугактивепроцесс**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} При обработке запроса API **дебугактивепроцесс** произошла непредвиденная ошибка. Вы можете нажать кнопку ОК, чтобы завершить процесс, или кнопку Отмена, чтобы пропустить ошибку.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**Ошибка \_ системного \_ процесса \_ завершена**
</dt> <dd> <dl> <dt>

591 (0x24F)
</dt> <dt>



{Неустранимая системная ошибка} Непредвиденное завершение системного процесса% HS с состоянием 0x% 08x (0x% 08x 0x% 08x). Работа системы завершена.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**данные об ОШИБКАх \_ \_ не \_ приняты**
</dt> <dd> <dl> <dt>

592 (0x250)
</dt> <dt>



{Данные не приняты} Клиенту TDI не удалось справиться с данными, полученными во время индикации.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**Ошибка при возникновении \_ \_ жесткой \_ ошибки VDM**
</dt> <dd> <dl> <dt>

593 (0x251)
</dt> <dt>



В NTVDM произошла несложная ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**Ошибка \_ при \_ отмене \_ истечения срока действия драйвера**
</dt> <dd> <dl> <dt>

594 (0x252)
</dt> <dt>



{Отмена времени ожидания} Драйверу% HS не удалось завершить отмененный запрос ввода-вывода за отведенное время.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**\_несоответствие \_ сообщения об ошибке \_**
</dt> <dd> <dl> <dt>

595 (0x253)
</dt> <dt>



{Несоответствие сообщения ответа} Предпринята попытка ответить на сообщение LPC, но поток, указанный ИДЕНТИФИКАТОРом клиента в сообщении, не ожидал этого сообщения.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**Ошибка \_ потери \_ \_ данных вритебехинд**
</dt> <dd> <dl> <dt>

596 (0x254)
</dt> <dt>



{Сбой отложенной записи} Windows не удалось сохранить все данные для файла% HS. Данные потеряны. Эта ошибка может быть вызвана сбоем оборудования или сетевого подключения компьютера. Попробуйте сохранить этот файл в другой части.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**Ошибка \_ \_ \_ \_ недопустимых параметров сервера клиента**
</dt> <dd> <dl> <dt>

597 (0x255)
</dt> <dt>



На сервер в окне общей памяти клиента или сервера переданы недопустимые параметры. В окне общей памяти может быть помещено слишком много данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**Ошибка \_ не является \_ крошечным \_ потоком**
</dt> <dd> <dl> <dt>

598 (0x256)
</dt> <dt>



Поток не является немаленькими потоком.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**\_ \_ Чтение переполнения СТЕКа ошибок \_**
</dt> <dd> <dl> <dt>

599 (0x257)
</dt> <dt>



Запрос должен обрабатываться кодом переполнения стека.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**Ошибка \_ преобразования \_ в \_ крупный**
</dt> <dd> <dl> <dt>

600 (0x258)
</dt> <dt>



Внутренние коды состояний OFS, указывающие, как обрабатывается операция выделения. Либо предпринимается повторная попытка после перемещения содержащего оноде, либо поток экстента преобразуется в большой поток.


</dt> </dl> </dd> <dt>

<span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**\_обнаружена \_ Ошибка \_ вне \_ области**
</dt> <dd> <dl> <dt>

601 (0x259)
</dt> <dt>



При попытке найти объект найден объект, совпадающий по ИДЕНТИФИКАТОРу на томе, но он выходит за пределы области действия маркера, используемого для операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**Ошибка при \_ выделении \_ контейнера**
</dt> <dd> <dl> <dt>

602 (0x25A)
</dt> <dt>



Массив контейнеров должен быть увеличен. Повторите транзакцию после этого.


</dt> </dl> </dd> <dt>

<span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**Ошибка \_ Маршалловы о \_ переполнении**
</dt> <dd> <dl> <dt>

603 (0x25B)
</dt> <dt>



Переполнение буфера упаковки пользователя или ядра.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**Ошибка \_ недопустимого \_ варианта**
</dt> <dd> <dl> <dt>

604 (0x25C)
</dt> <dt>



Указанная структура Variant содержит недопустимые данные.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**Ошибка \_ неправильного \_ \_ буфера сжатия**
</dt> <dd> <dl> <dt>

605 (0x25D)
</dt> <dt>



Указанный буфер содержит некорректные данные.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**Ошибка \_ при аудите ошибок \_**
</dt> <dd> <dl> <dt>

606 (0x25E)
</dt> <dt>



{Сбой аудита} Сбой при создании аудита безопасности.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**\_ \_ \_ не \_ задано разрешение таймера ошибок**
</dt> <dd> <dl> <dt>

607 (0x25F)
</dt> <dt>



Разрешение таймера не было ранее задано текущим процессом.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**Ошибка при \_ нехватке \_ сведений для входа \_**
</dt> <dd> <dl> <dt>

608 (0x260)
</dt> <dt>



Недостаточно сведений об учетной записи для входа в систему.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**Ошибка- \_ неправильная \_ \_ точка входа DLL**
</dt> <dd> <dl> <dt>

609 (0x261)
</dt> <dt>



{Недопустимая точка входа DLL} Библиотека динамической компоновки% HS записана неправильно. Указатель стека остался в непротиворечивом состоянии. Точка входа должна быть объявлена как WINAPI или STDCALL. Выберите Да, чтобы не загружать DLL. Выберите Нет, чтобы продолжить выполнение. Выбор параметра нет может привести к неправильной работе приложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**Ошибка \_ ошибочной \_ \_ точки входа службы**
</dt> <dd> <dl> <dt>

610 (0x262)
</dt> <dt>



{Недопустимая точка входа обратного вызова службы} Служба% HS записана неправильно. Указатель стека остался в непротиворечивом состоянии. Точка входа обратного вызова должна быть объявлена как WINAPI или STDCALL. При нажатии кнопки "ОК" служба будет продолжать работу. Однако процесс службы может выполняться неправильно.


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**Ошибка \_ IP- \_ адреса \_ CONFLICT1**
</dt> <dd> <dl> <dt>

611 (0x263)
</dt> <dt>



IP-адрес конфликтует с другой системой в сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**Ошибка \_ IP- \_ адреса \_ CONFLICT2**
</dt> <dd> <dl> <dt>

612 (0x264)
</dt> <dt>



IP-адрес конфликтует с другой системой в сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**\_ \_ ограничение квоты для реестра с ошибками \_**
</dt> <dd> <dl> <dt>

613 (0x265)
</dt> <dt>



{Недостаточно свободного пространства в реестре} Система достигла максимального размера, допустимого для системной части реестра. Дополнительные запросы к хранилищу будут игнорироваться.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**Ошибка при \_ отсутствии \_ активного обратного вызова \_**
</dt> <dd> <dl> <dt>

614 (0x266)
</dt> <dt>



Если обратный вызов не активен, то системная служба возврата обратного вызова не может быть выполнена.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**Ошибка \_ PWD \_ слишком \_ короткий**
</dt> <dd> <dl> <dt>

615 (0x267)
</dt> <dt>



Предоставленный пароль слишком короткий для соответствия политике учетной записи пользователя. Выберите более длинный пароль.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**\_недавняя ошибка PWD \_ \_**
</dt> <dd> <dl> <dt>

616 (0x268)
</dt> <dt>



Политика учетной записи пользователя не позволяет изменять пароли слишком часто. Это делается для того, чтобы предотвратить переход пользователей на знакомый, но потенциально обнаруженный пароль. Если вы считаете, что ваш пароль был скомпрометирован, немедленно обратитесь к администратору, чтобы назначить новый.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**Ошибка \_ при \_ \_ конфликте журнала PWD**
</dt> <dd> <dl> <dt>

617 (0x269)
</dt> <dt>



Вы попытались изменить пароль на тот, который использовался в прошлом. Это не разрешено политикой учетной записи пользователя. Выберите пароль, который ранее не использовался.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**Ошибка \_ НЕподдерживаемого \_ сжатия**
</dt> <dd> <dl> <dt>

618 (0x26A)
</dt> <dt>



Указанный формат сжатия не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**Ошибка \_ недопустимого \_ \_ профиля оборудования**
</dt> <dd> <dl> <dt>

619 (0x26B)
</dt> <dt>



Указана недопустимая конфигурация профиля оборудования.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**Ошибка \_ недопустимого \_ \_ \_ пути к устройству плугплай**
</dt> <dd> <dl> <dt>

620 (0x26C)
</dt> <dt>



Указан недопустимый путь к устройству реестра самонастраивающийся.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**список квот на ошибки не \_ \_ \_ согласуется**
</dt> <dd> <dl> <dt>

621 (0x26D)
</dt> <dt>



Указанный список квот внутренне не соответствует его дескриптору.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**\_ \_ срок действия оценки ошибки**
</dt> <dd> <dl> <dt>

622 (0x26E)
</dt> <dt>



{Уведомление Windows Evaluation} Период ознакомительного использования Windows истек. Эта система завершит работу через 1 час. Чтобы восстановить доступ к этой установке Windows, обновите эту установку с помощью лицензированного дистрибутива этого продукта.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**Ошибка \_ недопустимого \_ \_ перемещения DLL**
</dt> <dd> <dl> <dt>

623 (0x26F)
</dt> <dt>



{Недопустимое перемещение системной библиотеки DLL} Системная библиотека DLL% HS была перемещена в память. Приложение не будет работать должным образом. Перемещение произошло, так как библиотека DLL% HS занята диапазоном адресов, зарезервированным для системных библиотек Windows. Поставщик, предоставляющий библиотеку DLL, должен быть обращен к новой библиотеке DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**Ошибка \_ \_ инициализации DLL \_ при неудачном \_ выходе**
</dt> <dd> <dl> <dt>

624 (0x270)
</dt> <dt>



{Ошибка при инициализации DLL} Не удалось инициализировать приложение, так как работа станции Windows завершается.


</dt> </dl> </dd> <dt>

<span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**Ошибка при \_ проверке \_ продолжения**
</dt> <dd> <dl> <dt>

625 (0x271)
</dt> <dt>



Процесс проверки должен перейти к следующему шагу.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**Ошибка \_ больше не найдено \_ \_**
</dt> <dd> <dl> <dt>

626 (0x272)
</dt> <dt>



Больше нет соответствий для текущего перечисления индекса.


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**\_конфликт списка диапазонов ошибок \_ \_**
</dt> <dd> <dl> <dt>

627 (0x273)
</dt> <dt>



Не удалось добавить диапазон в список диапазонов из-за конфликта.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**\_несоответствие \_ идентификатора безопасности сервера ошибок \_**
</dt> <dd> <dl> <dt>

628 (0x274)
</dt> <dt>



Серверный процесс выполняется с идентификатором безопасности, отличным от того, который требуется клиенту.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**Ошибка \_ не \_ удается \_ включить \_ только Deny**
</dt> <dd> <dl> <dt>

629 (0x275)
</dt> <dt>



Группа, помеченная как "использовать только для запрета", не может быть включена.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ОШИБКА с \_ плавающей запятой \_ нескольких \_ ошибок**
</dt> <dd> <dl> <dt>

630 (0x276)
</dt> <dt>



ОБ Множественные ошибки с плавающей запятой.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ОШИБКА с \_ плавающей запятой \_ множественная \_ ловушка**
</dt> <dd> <dl> <dt>

631 (0x277)
</dt> <dt>



ОБ Несколько ловушек с плавающей точкой.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**Ошибка \_ НЕинтерфейса**
</dt> <dd> <dl> <dt>

632 (0x278)
</dt> <dt>



Запрошенный интерфейс не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**\_сбой драйвера ошибки в \_ \_ спящем режиме**
</dt> <dd> <dl> <dt>

633 (0x279)
</dt> <dt>



{Сбой системы в ждущем режиме} Драйвер% HS не поддерживает режим ожидания. Обновление этого драйвера может привести к переходу системы в режим ожидания.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**Ошибка при \_ повреждении \_ системного \_ файла**
</dt> <dd> <dl> <dt>

634 (0x27A)
</dt> <dt>



Системный файл %1 оказался поврежденным и был заменен.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**\_минимум обязательств по ошибкам \_**
</dt> <dd> <dl> <dt>

635 (0x27B)
</dt> <dt>



{Слишком низкая виртуальная память} В системе недостаточно виртуальной памяти. Windows увеличивает размер файла подкачки виртуальной памяти. Во время этого процесса запросы памяти для некоторых приложений могут быть отклонены. Дополнительные сведения см. в справке.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**Ошибка \_ при \_ перечислении PnP при перезапуске \_**
</dt> <dd> <dl> <dt>

636 (0x27C)
</dt> <dt>



Устройство было удалено, поэтому перечисление необходимо перезапустить.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**\_ \_ \_ Неправильная подпись системного образа ошибки \_**
</dt> <dd> <dl> <dt>

637 (0x27D)
</dt> <dt>



{Неустранимая системная ошибка} Образ системы% s не подписан должным образом. Файл был заменен подписанным файлом. Работа системы завершена.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**Ошибка \_ при \_ перезагрузке PnP \_**
</dt> <dd> <dl> <dt>

638 (0x27E)
</dt> <dt>



Устройство не будет запущено без перезагрузки.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**Ошибка " \_ недостаточно \_ энергии"**
</dt> <dd> <dl> <dt>

639 (0x27F)
</dt> <dt>



Недостаточно энергии для завершения запрошенной операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**Ошибка \_ множественного \_ \_ нарушения сбоя**
</dt> <dd> <dl> <dt>

640 (0x280)
</dt> <dt>



Ошибка \_ множественного \_ \_ нарушения сбоя


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**Ошибка \_ при \_ завершении работы системы**
</dt> <dd> <dl> <dt>

641 (0x281)
</dt> <dt>



Система находится в процессе завершения работы.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**\_порт ошибки \_ не \_ задан**
</dt> <dd> <dl> <dt>

642 (0x282)
</dt> <dt>



Выполнена попытка удаления процессов Дебугпорт, но порт не был связан с процессом.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**Ошибка \_ \_ \_ при проверке версии \_ DS**
</dt> <dd> <dl> <dt>

643 (0x283)
</dt> <dt>



Эта версия Windows несовместима с версией поведения леса каталога, домена или контроллера домена.


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**\_диапазон ошибок \_ не \_ найден**
</dt> <dd> <dl> <dt>

644 (0x284)
</dt> <dt>



Указанный диапазон не найден в списке диапазонов.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**Ошибка \_ \_ незащищенного \_ режима \_ драйвера**
</dt> <dd> <dl> <dt>

646 (0x286)
</dt> <dt>



Драйвер не был загружен, так как система загружается в безопасный режим.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**Ошибка \_ при ошибке \_ \_ записи драйвера**
</dt> <dd> <dl> <dt>

647 (0x287)
</dt> <dt>



Драйвер не был загружен из-за сбоя вызова инициализации.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**Ошибка \_ \_ перечисления устройств \_**
</dt> <dd> <dl> <dt>

648 (0x288)
</dt> <dt>



"% HS" обнаружил ошибку при применении питания или чтении конфигурации устройства. Это может быть вызвано сбоем оборудования или неудачным подключением.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**\_точка подключения \_ ошибок \_ не \_ разрешена**
</dt> <dd> <dl> <dt>

649 (0x289)
</dt> <dt>



Не удалось выполнить операцию создания, так как имя содержит по крайней мере одну точку подключения, которая разрешается в том, к которому не присоединен указанный объект устройства.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**Ошибка \_ недопустимого \_ \_ параметра объекта устройства \_**
</dt> <dd> <dl> <dt>

650 (0x28A)
</dt> <dt>



Параметр объекта устройства либо не является допустимым объектом устройства, либо не подключен к тому, указанному в имени файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**произошла ошибка \_ MCA \_**
</dt> <dd> <dl> <dt>

651 (0x28B)
</dt> <dt>



Произошла ошибка проверки компьютера. Дополнительные сведения см. в системном журнале событий.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**Ошибка \_ \_ базы данных драйвера ошибки \_**
</dt> <dd> <dl> <dt>

652 (0x28C)
</dt> <dt>



Произошла ошибка \[ %2 при \] обработке базы данных драйвера.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**\_ \_ \_ слишком большой системный куст \_ ошибки**
</dt> <dd> <dl> <dt>

653 (0x28D)
</dt> <dt>



Размер системного куста превысил установленный предел.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**Ошибка \_ драйвера \_ ошибки \_ предыдущей \_ выгрузки**
</dt> <dd> <dl> <dt>

654 (0x28E)
</dt> <dt>



Не удалось загрузить драйвер, поскольку предыдущая версия драйвера по-прежнему находится в памяти.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**Ошибка \_ VOLSNAP \_ Подготовка \_ гибернации**
</dt> <dd> <dl> <dt>

655 (0x28F)
</dt> <dt>



{Служба теневого копирования томов} Дождитесь, пока служба теневого копирования томов подготовит том% HS для спящего режима.


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**Ошибка при переходе в \_ спящий режим \_**
</dt> <dd> <dl> <dt>

656 (0x290)
</dt> <dt>



Системе не удалось перейти в режим гибернации (код ошибки% HS). Режим гибернации будет отключен до перезапуска системы.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**Ошибка \_ PWD \_ слишком \_ длинный**
</dt> <dd> <dl> <dt>

657 (0x291)
</dt> <dt>



Предоставленный пароль слишком длинный для соответствия политике учетной записи пользователя. Выберите более короткий пароль.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**Ошибка \_ \_ ограничения файловой системы \_**
</dt> <dd> <dl> <dt>

665 (0x299)
</dt> <dt>



Запрошенная операция не может быть завершена из-за ограничения файловой системы.


</dt> </dl> </dd> <dt>

<span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**Ошибка \_ утверждения ошибки \_**
</dt> <dd> <dl> <dt>

668 (0x29C)
</dt> <dt>



Произошла ошибка утверждения.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**Ошибка \_ ACPI \_**
</dt> <dd> <dl> <dt>

669 (0x29D)
</dt> <dt>



В подсистеме ACPI произошла ошибка.


</dt> </dl> </dd> <dt>

<span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**\_утверждение ошибки WOW \_**
</dt> <dd> <dl> <dt>

670 (0x29E)
</dt> <dt>



Ошибка утверждения WOW.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**Ошибка \_ PnP — \_ неправильная \_ \_ Таблица MPS**
</dt> <dd> <dl> <dt>

671 (0x29F)
</dt> <dt>



В таблице MPS системного BIOS отсутствует устройство. Это устройство не будет использоваться. Обратитесь к поставщику системы за обновлением BIOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**Ошибка \_ \_ перевода PnP \_ при ошибке**
</dt> <dd> <dl> <dt>

672 (0x2A0)
</dt> <dt>



Транслятору не удалось перевести ресурсы.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**Ошибка \_ \_ \_ при преобразовании PnP IRQ \_**
</dt> <dd> <dl> <dt>

673 (0x2A1)
</dt> <dt>



Транслятору IRQ не удалось перевести ресурсы.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**Ошибка \_ \_ Недопустимый \_ идентификатор PNP**
</dt> <dd> <dl> <dt>

674 (0x2A2)
</dt> <dt>



Драйвер %2 вернул недопустимый идентификатор для дочернего устройства (%3).


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**Ошибка \_ \_ отладчика системы пробуждения \_**
</dt> <dd> <dl> <dt>

675 (0x2A3)
</dt> <dt>



{Запущен отладчик ядра}. Системный отладчик был вызван прерыванием.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**\_дескрипторы ошибок \_ закрыты**
</dt> <dd> <dl> <dt>

676 (0x2A4)
</dt> <dt>



{Handles Closed} Дескрипторы объектов были автоматически закрыты в результате выполнения запрошенной операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**Ошибка при возникновении \_ лишних \_ сведений**
</dt> <dd> <dl> <dt>

677 (0x2A5)
</dt> <dt>



{Слишком много сведений} Указанный список управления доступом (ACL) содержит больше сведений, чем ожидалось.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**Ошибка \_ рксакт, \_ необходимая для фиксации \_**
</dt> <dd> <dl> <dt>

678 (0x2A6)
</dt> <dt>



Это состояние предупреждения указывает на то, что состояние транзакции уже существует для поддерева реестра, но фиксация транзакции была ранее прервана. Фиксация не выполнена, но откат не выполнен (поэтому при необходимости его можно зафиксировать).


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**\_Проверка носителя с ошибками \_**
</dt> <dd> <dl> <dt>

679 (0x2A7)
</dt> <dt>



{Носитель изменен} Возможно, носитель был изменен.


</dt> </dl> </dd> <dt>

<span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**\_ \_ выполнена подстановка GUID ошибки \_**
</dt> <dd> <dl> <dt>

680 (0x2A8)
</dt> <dt>



{Подстановка GUID} Во время преобразования глобального идентификатора (GUID) в идентификатор безопасности Windows (SID) не найден префикс GUID, определенный администратором. Использовался заменяющий префикс, который не повлечет за собой нарушение безопасности системы. Однако это может обеспечить более четкий доступ, чем планировалось.


</dt> </dl> </dd> <dt>

<span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**Ошибка \_ остановлена \_ в \_ символьную ссылку**
</dt> <dd> <dl> <dt>

681 (0x2A9)
</dt> <dt>



Операция создания остановлена после достижения символьной ссылки.


</dt> </dl> </dd> <dt>

<span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**Ошибка \_ лонгжумп**
</dt> <dd> <dl> <dt>

682 (0x2AA)
</dt> <dt>



Выполнен длинный переход.


</dt> </dl> </dd> <dt>

<span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**Ошибка \_ плугплай \_ запрос \_**
</dt> <dd> <dl> <dt>

683 (0x2AB)
</dt> <dt>



Операция запроса самонастраивающийся не выполнена.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**Ошибка \_ очистки \_ консолидации**
</dt> <dd> <dl> <dt>

684 (0x2AC)
</dt> <dt>



Выполнена консолидация кадров.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**\_ \_ восстановлен КУСТ реестра \_ ошибок**
</dt> <dd> <dl> <dt>

685 (0x2AD)
</dt> <dt>



{Восстановленный куст реестра} Куст реестра (файл):% HS поврежден и восстановлен. Некоторые данные могли быть потеряны.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**\_DLL-библиотека ошибок \_ может \_ быть \_ небезопасной**
</dt> <dd> <dl> <dt>

686 (0x2AE)
</dt> <dt>



Приложение пытается запустить исполняемый код из модуля% HS. Это может быть небезопасным. Доступен альтернативный вариант,% HS. Должно ли приложение использовать защищенный модуль% HS?


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**\_DLL-библиотека ошибок \_ может \_ быть \_ несовместима**
</dt> <dd> <dl> <dt>

687 (0x2AF)
</dt> <dt>



Приложение загружает исполняемый код из модуля% HS. Это безопасно, но может быть несовместимо с предыдущими выпусками операционной системы. Доступен альтернативный вариант,% HS. Должно ли приложение использовать защищенный модуль% HS?


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**Ошибка \_ DBG, \_ исключение \_ не \_ обработано**
</dt> <dd> <dl> <dt>

688 (0x2B0)
</dt> <dt>



Отладчик не обработал исключение.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**Ошибка \_ \_ ответа dbg \_ позже**
</dt> <dd> <dl> <dt>

689 (0x2B1)
</dt> <dt>



Отладчик ответит позже.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**Ошибка \_ dbg \_ не \_ удалось \_ предоставить \_ обработчик**
</dt> <dd> <dl> <dt>

690 (0x2B2)
</dt> <dt>



Отладчик не может предоставить Handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**Ошибка \_ \_ прерывания \_ потока dbg**
</dt> <dd> <dl> <dt>

691 (0x2B3)
</dt> <dt>



Отладчик завершил поток.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**Ошибка \_ \_ завершения \_ процесса dbg**
</dt> <dd> <dl> <dt>

692 (0x2B4)
</dt> <dt>



Отладчик завершил процесс.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**Ошибка \_ \_ элемента управления dbg \_ C**
</dt> <dd> <dl> <dt>

693 (0x2B5)
</dt> <dt>



Отладчик получил управление C.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**Ошибка \_ dbg \_ PRINTEXCEPTION \_ C**
</dt> <dd> <dl> <dt>

694 (0x2B6)
</dt> <dt>



Отладчик выпечатал исключение для элемента управления C.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**Ошибка \_ dbg \_ рипексцептион**
</dt> <dd> <dl> <dt>

695 (0x2B7)
</dt> <dt>



Отладчик получил исключение RIP.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**Ошибка \_ при \_ разрыве элемента управления dbg \_**
</dt> <dd> <dl> <dt>

696 (0x2B8)
</dt> <dt>



Отладчик получил прерывание управления.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**Ошибка \_ при \_ \_ возникновении команды dbg**
</dt> <dd> <dl> <dt>

697 (0x2B9)
</dt> <dt>



Исключение при обмене данными команды отладчика.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**\_имя объекта \_ ошибки \_ существует**
</dt> <dd> <dl> <dt>

698 (0x2BA)
</dt> <dt>



{Объект существует} Предпринята попытка создать объект, и уже существовало имя объекта.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**\_поток ошибок \_ был \_ приостановлен**
</dt> <dd> <dl> <dt>

699 (0x2BB)
</dt> <dt>



{Поток приостановлен} Прерывание потока произошло во время приостановки потока. Поток возобновлен, и завершение завершено.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**\_изображение ошибки \_ не \_ в \_ базовом**
</dt> <dd> <dl> <dt>

700 (0x2BC)
</dt> <dt>



{Перемещается образ} Не удалось сопоставить файл изображения по адресу, указанному в файле изображения. На этом образе должны быть выполнены локальные исправления.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**Ошибка \_ при \_ создании состояния рксакт \_**
</dt> <dd> <dl> <dt>

701 (0x2BD)
</dt> <dt>



Это состояние информационного уровня указывает на то, что указанное состояние транзакции поддерева реестра еще не существует и его пришлось создавать.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**\_уведомление о сегменте ошибки \_**
</dt> <dd> <dl> <dt>

702 (0x2BE)
</dt> <dt>



{Загрузка сегмента} Виртуальная машина DOS (VDM) загружает, выгружает или перемещает образ сегмента программы MS-DOS или Win16. Исключение вызывается, чтобы отладчик мог загружать, выгружать или отлаживать символы и точки останова в этих 16-битных сегментах.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**Ошибка при \_ неправильном \_ текущем \_ каталоге**
</dt> <dd> <dl> <dt>

703 (0x2BF)
</dt> <dt>



{Недопустимый текущий каталог} Процесс не может переключиться на текущий каталог запуска% HS. Нажмите кнопку ОК, чтобы присвоить текущему каталогу значение% HS, или нажмите кнопку Отмена для выхода.


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**Ошибка \_ \_ чтения ft \_ Read \_ из \_ резервной копии**
</dt> <dd> <dl> <dt>

704 (0x2C0)
</dt> <dt>



{Избыточное чтение} Чтобы удовлетворить запрос на чтение, отказоустойчивая файловая система NT успешно прочитала запрошенные данные из избыточной копии. Это было сделано из-за сбоя файловой системы на члене отказоустойчивого тома, но ему не удалось переназначить неисправный участок устройства.


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**Ошибка \_ при \_ \_ восстановлении записи ft**
</dt> <dd> <dl> <dt>

705 (0x2C1)
</dt> <dt>



{Избыточная запись} Для удовлетворения запроса на запись отказоустойчивая файловая система NT успешно написала избыточную копию информации. Это было сделано из-за того, что в файловой системе произошла ошибка на члене отказоустойчивого тома, но ему не удалось переназначить неисправный участок устройства.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**\_несоответствие \_ типов компьютеров с ИЗОБРАЖЕНИЕм ошибки \_ \_**
</dt> <dd> <dl> <dt>

706 (0x2C2)
</dt> <dt>



{Несоответствие типа компьютера} Файл образа% HS допустим, но относится к типу компьютера, отличного от текущего компьютера. Нажмите кнопку ОК, чтобы продолжить, или кнопку Отмена, чтобы завершить загрузку библиотеки DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**Ошибка при \_ получении \_ части**
</dt> <dd> <dl> <dt>

707 (0x2C3)
</dt> <dt>



{Получено частичных данных} Сетевой транспорт вернул частичные данные клиенту. Остальные данные будут отправлены позже.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**сообщение об ОШИБКе \_ Отправлено \_**
</dt> <dd> <dl> <dt>

708 (0x2C4)
</dt> <dt>



{Получено срочных данных} Сетевой транспорт вернул данные клиенту, который был помечен как отправленный удаленной системой.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**Ошибка при \_ получении частично отправленного сообщения \_ \_**
</dt> <dd> <dl> <dt>

709 (0x2C5)
</dt> <dt>



{Получено частично отправленных данных} Сетевой транспорт вернул частичные данные клиенту, и эти данные были помечены удаленной системой как отправленные. Остальные данные будут отправлены позже.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**\_событие ошибки \_ выполнено**
</dt> <dd> <dl> <dt>

710 (0x2C6)
</dt> <dt>



{Событие TDI завершено} Индикатор TDI успешно завершил работу.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**\_ \_ ожидание события ошибки**
</dt> <dd> <dl> <dt>

711 (0x2C7)
</dt> <dt>



{Ожидается событие TDI} Индикатор TDI перешел в состояние ожидания.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**Ошибка при \_ проверке \_ файловой \_ системы**
</dt> <dd> <dl> <dt>

712 (0x2C8)
</dt> <dt>



Проверка файловой системы на% wZ.


</dt> </dl> </dd> <dt>

<span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**Ошибка при \_ неустранимом \_ \_ выходе из приложения**
</dt> <dd> <dl> <dt>

713 (0x2C9)
</dt> <dt>



{Неустранимый выход из приложения}% HS.


</dt> </dl> </dd> <dt>

<span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**Ошибка \_ предопределенного \_ маркера**
</dt> <dd> <dl> <dt>

714 (0x2CA)
</dt> <dt>



На указанный раздел реестра ссылается Стандартный маркер.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**Ошибка \_ была \_ разблокирована**
</dt> <dd> <dl> <dt>

715 (0x2CB)
</dt> <dt>



{Страница разблокирована} Защита страницы заблокированной страницы изменена на "нет доступа", и страница была разблокирована из памяти и из процесса.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**\_Уведомление службы \_ ошибок**
</dt> <dd> <dl> <dt>

716 (0x2CC)
</dt> <dt>



% HS


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**Ошибка \_ \_ заблокирована**
</dt> <dd> <dl> <dt>

717 (0x2CD)
</dt> <dt>



{Страница заблокирована} Одна из страниц для блокировки уже заблокирована.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**Ошибка \_ журнала \_ ошибок \_**
</dt> <dd> <dl> <dt>

718 (0x2CE)
</dt> <dt>



Всплывающее окно приложения: %1: %2


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**Ошибка \_ уже \_ Win32**
</dt> <dd> <dl> <dt>

719 (0x2CF)
</dt> <dt>



Ошибка \_ уже \_ Win32


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**\_несоответствие типов компьютеров с изображением ошибки \_ \_ \_ \_ exe**
</dt> <dd> <dl> <dt>

720 (0x2D0)
</dt> <dt>



{Несоответствие типа компьютера} Файл образа% HS допустим, но относится к типу компьютера, отличного от текущего компьютера.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**Ошибка \_ не \_ \_ выполнен**
</dt> <dd> <dl> <dt>

721 (0x2D1)
</dt> <dt>



Выполнен оператор yield, и нет доступных потоков для выполнения.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**\_возобновление таймера ошибок \_ \_ проигнорировано**
</dt> <dd> <dl> <dt>

722 (0x2D2)
</dt> <dt>



Флаг возобновляемости для API таймера проигнорирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**\_НЕобработанное арбитраж ошибок \_**
</dt> <dd> <dl> <dt>

723 (0x2D3)
</dt> <dt>



Арбитр имеет отложенное разрешение на эти ресурсы родительскому элементу.


</dt> </dl> </dd> <dt>

<span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**Ошибка \_ CARDBUS \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

724 (0x2D4)
</dt> <dt>



Не удается запустить вставленное устройство CardBus из-за ошибки конфигурации в "% HS".


</dt> </dl> </dd> <dt>

<span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии процессора MP**
</dt> <dd> <dl> <dt>

725 (0x2D5)
</dt> <dt>



Процессоры в этой многопроцессорной системе имеют разные уровни редакции. Чтобы использовать все процессоры, операционная система ограничена функциями минимально производительного процессора в системе. При возникновении проблем с этой системой обратитесь к производителю ЦП, чтобы узнать, поддерживается ли этот сочетание процессоров.


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**Ошибка в \_ режиме гибернации**
</dt> <dd> <dl> <dt>

726 (0x2D6)
</dt> <dt>



Система переведена в режим гибернации.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**Ошибка \_ возобновления \_ режима гибернации**
</dt> <dd> <dl> <dt>

727 (0x2D7)
</dt> <dt>



Система была восстановлена из режима гибернации.


</dt> </dl> </dd> <dt>

<span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**\_встроенное по ошибки \_ Обновлено**
</dt> <dd> <dl> <dt>

728 (0x2D8)
</dt> <dt>



Windows обнаружила, что системное встроенное по (BIOS) обновило \[ предыдущую дату встроенного по (%2, текущая дата встроенного по "%3") \] .


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**драйверы с ОШИБКАми \_ \_ утечка \_ заблокированных \_ страниц**
</dt> <dd> <dl> <dt>

729 (0x2D9)
</dt> <dt>



Драйвер устройства вызывает утечку заблокированных страниц ввода-вывода, что приводит к снижению производительности системы. Система автоматически включила код отслеживания, чтобы попытаться обнаружить причину.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**\_Система пробуждения с ошибкой \_**
</dt> <dd> <dl> <dt>

730 (0x2DA)
</dt> <dt>



Система имеет пробудится.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**\_Ожидание ошибки \_ 1**
</dt> <dd> <dl> <dt>

731 (0x2DB)
</dt> <dt>



\_Ожидание ошибки \_ 1


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**\_Ожидание ошибки \_ 2**
</dt> <dd> <dl> <dt>

732 (0x2DC)
</dt> <dt>



\_Ожидание ошибки \_ 2


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**Ошибка \_ ожидания \_ 3**
</dt> <dd> <dl> <dt>

733 (0x2DD)
</dt> <dt>



Ошибка \_ ожидания \_ 3


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**Ошибка \_ ожидания \_ 63**
</dt> <dd> <dl> <dt>

734 (0x2DE)
</dt> <dt>



Ошибка \_ ожидания \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**Ошибка \_ прекращения \_ ожидания \_ 0**
</dt> <dd> <dl> <dt>

735 (0x2DF)
</dt> <dt>



Ошибка \_ прекращения \_ ожидания \_ 0


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**Ошибка \_ прекращения \_ ожидания \_ 63**
</dt> <dd> <dl> <dt>

736 (0x2E0)
</dt> <dt>



Ошибка \_ прекращения \_ ожидания \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**Ошибка \_ пользователь \_ APC**
</dt> <dd> <dl> <dt>

737 (0x2E1)
</dt> <dt>



Ошибка \_ пользователь \_ APC


</dt> </dl> </dd> <dt>

<span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**Ошибка при \_ ядре \_ APC**
</dt> <dd> <dl> <dt>

738 (0x2E2)
</dt> <dt>



Ошибка при \_ ядре \_ APC


</dt> </dl> </dd> <dt>

<span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**предупреждение об ОШИБКе \_**
</dt> <dd> <dl> <dt>

739 (0x2E3)
</dt> <dt>



предупреждение об ОШИБКе \_


</dt> </dl> </dd> <dt>

<span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**\_требуется повышение уровня ошибки \_**
</dt> <dd> <dl> <dt>

740 (0x2E4)
</dt> <dt>



Запрошенная операция требует повышения прав.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**Ошибка \_ при повторном анализе**
</dt> <dd> <dl> <dt>

741 (0x2E5)
</dt> <dt>



Диспетчер объектов должен выполнить повторное синтаксический анализ, так как имя файла привело к созданию символьной ссылки.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**Ошибка \_ OPLOCK \_ break \_ \_**
</dt> <dd> <dl> <dt>

742 (0x2E6)
</dt> <dt>



Операция открытия или создания завершена во время разрыва оппортунистической блокировки.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**Ошибка \_ \_ подключения тома**
</dt> <dd> <dl> <dt>

743 (0x2E7)
</dt> <dt>



Файловая система подключила новый том.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**Ошибка \_ рксакт \_ COMMITTED**
</dt> <dd> <dl> <dt>

744 (0x2E8)
</dt> <dt>



Это состояние успешного выполнения указывает, что состояние транзакции уже существует для поддерева реестра, но фиксация транзакции была ранее прервана. Фиксация завершена.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**\_Очистка уведомления об ошибке \_**
</dt> <dd> <dl> <dt>

745 (0x2E9)
</dt> <dt>



Это означает, что запрос на уведомление об изменении был завершен из-за закрытия маркера, который сделал запрос на уведомление об изменении.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**Ошибка \_ основного \_ транспортного \_ подключения \_ не удалось**
</dt> <dd> <dl> <dt>

746 (0x2EA)
</dt> <dt>



{Сбой подключения к основному транспорту} Предпринята попытка подключения к удаленному серверу% HS на основном транспорте, но подключение не выполнено. Компьютер смог подключиться к дополнительному транспорту.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**\_Переход на \_ сбой \_ страницы ошибок**
</dt> <dd> <dl> <dt>

747 (0x2EB)
</dt> <dt>



Ошибка страницы была вызвана ошибкой перехода.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**\_ \_ \_ нулевое требование к ошибке страницы \_**
</dt> <dd> <dl> <dt>

748 (0x2EC)
</dt> <dt>



Ошибка страницы была вызвана нулевой ошибкой спроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**Ошибка \_ \_ \_ при копировании ошибки страницы \_ при \_ записи**
</dt> <dd> <dl> <dt>

749 (0x2ED)
</dt> <dt>



Ошибка страницы была вызвана нулевой ошибкой спроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**\_Страница " \_ сбой страницы \_ защиты \_ страниц ошибок"**
</dt> <dd> <dl> <dt>

750 (0x2EE)
</dt> <dt>



Ошибка страницы была вызвана нулевой ошибкой спроса.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**\_ \_ \_ файл подкачки ошибки страницы ошибок \_**
</dt> <dd> <dl> <dt>

751 (0x2EF)
</dt> <dt>



Ошибка страницы была удовлетворена считыванием данных с дополнительного устройства хранения.


</dt> </dl> </dd> <dt>

<span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**\_ \_ Блокировка страницы кэша \_ ошибок**
</dt> <dd> <dl> <dt>

752 (0x2F0)
</dt> <dt>



Кэшированная страница заблокирована во время операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**аварийный \_ \_ дамп ошибок**
</dt> <dd> <dl> <dt>

753 (0x2F1)
</dt> <dt>



Аварийный дамп существует в файле подкачки.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**\_буферы ошибок \_ все \_ нули**
</dt> <dd> <dl> <dt>

754 (0x2F2)
</dt> <dt>



Указанный буфер содержит все нули.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**Ошибка \_ при повторном анализе \_ объекта**
</dt> <dd> <dl> <dt>

755 (0x2F3)
</dt> <dt>



Диспетчер объектов должен выполнить повторное синтаксический анализ, так как имя файла привело к созданию символьной ссылки.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**\_ \_ изменились требования к РЕСУРСУ об ошибке \_**
</dt> <dd> <dl> <dt>

756 (0x2F4)
</dt> <dt>



Устройство успешно выполнило запрос на завершение и его требования к ресурсам изменились.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**\_Преобразование ошибок \_ завершено**
</dt> <dd> <dl> <dt>

757 (0x2F5)
</dt> <dt>



Переводчик преобразует эти ресурсы в глобальное пространство, и дальнейшие переводы не выполняются.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**\_нет ошибок \_ для \_ завершения**
</dt> <dd> <dl> <dt>

758 (0x2F6)
</dt> <dt>



Завершение процесса не имеет потоков для завершения.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**Ошибка \_ процесса, \_ не \_ в \_ задании**
</dt> <dd> <dl> <dt>

759 (0x2F7)
</dt> <dt>



Указанный процесс не является частью задания.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**Ошибка \_ процесса \_ в \_ задании**
</dt> <dd> <dl> <dt>

760 (0x2F8)
</dt> <dt>



Указанный процесс является частью задания.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**Ошибка \_ VOLSNAP \_ режим гибернации \_ готов**
</dt> <dd> <dl> <dt>

761 (0x2F9)
</dt> <dt>



{Служба теневого копирования томов} Теперь система готова к переходу в спящий режим.


</dt> </dl> </dd> <dt>

<span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**Ошибка \_ фсфилтер \_ операция \_ \_ успешно завершена**
</dt> <dd> <dl> <dt>

762 (0x2FA)
</dt> <dt>



Файловая система или драйвер фильтра файловой системы успешно завершили операцию Фсфилтер.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**\_вектор прерываний ошибок \_ \_ уже \_ подключен**
</dt> <dd> <dl> <dt>

763 (0x2FB)
</dt> <dt>



Указанный вектор прерывания уже подключен.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**\_прерывание ошибки \_ по-прежнему \_ подключено**
</dt> <dd> <dl> <dt>

764 (0x2FC)
</dt> <dt>



Указанный вектор прерывания все еще подключен.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**Ошибка при \_ ожидании \_ \_ жесткой блокировки**
</dt> <dd> <dl> <dt>

765 (0x2FD)
</dt> <dt>



Операция заблокирована в ожидании нежесткой блокировки.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**Ошибка \_ \_ обработки исключения \_ dbg**
</dt> <dd> <dl> <dt>

766 (0x2FE)
</dt> <dt>



Отладчик обработал исключение.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**Ошибка \_ dbg \_ Continue**
</dt> <dd> <dl> <dt>

767 (0x2FF)
</dt> <dt>



Продолжение работы отладчика.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**\_стек POP обратного вызова ошибки \_ \_**
</dt> <dd> <dl> <dt>

768 (0x300)
</dt> <dt>



В обратном вызове пользовательского режима возникло исключение, и необходимо удалить кадр обратного вызова ядра.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**\_Сжатие ошибок \_ отключено**
</dt> <dd> <dl> <dt>

769 (0x301)
</dt> <dt>



Сжатие для этого тома отключено.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**Ошибка \_ кантфетчбакквардс**
</dt> <dd> <dl> <dt>

770 (0x302)
</dt> <dt>



Поставщик данных не может получить обратно через результирующий набор.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**Ошибка \_ кантскроллбакквардс**
</dt> <dd> <dl> <dt>

771 (0x303)
</dt> <dt>



Поставщик данных не может прокручиваться назад по результирующему набору.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**Ошибка \_ ровснотрелеасед**
</dt> <dd> <dl> <dt>

772 (0x304)
</dt> <dt>



Поставщик данных требует, чтобы ранее выбранные данные были освобождены перед запросом на получение дополнительных данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**Ошибка \_ неверных \_ \_ флагов доступа**
</dt> <dd> <dl> <dt>

773 (0x305)
</dt> <dt>



Поставщику данных не удалось интерпретировать флаги, заданные для привязки столбца в методе доступа.


</dt> </dl> </dd> <dt>

<span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**\_ \_ обнаружены ошибки**
</dt> <dd> <dl> <dt>

774 (0x306)
</dt> <dt>



При обработке запроса произошла одна или несколько ошибок.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**Ошибка \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

775 (0x307)
</dt> <dt>



Реализация не может выполнить запрос.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**запрос об ОШИБКе \_ \_ вне \_ \_ последовательности**
</dt> <dd> <dl> <dt>

776 (0x308)
</dt> <dt>



Клиент компонента запросил операцию, которая не является допустимой для состояния экземпляра компонента.


</dt> </dl> </dd> <dt>

<span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**Ошибка \_ \_ при синтаксическом АНАЛИЗЕ версии ошибки \_**
</dt> <dd> <dl> <dt>

777 (0x309)
</dt> <dt>



Не удалось проанализировать номер версии.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**Ошибка \_ бадстартпоситион**
</dt> <dd> <dl> <dt>

778 (0x30A)
</dt> <dt>



Недопустимая Начальная Расположение итератора.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**\_аппаратная память с ошибками \_**
</dt> <dd> <dl> <dt>

779 (0x30B)
</dt> <dt>



Оборудование сообщило о неисправимой ошибке памяти.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**Ошибка \_ \_ восстановления диска \_ отключена**
</dt> <dd> <dl> <dt>

780 (0x30C)
</dt> <dt>



Запрошенная операция требует, чтобы была включена самовосстановление.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ОШИБКА не \_ хватает \_ ресурсов \_ для \_ указанного \_ общего \_ \_ размера раздела**
</dt> <dd> <dl> <dt>

781 (0x30D)
</dt> <dt>



В куче рабочего стола произошла ошибка при выделении памяти для сеанса. Дополнительные сведения см. в журнале системных событий.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**Переход на нечувствительный к \_ системе ошибка \_ \_**
</dt> <dd> <dl> <dt>

782 (0x30E)
</dt> <dt>



Состояние питания системы переходит с %2 на %3.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**\_ \_ \_ сложный переход от системы \_ с ошибками**
</dt> <dd> <dl> <dt>

783 (0x30F)
</dt> <dt>



Состояние питания системы переходит с %2 на %3, но может ввести %4.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**Ошибка \_ MCA, \_ исключение**
</dt> <dd> <dl> <dt>

784 (0x310)
</dt> <dt>



Поток отправляется с ИСКЛЮЧЕНИЕм MCA из-за MCA.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**Ошибка \_ доступа к \_ аудиту \_ с помощью \_ политики**
</dt> <dd> <dl> <dt>

785 (0x311)
</dt> <dt>



Доступ к %1 отслеживается правилом политики %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**\_доступ к ошибкам \_ \_ не отключен \_ безопасный \_ Пользовательский интерфейс \_ с помощью \_ политики**
</dt> <dd> <dl> <dt>

786 (0x312)
</dt> <dt>



Доступ к %1 ограничен администратором с помощью правила политики %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**Ошибка при отмене \_ \_ хиберфиле**
</dt> <dd> <dl> <dt>

787 (0x313)
</dt> <dt>



Допустимый файл гибернации стал недействительным и должен быть отменен.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**Ошибка при потере связи с \_ \_ вритебехинд \_ данных \_ сети \_**
</dt> <dd> <dl> <dt>

788 (0x314)
</dt> <dt>



{Сбой отложенной записи} Windows не удалось сохранить все данные для файла% HS; данные потеряны. Эта ошибка может быть вызвана проблемами с сетевым подключением. Попробуйте сохранить этот файл в другой части.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**произошла ошибка при \_ утере \_ \_ \_ сетевого \_ сервера данных вритебехинд \_**
</dt> <dd> <dl> <dt>

789 (0x315)
</dt> <dt>



{Сбой отложенной записи} Windows не удалось сохранить все данные для файла% HS; данные потеряны. Эта ошибка была возвращена сервером, на котором существует файл. Попробуйте сохранить этот файл в другой части.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**Ошибка \_ потери \_ \_ данных о \_ локальном \_ диске \_ вритебехинд**
</dt> <dd> <dl> <dt>

790 (0x316)
</dt> <dt>



{Сбой отложенной записи} Windows не удалось сохранить все данные для файла% HS; данные потеряны. Эта ошибка может возникать, если устройство было удалено или носитель защищен от записи.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**Ошибка \_ неправильной \_ \_ таблицы мкфг**
</dt> <dd> <dl> <dt>

791 (0x317)
</dt> <dt>



Ресурсы, необходимые для этого устройства, конфликтуют с таблицей МКФГ.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**Ошибка \_ \_ восстановления диска \_ перенаправлено**
</dt> <dd> <dl> <dt>

792 (0x318)
</dt> <dt>



Не удалось выполнить восстановление тома, пока оно находится в сети. Запланируйте отключение тома в автономном режиме, чтобы его можно было восстановить.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**Ошибка \_ при \_ восстановлении диска \_**
</dt> <dd> <dl> <dt>

793 (0x319)
</dt> <dt>



Восстановление тома не выполнено.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**Ошибка \_ повреждения \_ \_ переполнения журнала**
</dt> <dd> <dl> <dt>

794 (0x31A)
</dt> <dt>



Один из журналов повреждений тома полон. Последующие повреждения, которые могут быть обнаружены, не регистрируются.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**Ошибка \_ поврежденного \_ журнала \_**
</dt> <dd> <dl> <dt>

795 (0x31B)
</dt> <dt>



Один из журналов повреждений тома внутренне поврежден и должен быть создан повторно. Том может содержать необнаруженные повреждения и должен быть проверен.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**Ошибка \_ повреждения \_ журнала \_ недоступен**
</dt> <dd> <dl> <dt>

796 (0x31C)
</dt> <dt>



Один из журналов повреждений тома недоступен для работы.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**Ошибка \_ при \_ \_ полном удалении \_ журнала**
</dt> <dd> <dl> <dt>

797 (0x31D)
</dt> <dt>



Один из журналов повреждений тома был удален, и в нем остались записи о повреждениях. Том содержит обнаруженные повреждения и должен быть проверен.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**Ошибка \_ — \_ Очистка журнала повреждена \_**
</dt> <dd> <dl> <dt>

798 (0x31E)
</dt> <dt>



Один из журналов повреждений тома был удален программой chkdsk и больше не содержит реальных повреждений.


</dt> </dl> </dd> <dt>

<span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**Ошибка \_ потерянного \_ имени \_**
</dt> <dd> <dl> <dt>

799 (0x31F)
</dt> <dt>



Потерянные файлы существуют на томе, но их не удалось восстановить, так как в каталоге восстановления не удалось создать новые имена. Файлы должны быть перемещены из каталога восстановления.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**Ошибка \_ жесткой блокировки при \_ переключении \_ на \_ новый \_ маркер**
</dt> <dd> <dl> <dt>

800 (0x320)
</dt> <dt>



Жесткая блокировка, связанная с этим маркером, теперь связана с другим маркером.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**Ошибка \_ не может \_ предоставить \_ запрошенную \_ нежесткую блокировку**
</dt> <dd> <dl> <dt>

801 (0x321)
</dt> <dt>



Невозможно предоставить нежесткую блокировку запрошенного уровня. Может быть доступна нежесткая блокировка нижнего уровня.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**Ошибка \_ не может привести к \_ нарушению \_ оппортунистической блокировки**
</dt> <dd> <dl> <dt>

802 (0x322)
</dt> <dt>



Операция не была успешно завершена, поскольку это привело бы к нарушению оппортунистической блокировки. Вызывающий объект запросил, чтобы существующие операционные блокировки не были разорваны.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**Ошибка \_ \_ закрытого маркера блокировки ошибок \_**
</dt> <dd> <dl> <dt>

803 (0x323)
</dt> <dt>



Маркер, с которым связана эта жесткая блокировка, закрыт. Нежесткая блокировка теперь разорвана.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**Ошибка \_ без \_ \_ условия ACE**
</dt> <dd> <dl> <dt>

804 (0x324)
</dt> <dt>



Указанная запись управления доступом (ACE) не содержит условие.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**Ошибка \_ недопустимого \_ \_ условия ACE**
</dt> <dd> <dl> <dt>

805 (0x325)
</dt> <dt>



Указанная запись управления доступом (ACE) содержит недопустимое условие.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**Ошибка \_ при \_ отмене обработчика файла \_**
</dt> <dd> <dl> <dt>

806 (0x326)
</dt> <dt>



Доступ к указанному обработчику файлов был отозван.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**\_изображение ошибки \_ в \_ другой \_ базе**
</dt> <dd> <dl> <dt>

807 (0x327)
</dt> <dt>



Файл изображения был сопоставлен по адресу, отличному от адреса, указанного в файле изображения, но исправления по-прежнему будут автоматически выполняться на образе.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**Ошибка \_ при \_ доступе EA \_**
</dt> <dd> <dl> <dt>

994 (0x3E2)
</dt> <dt>



Отказано в доступе к расширенному атрибуту.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**операция с ошибкой \_ \_ прервана**
</dt> <dd> <dl> <dt>

995 (0x3E3)
</dt> <dt>



Операция ввода-вывода прервана из-за завершения потока или запроса приложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**Ошибка ввода-вывода при ошибке \_ \_**
</dt> <dd> <dl> <dt>

996 (0x3E4)
</dt> <dt>



Перекрытое событие ввода-вывода не находится в сигнальном состоянии.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**\_Ожидание ввода-вывода при ошибке \_**
</dt> <dd> <dl> <dt>

997 (0x3E5)
</dt> <dt>



Выполняется перекрывающаяся операция ввода-вывода.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**Ошибка \_ НЕдоступности**
</dt> <dd> <dl> <dt>

998 (0x3E6)
</dt> <dt>



Недопустимый доступ к расположению в памяти.


</dt> </dl> </dd> <dt>

<span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**Ошибка \_ сваперрор**
</dt> <dd> <dl> <dt>

999 (0x3E7)
</dt> <dt>



Ошибка при выполнении операции со страницей.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды системных ошибок](system-error-codes.md)
</dt> </dl>

 

 
