---
title: Синхронизация с несколькими модулями
description: В этом разделе обсуждается синхронизация доступа к нескольким независимым механизмам, найденным в большинстве современных графических процессоров.
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d60704e411a1ba45dd4902ad9101a416391743dd
ms.sourcegitcommit: 622d149edf775af5a9633c2d12ccfddf7000b8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2020
ms.locfileid: "104548921"
---
# <a name="multi-engine-synchronization"></a>Синхронизация с несколькими модулями

Большинство современных графических процессоров содержат несколько независимых ядер, предоставляющих специализированные функциональные возможности. Многие имеют один или несколько выделенных ядер и ядро вычислений, которое обычно отличается от модуля 3D. Каждый из этих ядер может выполнять команды параллельно друг с другом. Direct3D 12 обеспечивает детальный доступ к модулям 3D, COMPUTE и Copy, используя очереди и списки команд.

## <a name="gpu-engines"></a>Обработчики GPU

На следующей схеме показаны потоки ЦП заголовка, каждый из которых заполняет одну или несколько копий, вычислений и трехмерных очередей. В объеме трехмерной очереди могут быть все три ядра GPU; очередь вычислений может управлять механизмами вычислений и копирования; а очередь копирования — просто механизм копирования.

Так как различные потоки заполняют очереди, не существует простой гарантии порядка выполнения, поэтому потребность в механизмах синхронизации, &mdash; когда они требуются.

![четыре потока, отправляющие команды в три очереди](images/gpu-engines.png)

На следующем рисунке показано, как запланировать работу заголовка для нескольких ядер GPU, включая синхронизацию между ядрами, если это необходимо: в нем показаны рабочие нагрузки отдельных ядер с зависимостями между ядрами. В этом примере ядро копирования сначала копирует некоторую геометрию, необходимую для подготовки к просмотру. Модуль обработки трехмерных процессоров ждет завершения этих копий и визуализирует предварительную отработку по геометрии. Затем он потребляется ядром вычислений. Результаты [**диспетчеризации**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)модуля вычислений, а также несколько операций копирования текстур в механизм копирования используются трехмерным механизмом для завершающего вызова [**Draw**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) .

![Обмен данными между механизмами копирования, графики и вычислений](images/gpu-sync.png)

В следующем псевдо-коде показано, как заголовок может отправить такую рабочую нагрузку.

``` syntax
// Get per-engine contexts. Note that multiple queues may be exposed
// per engine, however that design is not reflected here.
copyEngine = device->GetCopyEngineContext();
renderEngine = device->GetRenderEngineContext();
computeEngine = device->GetComputeEngineContext();
copyEngine->CopyResource(geometry, ...); // copy geometry
copyEngine->Signal(copyFence, 101);
copyEngine->CopyResource(tex1, ...); // copy textures
copyEngine->CopyResource(tex2, ...); // copy more textures
copyEngine->CopyResource(tex3, ...); // copy more textures
copyEngine->CopyResource(tex4, ...); // copy more textures
copyEngine->Signal(copyFence, 102);
renderEngine->Wait(copyFence, 101); // geometry copied
renderEngine->Draw(); // pre-pass using geometry only into rt1
renderEngine->Signal(renderFence, 201);
computeEngine->Wait(renderFence, 201); // prepass completed
computeEngine->Dispatch(); // lighting calculations on pre-pass (using rt1 as SRV)
computeEngine->Signal(computeFence, 301);
renderEngine->Wait(computeFence, 301); // lighting calculated into buf1
renderEngine->Wait(copyFence, 102); // textures copied
renderEngine->Draw(); // final render using buf1 as SRV, and tex[1-4] SRVs
```

В следующем псевдокоде показана синхронизация между механизмами копирования и трехмерных систем для выполнения выделения памяти, похожего на кучу, с помощью кольцевого буфера. Заголовки имеют гибкие возможности выбора правильного баланса между максимизацией параллелизма (через большой буфер) и снижают потребление памяти и задержку (с помощью небольшого буфера).

