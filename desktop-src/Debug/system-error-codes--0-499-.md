---
description: Описание кодов ошибок 0-499, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: Коды системных ошибок (0-499) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: a9eddec2baf098f62bb1c0ad88e632360807e7f3fd0ea045f2565587f13e93a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405653"
---
# <a name="system-error-codes-0-499"></a>Коды системных ошибок (0-499)

> [!NOTE]
> Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки. для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.

В следующем списке приведены [коды системных ошибок](system-error-codes.md) (ошибки от 0 до 499). Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций. Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .

<dl> <dt>

<span id="ERROR_SUCCESS"></span><span id="error_success"></span>**Ошибка при \_ успешном выполнении**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Операция выполнена успешно.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**Ошибка \_ Недопустимая \_ функция**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Неверная функция.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**\_файл ошибок \_ не \_ найден**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Системе не удается найти указанный файл.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**\_путь к ошибке \_ не \_ найден**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



Системе не удается найти указанный путь.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**Ошибка \_ слишком \_ много \_ открытых \_ файлов**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Системе не удается открыть файл.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**Ошибка \_ отказа в доступе \_**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



Отказано в доступе".


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**Ошибка \_ недопустимого \_ маркера**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



Дескриптор недействителен.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**некоторая ошибка в \_ \_ корзине**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



Блоки управления хранилищем были уничтожены.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**Ошибка \_ не \_ хватает \_ памяти**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Недостаточно ресурсов памяти для обработки этой команды.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**Ошибка \_ недопустимого \_ блока**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



Недопустимый адрес управляющего блока хранения.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**Ошибка \_ неправильной \_ среды**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



Неверное окружение.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**\_неправильный \_ Формат ошибки**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Была сделана попытка загрузить программу, имеющую неверный формат.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**Ошибка \_ доступа к недопустимым \_ данным**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



Недопустимый код доступа.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**Ошибка при \_ недопустимых \_ данных**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



Недопустимые данные.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**Ошибка \_ OUTOFMEMORY**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



Недостаточно свободного места для выполнения этой операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**Ошибка \_ недопустимого \_ диска**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



Системе не удается найти указанный диск.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**Ошибка в \_ текущем \_ каталоге**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Невозможно удалить каталог.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**Ошибка \_ не на \_ том же \_ устройстве**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



Системе не удается переместить файл на другой диск.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**Ошибка \_ больше \_ нет \_ файлов**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



Больше нет файлов.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**Ошибка \_ записи для \_ защиты**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



Носитель защищен от записи.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**Ошибка \_ неправильной \_ единицы**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



Системе не удается найти указанное устройство.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**Ошибка \_ не \_ готова**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



Устройство не готово.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**Ошибка \_ неправильной \_ команды**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



Устройство не распознает команду.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRC"></span><span id="error_crc"></span>**CRC, ошибка \_**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Ошибка данных (циклическая проверка избыточности).


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**Ошибка \_ неправильной \_ длины**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



Программа выдала команду, но длина команды неверна.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK"></span><span id="error_seek"></span>**\_Поиск ошибок**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



Диску не удается найти определенную область или отслеживание на диске.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**Ошибка \_ при \_ отсутствии \_ диска DOS**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



Не удается получить доступ к указанному диску или дискете.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**\_сектор ошибок \_ не \_ найден**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



Диску не удалось найти запрошенный сектор.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**Ошибка \_ вне \_ \_ бумаги**
</dt> <dd> <dl> <dt>

28 (0x1C)
</dt> <dt>



В принтере нет бумаги.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**Ошибка \_ записи \_ ошибки**
</dt> <dd> <dl> <dt>

29 (0x1D)
</dt> <dt>



Системе не удается выполнить запись на указанное устройство.


</dt> </dl> </dd> <dt>

<span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**Ошибка при \_ чтении \_**
</dt> <dd> <dl> <dt>

30 (0x1E)
</dt> <dt>



Системе не удается выполнить чтение с указанного устройства.


</dt> </dl> </dd> <dt>

<span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**Ошибка \_ \_ при Gen**
</dt> <dd> <dl> <dt>

31 (0x1F)
</dt> <dt>



Устройство, подключенное к системе, не работает.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**\_нарушение общего доступа к ошибке \_**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



The process cannot access the file because it is being used by another process.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**\_нарушение блокировки \_ ошибки**
</dt> <dd> <dl> <dt>

33 (0x21)
</dt> <dt>



Процессу не удается получить доступ к файлу, так как другой процесс заблокировал часть этого файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**Ошибка \_ неправильного \_ диска**
</dt> <dd> <dl> <dt>

34 (0x22)
</dt> <dt>



В дисководе находится неверная дискета. Вставьте %2 (серийный номер тома: %3) в диск %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**превышено общее количество ошибок в \_ общем \_ буфере \_**
</dt> <dd> <dl> <dt>

36 (0x24)
</dt> <dt>



Слишком много файлов открыто для совместного использования.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**Ошибка при \_ обработке \_ EOF**
</dt> <dd> <dl> <dt>

38 (0x26)
</dt> <dt>



Достигнут конец файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**Ошибка при \_ обработке \_ диска \_ переполнена**
</dt> <dd> <dl> <dt>

39 (0x27)
</dt> <dt>



Диск полон.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**Ошибка \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

50 (0x32)
</dt> <dt>



Запрос не поддерживается.


</dt> </dl> </dd> <dt>

<span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**Ошибка \_ REM \_ не \_ список**
</dt> <dd> <dl> <dt>

51 (0x33)
</dt> <dt>



Windows не удается найти сетевой путь. Убедитесь, что сетевой путь указан правильно и конечный компьютер не занят или отключен. если Windows по-прежнему не удается найти сетевой путь, обратитесь к администратору сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**Ошибка \_ DUP \_ имя**
</dt> <dd> <dl> <dt>

52 (0x34)
</dt> <dt>



