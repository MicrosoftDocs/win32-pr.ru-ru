---
description: Традиционная модель многопроцессорной поддержки — это симметричный многопроцессорный (SMP). В этой модели каждый процессор имеет равный доступ к памяти и операциям ввода-вывода. По мере добавления процессоров процессорная шина преобразуется в ограничение производительности системы.
ms.assetid: a1263968-2b26-45cc-bdd7-6aa354821a5a
title: Поддержка NUMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178f53c6b55b6ae291cd5cdcf99386515a441094
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549809"
---
# <a name="numa-support"></a>Поддержка NUMA

Традиционная модель многопроцессорной поддержки — это симметричный многопроцессорный (SMP). В этой модели каждый процессор имеет равный доступ к памяти и операциям ввода-вывода. По мере добавления процессоров процессорная шина преобразуется в ограничение производительности системы.

Конструкторы систем используют неоднородный доступ к памяти (NUMA) для увеличения скорости процессора без увеличения нагрузки на процессорную шину. Архитектура является неоднородной, так как каждый процессор близко к некоторым частям памяти и более отдален от других частей памяти. Процессор быстро получает доступ к памяти, к которой он близок, в то время как может потребоваться больше времени для получения доступа к памяти, которая находится дальше.

В системе NUMA процессоры размещаются в небольших системах, именуемых *узлами*. Каждый узел имеет свои собственные процессоры и память и подключается к более крупной системе через шину Interconnect, ориентированную на кэш.

Система пытается повысить производительность, планируя потоки на процессорах, которые находятся в том же узле, что и используемая память. Он пытается удовлетворить запросы на выделение памяти в пределах узла, но при необходимости выделит память с других узлов. Он также предоставляет API, чтобы сделать топологию системы доступной для приложений. Вы можете повысить производительность приложений с помощью функций NUMA, чтобы оптимизировать планирование и использование памяти.

Во – первых, необходимо определить макет узлов в системе. Чтобы получить узел с наибольшим номером в системе, используйте функцию [**жетнумахигхестноденумбер**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber) . Обратите внимание, что это число не гарантировано равно общему количеству узлов в системе. Кроме того, не гарантируется, что узлы с последовательными числами близки друг к другу. Чтобы получить список процессоров в системе, используйте функцию [**жетпроцессаффинитимаск**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) . Вы можете определить узел для каждого процессора в списке с помощью функции [**жетнумапроцессорноде**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode) . Кроме того, чтобы получить список всех процессоров в узле, используйте функцию [**жетнуманодепроцессормаск**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask) .

После определения того, какие процессоры принадлежат какому узлу, можно оптимизировать производительность приложения. Чтобы убедиться, что все потоки процесса выполняются на одном узле, используйте функцию [**сетпроцессаффинитимаск**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) с маской сходства процессов, указывающей процессоры в одном узле. Это повышает эффективность приложений, потоки которых должны иметь доступ к одной и той же памяти. Кроме того, чтобы ограничить количество потоков на каждом узле, используйте функцию [**сетсреадаффинитимаск**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) .

Приложения, интенсивно использующие память, должны оптимизировать использование памяти. Чтобы получить объем свободной памяти, доступной для узла, используйте функцию [**жетнумааваилаблемемориноде**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode) . Функция [**виртуалаллоцекснума**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) позволяет приложению указать предпочитаемый узел для выделения памяти. **Виртуалаллоцекснума** не выделяет физические страницы, поэтому она будет выполнена, независимо от того, доступны ли страницы на этом узле или в других местах системы. Физические страницы выделяются по запросу. Если на предпочитаемом узле не хватает страниц, диспетчер памяти будет использовать страницы из других узлов. Если память выведена из памяти, то тот же процесс используется при возвращении.

### <a name="numa-support-on-systems-with-more-than-64-logical-processors"></a>Поддержка NUMA в системах с более чем 64 логическими процессорами

В системах с более чем 64 логическими процессорами узлы назначаются [группам процессоров](processor-groups.md) в соответствии с емкостью узлов. Емкость узла — это количество процессоров, имеющихся при запуске системы вместе со всеми дополнительными логическими процессорами, которые могут быть добавлены во время работы системы.

Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Группы процессоров не поддерживаются.