``` syntax
device->CreateBuffer(&ringCB);
for(int i=1;i++){
  if(i > length) copyEngine->Wait(fence1, i - length);
  copyEngine->Map(ringCB, value%length, WRITE, pData); // copy new data
  copyEngine->Signal(fence2, i);
  renderEngine->Wait(fence2, i);
  renderEngine->Draw(); // draw using copied data
  renderEngine->Signal(fence1, i);
}

// example for length = 3:
// copyEngine->Map();
// copyEngine->Signal(fence2, 1); // fence2 = 1  
// copyEngine->Map();
// copyEngine->Signal(fence2, 2); // fence2 = 2
// copyEngine->Map();
// copyEngine->Signal(fence2, 3); // fence2 = 3
// copy engine has exhausted the ring buffer, so must wait for render to consume it
// copyEngine->Wait(fence1, 1); // fence1 == 0, wait
// renderEngine->Wait(fence2, 1); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 1); // fence1 = 1, copy engine now unblocked
// renderEngine->Wait(fence2, 2); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 2); // fence1 = 2
// renderEngine->Wait(fence2, 3); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 3); // fence1 = 3
// now render engine is starved, and so must wait for the copy engine
// renderEngine->Wait(fence2, 4); // fence2 == 3, wait
```

## <a name="multi-engine-scenarios"></a>Сценарии с несколькими модулями

Direct3D 12 позволяет избежать случайной неэффективной работы, вызванной непредвиденными задержками синхронизации. Кроме того, он позволяет создавать синхронизацию на более высоком уровне, где требуемая синхронизация может быть определена с большей степенью уверенности. Вторая ошибка, связанная с несколькими модулями, заключается в более явном выполнении ресурсоемких операций, включая переходы между трехмерными и видеороликами, которые традиционно были дорогостоящими из-за синхронизации между несколькими контекстами ядра.

В частности, с помощью Direct3D 12 можно обращаться к следующим сценариям.

-   Работа GPU с асинхронным и низким приоритетом. Это позволяет выполнять параллельное выполнение задач с низким приоритетом GPU и атомарных операций, которые позволяют одному потоку GPU использовать результаты другого несинхронизированного потока без блокировки.
-   Высокоприоритетная работа вычислений. С помощью фонового вычислений можно прервать трехмерную отрисовку для выполнения небольшого объема вычислительных операций с высоким приоритетом. Результаты этой работы можно получить на раннем этапе для дополнительной обработки ЦП.
-   Фоновая расчетная работа. Отдельная очередь с низким приоритетом для вычислительных рабочих нагрузок позволяет приложению использовать свободные циклы GPU для выполнения фоновых вычислений без негативного влияния на основные задачи отрисовки (или другие). Фоновые задачи могут включать распаковку ресурсов или обновление симуляций или структур ускорения. Фоновые задачи должны быть синхронизированы на ЦП нечасто (приблизительно один раз для каждого кадра), чтобы избежать зависания или снижения скорости работы переднего плана.
-   Потоковая передача и отправка данных. Отдельная очередь копирования заменяет D3D11 основные данные и обновляет ресурсы. Несмотря на то, что приложение отвечает за дополнительные сведения в модели Direct3D 12, эта ответственность полагается на электроэнергию. Приложение может управлять объемом системной памяти, выделяемой для буферизации передачи данных. Приложение может выбрать время и способ синхронизации (ЦП VS GPU, блокирование и неблокировка), а также отслеживать ход выполнения и контролировать объем работы в очереди.
-   Повышенный параллелизм. Приложения могут использовать более глубокие очереди для фоновых рабочих нагрузок (например, для расшифровки видео), если они имеют отдельные очереди для выполнения задач переднего плана.

В Direct3D 12 понятие очереди команд — это представление API примерно последовательной последовательности работы, отправленной приложением. Барьеры и другие методы позволяют выполнять эту работу в конвейере или в неопределенном порядке, но приложение видит только одну временную шкалу завершения. Это соответствует контексту интерпретации в D3D11.

## <a name="synchronization-apis"></a>API-интерфейсы синхронизации

### <a name="devices-and-queues"></a>Устройства и очереди

Устройство Direct3D 12 имеет методы для создания и получения очередей команд различных типов и приоритетов. Большинство приложений должны использовать очереди команд по умолчанию, так как они обеспечивают совместное использование другими компонентами. Приложения с дополнительными требованиями к параллелизму могут создавать дополнительные очереди. Очереди указываются типом списка команд, который они используют.

См. следующие методы создания [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).