Вы не подключены, так как в сети существует повторяющееся имя. При присоединении к домену перейдите в раздел система на панели управления, чтобы изменить имя компьютера, и повторите попытку. При присоединении к Рабочей группе Выберите другое имя рабочей группы.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**Ошибка \_ неправильного \_ нетпас**
</dt> <dd> <dl> <dt>

53 (0x35)
</dt> <dt>



Сетевой путь не найден".


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**Ошибка " \_ сеть \_ занята"**
</dt> <dd> <dl> <dt>

54 (0x36)
</dt> <dt>



Сеть занята.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**Ошибка \_ dev \_ не \_ существует**
</dt> <dd> <dl> <dt>

55 (0x37)
</dt> <dt>



Указанный сетевой ресурс или устройство больше не доступны.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**Ошибка \_ слишком \_ много \_ команд**
</dt> <dd> <dl> <dt>

56 (0x38)
</dt> <dt>



Достигнуто ограничение на количество команд в сети BIOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**Ошибка \_ ADAP \_ ХДВ \_ Err**
</dt> <dd> <dl> <dt>

57 (0x39)
</dt> <dt>



Произошла аппаратная ошибка сетевого адаптера.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**Ошибка \_ неправильного \_ net \_ отв**
</dt> <dd> <dl> <dt>

58 (0x3A)
</dt> <dt>



Указанный сервер не может выполнить запрошенную операцию.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**Ошибка \_ унексп \_ net \_ Err**
</dt> <dd> <dl> <dt>

59 (0x3B)
</dt> <dt>



Произошла непредвиденная ошибка сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ошибка с \_ плохой ошибкой \_ REM \_ ADAP**
</dt> <dd> <dl> <dt>

60 (0x3C)
</dt> <dt>



Удаленный адаптер несовместим.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**Ошибка \_ принтк \_ Full**
</dt> <dd> <dl> <dt>

61 (0x3D)
</dt> <dt>



Очередь принтера заполнена.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**Ошибка \_ без \_ \_ области очереди**
</dt> <dd> <dl> <dt>

62 (0x3E)
</dt> <dt>



Место для хранения файла, ожидающего печати, недоступно на сервере.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**\_Печать ошибки \_ отменена**
</dt> <dd> <dl> <dt>

63 (0x3F)
</dt> <dt>



Ваш файл, ожидающий печати, был удален.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**Ошибка \_ NETNAME \_ удалена**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Указанное сетевое имя более недоступно.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**Ошибка \_ \_ отказа в доступе к сети \_**
</dt> <dd> <dl> <dt>

65 (0x41 влево)
</dt> <dt>



Отказано в доступе к сети.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**Ошибка \_ неправильного \_ \_ типа dev**
</dt> <dd> <dl> <dt>

66 (0x42)
</dt> <dt>



Неверный тип сетевого ресурса.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**Ошибка \_ неправильного \_ сетевого \_ имени**
</dt> <dd> <dl> <dt>

67 (0x43)
</dt> <dt>



Не найдено сетевое имя".


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**Ошибка \_ слишком \_ много \_ имен**
</dt> <dd> <dl> <dt>

68 (0x44)
</dt> <dt>



Превышено ограничение на число имен для сетевого адаптера локального компьютера.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**Ошибка \_ слишком \_ много \_ подряд**
</dt> <dd> <dl> <dt>

69 (0x45)
</dt> <dt>



Превышено ограничение на количество сеансов сетевой BIOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**\_общий доступ к ошибкам \_ приостановлен**
</dt> <dd> <dl> <dt>

70 (0x46)
</dt> <dt>



Удаленный сервер приостановлен или находится в процессе запуска.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**Ошибка \_ req \_ не \_ акцеп**
</dt> <dd> <dl> <dt>

71 (0x47)
</dt> <dt>



В настоящее время больше нет доступных подключений к этому удаленному компьютеру, так как количество подключений, которое может принять компьютер, уже установлено.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**Ошибка \_ редир \_ приостановлена**
</dt> <dd> <dl> <dt>

72 (0x48)
</dt> <dt>



Указанный принтер или дисковое устройство приостановлены.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**\_файл ошибок \_ существует**
</dt> <dd> <dl> <dt>

80 (0x50)
</dt> <dt>



Файл существует


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**Ошибка \_ не может \_ быть**
</dt> <dd> <dl> <dt>

82 (0x52)
</dt> <dt>



Не удается создать каталог или файл.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**Ошибка при \_ сбое \_ I24**
</dt> <dd> <dl> <dt>

83 (0x53)
</dt> <dt>



Сбой на INT 24.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**Ошибка \_ из \_ \_ структур**
</dt> <dd> <dl> <dt>

84 (0x54)
</dt> <dt>



служба хранилища обработать этот запрос недоступен.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**Ошибка \_ уже \_ назначена**
</dt> <dd> <dl> <dt>

85 (0x55)
</dt> <dt>



Имя локального устройства уже используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**Ошибка \_ неправильного \_ пароля**
</dt> <dd> <dl> <dt>

86 (0x56)
</dt> <dt>



Указан неверный сетевой пароль.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**Ошибка \_ недопустимого \_ параметра**
</dt> <dd> <dl> <dt>

87 (0x57)
</dt> <dt>



Неправильный параметр".


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**Ошибка \_ ошибки \_ записи в сеть \_**
</dt> <dd> <dl> <dt>

88 (0x58)
</dt> <dt>



В сети произошла ошибка записи.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**Ошибка \_ без \_ \_ слотов процедур**
</dt> <dd> <dl> <dt>

89 (0x59)
</dt> <dt>



В данный момент система не может запустить другой процесс.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**Ошибка \_ слишком \_ большого числа \_ семафоров**
</dt> <dd> <dl> <dt>

100 (0x64)
</dt> <dt>



Невозможно создать другой системный семафор.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**Ошибка \_ без \_ \_ уже существующего \_ владельца SEM**
</dt> <dd> <dl> <dt>

101 (0x65)
</dt> <dt>



