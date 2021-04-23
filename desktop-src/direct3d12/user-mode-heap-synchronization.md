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
# <a name="multi-engine-synchronization"></a><span data-ttu-id="b5007-103">Синхронизация с несколькими модулями</span><span class="sxs-lookup"><span data-stu-id="b5007-103">Multi-engine synchronization</span></span>

<span data-ttu-id="b5007-104">Большинство современных графических процессоров содержат несколько независимых ядер, предоставляющих специализированные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="b5007-104">Most modern GPUs contain multiple independent engines that provide specialized functionality.</span></span> <span data-ttu-id="b5007-105">Многие имеют один или несколько выделенных ядер и ядро вычислений, которое обычно отличается от модуля 3D.</span><span class="sxs-lookup"><span data-stu-id="b5007-105">Many have one or more dedicated copy engines, and a compute engine, usually distinct from the 3D engine.</span></span> <span data-ttu-id="b5007-106">Каждый из этих ядер может выполнять команды параллельно друг с другом.</span><span class="sxs-lookup"><span data-stu-id="b5007-106">Each of these engines can execute commands in parallel with each other.</span></span> <span data-ttu-id="b5007-107">Direct3D 12 обеспечивает детальный доступ к модулям 3D, COMPUTE и Copy, используя очереди и списки команд.</span><span class="sxs-lookup"><span data-stu-id="b5007-107">Direct3D 12 provides fine-grained access to the 3D, compute, and copy engines, using queues and command lists.</span></span>

## <a name="gpu-engines"></a><span data-ttu-id="b5007-108">Обработчики GPU</span><span class="sxs-lookup"><span data-stu-id="b5007-108">GPU engines</span></span>

<span data-ttu-id="b5007-109">На следующей схеме показаны потоки ЦП заголовка, каждый из которых заполняет одну или несколько копий, вычислений и трехмерных очередей.</span><span class="sxs-lookup"><span data-stu-id="b5007-109">The following diagram shows a title's CPU threads, each populating one or more of the copy, compute, and 3D queues.</span></span> <span data-ttu-id="b5007-110">В объеме трехмерной очереди могут быть все три ядра GPU; очередь вычислений может управлять механизмами вычислений и копирования; а очередь копирования — просто механизм копирования.</span><span class="sxs-lookup"><span data-stu-id="b5007-110">The 3D queue can drive all three GPU engines; the compute queue can drive the compute and copy engines; and the copy queue simply the copy engine.</span></span>

<span data-ttu-id="b5007-111">Так как различные потоки заполняют очереди, не существует простой гарантии порядка выполнения, поэтому потребность в механизмах синхронизации, &mdash; когда они требуются.</span><span class="sxs-lookup"><span data-stu-id="b5007-111">As the different threads populate the queues, there can be no simple guarantee of the order of execution, hence the need for synchronization mechanisms&mdash;when the title requires them.</span></span>

![четыре потока, отправляющие команды в три очереди](images/gpu-engines.png)

<span data-ttu-id="b5007-113">На следующем рисунке показано, как запланировать работу заголовка для нескольких ядер GPU, включая синхронизацию между ядрами, если это необходимо: в нем показаны рабочие нагрузки отдельных ядер с зависимостями между ядрами.</span><span class="sxs-lookup"><span data-stu-id="b5007-113">The following image illustrate how a title might schedule work across multiple GPU engines, including inter-engine synchronization where necessary: it shows the per-engine workloads with inter-engine dependencies.</span></span> <span data-ttu-id="b5007-114">В этом примере ядро копирования сначала копирует некоторую геометрию, необходимую для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="b5007-114">In this example, the copy engine first copies some geometry necessary for rendering.</span></span> <span data-ttu-id="b5007-115">Модуль обработки трехмерных процессоров ждет завершения этих копий и визуализирует предварительную отработку по геометрии.</span><span class="sxs-lookup"><span data-stu-id="b5007-115">The 3D engine waits for these copies to complete, and renders a pre-pass over the geometry.</span></span> <span data-ttu-id="b5007-116">Затем он потребляется ядром вычислений.</span><span class="sxs-lookup"><span data-stu-id="b5007-116">This is then consumed by the compute engine.</span></span> <span data-ttu-id="b5007-117">Результаты [**диспетчеризации**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)модуля вычислений, а также несколько операций копирования текстур в механизм копирования используются трехмерным механизмом для завершающего вызова [**Draw**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) .</span><span class="sxs-lookup"><span data-stu-id="b5007-117">The results of the compute engine [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch), along with several texture copy operations on the copy engine, are consumed by the 3D engine for the final [**Draw**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) call.</span></span>

![Обмен данными между механизмами копирования, графики и вычислений](images/gpu-sync.png)

<span data-ttu-id="b5007-119">В следующем псевдо-коде показано, как заголовок может отправить такую рабочую нагрузку.</span><span class="sxs-lookup"><span data-stu-id="b5007-119">The following pseudo-code illustrates how a title might submit such a workload.</span></span>

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

<span data-ttu-id="b5007-120">В следующем псевдокоде показана синхронизация между механизмами копирования и трехмерных систем для выполнения выделения памяти, похожего на кучу, с помощью кольцевого буфера.</span><span class="sxs-lookup"><span data-stu-id="b5007-120">The following pseudo-code illustrates synchronization between the copy and 3D engines to accomplish heap-like memory allocation via a ring buffer.</span></span> <span data-ttu-id="b5007-121">Заголовки имеют гибкие возможности выбора правильного баланса между максимизацией параллелизма (через большой буфер) и снижают потребление памяти и задержку (с помощью небольшого буфера).</span><span class="sxs-lookup"><span data-stu-id="b5007-121">Titles have the flexibility to choose the right balance between maximizing parallelism (via a large buffer) and reducing memory consumption and latency (via a small buffer).</span></span>

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

