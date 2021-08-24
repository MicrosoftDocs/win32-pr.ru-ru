---
title: Поставщики систем
description: Включите события поставщика трассировки системы с помощью EnableTraceEx2.
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 46c141c6449594b8030ce24bb901b0afede33f3f6e2cefcaa36f4df4bf0dde0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812154"
---
# <a name="system-providers"></a>Поставщики систем
 
начиная с Windows 10 SDK сборки 20348, события поставщика трассировки системы могут быть включены так же, как другие поставщики ETW с [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).  Различные флаги и [маски групп](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) , связанные с системным поставщиком трассировки, были сопоставлены с новыми поставщиками трассировки, называемыми поставщиками систем, и совпадающими ключевыми словами.  
 
Как и непосредственное включение поставщика трассировки системы, поставщики систем можно включить только с помощью сеанса с набором [EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) .

## <a name="system-provider-reference"></a>Справочник по поставщику систем

* [Поставщик System ALPC](#system-alpc-provider)
* [Поставщик системных конфигураций](#system-config-provider)
* [Поставщик системных ЦП](#system-cpu-provider)
* [Поставщик низкоуровневой оболочки системы](#system-hypervisor-provider)
* [Поставщик системных прерываний](#system-interrupt-provider)
* [Поставщик системных операций ввода-вывода](#system-io-provider)
* [Поставщик фильтра ввода-вывода системы](#system-io-filter-provider)
* [Поставщик блокировки системы](#system-lock-provider)
* [Поставщик системной памяти](#system-memory-provider)
* [Поставщик системных объектов](#system-object-provider)
* [Системный поставщик питания](#system-power-provider)
* [Поставщик системных процессов](#system-process-provider)
* [Поставщик системного профиля](#system-profile-provider)
* [Поставщик системного реестра](#system-registry-provider)
* [Поставщик системного планировщика](#system-scheduler-provider)
* [Системный поставщик syscall](#system-syscall-provider)
* [Поставщик системного таймера](#system-timer-provider)
 
### <a name="system-alpc-provider"></a>Поставщик System ALPC

Предоставляет события, связанные с системой ALPC.

GUID: Системалпкпровидергуид {fcb9baaf-E529-4980-92e9-ced1a6aadfdf}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_ALPC_KW_GENERAL | PERF_ALPC, EVENT_TRACE_FLAG_ALPC |
 
### <a name="system-config-provider"></a>Поставщик системных конфигураций 

Предоставляет события конфигурации системы.

GUID: Системконфигпровидергуид {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_CONFIG_KW_SYSTEM | PERF_SYSCFG_SYSTEM |
| SYSTEM_CONFIG_KW_GRAPHICS | PERF_SYSCFG_GRAPHICS |
| SYSTEM_CONFIG_KW_STORAGE | PERF_SYSCFG_STORAGE |
| SYSTEM_CONFIG_KW_NETWORK | PERF_SYSCFG_NETWORK |
| SYSTEM_CONFIG_KW_SERVICES | PERF_SYSCFG_SERVICES |
| SYSTEM_CONFIG_KW_PNP | PERF_SYSCFG_PNP |
| SYSTEM_CONFIG_KW_OPTICAL | PERF_SYSCFG_OPTICAL |
 
### <a name="system-cpu-provider"></a>Поставщик системных ЦП 

Предоставляет события, связанные с ЦП.

GUID: Системкпупровидергуид {c6c5265f-eae8-4650-AAE4-9d48603d8510}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_CPU_KW_CONFIG | PERF_CPU_CONFIG |
| SYSTEM_CPU_KW_CACHE_FLUSH | PERF_CACHE_FLUSH |
| SYSTEM_CPU_KW_SPEC_CONTROL | PERF_SPEC_CONTROL |
 
### <a name="system-hypervisor-provider"></a>Поставщик низкоуровневой оболочки системы 

Предоставляет события, связанные с гипервизором.

GUID: Системхипервисорпровидергуид {bafa072a-918a-4bed-B622-bc152097098f}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_HYPERVISOR_KW_PROFILE | PERF_HV_PROFILE |
| SYSTEM_HYPERVISOR_KW_CALLOUTS | PERF_HV_CALLOUTS |
| SYSTEM_HYPERVISOR_KW_VTL_CHANGE | PERF_VTL_CHANGE |
 
### <a name="system-interrupt-provider"></a>Поставщик системных прерываний 

Предоставляет события, связанные с DPC и прерываниями.

GUID: Системинтерруптпровидергуид {d4bbee17-b545-4888-858b-744169015b25}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_INTERRUPT_KW_GENERAL | PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT |
| SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT | PERF_CLOCK_INTERRUPT |
| SYSTEM_INTERRUPT_KW_DPC | PERF_DPC, EVENT_TRACE_FLAG_DPC |
| SYSTEM_INTERRUPT_KW_DPC_QUEUE | PERF_DPC_QUEUE |
| SYSTEM_INTERRUPT_KW_WDF_DPC | PERF_WDF_DPC |
| SYSTEM_INTERRUPT_KW_WDF_INTERRUPT | PERF_WDF_INTERRUPT |
| SYSTEM_INTERRUPT_KW_IPI | PERF_IPI |
 
 
### <a name="system-io-provider"></a>Поставщик системных операций ввода-вывода 

Предоставляет события, связанные с несколькими типами операций ввода-вывода, включая диск, кэш и сеть.

GUID: Системиопровидергуид {3d5c43e3-0f1c-4202-b817-174c0070dc79}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_IO_KW_DISK | EVENT_TRACE_FLAG_DISK_IO |
| SYSTEM_IO_KW_DISK_INIT | PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT |
| SYSTEM_IO_KW_FILENAME | PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO |
| SYSTEM_IO_KW_SPLIT | PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO |
| SYSTEM_IO_KW_FILE | PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO |
| SYSTEM_IO_KW_OPTICAL | PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT |
| SYSTEM_IO_KW_OPTICAL_INIT | PERF_OPTICAL_IO_INIT |
| SYSTEM_IO_KW_DRIVERS | PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER |
| SYSTEM_IO_KW_CC | PERF_CC |
| SYSTEM_IO_KW_NETWORK | PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP |

Примечание. Включение ключевого слова SYSTEM_IO_KW_DRIVERS автоматически включит SYSTEM_IO_KW_FILENAME.  SYSTEM_IO_KW_FILENAME также автоматически включается при включении поставщика системной памяти с ключевым словом SYSTEM_MEMORY_KW_MEMORY.
 
### <a name="system-io-filter-provider"></a>Поставщик фильтра ввода-вывода системы 

Предоставляет события, связанные с фильтрацией операций ввода-вывода, включая время и сбои.

GUID: Системиофилтерпровидергуид {fbd09363-9e22-4661-b8bf-e7a34b535b8c}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_IOFILTER_KW_GENERAL | PERF_FLT_IO |
| SYSTEM_IOFILTER_KW_INIT | PERF_FLT_IO_INIT |
| SYSTEM_IOFILTER_KW_FASTIO | PERF_FLT_FASTIO |
| SYSTEM_IOFILTER_KW_FAILURE | PERF_FLT_IO_FAILURE |
 
### <a name="system-lock-provider"></a>Поставщик блокировки системы 

Предоставляет события, относящиеся к механизмам блокировки ядра.

GUID: Системлоккпровидергуид {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_LOCK_KW_SPINLOCK | PERF_SPINLOCK |
| SYSTEM_LOCK_KW_SPINLOCK_COUNTERS | PERF_SPINLOCK_CNTRS |
| SYSTEM_LOCK_KW_SYNC_OBJECTS | PERF_SYNC_OBJECTS |
 
### <a name="system-memory-provider"></a>Поставщик системной памяти 

Предоставляет события, относящиеся к диспетчеру памяти.

GUID: Системмеморипровидергуид {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_MEMORY_KW_GENERAL | PERF_MEMORY |
| SYSTEM_MEMORY_KW_HARD_FAULTS | PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS |
| SYSTEM_MEMORY_KW_ALL_FAULTS | PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS |
| SYSTEM_MEMORY_KW_POOL | PERF_POOL |
| SYSTEM_MEMORY_KW_MEMINFO | PERF_MEMINFO |
| SYSTEM_MEMORY_KW_PFSECTION | PERF_PFSECTION |
| SYSTEM_MEMORY_KW_MEMINFO_WS | PERF_MEMINFO_WS |
| SYSTEM_MEMORY_KW_HEAP | PERF_HEAP |
| SYSTEM_MEMORY_KW_WS | PERF_WS |
| SYSTEM_MEMORY_KW_CONTMEM_GEN | PERF_CONTMEM_GEN |
| SYSTEM_MEMORY_KW_VIRTUAL_ALLOC | PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC |
| SYSTEM_MEMORY_KW_FOOTPRINT | PERF_FOOTPRINT |
| SYSTEM_MEMORY_KW_SESSION | PERF_SESSION |
| SYSTEM_MEMORY_KW_REFSET | PERF_REFSET |
| SYSTEM_MEMORY_KW_VAMAP | PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP |

Примечания. 
* Включение ключевого слова SYSTEM_MEMORY_KW_MEMORY автоматически включит SYSTEM_IO_KW_FILENAME в системном поставщике ввода и вывода.
* События, включенные SYSTEM_MEMORY_KW_POOL, поддерживают фильтр тегов пула, чтобы выборочно записывать события только для определенных тегов пула.  Он настраивается в качестве [фильтра схематизированных](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) для поставщика системной памяти.  Фильтр Пултаг создается следующим образом:

    ```cpp
    {
    EVENT_FILTER_HEADER Header; 
    ULONG PoolTags[ETW_MAX_POOLTAG_FILTER];
    }
    ```

* [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) должны быть инициализированы с идентификатором, имеющим значение SYSTEM_MEMORY_POOL_FILTER_ID, а поле Size — размером заголовка и используемой части массива пултагс.  

* Каждый тег пула — это 4-символьная строка, которая хранится в фильтре в виде ULONG.  
 
 
### <a name="system-object-provider"></a>Поставщик системных объектов 

Предоставляет события, относящиеся к диспетчеру объектов.

GUID: Системобжектпровидергуид {febd7460-3d1d-47eb-af49-c9eeb1e146f2}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_OBJECT_KW_HANDLE | PERF_OB_HANDLE |
| SYSTEM_OBJECT_KW_OBJECT | PERF_OB_OBJECT |
 
### <a name="system-power-provider"></a>Системный поставщик питания 

Предоставляет события, относящиеся к системному состоянию питания.

GUID: Системповерпровидергуид {c134884a-32d5-4488-80e5-14ed7abb8269}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_POWER_KW_GENERAL | PERF_POWER |
| SYSTEM_POWER_KW_HIBER_RUNDOWN | PERF_HIBER_RUNDOWN |
| SYSTEM_POWER_KW_PROCESSOR_IDLE | PERF_PROCESSOR_IDLE |
| SYSTEM_POWER_KW_IDLE_SELECTION | PERF_IDLE_SELECTION |
| SYSTEM_POWER_KW_PPM_EXIT_LATENCY | PERF_PPM_EXIT_LATENCY |
 
### <a name="system-process-provider"></a>Поставщик системных процессов 

Предоставляет события, связанные с процессом, включая сведения о времени существования, событиях загрузки изображения и событиях, связанных с потоком.

GUID: Системпроцесспровидергуид {151f55dc-467d-471f-83b5-5f889d46ff66}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_PROCESS_KW_GENERAL | PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS |
| SYSTEM_PROCESS_KW_INSWAP | PERF_PROCESS_INSWAP |
| SYSTEM_PROCESS_KW_FREEZE | PERF_PROCESS_FREEZE |
| SYSTEM_PROCESS_KW_PERF_COUNTER | PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS |
| SYSTEM_PROCESS_KW_WAKE_COUNTER | PERF_WAKE_COUNTER |
| SYSTEM_PROCESS_KW_WAKE_DROP | PERF_WAKE_DROP |
| SYSTEM_PROCESS_KW_WAKE_EVENT | PERF_WAKE_EVENT |
| SYSTEM_PROCESS_KW_DEBUG_EVENTS | PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS |
| SYSTEM_PROCESS_KW_DBGPRINT | PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT |
| SYSTEM_PROCESS_KW_JOB | PERF_JOB, EVENT_TRACE_FLAG_JOB |
| SYSTEM_PROCESS_KW_WORKER_THREAD | PERF_WORKER_THREAD |
| SYSTEM_PROCESS_KW_THREAD | PERF_THREAD, EVENT_TRACE_FLAG_THREAD |
| SYSTEM_PROCESS_KW_LOADER | PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD |
 
### <a name="system-profile-provider"></a>Поставщик системного профиля 

Предоставляет события профилирования.

GUID: Системпрофилепровидергуид {bfeb0324-1cee-496f-A409-2ac2b48a6322}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_PROFILE_KW_GENERAL | PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE |
| SYSTEM_PROFILE_KW_PMC_PROFILE | PERF_PMC_PROFILE |
 
### <a name="system-registry-provider"></a>Поставщик системного реестра 

Предоставляет события, относящиеся к реестру.

GUID: Системрегистрипровидергуид {16156bd9-fab4-4cfa-a232-89d1099058e3}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_REGISTRY_KW_GENERAL | PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY |
| SYSTEM_REGISTRY_KW_HIVE | PERF_REG_HIVE |
| SYSTEM_REGISTRY_KW_NOTIFICATION | PERF_REG_NOTIF |
 
### <a name="system-scheduler-provider"></a>Поставщик системного планировщика 

Предоставляет события, связанные с планировщиком.

GUID: Системсчедулерпровидергуид {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_SCHEDULER_KW_XSCHEDULER | PERF_XSCHEDULER |
| SYSTEM_SCHEDULER_KW_DISPATCHER | PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER |
| SYSTEM_SCHEDULER_KW_KERNEL_QUEUE | PERF_KERNEL_QUEUE |
| SYSTEM_SCHEDULER_KW_SHOULD_YIELD | PERF_SHOULD_YIELD |
| SYSTEM_SCHEDULER_KW_ANTI_STARVATION | PERF_ANTI_STARVATION |
| SYSTEM_SCHEDULER_KW_LOAD_BALANCER | PERF_LOAD_BALANCER |
| SYSTEM_SCHEDULER_KW_AFFINITY | PERF_AFFINITY |
| SYSTEM_SCHEDULER_KW_PRIORITY | PERF_PRIORITY |
| SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR | PERF_IDEAL_PROCESSOR |
| SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH | PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH |
 
### <a name="system-syscall-provider"></a>Системный поставщик syscall 

Предоставляет события со сведениями о системных вызовах.

GUID: Системсискаллпровидергуид {434286f7-6f1b-45bb-b37e-95f623046c7c}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_SYSCALL_KW_GENERAL | PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL |
 
### <a name="system-timer-provider"></a>Поставщик системного таймера 

Предоставляет события, относящиеся к таймерам в ядре.

GUID: Системтимерпровидергуид {4f061568-e215-499f-ab2e-eda0ae890a5b}

| Ключевое слово | Соответствующие устаревшие флаги и группы |
| ------- | ------------------------------------- |
| SYSTEM_TIMER_KW_GENERAL | PERF_TIMER |
| SYSTEM_TIMER_KW_CLOCK_TIMER | PERF_CLOCK_TIMER |
 
## <a name="remarks"></a>Remarks

Этот новый механизм включения является дополнением к уже существующим методам для включения этих событий.  Любой код, который использовался для работы, продолжит это.
 
События, создаваемые поставщиком трассировки системы, не изменяются из-за этой новой функции.  Это означает, что выводимые события не помечаются как порожденные от поставщиков отдельных систем.
 
Дополнительные сведения о GUID поставщика и определениях ключевых слов см. в разделе [евнтраце. h](/windows/win32/api/evntrace/).

## <a name="see-also"></a>См. также:

[Настройка и запуск сеанса Системтрацепровидер](configuring-and-starting-a-systemtraceprovider-session.md)

[заголовок евнтраце. h](/windows/win32/api/evntrace/)