Эксклюзивный семафор принадлежит другому процессу.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**указана ошибка \_ SEM \_ \_**
</dt> <dd> <dl> <dt>

102 (0x66)
</dt> <dt>



Семафор установлен и не может быть закрыт.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**Ошибка \_ слишком \_ много \_ \_ запросов SEM**
</dt> <dd> <dl> <dt>

103 (0x67)
</dt> <dt>



Семафор не может быть установлен повторно.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**Ошибка \_ недопустима \_ во \_ \_ время прерывания**
</dt> <dd> <dl> <dt>

104 (0x68)
</dt> <dt>



Не удается запросить эксклюзивные семафоры во время прерывания.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**Ошибка \_ SEM \_ owner \_ умер**
</dt> <dd> <dl> <dt>

105 (0x69)
</dt> <dt>



Предыдущее владение этим семафором завершено.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**Ошибка \_ в \_ \_ ограничении пользователя SEM**
</dt> <dd> <dl> <dt>

106 (0x6A)
</dt> <dt>



Вставьте дискету для диска %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**Ошибка \_ при \_ изменении диска**
</dt> <dd> <dl> <dt>

107 (0x6B)
</dt> <dt>



Программа остановлена, так как не вставлена дополнительная дискета.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**Ошибка \_ \_ блокировки диска**
</dt> <dd> <dl> <dt>

108 (0x6C)
</dt> <dt>



Диск занят или заблокирован другим процессом.


</dt> </dl> </dd> <dt>

<span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**Ошибка при \_ нарушении \_ канала**
</dt> <dd> <dl> <dt>

109 (0x6D)
</dt> <dt>



Канал завершен.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**Ошибка \_ \_ при открытии**
</dt> <dd> <dl> <dt>

110 (0x6E)
</dt> <dt>



Системе не удается открыть указанное устройство или файл.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**\_ \_ переполнение буфера ошибки**
</dt> <dd> <dl> <dt>

111 (0x6F)
</dt> <dt>



Имя файла слишком длинное.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**Ошибка \_ \_ переполнения диска**
</dt> <dd> <dl> <dt>

112 (0x70)
</dt> <dt>



Недостаточно места на диске.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**Ошибка \_ больше \_ нет \_ \_ дескрипторов поиска**
</dt> <dd> <dl> <dt>

113 (0x71)
</dt> <dt>



Больше нет доступных идентификаторов внутренних файлов.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**Ошибка \_ недопустимого \_ целевого \_ маркера**
</dt> <dd> <dl> <dt>

114 (0x72)
</dt> <dt>



Неверный целевой внутренний идентификатор файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**Ошибка \_ недопустимой \_ категории**
</dt> <dd> <dl> <dt>

117 (0x75)
</dt> <dt>



Вызов IOCTL, сделанный программой приложения, неверен.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**Ошибка \_ при \_ проверке недопустимого \_ параметра**
</dt> <dd> <dl> <dt>

118 (0x76)
</dt> <dt>



Неправильное значение параметра проверки-on-Write.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ОШИБКА с \_ неправильным \_ \_ уровнем драйвера**
</dt> <dd> <dl> <dt>

119 (0x77)
</dt> <dt>



Система не поддерживает запрошенную команду.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**\_вызов ошибки \_ не \_ реализован**
</dt> <dd> <dl> <dt>

120 (0x78)
</dt> <dt>



Эта функция не поддерживается в этой системе.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**Ошибка \_ \_ времени ожидания SEM**
</dt> <dd> <dl> <dt>

121 (0x79)
</dt> <dt>



Истек период ожидания семафора.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**Ошибка \_ недостаточного \_ буфера**
</dt> <dd> <dl> <dt>

122 (0x7A)
</dt> <dt>



Область данных, переданная в системный вызов, слишком мала.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**Ошибка \_ недопустимое \_ имя**
</dt> <dd> <dl> <dt>

123 (0x7B)
</dt> <dt>



Синтаксическая ошибка в имени файла, имени каталога или метке тома.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**\_Недопустимый \_ уровень ошибки**
</dt> <dd> <dl> <dt>

124 (0x7C)
</dt> <dt>



Неверный уровень системного вызова.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**Ошибка \_ без \_ \_ метки тома**
</dt> <dd> <dl> <dt>

125 (0x7D)
</dt> <dt>



Диск не имеет метки тома.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**Ошибка \_ Mod \_ не \_ найдена**
</dt> <dd> <dl> <dt>

126 (0x7E)
</dt> <dt>



Не найден указанный модуль.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**Ошибка \_ \_ не \_ найдена процедура**
</dt> <dd> <dl> <dt>

127 (0x7F)
</dt> <dt>



Не удалось найти указанную процедуру.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**Ошибка \_ Ожидание \_ отсутствия \_ дочерних элементов**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Нет дочерних процессов для ожидания.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**Ошибка \_ дочернего элемента \_ не \_ завершена**
</dt> <dd> <dl> <dt>

129 (0x81)
</dt> <dt>



Приложение %1 не может быть запущено в режиме Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**Ошибка \_ прямого \_ доступа к \_ обработчику**
</dt> <dd> <dl> <dt>

130 (0x82)
</dt> <dt>



Попытка использовать маркер файла для открытого раздела диска для операции, отличной от операций ввода-вывода с необработанным диском.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**Ошибка при \_ поиске отрицательных результатов \_**
</dt> <dd> <dl> <dt>

131 (0x83)
</dt> <dt>



Предпринята попытка переместить указатель на файл перед началом файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**\_Поиск ошибок \_ на \_ устройстве**
</dt> <dd> <dl> <dt>

132 (0x84)
</dt> <dt>



Не удается задать указатель файла для указанного устройства или файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**Ошибка \_ : \_ Присоединение к \_ целевому объекту**
</dt> <dd> <dl> <dt>

133 (0x85)
</dt> <dt>



