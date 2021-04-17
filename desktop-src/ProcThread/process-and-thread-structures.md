---
description: В этом разделе перечислены структуры, которые используются с процессами, потоками, процессорами, объектами заданий и планированием пользовательского режима (UMS).
ms.assetid: dbb50193-4c67-494e-9c46-2ac3106fac9a
title: Структуры процессов и потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59b2b4a8209c3f1f9fb3163c849fa2c229d2bdf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673750"
---
# <a name="process-and-thread-structures"></a>Структуры процессов и потоков

В этом разделе перечислены структуры, которые используются с процессами, потоками, процессорами, объектами заданий и планированием пользовательского режима (UMS).

## <a name="process-and-thread-structures"></a>Структуры процессов и потоков

Для процессов и потоков используются следующие структуры:

-   [**\_ \_ сведения о памяти приложения**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [**\_состояние AR**](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [**\_дескриптор кэша**](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [**Счетчики ввода-вывода \_**](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [**\_предпочтения ориентации**](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [**пеб**](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [**\_данные пеб LDR \_**](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [**\_сведения о процессе**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [**\_ \_ \_ сведения о НЕхватке памяти процесса**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [**\_ \_ Политика ASLR для обработки \_ рисков**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [**\_ \_ Политика двоичной \_ подписи для процесса устранения рисков \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [**\_ \_ \_ \_ Политика защиты потока управления для процесса устранения рисков \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [**\_Политика DEP для устранения рисков \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [**\_ \_ \_ Политика динамического кода для устранения \_ рисков**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [**\_ \_ \_ \_ Политика отключения точки расширения процесса устранения рисков \_**](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [**\_ \_ \_ Политика отключения шрифтов для преодоления процессов \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [**\_ \_ \_ Политика загрузки образа для устранения рисков процесса \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [**\_ \_ Политика проверки ограниченного \_ управления процессами устранения рисков \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [**\_ \_ Политика отключения обработки системных \_ вызовов \_ для устранения рисков \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [**\_Параметры пользовательского \_ процесса \_ RTL**](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [**стартупинфоекс**](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [**TEB**](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a>Структуры процессора

Для процессоров и групп процессоров используются следующие структуры:

-   [**\_связь кэша**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [**\_сходство групп**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [**\_отношение группы**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [**\_отношение узла \_ NUMA**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [**\_сведения о группе процессоров \_**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [**\_номер процессора**](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [**связь ПРОЦЕССОРов \_**](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [**\_ \_ сведения о настройке ЦП системы \_**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [**\_ \_ сведения о логическом ПРОЦЕССОРе системы \_**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [**\_ \_ сведения о логическом ПРОЦЕССОРе системы, \_ \_ ex**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a>Структура очереди диспетчера

Для создания [диспатчеркуеуеконтроллер](/uwp/api/windows.system.dispatcherqueuecontroller)используется следующая структура.

-   [**диспатчеркуеуеоптионс**](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a>Структуры объектов заданий

Для объектов заданий используются следующие структуры:

-   [**\_ \_ порт завершения привязки \_ жобобжект**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [**ЖОБОБЖЕКТ \_ основные \_ \_ сведения о учете**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**\_ \_ \_ \_ учетные данные жобобжект Basic и IO \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [**\_ \_ сведения о базовом ОГРАНИЧЕНии жобобжект \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**\_ \_ \_ список идентификаторов процессов жобобжект Basic \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [**\_базовые \_ ограничения ПОЛЬЗОВАТЕЛЬСКОГО интерфейса \_ жобобжект**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**ЖОБОБЖЕКТ \_ конец \_ \_ \_ сведений о времени выполнения задания \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [**\_ \_ сведения о расширенном ОГРАНИЧЕНии жобобжект \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**\_ \_ сведения об ограничении безопасности жобобжект \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a>Структуры планирования User-Mode

С UMS используются следующие структуры:

-   [**\_Создание \_ атрибутов потока \_ для UMS**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [**\_ \_ сведения о запуске ПЛАНИРОВЩИКа UMS \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [**\_ \_ сведения о системном ПОТОКе UMS \_**](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