## <a name="multi-engine-scenarios"></a><span data-ttu-id="b5007-122">Сценарии с несколькими модулями</span><span class="sxs-lookup"><span data-stu-id="b5007-122">Multi-engine scenarios</span></span>

<span data-ttu-id="b5007-123">Direct3D 12 позволяет избежать случайной неэффективной работы, вызванной непредвиденными задержками синхронизации.</span><span class="sxs-lookup"><span data-stu-id="b5007-123">Direct3D 12 allows you to avoid accidentally running into inefficiencies caused by unexpected synchronization delays.</span></span> <span data-ttu-id="b5007-124">Кроме того, он позволяет создавать синхронизацию на более высоком уровне, где требуемая синхронизация может быть определена с большей степенью уверенности.</span><span class="sxs-lookup"><span data-stu-id="b5007-124">It also allows you to introduce synchronization at a higher level where the required synchronization can be determined with greater certainty.</span></span> <span data-ttu-id="b5007-125">Вторая ошибка, связанная с несколькими модулями, заключается в более явном выполнении ресурсоемких операций, включая переходы между трехмерными и видеороликами, которые традиционно были дорогостоящими из-за синхронизации между несколькими контекстами ядра.</span><span class="sxs-lookup"><span data-stu-id="b5007-125">A second issue that multi-engine addresses is to make expensive operations more explicit, which includes transitions between 3D and video that were traditionally costly because of synchronization between multiple kernel contexts.</span></span>

<span data-ttu-id="b5007-126">В частности, с помощью Direct3D 12 можно обращаться к следующим сценариям.</span><span class="sxs-lookup"><span data-stu-id="b5007-126">In particular, the following scenarios can be addressed with Direct3D 12.</span></span>

-   <span data-ttu-id="b5007-127">Работа GPU с асинхронным и низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="b5007-127">Asynchronous and low priority GPU work.</span></span> <span data-ttu-id="b5007-128">Это позволяет выполнять параллельное выполнение задач с низким приоритетом GPU и атомарных операций, которые позволяют одному потоку GPU использовать результаты другого несинхронизированного потока без блокировки.</span><span class="sxs-lookup"><span data-stu-id="b5007-128">This enables concurrent execution of low priority GPU work and atomic operations that enable one GPU thread to consume the results of another unsynchronized thread without blocking.</span></span>
-   <span data-ttu-id="b5007-129">Высокоприоритетная работа вычислений.</span><span class="sxs-lookup"><span data-stu-id="b5007-129">High priority compute work.</span></span> <span data-ttu-id="b5007-130">С помощью фонового вычислений можно прервать трехмерную отрисовку для выполнения небольшого объема вычислительных операций с высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="b5007-130">With background compute it is possible to interrupt 3D rendering to do a small amount of high priority compute work.</span></span> <span data-ttu-id="b5007-131">Результаты этой работы можно получить на раннем этапе для дополнительной обработки ЦП.</span><span class="sxs-lookup"><span data-stu-id="b5007-131">The results of this work can be obtained early for additional processing on the CPU.</span></span>
-   <span data-ttu-id="b5007-132">Фоновая расчетная работа.</span><span class="sxs-lookup"><span data-stu-id="b5007-132">Background compute work.</span></span> <span data-ttu-id="b5007-133">Отдельная очередь с низким приоритетом для вычислительных рабочих нагрузок позволяет приложению использовать свободные циклы GPU для выполнения фоновых вычислений без негативного влияния на основные задачи отрисовки (или другие).</span><span class="sxs-lookup"><span data-stu-id="b5007-133">A separate low priority queue for compute workloads allows an application to utilize spare GPU cycles to perform background computation without negative impact on the primary rendering (or other) tasks.</span></span> <span data-ttu-id="b5007-134">Фоновые задачи могут включать распаковку ресурсов или обновление симуляций или структур ускорения.</span><span class="sxs-lookup"><span data-stu-id="b5007-134">Background tasks may include decompression of resources or updating simulations or acceleration structures.</span></span> <span data-ttu-id="b5007-135">Фоновые задачи должны быть синхронизированы на ЦП нечасто (приблизительно один раз для каждого кадра), чтобы избежать зависания или снижения скорости работы переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b5007-135">Background tasks should be synchronized on the CPU infrequently (approximately once per frame) to avoid stalling or slowing foreground work.</span></span>
-   <span data-ttu-id="b5007-136">Потоковая передача и отправка данных.</span><span class="sxs-lookup"><span data-stu-id="b5007-136">Streaming and uploading data.</span></span> <span data-ttu-id="b5007-137">Отдельная очередь копирования заменяет D3D11 основные данные и обновляет ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b5007-137">A separate copy queue replaces the D3D11 concepts of initial data and updating resources.</span></span> <span data-ttu-id="b5007-138">Несмотря на то, что приложение отвечает за дополнительные сведения в модели Direct3D 12, эта ответственность полагается на электроэнергию.</span><span class="sxs-lookup"><span data-stu-id="b5007-138">Although the application is responsible for more details in the Direct3D 12 model, this responsibility comes with power.</span></span> <span data-ttu-id="b5007-139">Приложение может управлять объемом системной памяти, выделяемой для буферизации передачи данных.</span><span class="sxs-lookup"><span data-stu-id="b5007-139">The application can control how much system memory is devoted to buffering upload data.</span></span> <span data-ttu-id="b5007-140">Приложение может выбрать время и способ синхронизации (ЦП VS GPU, блокирование и неблокировка), а также отслеживать ход выполнения и контролировать объем работы в очереди.</span><span class="sxs-lookup"><span data-stu-id="b5007-140">The app can choose when and how (CPU vs GPU, blocking vs non-blocking) to synchronize, and can track progress and control the amount of queued work.</span></span>
-   <span data-ttu-id="b5007-141">Повышенный параллелизм.</span><span class="sxs-lookup"><span data-stu-id="b5007-141">Increased parallelism.</span></span> <span data-ttu-id="b5007-142">Приложения могут использовать более глубокие очереди для фоновых рабочих нагрузок (например, для расшифровки видео), если они имеют отдельные очереди для выполнения задач переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b5007-142">Applications can use deeper queues for background workloads (e.g. video decode) when they have separate queues for foreground work.</span></span>