Команду JOIN или SUBST нельзя использовать для диска, который содержит ранее подключенные диски.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**Ошибка \_ \_ присоединена**
</dt> <dd> <dl> <dt>

134 (0x86)
</dt> <dt>



Предпринята попытка использовать команду JOIN или SUBST на диске, который уже присоединен.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**\_указана \_ Ошибка**
</dt> <dd> <dl> <dt>

135 (0x87)
</dt> <dt>



Была предпринята попытка использовать команду JOIN или SUBST на диске, который уже был заменен.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**Ошибка \_ не \_ присоединена**
</dt> <dd> <dl> <dt>

136 (0x88)
</dt> <dt>



Система попыталась удалить соединение диска, который не присоединен.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**не удается отобразить ошибку \_ \_**
</dt> <dd> <dl> <dt>

137 (0x89)
</dt> <dt>



Система попыталась удалить подстановку незаменяемого диска.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**Ошибка при \_ присоединении \_ к \_ соединению**
</dt> <dd> <dl> <dt>

138 (0x8A)
</dt> <dt>



Система попыталась присоединить диск к каталогу на присоединенном диске.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**Ошибка \_ subst \_ для \_ subst**
</dt> <dd> <dl> <dt>

139 (0x8B)
</dt> <dt>



Система попыталась заменить диск на каталог на подставляемом диске.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**Ошибка при \_ присоединении \_ к \_ subst**
</dt> <dd> <dl> <dt>

140 (0x8C)
</dt> <dt>



Система попыталась присоединить диск к каталогу на подставляемом диске.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**Ошибка \_ subst \_ для \_ Присоединение**
</dt> <dd> <dl> <dt>

141 (0x8D)
</dt> <dt>



Система попыталась отобразить диск в каталог на присоединенном диске.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**\_диск занят \_**
</dt> <dd> <dl> <dt>

142 (0x8E)
</dt> <dt>



В настоящее время системе не удается выполнить соединение или SUBST.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**Ошибка на \_ том же \_ диске**
</dt> <dd> <dl> <dt>

143 (0x8F)
</dt> <dt>



Система не может присоединить или заменить диск на каталог или для каталога на том же диске.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**Ошибка \_ dir \_ не \_ корневая папка**
</dt> <dd> <dl> <dt>

144 (0x90)
</dt> <dt>



Каталог не является вложенным каталогом корневого каталога.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**Ошибка \_ dir, \_ не \_ пустая**
</dt> <dd> <dl> <dt>

145 (0x91)
</dt> <dt>



Каталог не пуст.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**Ошибка \_ — \_ \_ путь SUBST**
</dt> <dd> <dl> <dt>

146 (0x92)
</dt> <dt>



Указанный путь используется в подстановке.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**Ошибка \_ — \_ путь к соединению \_**
</dt> <dd> <dl> <dt>

147 (0x93)
</dt> <dt>



Недостаточно ресурсов для обработки этой команды.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**\_путь к ошибке \_ занят**
</dt> <dd> <dl> <dt>

148 (0x94)
</dt> <dt>



Указанный путь не может быть использован в настоящее время.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**Ошибка \_ : \_ subst \_ Target**
</dt> <dd> <dl> <dt>

149 (0x95)
</dt> <dt>



Предпринята попытка присоединить или заменить диск, для которого каталог на диске является целью предыдущего замены.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**Ошибка \_ \_ трассировки системы**
</dt> <dd> <dl> <dt>

150 (0x96)
</dt> <dt>



Данные трассировки системы не указаны в файле CONFIG.SYS, или трассировка запрещена.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**Ошибка при \_ неправильном \_ \_ числе событий**
</dt> <dd> <dl> <dt>

151 (0x97)
</dt> <dt>



Указано неправильное число указанных событий семафора для Досмукссемваит.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**Ошибка \_ слишком \_ много \_ муксваитерс**
</dt> <dd> <dl> <dt>

152 (0x98)
</dt> <dt>



Досмукссемваит не выполнен; уже задано слишком много семафоров.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**Ошибка \_ недопустимого \_ \_ формата списка**
</dt> <dd> <dl> <dt>

153 (0x99)
</dt> <dt>



Недопустимый список Досмукссемваит.


</dt> </dl> </dd> <dt>

<span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**\_ \_ слишком \_ ДЛИННая метка ошибки**
</dt> <dd> <dl> <dt>

154 (0x9A)
</dt> <dt>



Введенная метка тома превышает ограничение на количество символов в целевой файловой системе.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**Ошибка \_ слишком \_ много \_ ткбс**
</dt> <dd> <dl> <dt>

155 (0x9B)
</dt> <dt>



Не удается создать другой поток.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**\_сигнал ошибки \_ отклонен**
</dt> <dd> <dl> <dt>

156 (0x9C)
</dt> <dt>



Процесс получателя отклонил сигнал.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**Ошибка \_ отклонена**
</dt> <dd> <dl> <dt>

157 (0x9D)
</dt> <dt>



Сегмент уже удален и не может быть заблокирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**Ошибка \_ не \_ заблокирована**
</dt> <dd> <dl> <dt>

158 (0x9E)
</dt> <dt>



Сегмент уже разблокирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ОШИБКА с \_ неверным \_ \_ адресом THREADID**
</dt> <dd> <dl> <dt>

159 (0x9F)
</dt> <dt>



Неправильный адрес для идентификатора потока.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ошибочные \_ \_ аргументы**
</dt> <dd> <dl> <dt>

160 (0X82)
</dt> <dt>



Один или несколько аргументов неверны.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ОШИБКА с \_ неверным \_ путем**
</dt> <dd> <dl> <dt>

161 (0xA1)
</dt> <dt>



Указан недопустимый путь.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**\_сигнал ошибки \_ в ожидании**
</dt> <dd> <dl> <dt>

162 (0xA2)
</dt> <dt>



Сигнал уже находится в состоянии ожидания.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**Ошибка \_ Max \_ СРДС \_ достигнуто**
</dt> <dd> <dl> <dt>