Каждый узел должен быть полностью включен в группу. Если емкость узлов относительно мала, система назначает несколько узлов одной группе и выбирает узлы, которые физически близки друг к другу для повышения производительности. Если емкость узла превышает максимальное число процессоров в группе, система разделяет узел на несколько меньших узлов, каждый из которых достаточно мал для размещения в группе.

Идеальный узел NUMA для нового процесса можно запросить с помощью [**\_ атрибута потока процесса \_ \_ предпочтительный \_**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) Расширенный атрибут Node при создании процесса. Как и идеальный для потоков процессор, идеальный узел является указанием планировщика, который назначает новый процесс группе, содержащей запрошенный узел, если это возможно.

Расширенные функции NUMA [**жетнумааваилаблемеморинодикс**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex), [**жетнуманодепроцессормаскекс**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex), [**жетнумапроцессорнодикс**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)и [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex) отличаются от нерасширенных аналогев тем, что номер узла является значением **UShort** , а не **uchar**, для размещения потенциально большего числа узлов в системе с более чем 64 логическими процессорами. Кроме того, процессор, заданный или извлекаемый расширенными функциями, включает в себя группу процессоров; процессор, заданный или извлекаемый нерасширенными функциями, является относительным для группы. Дополнительные сведения см. в разделах справки по отдельным функциям.

Приложение с поддержкой групп может назначить все свои потоки определенному узлу аналогично описанному выше в этом разделе, используя соответствующие расширенные функции NUMA. Приложение использует [**жетлогикалпроцессоринформатионекс**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) для получения списка всех процессоров в системе. Обратите внимание, что приложение не может задать маску сходства процессов, если только этот процесс не назначен одной группе, а требуемый узел находится в этой группе. Обычно приложение должно вызвать [**сетсреадграупаффинити**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity) , чтобы ограничить его потоки до предполагаемого узла.


### <a name="behavior-starting-with-windows-10-build-20348"></a>Поведение, начиная с сборки Windows 10 20348 

> [!NOTE]
> Начиная с сборки Windows 10 20348, поведение этой и других функций NUMA было изменено для улучшения поддержки систем с узлами, содержащими больше процессоров 64.

Создание «фиктивных» узлов для размещения сопоставления 1:1 между группами и узлами привело к путанице в работе при обнаружении непредвиденного числа узлов NUMA, и, начиная с сборки Windows 10 Build 20348, операционная система изменилась на разрешение связи нескольких групп с узлом, поэтому теперь можно сообщить о истинной топологии NUMA системы.  

В рамках этих изменений операционной системы некоторые API NUMA были изменены для поддержки отчетов о нескольких группах, которые теперь можно связать с одним узлом NUMA. Обновленные и новые API-интерфейсы помечаются в таблице в разделе **API NUMA** ниже.

Поскольку удаление разделения узлов потенциально может повлиять на существующие приложения, доступно значение реестра, позволяющее воздействовать на работу разделения устаревших узлов. Разделение узлов можно включить повторно, создав **REG_DWORD** значение с именем "сплитларженодес" со значением 1 под HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\NUMA. Чтобы изменения этого параметра вступили в силу, требуется перезагрузка.

```powershell
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\NUMA" /v SplitLargeNumaNodes /t REG_DWORD /v 1
```

> [!NOTE]
> Приложения, которые обновляются для использования новых функций API, сообщающих о истинной топологии NUMA, будут продолжать работать должным образом в системах, где разделение большого узла было повторно включено с помощью этого раздела реестра.

В следующем примере сначала демонстрируются потенциальные проблемы с построением таблиц, сопоставленных процессорам с узлами NUMA с помощью устаревших API сходства, которые больше не предоставляют полный набор всех процессоров в системе. это может привести к созданию неполной таблицы. Последствия такой неполноты зависят от содержимого таблицы. Если в таблице просто хранится соответствующий номер узла, это, скорее всего, проблема с производительностью, если необнаруженные процессоры остаются в составе узла 0. Однако если таблица содержит указатели на структуру контекста для каждого узла, это может привести к ненулевым разыменованиям во время выполнения.

