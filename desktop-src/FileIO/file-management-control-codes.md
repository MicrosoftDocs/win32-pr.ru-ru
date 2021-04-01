---
description: Управляющие коды, используемые в управлении файлами.
ms.assetid: e27ded4b-d104-4244-b38e-5fed10d32e1e
title: Управляющие коды для управления файлами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cb3baf78c4066a640242afe8465592bc9a6f8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912860"
---
# <a name="file-management-control-codes"></a>Управляющие коды для управления файлами

В управлении файлами используются следующие управляющие коды.

## <a name="in-this-section"></a>Содержание раздела



| Контрольный код                                                                                    | Описание                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ФСКТЛ \_ Разрешить \_ Расширенные \_ \_ операции ввода-вывода дасд**](/windows/win32/api/winioctl/ni-winioctl-fsctl_allow_extended_dasd_io)<br/>             | Сообщает драйверу файловой системы, что не нужно выполнять проверку границ операций ввода-вывода при вызове секций чтения или записи.<br/>                                                                                  |
| [**ФСКТЛ \_ Создание \_ или \_ Получение \_ \_ идентификатора объекта**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)<br/>          | Возвращает идентификатор объекта для указанного файла или каталога. Если идентификатор объекта не существует, используется **фсктл \_ Create \_ или \_ Get \_ Object \_ ID** .<br/>                           |
| [**\_ \_ элемент управления CSV фсктл**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control)<br/>                                     | Возвращает результаты операции элемента управления CSV.<br/>                                                                                                                                        |
| [**ФСКТЛ \_ удалить \_ \_ идентификатор объекта**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)<br/>                          | Удаляет идентификатор объекта из указанного файла или каталога.<br/>                                                                                                                        |
| [**ФСКТЛ \_ дубликаты \_ экстентов \_ в \_ файл**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)<br/>       | Указывает файловой системе копировать диапазон байт файлов от имени приложения.<br/>                                                                                                     |
| [**ФСКТЛ \_ \_ обрезать на уровне файлов \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_file_level_trim)<br/>                            | Указывает системе хранения, что диапазоны в файле не нужны для хранения.<br/>                                                                                                    |
| [**\_ \_ Получение статистики файловой \_ системы фсктл**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics)<br/>        | Извлекает сведения из различных счетчиков производительности файловой системы.<br/>                                                                                                                 |
| [**ФСКТЛ \_ FILESYSTEM \_ Получение \_ статистики, \_ ex**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics_ex)<br/> | Извлекает сведения из различных счетчиков производительности файловой системы.<br/> Поддержка этого кода элемента управления начинается с Windows 10.<br/>                                               |
| [**ФСКТЛ \_ найти \_ файлы \_ по \_ идентификатору безопасности**](/windows/win32/api/winioctl/ni-winioctl-fsctl_find_files_by_sid)<br/>                       | Ищет в каталоге файл, владелец создателя которого соответствует указанному идентификатору безопасности.<br/>                                                                                                           |
| [**ФСКТЛ \_ получить \_ Сжатие**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)<br/>                             | Извлекает текущее состояние сжатия файла или каталога на томе, файловая система которого поддерживает сжатие на поток.<br/>                                                            |
| [**ФСКТЛ \_ получить \_ \_ запись файла \_ NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_file_record)<br/>                 | Извлекает первую используемую запись файла и имеет меньшее или равное порядковое значение, чем запрошенный номер ссылки на файл.<br/>                                                    |
| [**ФСКТЛ \_ получить \_ \_ идентификатор объекта**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)<br/>                                | Возвращает идентификатор объекта для указанного файла или каталога.<br/>                                                                                                                     |
| [**ФСКТЛ \_ получить \_ восстановление**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)<br/>                                       | Извлекает сведения о механизме самостоятельной восстановления файловой системы NTFS.<br/>                                                                                                               |
| [**ФСКТЛ \_ инициировать \_ восстановление**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)<br/>                             | Запускает файловую систему NTFS для запуска цикла самовосстановления в одном файле.<br/>                                                                                                            |
| [**ФСКТЛ \_ сделать \_ носитель \_ совместимым**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)<br/>                | Закрывает открытый сеанс UDF на носителе с однократным входом для обеспечения совместимости с Media ROM.<br/>                                                                                                         |
| [**\_ \_ \_ Ожидание закрытия фсктл опбатч ACK \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)<br/>       | Уведомляет сервер о том, что клиентское приложение готово к закрытию файла.<br/>                                                                                                                    |
| [**ФСКТЛ \_ OPLOCK \_ break \_ ACK \_ No \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)<br/>              | Реагирует на уведомление о том, что оппортунистическая блокировка файла собирается быть нарушена. Используйте эту операцию, чтобы разблокировать все оппортунистической блокировки файла, но не закрывайте файл.<br/>            |
| [**ФСКТЛ \_ OPLOCK \_ break, \_ подтверждение**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)<br/>          | Реагирует на уведомление о том, что монопольная оппортунистическая блокировка файла собирается быть нарушена. Используйте эту операцию, чтобы указать, что файл должен получить уступающую блокировку уровня 2.<br/> |
| [**\_ \_ уведомление о разрыве фсктл OPLOCK \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)<br/>                    | Позволяет вызывающему приложению ожидать завершения оппортунистической блокировки.<br/>                                                                                                   |
| [**ФСКТЛ \_ \_ выделенные \_ диапазоны запросов**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)<br/>              | Сканирует файл или альтернативный поток для поиска диапазонов, которые могут содержать ненулевые данные.<br/>                                                                                                       |
| [**ФСКТЛ \_ запрос \_ к \_ \_ \_ сведениям о томе диска**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)<br/>      | Запрашивает сведения о томе, относящиеся к определяемой пользователем функции.<br/>                                                                                                                                                |
| [**\_ \_ сведения о резервировании запросов фсктл \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)<br/>                      | Извлекает свойства управления исключениями для тома. Используется для файловых систем UDF.<br/>                                                                                                     |
| [**\_файл ОТЗЫВА \_ фсктл**](/windows/win32/api/winioctl/ni-winioctl-fsctl_recall_file)<br/>                                     | Вызывает файл из носителя хранилища, который управляется удаленным хранилищем и представляет собой иерархическое программное обеспечение для управления хранилищем.<br/>                                                                    |
| [**\_ \_ Пакетная блокировка запроса фсктл \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)<br/>                  | Запрашивает уступающую блокировку файла в пакете.<br/>                                                                                                                                           |
| [**ФСКТЛ \_ запрос \_ фильтрации \_ оппортунистической блокировки**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)<br/>                | Запрашивает фильтр оппортунистической блокировки файла.<br/>                                                                                                                                          |
| [**\_ \_ нежесткая блокировка запроса фсктл**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)<br/>                               | Запрашивает уступающую блокировку (Oplock) для файла и подтверждает, что произошла нежесткая блокировка.<br/>                                                                                    |
| [**\_Запрос фсктл \_ уровень жесткой блокировки \_ \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)<br/>             | Запрашивает уступающую блокировку уровня 1 для файла.<br/>                                                                                                                                         |
| [**\_Запрос фсктл \_ уровень жесткой блокировки \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)<br/>             | Запрашивает уступающую блокировку уровня 2 для файла.<br/>                                                                                                                                         |
| [**ФСКТЛ \_ Установка \_ сжатия**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                             | Задает состояние сжатия файла или каталога на томе, файловая система которого поддерживает сжатие на уровне файлов и на уровне каталога.<br/>                                                         |
| [**ФСКТЛ \_ Задание \_ управления дефектами \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)<br/>                | Задает состояние управления дефектами программного обеспечения для указанного файла. Используется для файловых систем UDF.<br/>                                                                                             |
| [**ФСКТЛ \_ задать \_ \_ идентификатор объекта**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)<br/>                                | Задает идентификатор объекта для указанного файла или каталога.<br/>                                                                                                                          |
| [**ФСКТЛ \_ \_ идентификатор объекта \_ для \_ расширенного набора данных**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)<br/>             | Изменяет пользовательские данные, связанные с идентификатором объекта для указанного файла или каталога.<br/>                                                                                            |
| [**ФСКТЛ \_ Set \_ Repair**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)<br/>                                       | Устанавливает режим возможности самостоятельной восстановления файловой системы NTFS.<br/>                                                                                                                          |
| [**ФСКТЛ \_ установить \_ разреженность**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)<br/>                                       | Помечает указанный файл как разреженный или неразреженный. В разреженном файле большие диапазоны нулей могут не требовать выделения места на диске.<br/>                                                               |
| [**ФСКТЛ \_ установить \_ нулевые \_ данные**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)<br/>                                | Заполняет указанный диапазон файла нулями (0).<br/>                                                                                                                                        |
| [**ФСКТЛ \_ установить \_ нулевое значение \_ при \_ освобождении**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_on_deallocation)<br/>         | Указывает, что при освобождении кластеров файловая система файловой системы NTFS должна быть заполнена нулями.<br/>                                                                             |
| [**ФСКТЛ \_ Ожидание \_ \_ восстановления**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)<br/>                            | Возвращает, когда заданные исправления завершены.<br/>                                                                                                                                        |



 

При [сжатии и](file-compression-and-decompression.md)распаковке файлов используются следующие управляющие коды.

<dl>

[**ФСКТЛ \_ получить \_ Сжатие**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)  
[**ФСКТЛ \_ Установка \_ сжатия**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)  
</dl>

С [идентификаторами объектов](distributed-link-tracking-and-object-identifiers.md)используются следующие управляющие коды.

<dl>

[**ФСКТЛ \_ Создание \_ или \_ Получение \_ \_ идентификатора объекта**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)  
[**ФСКТЛ \_ удалить \_ \_ идентификатор объекта**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)  
[**ФСКТЛ \_ получить \_ \_ идентификатор объекта**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)  
[**ФСКТЛ \_ задать \_ \_ идентификатор объекта**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)  
[**ФСКТЛ \_ \_ идентификатор объекта \_ для \_ расширенного набора данных**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)  
</dl>

Для [уступающей блокировки](opportunistic-locks.md)используются следующие управляющие коды.

<dl>

[**\_ \_ \_ Ожидание закрытия фсктл опбатч ACK \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**ФСКТЛ \_ OPLOCK \_ break \_ ACK \_ No \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**ФСКТЛ \_ OPLOCK \_ break, \_ подтверждение**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**\_ \_ уведомление о разрыве фсктл OPLOCK \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**\_ \_ Пакетная блокировка запроса фсктл \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**ФСКТЛ \_ запрос \_ фильтрации \_ оппортунистической блокировки**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**\_ \_ нежесткая блокировка запроса фсктл**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**\_Запрос фсктл \_ уровень жесткой блокировки \_ \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**\_Запрос фсктл \_ уровень жесткой блокировки \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

Для [разреженных файлов](sparse-files.md)используются следующие управляющие коды.

<dl>

[**ФСКТЛ \_ \_ выделенные \_ диапазоны запросов**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)  
[**ФСКТЛ \_ установить \_ разреженность**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)  
[**ФСКТЛ \_ установить \_ нулевые \_ данные**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)  
</dl>

С механизмом самостоятельной восстановления файловой системы NTFS используются следующие управляющие коды.

<dl>

[**ФСКТЛ \_ получить \_ восстановление**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)  
[**ФСКТЛ \_ инициировать \_ восстановление**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)  
[**ФСКТЛ \_ Set \_ Repair**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)  
[**ФСКТЛ \_ Ожидание \_ \_ восстановления**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)  
</dl>

Для UDF используются следующие управляющие коды.

<dl>

[**ФСКТЛ \_ сделать \_ носитель \_ совместимым**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)  
[**ФСКТЛ \_ запрос \_ к \_ \_ \_ сведениям о томе диска**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)  
[**\_ \_ сведения о резервировании запросов фсктл \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)  
[**ФСКТЛ \_ Задание \_ управления дефектами \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)  
</dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Управляющие коды управления каталогами](directory-management-control-codes.md)
</dt> <dt>

[Управляющие коды для управления томами](volume-management-control-codes.md)
</dt> </dl>

 