164 (токенов 0xA4)
</dt> <dt>



В системе больше нельзя создавать потоки.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**\_сбой блокировки \_ ошибки**
</dt> <dd> <dl> <dt>

167 (0xA7)
</dt> <dt>



Не удалось заблокировать область файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY"></span><span id="error_busy"></span>**Ошибка \_ занята**
</dt> <dd> <dl> <dt>

170 (0xAA)
</dt> <dt>



Запрошенный ресурс уже используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**Ошибка \_ \_ \_ в процессе поддержки \_ устройства**
</dt> <dd> <dl> <dt>

171 (0xAB)
</dt> <dt>



Идет обнаружение поддержки команд устройства.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**Ошибка \_ отмены \_ нарушения**
</dt> <dd> <dl> <dt>

173 (0xAD)
</dt> <dt>



Запрос блокировки не был выполнен для указанной региона отмены.


</dt> </dl> </dd> <dt>

<span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ОШИБКИ \_ атомарных \_ блокировок \_ не \_ поддерживаются**
</dt> <dd> <dl> <dt>

174 (0xAE)
</dt> <dt>



Файловая система не поддерживает атомарные изменения типа блокировки.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**Ошибка \_ недопустимого \_ \_ номера сегмента**
</dt> <dd> <dl> <dt>

180 (0xB4)
</dt> <dt>



Система обнаружила неверный номер сегмента.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ОШИБКА с \_ недопустимым \_ порядковым номером**
</dt> <dd> <dl> <dt>

182 (0xB6)
</dt> <dt>



Операционная система не может выполнить %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**Ошибка \_ уже \_ существует**
</dt> <dd> <dl> <dt>

183 (0xB7)
</dt> <dt>



невозможно создать файл, так как он уже существует.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**Ошибка \_ недопустимого \_ номера флага \_**
</dt> <dd> <dl> <dt>

186 (0xBA)
</dt> <dt>



Передан неверный флаг.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**Ошибка \_ SEM \_ не \_ найдена**
</dt> <dd> <dl> <dt>

187 (0xBB)
</dt> <dt>



Указанное имя системного семафора не найдено.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**Ошибка \_ при \_ запуске \_ кодесег**
</dt> <dd> <dl> <dt>

188 (0xBC)
</dt> <dt>



Операционная система не может выполнить %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**Ошибка \_ недопустимого \_ стакксег**
</dt> <dd> <dl> <dt>

189 (0xBD)
</dt> <dt>



Операционная система не может выполнить %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**Ошибка \_ недопустимого \_ MODULETYPE**
</dt> <dd> <dl> <dt>

190 (0xBE)
</dt> <dt>



Операционная система не может выполнить %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**Ошибка \_ недопустимой \_ \_ подписи exe**
</dt> <dd> <dl> <dt>

191 (0xBF)
</dt> <dt>



Не удается выполнить %1 в режиме Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**Ошибка \_ exe \_ помечена как \_ Недопустимая**
</dt> <dd> <dl> <dt>

192 (0xC0)
</dt> <dt>



Операционная система не может выполнить %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**Ошибка в \_ неправильном \_ \_ формате exe**
</dt> <dd> <dl> <dt>

193 (0xC1)
</dt> <dt>



%1 не является допустимым приложением Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**Данные об ошибках при \_ итерации \_ \_ превышают \_ 64 КБ**
</dt> <dd> <dl> <dt>

194 (0xC2)
</dt> <dt>



Операционная система не может выполнить %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**Ошибка \_ недопустимого \_ миналлоксизе**
</dt> <dd> <dl> <dt>

195 (0xC3)
</dt> <dt>



Операционная система не может выполнить %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**Ошибка \_ динлинк \_ из \_ недопустимого \_ кольца**
</dt> <dd> <dl> <dt>

196 (0xC4)
</dt> <dt>



Операционная система не может запустить эту программу приложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**Ошибка \_ иопл \_ не \_ включена**
</dt> <dd> <dl> <dt>

197 (0xC5)
</dt> <dt>



Операционная система в настоящее время не настроена для запуска этого приложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**Ошибка \_ недопустимого \_ сегдпл**
</dt> <dd> <dl> <dt>

198 (0xC6)
</dt> <dt>



Операционная система не может выполнить %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**Ошибка \_ аутодатасег \_ превышает \_ 64 КБ**
</dt> <dd> <dl> <dt>

199 (0xC7)
</dt> <dt>



Операционная система не может запустить эту программу приложения.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**Ошибка \_ RING2SEG \_ должна \_ быть \_ перемещаемой**
</dt> <dd> <dl> <dt>

200 (0xC8)
</dt> <dt>



Сегмент кода не может быть больше или равен 64 КБ.


</dt> </dl> </dd> <dt>

<span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERROR \_ reloc \_ chain \_ ксидс \_ сеглим**
</dt> <dd> <dl> <dt>

201 (0xC9)
</dt> <dt>



Операционная система не может выполнить %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**Ошибка \_ инфлуп \_ в \_ \_ цепочке reloc**
</dt> <dd> <dl> <dt>

202 (0xCA)
</dt> <dt>



Операционная система не может выполнить %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**Ошибка \_ ENVVAR \_ не \_ найдена**
</dt> <dd> <dl> <dt>

203 (0xCB)
</dt> <dt>



Системе не удалось найти указанный параметр среды.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**Ошибка \_ не \_ \_ отправлен сигнал**
</dt> <dd> <dl> <dt>

205 (0xCD)
</dt> <dt>



Ни один из процессов в поддереве команды не имеет обработчика сигналов.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**Ошибка \_ имя файла \_ ексцед \_ Range**
</dt> <dd> <dl> <dt>

206 (0xCE)
</dt> <dt>



Слишком длинное имя файла или расширение.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**Ошибка \_ \_ \_ при использовании стека RING2 \_**
</dt> <dd> <dl> <dt>