Далее в примере кода показаны два обходных решения проблемы. Первый заключается в переходе на многогрупповые интерфейсы API сходства узлов (пользовательский режим и режим ядра). Второй — использовать **кекуерилогикалпроцессоррелатионшип** для прямого запроса узла NUMA, связанного с данным номером процессора.

```cpp

//
// Problematic implementation using KeQueryNodeActiveAffinity.
//

USHORT CurrentNode;
USHORT HighestNodeNumber;
GROUP_AFFINITY NodeAffinity;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    KeQueryNodeActiveAffinity(CurrentNode, &NodeAffinity, NULL);
    while (NodeAffinity.Mask != 0) {

        ProcessorNumber.Group = NodeAffinity.Group;
        BitScanForward(&ProcessorNumber.Number, NodeAffinity.Mask);

        ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

        ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode;]

        NodeAffinity.Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
    }
}

//
// Resolution using KeQueryNodeActiveAffinity2.
//

USHORT CurrentIndex;
USHORT CurrentNode;
USHORT CurrentNodeAffinityCount;
USHORT HighestNodeNumber;
ULONG MaximumGroupCount;
PGROUP_AFFINITY NodeAffinityMasks;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

MaximumGroupCount = KeQueryMaximumGroupCount();
NodeAffinityMasks = ExAllocatePool2(POOL_FLAG_PAGED,
                                    sizeof(GROUP_AFFINITY) * MaximumGroupCount,
                                    'tseT');

if (NodeAffinityMasks == NULL) {
    return STATUS_NO_MEMORY;
}

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    Status = KeQueryNodeActiveAffinity2(CurrentNode,
                                        NodeAffinityMasks,
                                        MaximumGroupCount,
                                        &CurrentNodeAffinityCount);
    NT_ASSERT(NT_SUCCESS(Status));

    for (CurrentIndex = 0; CurrentIndex < CurrentNodeAffinityCount; CurrentIndex += 1) {

        CurrentAffinity = &NodeAffinityMasks[CurrentIndex];

        while (CurrentAffinity->Mask != 0) {

            ProcessorNumber.Group = CurrentAffinity.Group;
            BitScanForward(&ProcessorNumber.Number, CurrentAffinity->Mask);

            ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

            ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode];

            CurrentAffinity->Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
        }
    }
}

//
// Resolution using KeQueryLogicalProcessorRelationship.
//

ULONG ProcessorCount;
ULONG ProcessorIndex;
SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX ProcessorInformation;
ULONG ProcessorInformationSize;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

ProcessorCount = KeQueryActiveProcessorCountEx(ALL_PROCESSOR_GROUPS);

for (ProcessorIndex = 0; ProcessorIndex < ProcessorCount; ProcessorIndex += 1) {

    Status = KeGetProcessorNumberFromIndex(ProcessorIndex, &ProcessorNumber);
    NT_ASSERT(NT_SUCCESS(Status));

    ProcessorInformationSize = sizeof(ProcessorInformation);
    Status = KeQueryLogicalProcessorRelationship(&ProcessorNumber,
                                                    RelationNumaNode,
                                                    &ProcessorInformation,
                                                    &ProcesorInformationSize);
    NT_ASSERT(NT_SUCCESS(Status));

    NodeNumber = ProcessorInformation.NumaNode.NodeNumber;

    ProcessorNodeContexts[ProcessorIndex] = NodeContexts[NodeNumber];
}
```

## <a name="numa-api"></a>API NUMA

В следующей таблице описывается API NUMA.