<span data-ttu-id="b5007-143">В Direct3D 12 понятие очереди команд — это представление API примерно последовательной последовательности работы, отправленной приложением.</span><span class="sxs-lookup"><span data-stu-id="b5007-143">In Direct3D 12 the concept of a command queue is the API representation of a roughly serial sequence of work submitted by the application.</span></span> <span data-ttu-id="b5007-144">Барьеры и другие методы позволяют выполнять эту работу в конвейере или в неопределенном порядке, но приложение видит только одну временную шкалу завершения.</span><span class="sxs-lookup"><span data-stu-id="b5007-144">Barriers and other techniques allow this work to be executed in a pipeline or out of order, but the application only sees a single completion timeline.</span></span> <span data-ttu-id="b5007-145">Это соответствует контексту интерпретации в D3D11.</span><span class="sxs-lookup"><span data-stu-id="b5007-145">This corresponds to the immediate context in D3D11.</span></span>

## <a name="synchronization-apis"></a><span data-ttu-id="b5007-146">API-интерфейсы синхронизации</span><span class="sxs-lookup"><span data-stu-id="b5007-146">Synchronization APIs</span></span>

### <a name="devices-and-queues"></a><span data-ttu-id="b5007-147">Устройства и очереди</span><span class="sxs-lookup"><span data-stu-id="b5007-147">Devices and queues</span></span>

<span data-ttu-id="b5007-148">Устройство Direct3D 12 имеет методы для создания и получения очередей команд различных типов и приоритетов.</span><span class="sxs-lookup"><span data-stu-id="b5007-148">The Direct3D 12 device has methods to create and retrieve command queues of different types and priorities.</span></span> <span data-ttu-id="b5007-149">Большинство приложений должны использовать очереди команд по умолчанию, так как они обеспечивают совместное использование другими компонентами.</span><span class="sxs-lookup"><span data-stu-id="b5007-149">Most applications should use the default command queues because these allow for shared usage by other components.</span></span> <span data-ttu-id="b5007-150">Приложения с дополнительными требованиями к параллелизму могут создавать дополнительные очереди.</span><span class="sxs-lookup"><span data-stu-id="b5007-150">Applications with additional concurrency requirements can create additional queues.</span></span> <span data-ttu-id="b5007-151">Очереди указываются типом списка команд, который они используют.</span><span class="sxs-lookup"><span data-stu-id="b5007-151">Queues are specified by the command list type that they consume.</span></span>

<span data-ttu-id="b5007-152">См. следующие методы создания [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).</span><span class="sxs-lookup"><span data-stu-id="b5007-152">Refer to the following creation methods of [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).</span></span>