207 (0xCF)
</dt> <dt>



Стек Ring 2 используется.


</dt> </dl> </dd> <dt>

<span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**\_ \_ \_ слишком \_ длинное расширение мета для ошибки**
</dt> <dd> <dl> <dt>

208 (0xD0)
</dt> <dt>



Символы глобального имени файла \* или? введены неправильно или указано слишком много символов глобального имени файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**Ошибка \_ недопустимого \_ \_ номера сигнала**
</dt> <dd> <dl> <dt>

209 (0xD1)
</dt> <dt>



Отправляемый сигнал неверен.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**\_Поток ошибок \_ 1 \_ неактивен**
</dt> <dd> <dl> <dt>

210 (0xD2)
</dt> <dt>



Не удается установить обработчик сигналов.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCKED"></span><span id="error_locked"></span>**Ошибка \_ заблокирована**
</dt> <dd> <dl> <dt>

212 (0xD4)
</dt> <dt>



Сегмент заблокирован и не может быть выделен повторно.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**Ошибка \_ слишком \_ много \_ модулей**
</dt> <dd> <dl> <dt>

214 (0xD6)
</dt> <dt>



К этой программе или модулю динамической компоновки подключено слишком много модулей динамической компоновки.


</dt> </dl> </dd> <dt>

<span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**\_вложенность ошибок \_ \_ запрещена**
</dt> <dd> <dl> <dt>

215 (0xD7)
</dt> <dt>



Невозможно вложить вызовы в LoadModule.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**Ошибка \_ exe \_ \_ \_ несоответствие типов компьютеров**
</dt> <dd> <dl> <dt>

216 (0xD8)
</dt> <dt>



эта версия %1 несовместима с версией Windows, которую вы используете. Проверьте сведения о системе компьютера, а затем обратитесь к издателю программного обеспечения.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**Ошибка \_ exe \_ не \_ может \_ изменить \_ двоичный файл со знаком**
</dt> <dd> <dl> <dt>

217 (0xD9)
</dt> <dt>



Файл образа %1 подписан, его невозможно изменить.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**Ошибка \_ exe \_ не \_ может \_ изменить \_ \_ двоичный файл со строгим знаком**
</dt> <dd> <dl> <dt>

218 (0xDA)
</dt> <dt>



Файл образа %1 имеет строгие подписи, его невозможно изменить.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**файл с ОШИБКАми \_ \_ извлечен \_**
</dt> <dd> <dl> <dt>

220 (0xDC)
</dt> <dt>



Этот файл извлечен или заблокирован для редактирования другим пользователем.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**\_требуется извлечение \_ ошибок**
</dt> <dd> <dl> <dt>

221 (0xDD)
</dt> <dt>



Перед сохранением изменений необходимо извлечь файл.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**Ошибка \_ неправильного \_ \_ типа файла**
</dt> <dd> <dl> <dt>

222 (0xDE)
</dt> <dt>



Сохраняемый или извлекаемый тип файла заблокирован.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**\_файл ошибок \_ слишком \_ большой**
</dt> <dd> <dl> <dt>

223 (0xDF)
</dt> <dt>



Размер файла превышает допустимый предел и не может быть сохранен.


</dt> </dl> </dd> <dt>

<span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**\_ \_ требуется проверка подлинности форм с ошибками \_**
</dt> <dd> <dl> <dt>

224 (0xE0)
</dt> <dt>



Доступ запрещен. Перед открытием файлов в этом расположении необходимо сначала добавить веб-сайт в список надежных сайтов, перейти на веб-сайт и выбрать параметр автоматического входа.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**ОШИБОЧный \_ вирус \_ заражен**
</dt> <dd> <dl> <dt>

225 (0xE1)
</dt> <dt>



Операция не была успешно завершена, так как файл содержит вирус или потенциально нежелательное программное обеспечение.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**Ошибка \_ при \_ удалении вируса**
</dt> <dd> <dl> <dt>

226 (0xE2)
</dt> <dt>



Этот файл содержит вирус или потенциально нежелательное программное обеспечение и не может быть открыт. Из-за природы этого вируса или потенциально нежелательного программного обеспечения файл был удален из этого расположения.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**\_локальный канал \_ ошибки**
</dt> <dd> <dl> <dt>

229 (0xE5)
</dt> <dt>



Канал является локальным.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**Ошибка \_ неверного \_ канала**
</dt> <dd> <dl> <dt>

230 (0xE6)
</dt> <dt>



Недопустимое состояние канала.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**\_канал ошибки \_ занят**
</dt> <dd> <dl> <dt>

231 (0xE7)
</dt> <dt>



Все экземпляры канала заняты.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**Ошибка \_ без \_ данных**
</dt> <dd> <dl> <dt>

232 (0xE8)
</dt> <dt>



Канал закрывается.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**\_канал ошибки \_ не \_ подключен**
</dt> <dd> <dl> <dt>

233 (0xE9)
</dt> <dt>



Процесс отсутствует на другом конце канала.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**Ошибка \_ дополнительных \_ данных**
</dt> <dd> <dl> <dt>

234 (0xEA)
</dt> <dt>



More data is available.


</dt> </dl> </dd> <dt>

<span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**Ошибка \_ VC \_ DISCONNECTED**
</dt> <dd> <dl> <dt>

240 (0xF0)
</dt> <dt>



Сеанс был отменен.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**Ошибка \_ недопустимого \_ \_ имени EA**
</dt> <dd> <dl> <dt>

254 (0xFE)
</dt> <dt>



Указано недопустимое имя расширенного атрибута.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**\_несоответствие \_ списка EA с ошибками \_**
</dt> <dd> <dl> <dt>

255 (0xFF)
</dt> <dt>



Расширенные атрибуты непоследовательны.


</dt> </dl> </dd> <dt>

<span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**\_время ожидания ожидания**
</dt> <dd> <dl> <dt>

258 (0x102)
</dt> <dt>



