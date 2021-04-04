---
description: Перечисления, используемые в управлении файлами.
ms.assetid: 14b1cfff-5e47-4309-8e62-fb5c8da9ce97
title: Перечисления управления файлами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b53d8f53bf9dbe16c15d21171e52ea3dd0015d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999409"
---
# <a name="file-management-enumerations"></a>Перечисления управления файлами

В управлении файлами используются следующие перечисления.

## <a name="in-this-section"></a>Содержание раздела



| Перечисление                                                                   | Описание                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Стадия копирования \_ COPYFILE2**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_copy_phase)<br/>             | Указывает фазу копирования на момент возникновения ошибки.<br/>                                                                                                                                                                           |
| [**\_Действие сообщения \_ COPYFILE2**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_action)<br/>     | Возвращается функцией обратного вызова [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine) , чтобы указать, какое действие следует предпринять для операции, ожидающей копирования.<br/>                                                             |
| [**\_Тип сообщений \_ COPYFILE2**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_type)<br/>         | Указывает тип сообщения, переданного в структуре [**\_ сообщения COPYFILE2**](/windows/desktop/api/WinBase/ns-winbase-copyfile2_message) в функцию обратного вызова [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine) .<br/>                                       |
| [**\_операция управления \_ CSV**](/windows/desktop/api/WinIoCtl/ne-winioctl-csv_control_op)<br/>                         | Задает тип операции управления CSV для использования с управляющим кодом [**\_ \_ элемента управления CSV фсктл**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control) .<br/>                                                                                                       |
| [**\_тип идентификатора \_ файла**](/windows/desktop/api/WinBase/ne-winbase-file_id_type)<br/>                             | Дискриминатор для объединения в структуре [**\_ \_ дескриптора идентификатора файла**](/windows/desktop/api/WinBase/ns-winbase-file_id_descriptor) .<br/>                                                                                                                                 |
| [**\_сведения о \_ файле \_ по \_ классу Handle**](/windows/win32/api/minwinbase/ne-minwinbase-file_info_by_handle_class)<br/> | Определяет тип сведений о файле, которые должны извлекаться или [**сетфилеинформатионбихандлеся**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle) [**жетфилеинформатионбихандликс**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex) .<br/>                |
| [**\_уровни информации \_ Финдекс**](/windows/win32/api/minwinbase/ne-minwinbase-findex_info_levels)<br/>             | Определяет значения, используемые с функцией [**финдфирстфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) для указания информационного уровня возвращаемых данных.<br/>                                                                                 |
| [**ФИНДЕКС \_ поисковых \_ операций**](/windows/win32/api/minwinbase/ne-minwinbase-findex_search_ops)<br/>               | Определяет значения, используемые с функцией [**финдфирстфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) для указания типа фильтрации для выполнения.<br/>                                                                                           |
| [**ПОЛУЧЕНИЕ \_ \_ уровней информации \_ филикс**](/windows/win32/api/minwinbase/ne-minwinbase-get_fileex_info_levels)<br/>        | Определяет значения, используемые с функциями [**сбой getfileattributesex**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) и [**жетфилеаттрибутестрансактед**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda) для указания информационного уровня возвращаемых данных.<br/> |
| [**Указание ПРИОРИТЕТа \_**](/windows/desktop/api/WinBase/ne-winbase-priority_hint)<br/>                            | Определяет значения, используемые с структурой [**\_ \_ \_ \_ сведений о указании приоритета файлового ввода**](/windows/desktop/api/WinBase/ns-winbase-file_io_priority_hint_info) -вывода, чтобы указать указание приоритета для операции файлового ввода/вывода.<br/>                                                      |
| [**\_информационные \_ уровни потока**](/windows/desktop/api/fileapi/ne-fileapi-stream_info_levels)<br/>                 | Определяет значения, используемые с функцией [**финдфирстстреамв**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) для указания информационного уровня возвращаемых данных.<br/>                                                                               |



 

 

