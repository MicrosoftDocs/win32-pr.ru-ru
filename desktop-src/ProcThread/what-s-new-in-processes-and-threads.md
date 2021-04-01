---
description: Windows 7 и Windows Server 2008 R2 включают в себя следующие новые программные элементы для процессов и потоков.
ms.assetid: 69cd8713-b40c-4fec-a256-9c2ee3d73da5
title: Новые возможности в процессах и потоках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7dfb708a2890bab1fcd3fd66385f74bd8513b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909663"
---
# <a name="whats-new-in-processes-and-threads"></a>Новые возможности в процессах и потоках

Windows 7 и Windows Server 2008 R2 включают в себя следующие новые программные элементы для процессов и потоков.

## <a name="new-capabilities"></a>Новые возможности

64-разрядные версии Windows 7 и Windows Server 2008 R2 поддерживают более 64 логических процессоров на одном компьютере. Дополнительные сведения см. в разделе [группы процессоров](processor-groups.md).

Планирование пользовательского режима (UMS) — это упрощенный механизм, с помощью которого приложения могут планировать собственные потоки. Дополнительные сведения см. в разделе [Планирование пользовательского режима](user-mode-scheduling.md).

## <a name="new-functions"></a>Новые функции

Следующие новые функции используются с процессорами и группами процессоров.



| Функция                                                                                | Описание                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**креатеремотесреадекс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)<br/>                         | Создает поток, который выполняется в виртуальном адресном пространстве другого процесса и дополнительно задает расширенные атрибуты, такие как сходство групп процессоров.<br/> |
| [**жетактивепроцессоркаунт**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)<br/>                   | Возвращает число активных процессоров в группе процессоров или в системе.<br/>                                                                            |
| [**жетактивепроцессорграупкаунт**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)<br/>         | Возвращает число активных групп процессоров в системе.<br/>                                                                                              |
| [**жеткуррентпроцессорнумберекс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)<br/>           | Извлекает группу процессоров и номер логического процессора, в котором выполняется вызывающий поток.<br/>                                                 |
| [**жетлогикалпроцессоринформатионекс**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex)<br/> | Извлекает сведения о связях логических процессоров и связанного оборудования.<br/>                                                                 |
| [**жетмаксимумпроцессоркаунт**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)<br/>                 | Возвращает максимальное число логических процессоров, которое может иметь группа процессоров или система.<br/>                                                           |
| [**жетмаксимумпроцессорграупкаунт**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)<br/>       | Возвращает максимальное число групп процессоров, которое может иметь система. <br/>                                                                                 |
| [**жетнумааваилаблемеморинодикс**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)<br/>         | Извлекает объем памяти, доступный в указанном узле, в виде значения USHORT.<br/>                                                                 |
| [**жетнуманоденумберфромхандле**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)<br/>           | Извлекает узел NUMA, связанный с базовым устройством, для маркера файла.<br/>                                                                          |
| [**жетнуманодепроцессормаскекс**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)<br/>             | Извлекает маску процессора для указанного узла NUMA в виде значения USHORT.<br/>                                                                               |
| [**жетнумапроцессорнодикс**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)<br/>                     | Получает номер узла указанного логического процессора в виде значения USHORT.<br/>                                                                           |
| [**жетнумапроксимитинодикс**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)<br/>                     | Получает номер узла в виде значения USHORT для указанного идентификатора близости.<br/>                                                                       |
| [**жетпроцессграупаффинити**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)<br/>                   | Возвращает сходство группы процессоров указанного процесса.<br/>                                                                                          |
| [**жетпроцессорсистемциклетиме**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)<br/>           | Возвращает время цикла каждого процессора в указанной группе, затраченного на выполнение отложенных вызовов процедур (DPC) и процедур службы прерываний (ISR).<br/>     |
| [**жетсреадграупаффинити**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)<br/>                     | Возвращает соответствие группы процессоров указанному потоку.<br/>                                                                                           |
| [**жетсреадидеалпроцессорекс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)<br/>               | Возвращает номер процессора идеального процессора для указанного потока.<br/>                                                                           |
| [**куеридлепроцессорциклетимикс**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)<br/>       | Извлекает накопленное время цикла для бездействующего потока на каждом логическом процессоре в указанной группе процессоров. <br/>                                     |
| [**сетсреадграупаффинити**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)<br/>                     | Задает сходство групп процессоров для указанного потока.<br/>                                                                                               |
| [**сетсреадидеалпроцессорекс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)<br/>               | Задает идеальный процессор для указанного потока и при необходимости извлекает предыдущий идеальный процессор.<br/>                                                  |



 