Время операции ожидания истекло.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**Ошибка \_ больше \_ нет \_ элементов**
</dt> <dd> <dl> <dt>

259 (0x103)
</dt> <dt>



Больше нет доступных данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**Ошибка \_ при \_ копировании**
</dt> <dd> <dl> <dt>

266 (0x10A)
</dt> <dt>



Функции копирования использовать нельзя.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**\_Каталог ошибок**
</dt> <dd> <dl> <dt>

267 (0x10B)
</dt> <dt>



Недопустимое имя каталога.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**Ошибка \_ EAS \_ окончательный \_**
</dt> <dd> <dl> <dt>

275 (0x113)
</dt> <dt>



Расширенные атрибуты не помещаются в буфер.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**Ошибка \_ EA \_ File \_ поврежден**
</dt> <dd> <dl> <dt>

276 (0x114)
</dt> <dt>



Файл расширенного атрибута в подключенной файловой системе поврежден.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**Ошибка \_ \_ таблицы EA \_ Full**
</dt> <dd> <dl> <dt>

277 (0x115)
</dt> <dt>



Файл расширенной таблицы атрибутов заполнен.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**Ошибка \_ недопустимого \_ \_ маркера EA**
</dt> <dd> <dl> <dt>

278 (0x116)
</dt> <dt>



Указан недопустимый расширенный маркер атрибута.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**Ошибка \_ EAS \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

282 (0x11A)
</dt> <dt>



Подключенная файловая система не поддерживает расширенные атрибуты.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ОШИБКА, \_ не \_ владелец**
</dt> <dd> <dl> <dt>

288 (0x120)
</dt> <dt>



Попытка освободить мьютекс, не принадлежащий вызывающему объекту.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**Ошибка \_ слишком \_ много \_ записей**
</dt> <dd> <dl> <dt>

298 (0x12A)
</dt> <dt>



В семафоре создано слишком много записей.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**Ошибка \_ частичной \_ копии**
</dt> <dd> <dl> <dt>

299 (0x12B)
</dt> <dt>



Завершена только часть запроса Реадпроцессмемори или Вритепроцессмемори.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**Ошибка " \_ нежесткая блокировка \_ не \_ предоставлена"**
</dt> <dd> <dl> <dt>

300 (0x12C)
</dt> <dt>



Запрос на нежесткую блокировку отклоняется.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**Ошибка \_ недопустимого \_ протокола нежесткой блокировки \_**
</dt> <dd> <dl> <dt>

301 (0x12D)
</dt> <dt>



Система получила недопустимое подтверждение на нежесткую блокировку.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**Ошибка \_ \_ слишком \_ фрагментации диска**
</dt> <dd> <dl> <dt>

302 (0x12E)
</dt> <dt>



Том слишком фрагментирован для выполнения этой операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**Ошибка \_ удаления \_ в ожидании**
</dt> <dd> <dl> <dt>

303 (0x12F)
</dt> <dt>



Не удается открыть файл, так как он находится в процессе удаления.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**Ошибка \_ несовместима \_ с \_ глобальным \_ \_ \_ параметром реестра Short Name \_**
</dt> <dd> <dl> <dt>

304 (0x130)
</dt> <dt>



Параметры короткого имени не могут быть изменены на этом томе из-за параметра глобального реестра.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**\_ \_ \_ \_ \_ в томе не включены короткие имена \_ ошибок**
</dt> <dd> <dl> <dt>

305 (0x131)
</dt> <dt>



Короткие имена не включены на этом томе.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**\_несоответствие \_ потока \_ безопасности при ошибке \_**
</dt> <dd> <dl> <dt>

306 (0x132)
</dt> <dt>



Поток безопасности для данного тома находится в нестабильном состоянии. Запустите CHKDSK на томе.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**Ошибка \_ недопустимого \_ \_ диапазона блокировки**
</dt> <dd> <dl> <dt>

307 (0x133)
</dt> <dt>



Запрошенная операция блокировки файла не может быть обработана из-за недопустимого диапазона байтов.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**\_подсистема изображения ошибки \_ \_ отсутствует \_**
</dt> <dd> <dl> <dt>

308 (0x134)
</dt> <dt>



Отсутствует подсистема, необходимая для поддержки типа образа.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**GUID уведомления об ОШИБКе \_ \_ \_ уже \_ определен**
</dt> <dd> <dl> <dt>

309 (0x135)
</dt> <dt>



С указанным файлом уже связан GUID уведомления.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**Ошибка \_ недопустимого \_ \_ обработчика исключений**
</dt> <dd> <dl> <dt>

310 (0x136)
</dt> <dt>



Обнаружена недопустимая подсистема обработчика исключений.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**Ошибка при \_ дублировании \_ привилегий**
</dt> <dd> <dl> <dt>

311 (0x137)
</dt> <dt>



Для токена указаны дублирующиеся привилегии.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**Ошибка \_ не \_ \_ обработано диапазонов**
</dt> <dd> <dl> <dt>

312 (0x138)
</dt> <dt>



Не удалось обработать диапазоны для указанной операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**Ошибка \_ не \_ разрешена \_ в \_ системном \_ файле**
</dt> <dd> <dl> <dt>

313 (0x139)
</dt> <dt>



Операция не разрешена для внутреннего файла файловой системы.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**\_дисковые ресурсы с ошибками \_ \_ исчерпаны**
</dt> <dd> <dl> <dt>

314 (0x13A)
</dt> <dt>



Физические ресурсы этого диска исчерпаны.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**Ошибка \_ недопустимого \_ токена**
</dt> <dd> <dl> <dt>

315 (0x13B)
</dt> <dt>



Недопустимый токен, представляющий данные.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**Функция устройства с ОШИБКАми \_ \_ \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

316 (0x13C)
</dt> <dt>



Устройство не поддерживает функцию команды.


</dt> </dl> </dd> <dt>

<span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**Ошибка \_ MR \_ \_ не \_ найдена**
</dt> <dd> <dl> <dt>