| Функция                                                                     | Описание                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аллокатеусерфисикалпажеснума**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)      | Выделяет страницы физической памяти для сопоставления и несоответствия в любом регионе [расширений](../memory/address-windowing-extensions.md) AWE указанного процесса и указывает узел NUMA для физической памяти. |
| [**креатефилемаппингнума**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingnumaw)                      | Создает или открывает именованный или безымянный объект сопоставления файлов для указанного файла и указывает узел NUMA для физической памяти.                                                                                              |
| [**жетлогикалпроцессоринформатион**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Обновлено в сборке Windows 10 20348. Извлекает сведения о логических процессорах и связанном оборудовании.                                                                                                                                                            |
| [**жетлогикалпроцессоринформатионекс**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Обновлено в сборке Windows 10 20348. Извлекает сведения о связях логических процессоров и связанного оборудования.                                                                                                                                       |
| [**жетнумааваилаблемемориноде**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)             | Извлекает объем памяти, доступный в указанном узле.                                                                                                                                                                 |
| [**жетнумааваилаблемеморинодикс**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)         | Извлекает объем памяти, доступный в узле, указанном как значение **UShort** .                                                                                                                                             |
| [**жетнумахигхестноденумбер**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)                 | Возвращает узел, в котором в настоящее время имеется наибольший номер.                                                                                                                                                                       |
| [**жетнуманодепроцессормаск**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)                 | Обновлено в сборке Windows 10 20348. Извлекает маску процессора для указанного узла.                                                                                                                                                                            |
| [**GetNumaNodeProcessorMask2**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormask2)                         | Новые в Windows 10 Build 20348. Извлекает многогрупповую маску процессора для указанного узла.                                                                                                                                                                          |
| [**жетнуманодепроцессормаскекс**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)             | Обновлено в сборке Windows 10 20348. Извлекает маску процессора для узла, указанного как значение типа **UShort** .                                                                                                                                                        |
| [**жетнумапроцессорноде**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                         | Возвращает номер узла для указанного процессора.                                                                                                                                                                          |
| [**жетнумапроцессорнодикс**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                     | Получает номер узла в виде значения **UShort** для указанного процессора.                                                                                                                                                    |
| [**жетнумапроксимитиноде**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                         | Возвращает номер узла для указанного идентификатора близости.                                                                                                                                                               |
| [**жетнумапроксимитинодикс**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                     | Получает номер узла в виде значения **UShort** для указанного идентификатора близости.                                                                                                                                         |
| [**жетпроцессдефаулткпусетмаскс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessdefaultcpusetmasks)                     | Новые в Windows 10 Build 20348. Возвращает список наборов ЦП в наборе процессов по умолчанию, который был установлен с помощью Сетпроцессдефаулткпусетмаскс или Сетпроцессдефаулткпусетс.                                                                                                                                         |
| [**жетсреадселектедкпусетмаскс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadselectedcpusetmasks)                     | Новые в Windows 10 Build 20348. Задает назначение выбранных наборов ЦП для указанного потока. Это назначение переопределяет назначение процесса по умолчанию, если оно задано.                                                                                                                                          |
| [**мапвиевоффиликснума**](/windows/win32/api/winbase/nf-winbase-mapviewoffileexnuma)                          | Сопоставляет представление сопоставления файлов с адресным пространством вызывающего процесса и указывает узел NUMA для физической памяти.                                                                                                 |
| [**сетпроцессдефаулткпусетмаскс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessdefaultcpusetmasks)                     | Новые в Windows 10 Build 20348. Задает назначение наборов ЦП по умолчанию для потоков в указанном процессе.                                                                                                                                          |
| [**сетсреадселектедкпусетмаскс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadselectedcpusetmasks)                     | Новые в Windows 10 Build 20348. Задает назначение выбранных наборов ЦП для указанного потока. Это назначение переопределяет назначение процесса по умолчанию, если оно задано.                                                                                                                                          |
| [**виртуалаллоцекснума**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                            | Резервирует или фиксирует область памяти в пределах виртуального адресного пространства указанного процесса и указывает узел NUMA для физической памяти.                                                                          |



 

Функцию [**куериворкингсетекс**](/windows/win32/api/psapi/nf-psapi-queryworkingsetex) можно использовать для получения узла NUMA, на котором выделяется страница. Пример см. в разделе [выделение памяти из узла NUMA](../memory/allocating-memory-from-a-numa-node.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Выделение памяти из узла NUMA](../memory/allocating-memory-from-a-numa-node.md)
</dt> <dt>

[Несколько процессоров](multiple-processors.md)
</dt> <dt>

[Группы процессоров](processor-groups.md)
</dt> </dl>

 

 