-   [**Креатекоммандкуеуе**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : создает очередь команд на основе сведений, которые находятся в структуре в виде [**\_ \_ очереди \_ команд Direct3D 12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .
-   [**Креатекоммандлист**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : создает список команд типа [**\_ \_ списка \_ команд Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).
-   [**Креатефенце**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : создает ограждение, указывая флаги в [**\_ \_ флагах ограждения Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). Границы используются для синхронизации очередей.

Очереди всех типов (3D, COMPUTE и Copy) используют один и тот же интерфейс, и все они основаны на списке команд.

См. следующие методы [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).

-   [**Ексекутекоммандлистс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : отправляет массив списков команд для выполнения. Список команд, определяемый параметром [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).
-   [**Сигнал**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : задает значение ограждения, когда очередь (работающая на GPU) достигает определенной точки.
-   [**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : очередь ожидает, пока указанная ограждение не достигнет указанного значения.

Обратите внимание, что пакеты не используются ни одной очередью, поэтому этот тип нельзя использовать для создания очереди.

### <a name="fences"></a>Ограждения

API-интерфейс с несколькими модулями предоставляет явные API для создания и синхронизации с помощью ограждений. Ограждение — это конструкция синхронизации, управляемая значением UINT64. Значения ограждения задаются приложением. Операция сигнала изменяет значение ограждения, а операция ожидания блокируется до тех пор, пока ограждение не достигнет запрошенного значения или не станет большим. Событие может быть инициировано, когда ограждение достигает определенного значения.

См. методы интерфейса [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) .

-   [**Жеткомплетедвалуе**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : Возвращает текущее значение ограждения.
-   [**Сетевентонкомплетион**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : вызывает срабатывание события, когда ограждение достигает заданного значения.
-   [**Сигнал**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : задает ограждение с заданным значением.

Границы обеспечивают доступ ЦП к текущему значению ограждения, а также к ожиданиям и сигналам ЦП.

Метод [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) в интерфейсе [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) обновляет ограждение на стороне ЦП. Это обновление выполняется немедленно. Метод [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) в [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) обновляет ограждение на стороне GPU. Это обновление происходит после завершения всех других операций в очереди команд.

Все узлы в программе установки с несколькими модулями могут считывать и реагировать на любые границы, достигнутые правильного значения.

Приложения устанавливают свои значения ограждений. хорошей отправной точкой может быть увеличение ограждения по одному кадру.

Ограждение *может* быть *перевернуто*. Это означает, что для значения ограждения не требуется только приращение. Если операция **сигнализации** помещается в очередь двух различных командных очередей или если два потока ЦП являются **вызовом** на границе, то может возникнуть состязание за то, что **сигнал** завершается последним, и, следовательно, значение ограждения останется. При перераспределении ограждения все новые ожидания (включая запросы **сетевентонкомплетион** ) будут сравниваться с новым значением нижней границы и, следовательно, не будут удовлетворены, даже если значение ограждения было достаточно высоким, чтобы удовлетворить их. В случае состязания между значением, которое будет удовлетворять невыполненному ожиданию, и более низким значением, которое не будет выполняться, ожидание *будет* удовлетворено, независимо от того, какое значение остается впоследствии.

Интерфейсы API ограждения предоставляют мощные функции синхронизации, но могут создавать потенциально трудные для отладки проблемы. Рекомендуется использовать каждую ограждение только для указания хода выполнения на одной временной шкале, чтобы предотвратить состязания между SignalR.

### <a name="copy-and-compute-command-lists"></a>Копирование и вычисление списков команд

Все три типа списка команд используют интерфейс [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) , однако для копирования и вычислений поддерживаются только подмножества методов.

Списки команд копирования и вычислений могут использовать следующие методы.

-   [**Закрыть**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [**копибуфферрегион**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**копиресаурце**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**копитекстуререгион**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**копитилес**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**Перезапуск**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

Списки команд вычислений также могут использовать следующие методы.

-   [**клеарстате**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [**клеарунордередакцессвиевфлоат**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**клеарунордередакцессвиевуинт**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**дискардресаурце**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**ексекутеиндирект**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [**SetComputeRoot32BitConstant**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [**SetComputeRoot32BitConstants**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [**сеткомпутерутконстантбуффервиев**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**сеткомпутерутдескриптортабле**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [**сеткомпутерутшадерресаурцевиев**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**сеткомпутерутсигнатуре**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [**сеткомпутерутунордередакцессвиев**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**сетдескрипторхеапс**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [**сетпипелинестате**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [**сетпредикатион**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

Списки команд COMPUTE должны задавать PSO вычислений при вызове [**сетпипелинестате**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

Пакеты не могут использоваться при вычислении или копировании списков команд или очередей.

## <a name="pipelined-compute-and-graphics-example"></a>Пример конвейерных вычислений и графики

В этом примере показано, как можно использовать синхронизацию ограждений для создания конвейера вычислений в очереди (на которую ссылается `pComputeQueue` ), используемой графикой работы над очередью `pGraphicsQueue` . Работа вычислительных и графических операций конвейера связана с графикой, который использует результаты вычислительных операций из нескольких кадров назад, а событие ЦП используется для регулирования общего объема общей работы в очереди.

```cpp
void PipelinedComputeGraphics()
{
    const UINT CpuLatency = 3;
    const UINT ComputeGraphicsLatency = 2;

    HANDLE handle = CreateEvent(nullptr, FALSE, FALSE, nullptr);

    UINT64 FrameNumber = 0;

    while (1)
    {
        if (FrameNumber > ComputeGraphicsLatency)
        {
            pComputeQueue->Wait(pGraphicsFence,
                FrameNumber - ComputeGraphicsLatency);
        }

        if (FrameNumber > CpuLatency)
        {
            pComputeFence->SetEventOnFenceCompletion(
                FrameNumber - CpuLatency,
                handle);
            WaitForSingleObject(handle, INFINITE);
        }

        ++FrameNumber;

        pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
        pComputeQueue->Signal(pComputeFence, FrameNumber);
        if (FrameNumber > ComputeGraphicsLatency)
        {
            UINT GraphicsFrameNumber = FrameNumber - ComputeGraphicsLatency;
            pGraphicsQueue->Wait(pComputeFence, GraphicsFrameNumber);
            pGraphicsQueue->ExecuteCommandLists(1, &pGraphicsCommandList);
            pGraphicsQueue->Signal(pGraphicsFence, GraphicsFrameNumber);
        }
    }
}
```

Для поддержки этого конвейера должен существовать буфер `ComputeGraphicsLatency+1` различных копий данных, передаваемых из очереди вычислений в графическую очередь. Списки команд должны использовать Уавс и косвенное обращение для чтения и записи из соответствующей "версии" данных в буфере. Очередь вычислений должна подождать, пока очередь графики не завершит чтение данных для кадра N, прежде чем он сможет записать кадр `N+ComputeGraphicsLatency` .

Обратите внимание, что объем очереди вычислений, отработанной по отношению к ЦП, не зависит непосредственно от требуемого объема буферизации, однако менее ценным будет использование GPU очереди, превышающее объем доступного места в буфере.

Альтернативным механизмом для предотвращения косвенного обращения является создание нескольких списков команд, соответствующих каждой из переименованных версий данных. В следующем примере используется этот метод при расширении предыдущего примера для того, чтобы очереди вычислений и графики выполнялись более асинхронно.

## <a name="asynchronous-compute-and-graphics-example"></a>Пример асинхронного вычислений и графики

Следующий пример позволяет графику визуализироваться асинхронно из очереди вычислений. По-прежнему существует фиксированный объем буферизованных данных между двумя этапами, однако теперь работа с графикой продолжается независимо и использует наиболее актуальный результат этапа вычислений, как известно на ЦП при постановке графики в очередь. Это может быть полезно, если работа над графикой была обновлена другим источником, например вводом данных пользователем. Чтобы кадры графики можно было протестировать за раз, необходимо наличие нескольких списков команд `ComputeGraphicsLatency` , а функция `UpdateGraphicsCommandList` представляет обновление списка команд для включения последних входных данных и считывания данных из соответствующего буфера.

Очередь вычислений должна по-прежнему ждать завершения очереди графики с помощью буферов каналов, но третья ограждение () вводится `pGraphicsComputeFence` таким образом, чтобы ход выполнения графических операций чтения и обработки графики в целом можно было отслеживать. Это отражает тот факт, что теперь последовательные графические фреймы могут считаться из одного результата вычислений или пропускать результат вычислений. Более эффективная, но немного более сложная структура будет использовать только единую графическую границу и сохранить сопоставление с кадрами вычислений, используемыми в каждом графическом фрейме.

```cpp
void AsyncPipelinedComputeGraphics()
{
    const UINT CpuLatency{ 3 };
    const UINT ComputeGraphicsLatency{ 2 };

    // The compute fence is at index 0; the graphics fence is at index 1.
    ID3D12Fence* rgpFences[]{ pComputeFence, pGraphicsFence };
    HANDLE handles[2];
    handles[0] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    handles[1] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    UINT FrameNumbers[]{ 0, 0 };

    ID3D12GraphicsCommandList* rgpGraphicsCommandLists[CpuLatency];
    CreateGraphicsCommandLists(ARRAYSIZE(rgpGraphicsCommandLists),
        rgpGraphicsCommandLists);

    // Graphics needs to wait for the first compute frame to complete; this is the
    // only wait that the graphics queue will perform.
    pGraphicsQueue->Wait(pComputeFence, 1);

    while (true)
    {
        for (auto i = 0; i < 2; ++i)
        {
            if (FrameNumbers[i] > CpuLatency)
            {
                rgpFences[i]->SetEventOnCompletion(
                    FrameNumbers[i] - CpuLatency,
                    handles[i]);
            }
            else
            {
                ::SetEvent(handles[i]);
            }
        }


        auto WaitResult = ::WaitForMultipleObjects(2, handles, FALSE, INFINITE);
        if (WaitResult > WAIT_OBJECT_0 + 1) continue;
        auto Stage = WaitResult - WAIT_OBJECT_0;
        ++FrameNumbers[Stage];

        switch (Stage)
        {
        case 0:
        {
            if (FrameNumbers[Stage] > ComputeGraphicsLatency)
            {
                pComputeQueue->Wait(pGraphicsComputeFence,
                    FrameNumbers[Stage] - ComputeGraphicsLatency);
            }
            pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
            pComputeQueue->Signal(pComputeFence, FrameNumbers[Stage]);
            break;
        }
        case 1:
        {
            // Recall that the GPU queue started with a wait for pComputeFence, 1
            UINT64 CompletedComputeFrames = min(1,
                pComputeFence->GetCompletedValue());
            UINT64 PipeBufferIndex =
                (CompletedComputeFrames - 1) % ComputeGraphicsLatency;
            UINT64 CommandListIndex = (FrameNumbers[Stage] - 1) % CpuLatency;
            // Update graphics command list based on CPU input and using the appropriate
            // buffer index for data produced by compute.
            UpdateGraphicsCommandList(PipeBufferIndex,
                rgpGraphicsCommandLists[CommandListIndex]);

            // Signal *before* new rendering to indicate what compute work
            // the graphics queue is DONE with
            pGraphicsQueue->Signal(pGraphicsComputeFence, CompletedComputeFrames - 1);
            pGraphicsQueue->ExecuteCommandLists(1,
                rgpGraphicsCommandLists + PipeBufferIndex);
            pGraphicsQueue->Signal(pGraphicsFence, FrameNumbers[Stage]);
            break;
        }
        }
    }
}
```

## <a name="multi-queue-resource-access"></a>Доступ к ресурсам с несколькими очередями

Для доступа к ресурсу в более чем одной очереди приложение должно соответствовать следующим правилам.

-   Доступ к ресурсам (см. сведения о [**\_ \_ состояниях ресурсов Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) определяется классом типа очереди, а не объектом Queue. Существует два типа классов очереди: очередь вычислений или объемной графики — это один класс типа, Copy — второй класс типа. Таким образом, ресурс, который имеет барьер на \_ состояние ресурса шейдера, отличного от пикселя \_ \_ в одной объемной очереди, может использоваться в этом состоянии в любой трехмерной очереди или в любой из очередей вычислений с учетом требований к синхронизации, требующих для сериализации большей части операций записи. Состояния ресурсов, совместно используемые двумя классами типов ( \_ Источник копирования и конечный объект копирования \_ ), считаются разными состояниями для каждого класса типа. Таким образом, если ресурс переходит на копирование \_ приемника в очереди копирования, он недоступен в качестве места назначения копирования из объемных и нересурсоемких очередей и наоборот.

    Для суммирования.

    -   Очередь "объект" — это любая отдельная очередь.
    -   Очередь "тип" — это один из следующих трех типов: COMPUTE, 3D и Copy.
    -   Очередь "тип класса" — это один из следующих двух: COMPUTE/3D и Copy.

-   Флаги копирования (копирование \_ \_ источника и источник копирования), используемые в качестве начальных состояний, представляют состояния в классе объемного или типа вычислений. Чтобы использовать ресурс изначально в очереди копирования, он должен начаться в общем состоянии. Общее состояние можно использовать для всех использований в очереди копирования с помощью переходов неявного состояния. 
-   Несмотря на то, что состояние ресурса является общим для всех вычислений и трехмерных очередей, запись в ресурс не разрешается одновременно в разных очередях. "Одновременно" в этом случае означает Несинхронизированное выполнение, что говорит о несинхронизированном выполнении на определенном оборудовании. Применяются следующие правила.

    -   Только одна очередь может записывать в ресурс за раз.
    -   Несколько очередей могут считывать из ресурса, если они не считывают байты, изменяемые модулем записи (считывание одновременно записанных байтов приводит к неопределенному результату).
    -   Ограждение необходимо использовать для синхронизации после записи, прежде чем другая очередь сможет считывать записанные байты или предоставлять доступ на запись.

-   Представляемые задние буферы должны находиться в \_ общем состоянии "состояние ресурса Direct3D 12" \_ \_ . 

## <a name="related-topics"></a>Связанные темы

[Инструкции по программированию Direct3D 12](directx-12-programming-guide.md)

[Использование барьеров ресурсов для синхронизации состояний ресурсов в Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[Управление памятью в Direct3D 12](memory-management.md)