-   <span data-ttu-id="b5007-153">[**Креатекоммандкуеуе**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : создает очередь команд на основе сведений, которые находятся в структуре в виде [**\_ \_ очереди \_ команд Direct3D 12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .</span><span class="sxs-lookup"><span data-stu-id="b5007-153">[**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : creates a command queue based on information in a [**Direct3D 12\_COMMAND\_QUEUE\_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) structure.</span></span>
-   <span data-ttu-id="b5007-154">[**Креатекоммандлист**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : создает список команд типа [**\_ \_ списка \_ команд Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span><span class="sxs-lookup"><span data-stu-id="b5007-154">[**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : creates a command list of type [**Direct3D 12\_COMMAND\_LIST\_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span></span>
-   <span data-ttu-id="b5007-155">[**Креатефенце**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : создает ограждение, указывая флаги в [**\_ \_ флагах ограждения Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags).</span><span class="sxs-lookup"><span data-stu-id="b5007-155">[**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : creates a fence, noting the flags in [**Direct3D 12\_FENCE\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags).</span></span> <span data-ttu-id="b5007-156">Границы используются для синхронизации очередей.</span><span class="sxs-lookup"><span data-stu-id="b5007-156">Fences are used to synchronize queues.</span></span>

<span data-ttu-id="b5007-157">Очереди всех типов (3D, COMPUTE и Copy) используют один и тот же интерфейс, и все они основаны на списке команд.</span><span class="sxs-lookup"><span data-stu-id="b5007-157">Queues of all types (3D, compute and copy) share the same interface and are all command-list based.</span></span>

<span data-ttu-id="b5007-158">См. следующие методы [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).</span><span class="sxs-lookup"><span data-stu-id="b5007-158">Refer to the following methods of [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).</span></span>

-   <span data-ttu-id="b5007-159">[**Ексекутекоммандлистс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : отправляет массив списков команд для выполнения.</span><span class="sxs-lookup"><span data-stu-id="b5007-159">[**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : submits an array of command lists for execution.</span></span> <span data-ttu-id="b5007-160">Список команд, определяемый параметром [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).</span><span class="sxs-lookup"><span data-stu-id="b5007-160">Each command list being defined by [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).</span></span>
-   <span data-ttu-id="b5007-161">[**Сигнал**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : задает значение ограждения, когда очередь (работающая на GPU) достигает определенной точки.</span><span class="sxs-lookup"><span data-stu-id="b5007-161">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : sets a fence value when the queue (running on the GPU) reaches a certain point.</span></span>
-   <span data-ttu-id="b5007-162">[**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : очередь ожидает, пока указанная ограждение не достигнет указанного значения.</span><span class="sxs-lookup"><span data-stu-id="b5007-162">[**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : the queue waits until the specified fence reaches the specified value.</span></span>

<span data-ttu-id="b5007-163">Обратите внимание, что пакеты не используются ни одной очередью, поэтому этот тип нельзя использовать для создания очереди.</span><span class="sxs-lookup"><span data-stu-id="b5007-163">Note that bundles are not consumed by any queues and therefore this type cannot be used to create a queue.</span></span>

### <a name="fences"></a><span data-ttu-id="b5007-164">Ограждения</span><span class="sxs-lookup"><span data-stu-id="b5007-164">Fences</span></span>

<span data-ttu-id="b5007-165">API-интерфейс с несколькими модулями предоставляет явные API для создания и синхронизации с помощью ограждений.</span><span class="sxs-lookup"><span data-stu-id="b5007-165">The multi-engine API provides explicit APIs to create and synchronize using fences.</span></span> <span data-ttu-id="b5007-166">Ограждение — это конструкция синхронизации, управляемая значением UINT64.</span><span class="sxs-lookup"><span data-stu-id="b5007-166">A fence is a synchronization construct controlled by a UINT64 value.</span></span> <span data-ttu-id="b5007-167">Значения ограждения задаются приложением.</span><span class="sxs-lookup"><span data-stu-id="b5007-167">Fence values are set by the application.</span></span> <span data-ttu-id="b5007-168">Операция сигнала изменяет значение ограждения, а операция ожидания блокируется до тех пор, пока ограждение не достигнет запрошенного значения или не станет большим.</span><span class="sxs-lookup"><span data-stu-id="b5007-168">A signal operation modifies the fence value and a wait operation blocks until the fence has reached the requested value or greater.</span></span> <span data-ttu-id="b5007-169">Событие может быть инициировано, когда ограждение достигает определенного значения.</span><span class="sxs-lookup"><span data-stu-id="b5007-169">An event can be fired when a fence reaches a certain value.</span></span>

<span data-ttu-id="b5007-170">См. методы интерфейса [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) .</span><span class="sxs-lookup"><span data-stu-id="b5007-170">Refer to the methods of the [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) interface.</span></span>

-   <span data-ttu-id="b5007-171">[**Жеткомплетедвалуе**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : Возвращает текущее значение ограждения.</span><span class="sxs-lookup"><span data-stu-id="b5007-171">[**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : returns the current value of the fence.</span></span>
-   <span data-ttu-id="b5007-172">[**Сетевентонкомплетион**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : вызывает срабатывание события, когда ограждение достигает заданного значения.</span><span class="sxs-lookup"><span data-stu-id="b5007-172">[**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : causes an event to fire when the fence reaches a given value.</span></span>
-   <span data-ttu-id="b5007-173">[**Сигнал**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : задает ограждение с заданным значением.</span><span class="sxs-lookup"><span data-stu-id="b5007-173">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : sets the fence to the given value.</span></span>

<span data-ttu-id="b5007-174">Границы обеспечивают доступ ЦП к текущему значению ограждения, а также к ожиданиям и сигналам ЦП.</span><span class="sxs-lookup"><span data-stu-id="b5007-174">Fences allow CPU access to the current fence value, and CPU waits and signals.</span></span>

<span data-ttu-id="b5007-175">Метод [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) в интерфейсе [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) обновляет ограждение на стороне ЦП.</span><span class="sxs-lookup"><span data-stu-id="b5007-175">The [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) method on the [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) interface updates a fence from the CPU side.</span></span> <span data-ttu-id="b5007-176">Это обновление выполняется немедленно.</span><span class="sxs-lookup"><span data-stu-id="b5007-176">This update occurs immediately.</span></span> <span data-ttu-id="b5007-177">Метод [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) в [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) обновляет ограждение на стороне GPU.</span><span class="sxs-lookup"><span data-stu-id="b5007-177">The [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) method on [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) updates a fence from the GPU side.</span></span> <span data-ttu-id="b5007-178">Это обновление происходит после завершения всех других операций в очереди команд.</span><span class="sxs-lookup"><span data-stu-id="b5007-178">This update occurs after all other operations on the command queue have been completed.</span></span>

<span data-ttu-id="b5007-179">Все узлы в программе установки с несколькими модулями могут считывать и реагировать на любые границы, достигнутые правильного значения.</span><span class="sxs-lookup"><span data-stu-id="b5007-179">All nodes in a multi-engine setup can read and react to any fence reaching the right value.</span></span>

<span data-ttu-id="b5007-180">Приложения устанавливают свои значения ограждений. хорошей отправной точкой может быть увеличение ограждения по одному кадру.</span><span class="sxs-lookup"><span data-stu-id="b5007-180">Applications set their own fence values, a good starting point might be increasing a fence once per frame.</span></span>

<span data-ttu-id="b5007-181">Ограждение *может* быть *перевернуто*.</span><span class="sxs-lookup"><span data-stu-id="b5007-181">A fence *may* be *rewound*.</span></span> <span data-ttu-id="b5007-182">Это означает, что для значения ограждения не требуется только приращение.</span><span class="sxs-lookup"><span data-stu-id="b5007-182">This means that the fence value does not need to solely increment.</span></span> <span data-ttu-id="b5007-183">Если операция **сигнализации** помещается в очередь двух различных командных очередей или если два потока ЦП являются **вызовом** на границе, то может возникнуть состязание за то, что **сигнал** завершается последним, и, следовательно, значение ограждения останется.</span><span class="sxs-lookup"><span data-stu-id="b5007-183">If a **Signal** operation is enqueued on two different command queues, or if two CPU threads are both calling **Signal** on a fence, there may be a race to determine which **Signal** completes last, and therefore which fence value is the one which will remain.</span></span> <span data-ttu-id="b5007-184">При перераспределении ограждения все новые ожидания (включая запросы **сетевентонкомплетион** ) будут сравниваться с новым значением нижней границы и, следовательно, не будут удовлетворены, даже если значение ограждения было достаточно высоким, чтобы удовлетворить их.</span><span class="sxs-lookup"><span data-stu-id="b5007-184">If a fence is rewound, any new waits (including **SetEventOnCompletion** requests) will be compared against the new lower fence value, and therefore may not be satisfied, even if the fence value had previously been high enough to satisfy them.</span></span> <span data-ttu-id="b5007-185">В случае состязания между значением, которое будет удовлетворять невыполненному ожиданию, и более низким значением, которое не будет выполняться, ожидание *будет* удовлетворено, независимо от того, какое значение остается впоследствии.</span><span class="sxs-lookup"><span data-stu-id="b5007-185">If a race does occur, between a value which will satisfy an outstanding wait, and a lower value which will not, the wait *will* be satisfied regardless of which value remains afterwards.</span></span>

<span data-ttu-id="b5007-186">Интерфейсы API ограждения предоставляют мощные функции синхронизации, но могут создавать потенциально трудные для отладки проблемы.</span><span class="sxs-lookup"><span data-stu-id="b5007-186">The fence APIs provide powerful synchronization functionality but can create potentially difficult to debug issues.</span></span> <span data-ttu-id="b5007-187">Рекомендуется использовать каждую ограждение только для указания хода выполнения на одной временной шкале, чтобы предотвратить состязания между SignalR.</span><span class="sxs-lookup"><span data-stu-id="b5007-187">It is recommended that each fence only be used to indicate progress on one timeline to prevent races between signalers.</span></span>

### <a name="copy-and-compute-command-lists"></a><span data-ttu-id="b5007-188">Копирование и вычисление списков команд</span><span class="sxs-lookup"><span data-stu-id="b5007-188">Copy and compute command lists</span></span>

<span data-ttu-id="b5007-189">Все три типа списка команд используют интерфейс [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) , однако для копирования и вычислений поддерживаются только подмножества методов.</span><span class="sxs-lookup"><span data-stu-id="b5007-189">All three types of command list use the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface, however only a subset of the methods are supported for copy and compute.</span></span>

<span data-ttu-id="b5007-190">Списки команд копирования и вычислений могут использовать следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b5007-190">Copy and compute command lists can use the following methods.</span></span>

-   [<span data-ttu-id="b5007-191">**Закрыть**</span><span class="sxs-lookup"><span data-stu-id="b5007-191">**Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [<span data-ttu-id="b5007-192">**копибуфферрегион**</span><span class="sxs-lookup"><span data-stu-id="b5007-192">**CopyBufferRegion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="b5007-193">**копиресаурце**</span><span class="sxs-lookup"><span data-stu-id="b5007-193">**CopyResource**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="b5007-194">**копитекстуререгион**</span><span class="sxs-lookup"><span data-stu-id="b5007-194">**CopyTextureRegion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="b5007-195">**копитилес**</span><span class="sxs-lookup"><span data-stu-id="b5007-195">**CopyTiles**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="b5007-196">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="b5007-196">**Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [<span data-ttu-id="b5007-197">**ресаурцебарриер**</span><span class="sxs-lookup"><span data-stu-id="b5007-197">**ResourceBarrier**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

<span data-ttu-id="b5007-198">Списки команд вычислений также могут использовать следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b5007-198">Compute command lists can also use the following methods.</span></span>

-   [<span data-ttu-id="b5007-199">**клеарстате**</span><span class="sxs-lookup"><span data-stu-id="b5007-199">**ClearState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [<span data-ttu-id="b5007-200">**клеарунордередакцессвиевфлоат**</span><span class="sxs-lookup"><span data-stu-id="b5007-200">**ClearUnorderedAccessViewFloat**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [<span data-ttu-id="b5007-201">**клеарунордередакцессвиевуинт**</span><span class="sxs-lookup"><span data-stu-id="b5007-201">**ClearUnorderedAccessViewUint**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="b5007-202">**дискардресаурце**</span><span class="sxs-lookup"><span data-stu-id="b5007-202">**DiscardResource**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [<span data-ttu-id="b5007-203">**Dispatch**</span><span class="sxs-lookup"><span data-stu-id="b5007-203">**Dispatch**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [<span data-ttu-id="b5007-204">**ексекутеиндирект**</span><span class="sxs-lookup"><span data-stu-id="b5007-204">**ExecuteIndirect**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [<span data-ttu-id="b5007-205">**SetComputeRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="b5007-205">**SetComputeRoot32BitConstant**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [<span data-ttu-id="b5007-206">**SetComputeRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="b5007-206">**SetComputeRoot32BitConstants**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [<span data-ttu-id="b5007-207">**сеткомпутерутконстантбуффервиев**</span><span class="sxs-lookup"><span data-stu-id="b5007-207">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="b5007-208">**сеткомпутерутдескриптортабле**</span><span class="sxs-lookup"><span data-stu-id="b5007-208">**SetComputeRootDescriptorTable**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [<span data-ttu-id="b5007-209">**сеткомпутерутшадерресаурцевиев**</span><span class="sxs-lookup"><span data-stu-id="b5007-209">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="b5007-210">**сеткомпутерутсигнатуре**</span><span class="sxs-lookup"><span data-stu-id="b5007-210">**SetComputeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [<span data-ttu-id="b5007-211">**сеткомпутерутунордередакцессвиев**</span><span class="sxs-lookup"><span data-stu-id="b5007-211">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="b5007-212">**сетдескрипторхеапс**</span><span class="sxs-lookup"><span data-stu-id="b5007-212">**SetDescriptorHeaps**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [<span data-ttu-id="b5007-213">**сетпипелинестате**</span><span class="sxs-lookup"><span data-stu-id="b5007-213">**SetPipelineState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [<span data-ttu-id="b5007-214">**сетпредикатион**</span><span class="sxs-lookup"><span data-stu-id="b5007-214">**SetPredication**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

<span data-ttu-id="b5007-215">Списки команд COMPUTE должны задавать PSO вычислений при вызове [**сетпипелинестате**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).</span><span class="sxs-lookup"><span data-stu-id="b5007-215">Compute command lists must set a compute PSO when calling [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).</span></span>

<span data-ttu-id="b5007-216">Пакеты не могут использоваться при вычислении или копировании списков команд или очередей.</span><span class="sxs-lookup"><span data-stu-id="b5007-216">Bundles cannot be used with compute or copy command lists or queues.</span></span>

## <a name="pipelined-compute-and-graphics-example"></a><span data-ttu-id="b5007-217">Пример конвейерных вычислений и графики</span><span class="sxs-lookup"><span data-stu-id="b5007-217">Pipelined compute and graphics example</span></span>

<span data-ttu-id="b5007-218">В этом примере показано, как можно использовать синхронизацию ограждений для создания конвейера вычислений в очереди (на которую ссылается `pComputeQueue` ), используемой графикой работы над очередью `pGraphicsQueue` .</span><span class="sxs-lookup"><span data-stu-id="b5007-218">This example shows how fence synchronization can be used to create a pipeline of compute work on a queue (referenced by `pComputeQueue`) that's consumed by graphics work on queue `pGraphicsQueue`.</span></span> <span data-ttu-id="b5007-219">Работа вычислительных и графических операций конвейера связана с графикой, который использует результаты вычислительных операций из нескольких кадров назад, а событие ЦП используется для регулирования общего объема общей работы в очереди.</span><span class="sxs-lookup"><span data-stu-id="b5007-219">The compute and graphics work is pipelined with the graphics queue consuming the result of compute work from several frames back, and a CPU event is used to throttle the total work queued overall.</span></span>

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

<span data-ttu-id="b5007-220">Для поддержки этого конвейера должен существовать буфер `ComputeGraphicsLatency+1` различных копий данных, передаваемых из очереди вычислений в графическую очередь.</span><span class="sxs-lookup"><span data-stu-id="b5007-220">To support this pipelining, there must be a buffer of `ComputeGraphicsLatency+1` different copies of the data passing from the compute queue to the graphics queue.</span></span> <span data-ttu-id="b5007-221">Списки команд должны использовать Уавс и косвенное обращение для чтения и записи из соответствующей "версии" данных в буфере.</span><span class="sxs-lookup"><span data-stu-id="b5007-221">The command lists must use UAVs and indirection to read and write from the appropriate “version” of the data in the buffer.</span></span> <span data-ttu-id="b5007-222">Очередь вычислений должна подождать, пока очередь графики не завершит чтение данных для кадра N, прежде чем он сможет записать кадр `N+ComputeGraphicsLatency` .</span><span class="sxs-lookup"><span data-stu-id="b5007-222">The compute queue must wait until the graphics queue has finished reading from the data for frame N before it can write frame `N+ComputeGraphicsLatency`.</span></span>

<span data-ttu-id="b5007-223">Обратите внимание, что объем очереди вычислений, отработанной по отношению к ЦП, не зависит непосредственно от требуемого объема буферизации, однако менее ценным будет использование GPU очереди, превышающее объем доступного места в буфере.</span><span class="sxs-lookup"><span data-stu-id="b5007-223">Note that the amount of compute queue worked relative to the CPU does not depend directly on the amount of buffering required, however, queuing GPU work beyond the amount of buffer space available is less valuable.</span></span>

<span data-ttu-id="b5007-224">Альтернативным механизмом для предотвращения косвенного обращения является создание нескольких списков команд, соответствующих каждой из переименованных версий данных.</span><span class="sxs-lookup"><span data-stu-id="b5007-224">An alternative mechanism to avoid indirection would be to create multiple command lists corresponding to each of the “renamed” versions of the data.</span></span> <span data-ttu-id="b5007-225">В следующем примере используется этот метод при расширении предыдущего примера для того, чтобы очереди вычислений и графики выполнялись более асинхронно.</span><span class="sxs-lookup"><span data-stu-id="b5007-225">The next example uses this technique while extending the previous example to allow the compute and graphics queues to run more asynchronously.</span></span>

## <a name="asynchronous-compute-and-graphics-example"></a><span data-ttu-id="b5007-226">Пример асинхронного вычислений и графики</span><span class="sxs-lookup"><span data-stu-id="b5007-226">Asynchronous compute and graphics example</span></span>

<span data-ttu-id="b5007-227">Следующий пример позволяет графику визуализироваться асинхронно из очереди вычислений.</span><span class="sxs-lookup"><span data-stu-id="b5007-227">This next example allows graphics to render asynchronously from the compute queue.</span></span> <span data-ttu-id="b5007-228">По-прежнему существует фиксированный объем буферизованных данных между двумя этапами, однако теперь работа с графикой продолжается независимо и использует наиболее актуальный результат этапа вычислений, как известно на ЦП при постановке графики в очередь.</span><span class="sxs-lookup"><span data-stu-id="b5007-228">There is still a fixed amount of buffered data between the two stages, however now graphics work proceeds independently and uses the most up-to-date result of the compute stage as known on the CPU when the graphics work is queued.</span></span> <span data-ttu-id="b5007-229">Это может быть полезно, если работа над графикой была обновлена другим источником, например вводом данных пользователем.</span><span class="sxs-lookup"><span data-stu-id="b5007-229">This would be useful if the graphics work was being updated by another source, for example user input.</span></span> <span data-ttu-id="b5007-230">Чтобы кадры графики можно было протестировать за раз, необходимо наличие нескольких списков команд `ComputeGraphicsLatency` , а функция `UpdateGraphicsCommandList` представляет обновление списка команд для включения последних входных данных и считывания данных из соответствующего буфера.</span><span class="sxs-lookup"><span data-stu-id="b5007-230">There must be multiple command lists to allow the `ComputeGraphicsLatency` frames of graphics work to be in flight at a time, and the function `UpdateGraphicsCommandList` represents updating the command list to include the most recent input data and read from the compute data from the appropriate buffer.</span></span>

<span data-ttu-id="b5007-231">Очередь вычислений должна по-прежнему ждать завершения очереди графики с помощью буферов каналов, но третья ограждение () вводится `pGraphicsComputeFence` таким образом, чтобы ход выполнения графических операций чтения и обработки графики в целом можно было отслеживать.</span><span class="sxs-lookup"><span data-stu-id="b5007-231">The compute queue must still wait for the graphics queue to finish with the pipe buffers, but a third fence (`pGraphicsComputeFence`) is introduced so that the progress of graphics reading compute work versus graphics progress in general can be tracked.</span></span> <span data-ttu-id="b5007-232">Это отражает тот факт, что теперь последовательные графические фреймы могут считаться из одного результата вычислений или пропускать результат вычислений.</span><span class="sxs-lookup"><span data-stu-id="b5007-232">This reflects the fact that now consecutive graphics frames could read from the same compute result or could skip a compute result.</span></span> <span data-ttu-id="b5007-233">Более эффективная, но немного более сложная структура будет использовать только единую графическую границу и сохранить сопоставление с кадрами вычислений, используемыми в каждом графическом фрейме.</span><span class="sxs-lookup"><span data-stu-id="b5007-233">A more efficient but slightly more complicated design would use just the single graphics fence and store a mapping to the compute frames used by each graphics frame.</span></span>

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

## <a name="multi-queue-resource-access"></a><span data-ttu-id="b5007-234">Доступ к ресурсам с несколькими очередями</span><span class="sxs-lookup"><span data-stu-id="b5007-234">Multi-queue resource access</span></span>

<span data-ttu-id="b5007-235">Для доступа к ресурсу в более чем одной очереди приложение должно соответствовать следующим правилам.</span><span class="sxs-lookup"><span data-stu-id="b5007-235">To access a resource on more than one queue an application must adhere to the following rules.</span></span>

-   <span data-ttu-id="b5007-236">Доступ к ресурсам (см. сведения о [**\_ \_ состояниях ресурсов Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) определяется классом типа очереди, а не объектом Queue.</span><span class="sxs-lookup"><span data-stu-id="b5007-236">Resource access (refer to [**Direct3D 12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) is determined by queue type class not queue object.</span></span> <span data-ttu-id="b5007-237">Существует два типа классов очереди: очередь вычислений или объемной графики — это один класс типа, Copy — второй класс типа.</span><span class="sxs-lookup"><span data-stu-id="b5007-237">There are two type classes of queue: Compute/3D queue is one type class, Copy is a second type class.</span></span> <span data-ttu-id="b5007-238">Таким образом, ресурс, который имеет барьер на \_ состояние ресурса шейдера, отличного от пикселя \_ \_ в одной объемной очереди, может использоваться в этом состоянии в любой трехмерной очереди или в любой из очередей вычислений с учетом требований к синхронизации, требующих для сериализации большей части операций записи.</span><span class="sxs-lookup"><span data-stu-id="b5007-238">So a resource that has a barrier to the NON\_PIXEL\_SHADER\_RESOURCE state on one 3D queue can be used in that state on any 3D or Compute queue, subject to synchronization requirements which require most writes to be serialized.</span></span> <span data-ttu-id="b5007-239">Состояния ресурсов, совместно используемые двумя классами типов ( \_ Источник копирования и конечный объект копирования \_ ), считаются разными состояниями для каждого класса типа.</span><span class="sxs-lookup"><span data-stu-id="b5007-239">The resource states that are shared between the two type classes (COPY\_SOURCE and COPY\_DEST) are considered different states for each type class.</span></span> <span data-ttu-id="b5007-240">Таким образом, если ресурс переходит на копирование \_ приемника в очереди копирования, он недоступен в качестве места назначения копирования из объемных и нересурсоемких очередей и наоборот.</span><span class="sxs-lookup"><span data-stu-id="b5007-240">So that if a resource transitions to COPY\_DEST on a Copy queue it is not accessible as a copy destination from 3D or Compute queues and vice versa.</span></span>

    <span data-ttu-id="b5007-241">Для суммирования.</span><span class="sxs-lookup"><span data-stu-id="b5007-241">To summarize.</span></span>

    -   <span data-ttu-id="b5007-242">Очередь "объект" — это любая отдельная очередь.</span><span class="sxs-lookup"><span data-stu-id="b5007-242">A queue "object" is any single queue.</span></span>
    -   <span data-ttu-id="b5007-243">Очередь "тип" — это один из следующих трех типов: COMPUTE, 3D и Copy.</span><span class="sxs-lookup"><span data-stu-id="b5007-243">A queue "type" is any one of these three: Compute, 3D, and Copy.</span></span>
    -   <span data-ttu-id="b5007-244">Очередь "тип класса" — это один из следующих двух: COMPUTE/3D и Copy.</span><span class="sxs-lookup"><span data-stu-id="b5007-244">A queue "type class" is any one of these two: Compute/3D and Copy.</span></span>

-   <span data-ttu-id="b5007-245">Флаги копирования (копирование \_ \_ источника и источник копирования), используемые в качестве начальных состояний, представляют состояния в классе объемного или типа вычислений.</span><span class="sxs-lookup"><span data-stu-id="b5007-245">The COPY flags (COPY\_DEST and COPY\_SOURCE) used as initial states represent states in the 3D/Compute type class.</span></span> <span data-ttu-id="b5007-246">Чтобы использовать ресурс изначально в очереди копирования, он должен начаться в общем состоянии.</span><span class="sxs-lookup"><span data-stu-id="b5007-246">To use a resource initially on a Copy queue it should start in the COMMON state.</span></span> <span data-ttu-id="b5007-247">Общее состояние можно использовать для всех использований в очереди копирования с помощью переходов неявного состояния.</span><span class="sxs-lookup"><span data-stu-id="b5007-247">The COMMON state can be used for all usages on a Copy queue using the implicit state transitions.</span></span> 
-   <span data-ttu-id="b5007-248">Несмотря на то, что состояние ресурса является общим для всех вычислений и трехмерных очередей, запись в ресурс не разрешается одновременно в разных очередях.</span><span class="sxs-lookup"><span data-stu-id="b5007-248">Although resource state is shared across all Compute and 3D queues, it is not permitted to write to the resource simultaneously on different queues.</span></span> <span data-ttu-id="b5007-249">"Одновременно" в этом случае означает Несинхронизированное выполнение, что говорит о несинхронизированном выполнении на определенном оборудовании.</span><span class="sxs-lookup"><span data-stu-id="b5007-249">"Simultaneously" here means unsynchronized, noting unsynchronized execution is not possible on some hardware.</span></span> <span data-ttu-id="b5007-250">Применяются следующие правила.</span><span class="sxs-lookup"><span data-stu-id="b5007-250">The following rules apply.</span></span>

    -   <span data-ttu-id="b5007-251">Только одна очередь может записывать в ресурс за раз.</span><span class="sxs-lookup"><span data-stu-id="b5007-251">Only one queue can write to a resource at a time.</span></span>
    -   <span data-ttu-id="b5007-252">Несколько очередей могут считывать из ресурса, если они не считывают байты, изменяемые модулем записи (считывание одновременно записанных байтов приводит к неопределенному результату).</span><span class="sxs-lookup"><span data-stu-id="b5007-252">Multiple queues can read from the resource as long as they don’t read the bytes being modified by the writer (reading bytes being simultaneously written produces undefined results).</span></span>
    -   <span data-ttu-id="b5007-253">Ограждение необходимо использовать для синхронизации после записи, прежде чем другая очередь сможет считывать записанные байты или предоставлять доступ на запись.</span><span class="sxs-lookup"><span data-stu-id="b5007-253">A fence must be used to synchronize after writing before another queue can read the written bytes or make any write access.</span></span>

-   <span data-ttu-id="b5007-254">Представляемые задние буферы должны находиться в \_ общем состоянии "состояние ресурса Direct3D 12" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b5007-254">Back buffers being presented must be in the Direct3D 12\_RESOURCE\_STATE\_COMMON state.</span></span> 

## <a name="related-topics"></a><span data-ttu-id="b5007-255">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b5007-255">Related topics</span></span>

[<span data-ttu-id="b5007-256">Инструкции по программированию Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b5007-256">Direct3D 12 programming guide</span></span>](directx-12-programming-guide.md)

[<span data-ttu-id="b5007-257">Использование барьеров ресурсов для синхронизации состояний ресурсов в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b5007-257">Using resource barriers to synchronize resource states in Direct3D 12</span></span>](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[<span data-ttu-id="b5007-258">Управление памятью в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b5007-258">Memory management in Direct3D 12</span></span>](memory-management.md)