Следующие новые функции используются с пулами потоков.



| Функция                                                                              | Описание                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**куерисреадпулстаккинформатион**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)<br/> | Возвращает размеры резерва стека и фиксации для потоков в указанном пуле потоков.<br/>              |
| [**сетсреадпулкаллбаккперсистент**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)<br/> | Указывает, что обратный вызов должен выполняться в постоянном потоке.<br/>                                      |
| [**сетсреадпулкаллбаккприорити**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)<br/>     | Указывает приоритет функции обратного вызова относительно других рабочих элементов в том же пуле потоков.<br/> |
| [**сетсреадпулстаккинформатион**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)<br/>     | Устанавливает размер резервирования и фиксации стека для новых потоков в указанном пуле потоков. <br/>              |



 

Следующие новые функции используются с UMS.



| Функция                                                                          | Описание                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**креатеумскомплетионлист**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)<br/>             | Создает список завершения UMS.<br/>                                                                     |
| [**креатеумссреадконтекст**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)<br/>               | Создает контекст потока UMS для представления рабочего потока UMS.<br/>                                     |
| [**делетеумскомплетионлист**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)<br/>             | Удаляет указанный список завершения UMS. Список должен быть пустым.<br/>                                 |
| [**делетеумссреадконтекст**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)<br/>               | Удаляет указанный контекст потока UMS. Поток должен быть завершен.<br/>                           |
| [**декуеуеумскомплетионлиститемс**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems)<br/> | Извлекает рабочие потоки UMS из указанного списка завершения UMS.<br/>                               |
| [**ентерумссчедулингмоде**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)<br/>               | Преобразует вызывающий поток в поток планировщика UMS.<br/>                                           |
| [**ексекутеумссреад**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)<br/>                           | Запускает указанный рабочий поток UMS.<br/>                                                              |
| [**жеткуррентумссреад**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)<br/>                     | Возвращает контекст потока UMS вызывающего потока UMS.<br/>                                          |
| [**жетнекстумслиститем**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)<br/>                       | Возвращает следующий контекст потока UMS в списке контекстов потоков UMS.<br/>                              |
| [**жетумскомплетионлистевент**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)<br/>         | Извлекает маркер события, связанного с указанным списком завершения UMS.<br/>                 |
| [**куерюмссреадинформатион**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)<br/>         | Извлекает сведения о указанном рабочем потоке UMS.<br/>                                       |
| [**сетумссреадинформатион**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)<br/>             | Задает зависящую от приложения контекстную информацию для указанного рабочего потока UMS.<br/>                 |
| [*умссчедулерпрок*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)<br/>                             | Определяемая приложением функция точки входа планировщика UMS, связанная с списком завершения UMS. <br/> |
| [**умссреадиелд**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)<br/>                               | Передает управление потоку планировщика UMS, в котором работает вызывающий рабочий поток UMS.<br/>      |



 

## <a name="new-structures"></a>Новые структуры



| Структура                                                                                                 | Описание                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**\_связь кэша**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)<br/>                                              | Описывает атрибуты кэша. <br/>                                                             |
| [**\_сходство групп**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)<br/>                                                      | Содержит сходство для определенной группы процессоров, например сходство потока.<br/>          |
| [**\_отношение группы**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)<br/>                                              | Содержит сведения о группах процессоров. <br/>                                            |
| [**\_отношение узла \_ NUMA**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)<br/>                                     | Содержит сведения об узле NUMA в группе процессоров. <br/>                            |
| [**\_сведения о группе процессоров \_**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)<br/>                                         | Содержит число и сходство процессоров в группе процессоров.<br/>                     |
| [**\_номер процессора**](/windows/desktop/api/WinNT/ns-winnt-processor_number)<br/>                                                  | Представляет логический процессор в группе процессоров.<br/>                                     |
| [**связь ПРОЦЕССОРов \_**](/windows/desktop/api/WinNT/ns-winnt-processor_relationship)<br/>                                      | Содержит сведения о сходстве в пределах группы процессоров.<br/>                            |
| [**\_ \_ сведения о логическом ПРОЦЕССОРе системы, \_ \_ ex**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)<br/> | Содержит сведения о связях логических процессоров и связанного оборудования.<br/> |
| [**\_Создание \_ атрибутов потока \_ для UMS**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)<br/>                        | Задает атрибуты для потока UMS Worker. <br/>                                           |
| [**\_ \_ сведения о запуске ПЛАНИРОВЩИКа UMS \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)<br/>                            | Задает атрибуты для потока планировщика UMS<br/>                                          |



 

 

 