317 (0x13D)
</dt> <dt>



Системе не удается найти текст сообщения с номером 0x %1 в файле сообщений для %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**\_область ошибок \_ не \_ найдена**
</dt> <dd> <dl> <dt>

318 (0x13E)
</dt> <dt>



Указанная область не найдена.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**Ошибка \_ НЕопределенной \_ области**
</dt> <dd> <dl> <dt>

319 (0x13F)
</dt> <dt>



Указанная Централизованная политика доступа не определена на целевом компьютере.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**Ошибка \_ недопустимого \_ ограничения**
</dt> <dd> <dl> <dt>

320 (0x140)
</dt> <dt>



Централизованная политика доступа, полученная из Active Directory, недопустима.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**устройство с ОШИБКАми \_ \_ недоступно**
</dt> <dd> <dl> <dt>

321 (0x141)
</dt> <dt>



Устройство недоступно.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**устройство с ОШИБКАми — \_ \_ нет \_ ресурсов**
</dt> <dd> <dl> <dt>

322 (0x142)
</dt> <dt>



На целевом устройстве недостаточно ресурсов для завершения операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**Ошибка \_ \_ контрольной суммы данных об ошибках \_**
</dt> <dd> <dl> <dt>

323 (0x143)
</dt> <dt>



Произошла ошибка контрольной суммы целостности данных. Данные в файловом потоке повреждены.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**Ошибка при \_ ВЗАИМОсмешанных \_ \_ \_ операциях ядра EA**
</dt> <dd> <dl> <dt>

324 (0x144)
</dt> <dt>



Была предпринята попытка изменить как ядро, так и нормальный Расширенный атрибут (EA) в одной операции.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**Ошибка \_ \_ Trim на уровне файлов \_ \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

326 (0x146)
</dt> <dt>



Устройство не поддерживает УСЕЧЕНИЕ на уровне файлов.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**\_ \_ нарушение выравнивания по СМЕЩЕНию ошибок \_**
</dt> <dd> <dl> <dt>

327 (0x147)
</dt> <dt>



В команде указано смещение данных, которое не соответствует детализации или выравниванию устройства.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**Ошибка \_ недопустимого \_ поля \_ в \_ \_ списке параметров**
</dt> <dd> <dl> <dt>

328 (0x148)
</dt> <dt>



В списке параметров команды указано недопустимое поле.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**Ошибка \_ при выполнении операции \_ \_**
</dt> <dd> <dl> <dt>

329 (0x149)
</dt> <dt>



В настоящее время выполняется операция с устройством.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**Ошибка \_ неправильного \_ \_ пути к устройству**
</dt> <dd> <dl> <dt>

330 (0x14A)
</dt> <dt>



Предпринята попытка отправить команду через недопустимый путь к целевому устройству.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**Ошибка \_ слишком \_ большого числа \_ дескрипторов**
</dt> <dd> <dl> <dt>

331 (0x14B)
</dt> <dt>



В команде указано число дескрипторов, превышающих максимальное поддерживаемое устройством.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**Ошибка \_ очистки \_ данных \_ отключена**
</dt> <dd> <dl> <dt>

332 (0x14C)
</dt> <dt>



Очистка в указанном файле отключена.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**Ошибка \_ не является \_ избыточным \_ хранилищем**
</dt> <dd> <dl> <dt>

333 (0x14D)
</dt> <dt>



Устройство хранения данных не обеспечивает избыточность.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**\_резидентный \_ файл ошибок \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

334 (0x14E)
</dt> <dt>



Операция не поддерживается для резидентных файлов.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**сжатый файл с ОШИБКАми \_ \_ \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

335 (0x14F)
</dt> <dt>



Операция не поддерживается для сжатого файла.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**\_Каталог ошибок \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

336 (0x150)
</dt> <dt>



Операция не поддерживается в каталоге.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**Ошибка \_ \_ чтения \_ из \_ копии**
</dt> <dd> <dl> <dt>

337 (0x151)
</dt> <dt>



Не удалось прочитать указанную копию запрошенных данных.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**Ошибка \_ при \_ перезагрузке "Недействие" \_**
</dt> <dd> <dl> <dt>

350 (0x15E)
</dt> <dt>



Не было предпринято никаких действий, так как требуется перезагрузка системы.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**Ошибка \_ при \_ завершении работы**
</dt> <dd> <dl> <dt>

351 (0x15F)
</dt> <dt>



Сбой операции завершения работы.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**Ошибка \_ при \_ перезапуске**
</dt> <dd> <dl> <dt>

352 (0x160)
</dt> <dt>



Сбой операции перезапуска.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**ОШИБОК \_ \_ достигнуто максимальное число сеансов \_**
</dt> <dd> <dl> <dt>

353 (0x161)
</dt> <dt>



Достигнуто максимальное число сеансов.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**\_режим потока \_ ошибок \_ уже является \_ фоновым**
</dt> <dd> <dl> <dt>

400 (0x190)
</dt> <dt>



Поток уже находится в режиме фоновой обработки.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**\_режим потока \_ ошибок \_ не является \_ фоновым**
</dt> <dd> <dl> <dt>

401 (0x191)
</dt> <dt>



Поток не находится в режиме фоновой обработки.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**\_режим обработки \_ ошибок \_ уже является \_ фоновым**
</dt> <dd> <dl> <dt>

402 (0x192)
</dt> <dt>



Процесс уже находится в режиме фоновой обработки.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**\_режим обработки \_ ошибок \_ не является \_ фоновым**
</dt> <dd> <dl> <dt>

403 (0x193)
</dt> <dt>



Процесс не находится в режиме фоновой обработки.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**Ошибка \_ недопустимого \_ адреса**
</dt> <dd> <dl> <dt>

487 (0x1E7)
</dt> <dt>



Попытка доступа к недопустимому адресу.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>WinError. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды системных ошибок](system-error-codes.md)
</dt> </dl>

 

 




