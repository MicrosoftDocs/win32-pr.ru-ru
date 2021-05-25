---
title: Использование барьеров ресурсов для синхронизации состояний ресурсов в Direct3D 12
description: Чтобы снизить общую загрузку ЦП и включить многопотоковую обработку и поддержку драйвера, Direct3D 12 перенесет ответственность за управление состоянием каждого ресурса из драйвера графики в приложение.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df27e7997b4f3f56ae8e87688e5cc136dc7eb87d
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343479"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a><span data-ttu-id="d14ae-103">Использование барьеров ресурсов для синхронизации состояний ресурсов в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d14ae-103">Using Resource Barriers to Synchronize Resource States in Direct3D 12</span></span>

<span data-ttu-id="d14ae-104">Чтобы снизить общую загрузку ЦП и включить многопотоковую обработку и поддержку драйвера, Direct3D 12 перенесет ответственность за управление состоянием каждого ресурса из драйвера графики в приложение.</span><span class="sxs-lookup"><span data-stu-id="d14ae-104">To reduce overall CPU usage and enable driver multi-threading and pre-processing, Direct3D 12 moves the responsibility of per-resource state management from the graphics driver to the application.</span></span> <span data-ttu-id="d14ae-105">Пример состояния для каждого ресурса — указывает, осуществляется ли доступ к ресурсу текстуры в данный момент как через шейдер представление ресурсов или как представление целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="d14ae-105">An example of per-resource state is whether a texture resource is currently being accessed as through a Shader Resource View or as a Render Target View.</span></span> <span data-ttu-id="d14ae-106">В Direct3D 11 для отслеживания этого состояния в фоновом режиме были необходимы драйверы.</span><span class="sxs-lookup"><span data-stu-id="d14ae-106">In Direct3D 11, drivers were required to track this state in the background.</span></span> <span data-ttu-id="d14ae-107">Это дорого с точки зрения ЦП и существенно усложняется при любом многопоточном проектировании.</span><span class="sxs-lookup"><span data-stu-id="d14ae-107">This is expensive from a CPU perspective and significantly complicates any sort of multi-threaded design.</span></span> <span data-ttu-id="d14ae-108">В Microsoft Direct3D 12 большая часть состояния каждого ресурса управляется приложением с одним API, [**ID3D12GraphicsCommandList:: ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="d14ae-108">In Microsoft Direct3D 12, most per-resource state is managed by the application with a single API, [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>

-   [<span data-ttu-id="d14ae-109">Использование API Ресаурцебарриер для управления состоянием каждого ресурса</span><span class="sxs-lookup"><span data-stu-id="d14ae-109">Using the ResourceBarrier API to manage per-resource state</span></span>](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [<span data-ttu-id="d14ae-110">Состояния ресурсов</span><span class="sxs-lookup"><span data-stu-id="d14ae-110">Resource states</span></span>](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [<span data-ttu-id="d14ae-111">Начальные состояния для ресурсов</span><span class="sxs-lookup"><span data-stu-id="d14ae-111">Initial states for resources</span></span>](#initial-states-for-resources)
    -   [<span data-ttu-id="d14ae-112">Ограничения состояния ресурсов для чтения и записи</span><span class="sxs-lookup"><span data-stu-id="d14ae-112">Read/write resource state restrictions</span></span>](#readwrite-resource-state-restrictions)
    -   [<span data-ttu-id="d14ae-113">Состояния ресурсов для представления задних буферов</span><span class="sxs-lookup"><span data-stu-id="d14ae-113">Resource states for presenting back buffers</span></span>](#resource-states-for-presenting-back-buffers)
    -   [<span data-ttu-id="d14ae-114">Отмена ресурсов</span><span class="sxs-lookup"><span data-stu-id="d14ae-114">Discarding resources</span></span>](#discarding-resources)
-   [<span data-ttu-id="d14ae-115">Неявные переходы состояний</span><span class="sxs-lookup"><span data-stu-id="d14ae-115">Implicit State Transitions</span></span>](#implicit-state-transitions)
    -   [<span data-ttu-id="d14ae-116">Повышение общего состояния</span><span class="sxs-lookup"><span data-stu-id="d14ae-116">Common state promotion</span></span>](#common-state-promotion)
    -   [<span data-ttu-id="d14ae-117">Decay состояния для общего</span><span class="sxs-lookup"><span data-stu-id="d14ae-117">State decay to common</span></span>](#state-decay-to-common)
    -   [<span data-ttu-id="d14ae-118">Влияние на производительность</span><span class="sxs-lookup"><span data-stu-id="d14ae-118">Performance implications</span></span>](#performance-implications)
-   [<span data-ttu-id="d14ae-119">Разделите барьеры</span><span class="sxs-lookup"><span data-stu-id="d14ae-119">Split Barriers</span></span>](#split-barriers)
-   [<span data-ttu-id="d14ae-120">Пример сценария барьера ресурсов</span><span class="sxs-lookup"><span data-stu-id="d14ae-120">Resource barrier example scenario</span></span>](#resource-barrier-example-scenario)
-   [<span data-ttu-id="d14ae-121">Пример повышения общего состояния и Decay</span><span class="sxs-lookup"><span data-stu-id="d14ae-121">Common state promotion and decay sample</span></span>](#common-state-promotion-and-decay-sample)
-   [<span data-ttu-id="d14ae-122">Пример разделенных барьеров</span><span class="sxs-lookup"><span data-stu-id="d14ae-122">Example of split barriers</span></span>](#example-of-split-barriers)
-   [<span data-ttu-id="d14ae-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d14ae-123">Related topics</span></span>](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a><span data-ttu-id="d14ae-124">Использование API Ресаурцебарриер для управления состоянием каждого ресурса</span><span class="sxs-lookup"><span data-stu-id="d14ae-124">Using the ResourceBarrier API to manage per-resource state</span></span>

<span data-ttu-id="d14ae-125">[**Ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) уведомляет графический драйвер о ситуациях, в которых драйверу может потребоваться синхронизировать несколько обращений к памяти, в которой хранится ресурс.</span><span class="sxs-lookup"><span data-stu-id="d14ae-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifies the graphics driver of situations in which the driver may need to synchronize multiple accesses to the memory in which a resource is stored.</span></span> <span data-ttu-id="d14ae-126">Метод вызывается с одной или несколькими структурами описания барьера ресурсов, которые указывают тип объявляемого барьера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d14ae-126">The method is called with one or more resource barrier description structures indicating the type of resource barrier being declared.</span></span>

<span data-ttu-id="d14ae-127">Существует три типа барьеров ресурсов:</span><span class="sxs-lookup"><span data-stu-id="d14ae-127">There are three types of resource barriers:</span></span>

-   <span data-ttu-id="d14ae-128">**Барьер перехода** . барьер перехода указывает, что набор подресурсов переходит между различными использованиями.</span><span class="sxs-lookup"><span data-stu-id="d14ae-128">**Transition barrier** - A transition barrier indicates that a set of subresources transition between different usages.</span></span> <span data-ttu-id="d14ae-129">Структура [**\_ \_ \_ барьера переключения ресурсов D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) используется для указания подресурса, который перемещается, а также состояний *до* и *после* подресурсов.</span><span class="sxs-lookup"><span data-stu-id="d14ae-129">A [**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) structure is used to specify the subresource that is transitioning as well as the *before* and *after* states of the subresource.</span></span>

    <span data-ttu-id="d14ae-130">Система проверяет, что переходы между подресурсами в списке команд соответствуют предыдущим переходам в том же списке команд.</span><span class="sxs-lookup"><span data-stu-id="d14ae-130">The system verifies that subresource transitions in a command list are consistent with previous transitions in the same command list.</span></span> <span data-ttu-id="d14ae-131">Слой отладки дополнительно отслеживает состояние подресурсов для поиска других ошибок, однако эта проверка является консервативной и не является исчерпывающей.</span><span class="sxs-lookup"><span data-stu-id="d14ae-131">The debug layer further tracks subresource state to find other errors however this validation is conservative and not exhaustive.</span></span>

    <span data-ttu-id="d14ae-132">Обратите внимание, что можно использовать \_ флаг D3D12 ресурсов " \_ \_ все \_ подресурсы", чтобы указать, что перемещаются все подресурсы в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="d14ae-132">Note that you can use the D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES flag to specify that all subresources within a resource are being transitioned.</span></span>

-   <span data-ttu-id="d14ae-133">**Барьер псевдонима** . барьер псевдонима указывает переход между использованием двух разных ресурсов, которые имеют перекрывающиеся сопоставления в одну кучу.</span><span class="sxs-lookup"><span data-stu-id="d14ae-133">**Aliasing barrier** - An aliasing barrier indicates a transition between usages of two different resources which have overlapping mappings into the same heap.</span></span> <span data-ttu-id="d14ae-134">Это относится как к зарезервированным, так и к размещенным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="d14ae-134">This applies to both reserved and placed resources.</span></span> <span data-ttu-id="d14ae-135">Структура [**\_ \_ \_ барьера с псевдонимами ресурсов D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) используется для указания ресурсов *Before* и *After* .</span><span class="sxs-lookup"><span data-stu-id="d14ae-135">A [**D3D12\_RESOURCE\_ALIASING\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) structure is used to specify both the *before* resource and the *after* resource.</span></span>

    <span data-ttu-id="d14ae-136">Обратите внимание, что один или оба ресурса могут иметь значение NULL, что означает, что любой мозаичный ресурс может вызвать присвоение псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="d14ae-136">Note that one or both resources can be NULL, which indicates that any tiled resource could cause aliasing.</span></span> <span data-ttu-id="d14ae-137">Дополнительные сведения об использовании мозаичных ресурсов см. в разделе [мозаичные](../direct3d11/tiled-resources.md) ресурсы и [ресурсы мозаики тома](volume-tiled-resources.md).</span><span class="sxs-lookup"><span data-stu-id="d14ae-137">For more information about using tiled resources, see [Tiled resources](../direct3d11/tiled-resources.md) and [Volume Tiled Resources](volume-tiled-resources.md).</span></span>

-   <span data-ttu-id="d14ae-138">**Неупорядоченное представление доступа (UAV)** . барьер UAV указывает, что все доступ UAV (чтение или запись) к определенному ресурсу должно быть завершено между любыми последующими UAV доступом, как для чтения, так и для записи.</span><span class="sxs-lookup"><span data-stu-id="d14ae-138">**Unordered access view (UAV) barrier** - A UAV barrier indicates that all UAV accesses, both read or write, to a particular resource must complete between any future UAV accesses, both read or write.</span></span> <span data-ttu-id="d14ae-139">Приложение не обязательно помещает UAV барьер между двумя вызовами Draw или Dispatch, которые считывают только из UAV.</span><span class="sxs-lookup"><span data-stu-id="d14ae-139">It's not necessary for an app to put a UAV barrier between two draw or dispatch calls that only read from a UAV.</span></span> <span data-ttu-id="d14ae-140">Кроме того, нет необходимости поUAV барьер между двумя вызовами Draw или Dispatch, которые выполняют запись в один и тот же UAV, если приложение знает, что можно обеспечить безопасность доступа UAV в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="d14ae-140">Also, it's not necessary to put a UAV barrier between two draw or dispatch calls that write to the same UAV if the application knows that it is safe to execute the UAV access in any order.</span></span> <span data-ttu-id="d14ae-141">Структура [**\_ \_ \_ барьера UAV ресурсов D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) используется для указания ресурса UAV, к которому применяется барьер.</span><span class="sxs-lookup"><span data-stu-id="d14ae-141">A [**D3D12\_RESOURCE\_UAV\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) structure is used to specify the UAV resource to which the barrier applies.</span></span> <span data-ttu-id="d14ae-142">Приложение может указать значение NULL для UAV барьера, что означает, что любой доступ UAV может потребовать барьера.</span><span class="sxs-lookup"><span data-stu-id="d14ae-142">The application can specify NULL for the barrier's UAV, which indicates that any UAV access could require the barrier.</span></span>

<span data-ttu-id="d14ae-143">При вызове [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) с массивом описаний барьера ресурсов API ведет себя так, как если бы он вызывался для каждого элемента в том порядке, в котором они были предоставлены.</span><span class="sxs-lookup"><span data-stu-id="d14ae-143">When [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) is called with an array of resource barrier descriptions, the API behaves as if it was called once for each element, in the order in which they were supplied.</span></span>

<span data-ttu-id="d14ae-144">В любой момент времени подресурс находится в одном состоянии, определяемом набором флагов [**\_ \_ состояний ресурсов D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) , предоставленных для [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="d14ae-144">At any given time, a subresource is in exactly one state, determined by the set of [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) flags supplied to [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span> <span data-ttu-id="d14ae-145">Приложение должно гарантировать, что состояния *Before* и *After* последовательных вызовов **ресаурцебарриер** согласуются.</span><span class="sxs-lookup"><span data-stu-id="d14ae-145">The application must ensure that the *before* and *after* states of consecutive calls to **ResourceBarrier** agree.</span></span>

> [!TIP]
>
> <span data-ttu-id="d14ae-146">По возможности приложения должны объединять несколько переходов в один вызов API.</span><span class="sxs-lookup"><span data-stu-id="d14ae-146">Applications should batch multiple transitions into one API call wherever possible.</span></span>

 

### <a name="resource-states"></a><span data-ttu-id="d14ae-147">Состояния ресурсов</span><span class="sxs-lookup"><span data-stu-id="d14ae-147">Resource states</span></span>

<span data-ttu-id="d14ae-148">Полный список состояний ресурсов, между которыми может переходить ресурс, см. в справочном разделе о перечислении [**\_ \_ состояний ресурсов D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .</span><span class="sxs-lookup"><span data-stu-id="d14ae-148">For the complete list of resource states that a resource can transition between, see the reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) enumeration.</span></span>

<span data-ttu-id="d14ae-149">Для раздельных барьеров ресурсов также можно использовать [**\_ \_ \_ Флаги D3D12 Resource барьера**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span><span class="sxs-lookup"><span data-stu-id="d14ae-149">For split resource barriers, also refer to [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span></span>

### <a name="initial-states-for-resources"></a><span data-ttu-id="d14ae-150">Начальные состояния для ресурсов</span><span class="sxs-lookup"><span data-stu-id="d14ae-150">Initial states for resources</span></span>

<span data-ttu-id="d14ae-151">Ресурсы могут быть созданы с любым пользовательским начальным состоянием (допустимо для описания ресурса) со следующими исключениями.</span><span class="sxs-lookup"><span data-stu-id="d14ae-151">Resources may be created with any user-specified initial state (valid for the resource description), with the following exceptions:</span></span>

-   <span data-ttu-id="d14ae-152">Отправка куч должна начаться в состоянии \_ ресурса D3D12 \_ \_ универсальное чтение состояние, \_ которое является побитовым или сочетанием:</span><span class="sxs-lookup"><span data-stu-id="d14ae-152">Upload heaps must start out in the state D3D12\_RESOURCE\_STATE\_GENERIC\_READ which is a bitwise OR combination of:</span></span>
    -   <span data-ttu-id="d14ae-153">D3D12 \_ \_ \_ вершину \_ и \_ буфер постоянного \_ состояния ресурса</span><span class="sxs-lookup"><span data-stu-id="d14ae-153">D3D12\_RESOURCE\_STATE\_VERTEX\_AND\_CONSTANT\_BUFFER</span></span>
    -   <span data-ttu-id="d14ae-154">\_ \_ \_ Буфер индекса состояния ресурса \_ D3D12</span><span class="sxs-lookup"><span data-stu-id="d14ae-154">D3D12\_RESOURCE\_STATE\_INDEX\_BUFFER</span></span>
    -   <span data-ttu-id="d14ae-155">\_ \_ \_ Источник копирования состояния ресурса \_ D3D12</span><span class="sxs-lookup"><span data-stu-id="d14ae-155">D3D12\_RESOURCE\_STATE\_COPY\_SOURCE</span></span>
    -   <span data-ttu-id="d14ae-156">Ресурс D3D12 с \_ \_ состоянием ресурса \_ \_ шейдер не пикселей \_ \_</span><span class="sxs-lookup"><span data-stu-id="d14ae-156">D3D12\_RESOURCE\_STATE\_NON\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="d14ae-157">\_ \_ \_ \_ Ресурс построителя текстуры состояния ресурса \_ D3D12</span><span class="sxs-lookup"><span data-stu-id="d14ae-157">D3D12\_RESOURCE\_STATE\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="d14ae-158">\_ \_ \_ Косвенный аргумент состояния ресурса D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="d14ae-158">D3D12\_RESOURCE\_STATE\_INDIRECT\_ARGUMENT</span></span>
-   <span data-ttu-id="d14ae-159">Реадбакк кучи должны начинаться в \_ состоянии ресурса D3D12 \_ копирование состояния \_ \_ приемника.</span><span class="sxs-lookup"><span data-stu-id="d14ae-159">Readback heaps must start out in the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span>
-   <span data-ttu-id="d14ae-160">Буферы обратного переключения цепочки автоматически запускаются в \_ общем состоянии "состояние ресурса D3D12" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d14ae-160">Swap chain back buffers automatically start out in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span>

<span data-ttu-id="d14ae-161">Прежде чем кучу может быть целевым объектом операции копирования GPU, обычно куча должна быть переведена в \_ \_ \_ состояние приемника D3D12 для копирования состояния ресурса \_ .</span><span class="sxs-lookup"><span data-stu-id="d14ae-161">Before a heap can be the target of a GPU copy operation, normally the heap must first be transitioned to the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span> <span data-ttu-id="d14ae-162">Тем не менее ресурсы, созданные в кучах отправки, должны запускаться и не могут измениться из общего \_ состояния чтения, так как только процессор будет выполнять запись.</span><span class="sxs-lookup"><span data-stu-id="d14ae-162">However, resources created on UPLOAD heaps must start in and cannot change from the GENERIC\_READ state since only the CPU will be doing writing.</span></span> <span data-ttu-id="d14ae-163">И наоборот, зафиксированные ресурсы, созданные в кучах РЕАДБАКК, должны запускаться в и не могут изменяться из \_ состояния приемника копирования.</span><span class="sxs-lookup"><span data-stu-id="d14ae-163">Conversely, committed resources created in READBACK heaps must start in and cannot change from the COPY\_DEST state.</span></span>

### <a name="readwrite-resource-state-restrictions"></a><span data-ttu-id="d14ae-164">Ограничения состояния ресурсов для чтения и записи</span><span class="sxs-lookup"><span data-stu-id="d14ae-164">Read/write resource state restrictions</span></span>

<span data-ttu-id="d14ae-165">Биты использования состояния ресурсов, которые используются для описания состояния ресурса, делятся на состояния "только для чтения" и "чтение/запись".</span><span class="sxs-lookup"><span data-stu-id="d14ae-165">The resource state usage bits that are used to describe a resource state are divided into read-only and read/write states.</span></span> <span data-ttu-id="d14ae-166">В справочном разделе, посвященном [**\_ \_ состояниям ресурсов D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) , указывается уровень доступа для чтения и записи для каждого бита в перечислении.</span><span class="sxs-lookup"><span data-stu-id="d14ae-166">The reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indicates the read/write access level for each bit in the enumeration.</span></span>

<span data-ttu-id="d14ae-167">Для любого ресурса можно задать только один бит чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d14ae-167">At most, only one read/write bit can be set for any resource.</span></span> <span data-ttu-id="d14ae-168">Если задан бит записи, для этого ресурса не может быть установлен бит, доступный только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d14ae-168">If a write bit is set, then no read-only bit may be set for that resource.</span></span> <span data-ttu-id="d14ae-169">Если бит записи не задан, может быть задано любое число бит чтения.</span><span class="sxs-lookup"><span data-stu-id="d14ae-169">If no write bit is set, then any number of read bits may be set.</span></span>

### <a name="resource-states-for-presenting-back-buffers"></a><span data-ttu-id="d14ae-170">Состояния ресурсов для представления задних буферов</span><span class="sxs-lookup"><span data-stu-id="d14ae-170">Resource states for presenting back buffers</span></span>

<span data-ttu-id="d14ae-171">Перед выводом заднего буфера он должен находиться в \_ общем состоянии ресурса D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d14ae-171">Before a back buffer is presented, it must be in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span> <span data-ttu-id="d14ae-172">Обратите внимание, что состояние ресурса D3D12 \_ ресурсов \_ \_ представляет собой синоним для \_ состояния ресурса \_ D3D12 \_ Common, и оба они имеют значение 0.</span><span class="sxs-lookup"><span data-stu-id="d14ae-172">Note, the resource state D3D12\_RESOURCE\_STATE\_PRESENT is a synonym for D3D12\_RESOURCE\_STATE\_COMMON, and they both have a value of 0.</span></span> <span data-ttu-id="d14ae-173">Если [**идксгисвапчаин::P**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) повторная отправка (или [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) вызывается для ресурса, который в настоящее время не находится в этом состоянии, выдается предупреждение слоя отладки.</span><span class="sxs-lookup"><span data-stu-id="d14ae-173">If [**IDXGISwapChain::Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (or [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) is called on a resource that is not currently in this state, a debug layer warning is emitted.</span></span>

### <a name="discarding-resources"></a><span data-ttu-id="d14ae-174">Отмена ресурсов</span><span class="sxs-lookup"><span data-stu-id="d14ae-174">Discarding resources</span></span>

<span data-ttu-id="d14ae-175">Все подресурсы в ресурсе должны находиться в \_ состоянии целевого объекта прорисовки или в глубине \_ записи для целевых объектов отрисовки и ресурсов трафарета глубины соответственно, при вызове [**ID3D12GraphicsCommandList::D искардресаурце**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) .</span><span class="sxs-lookup"><span data-stu-id="d14ae-175">All subresources in a resource must be in the RENDER\_TARGET state, or DEPTH\_WRITE state, for render targets/depth-stencil resources respectively, when [**ID3D12GraphicsCommandList::DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) is called.</span></span>

## <a name="implicit-state-transitions"></a><span data-ttu-id="d14ae-176">Неявные переходы состояний</span><span class="sxs-lookup"><span data-stu-id="d14ae-176">Implicit State Transitions</span></span>

<span data-ttu-id="d14ae-177">Ресурсы могут быть "более продвинутыми" из \_ состояния ресурса D3D12 " \_ Общее" \_ .</span><span class="sxs-lookup"><span data-stu-id="d14ae-177">Resources can only be "promoted" out of D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="d14ae-178">Аналогичным образом ресурсы будут иметь значение "Decay", чтобы D3D12 \_ состояние ресурса " \_ Общее" \_ .</span><span class="sxs-lookup"><span data-stu-id="d14ae-178">Similarly, resources will only "decay" to D3D12\_RESOURCE\_STATE\_COMMON.</span></span>

### <a name="common-state-promotion"></a><span data-ttu-id="d14ae-179">Повышение общего состояния</span><span class="sxs-lookup"><span data-stu-id="d14ae-179">Common state promotion</span></span>

<span data-ttu-id="d14ae-180">Все буферные ресурсы, а также текстуры с \_ \_ флагом ресурса D3D12 \_ Разрешить \_ одновременный \_ флаг доступа неявно получаются из D3D12ного \_ состояния ресурса, \_ \_ общего для соответствующего состояния при первом доступе к GPU, включая универсальное \_ чтение, охватывающее любой сценарий чтения.</span><span class="sxs-lookup"><span data-stu-id="d14ae-180">All buffer resources as well as textures with the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set are implicitly promoted from D3D12\_RESOURCE\_STATE\_COMMON to the relevant state on first GPU access, including GENERIC\_READ to cover any read scenario.</span></span> <span data-ttu-id="d14ae-181">Доступ к любому ресурсу в общем состоянии можно получить, как если бы он находился в одном состоянии с</span><span class="sxs-lookup"><span data-stu-id="d14ae-181">Any resource in the COMMON state can be accessed as through it were in a single state with</span></span>

<dl> <span data-ttu-id="d14ae-182">1 флаг записи или</span><span class="sxs-lookup"><span data-stu-id="d14ae-182">1 WRITE flag, or</span></span>  
<span data-ttu-id="d14ae-183">1 или несколько флагов чтения</span><span class="sxs-lookup"><span data-stu-id="d14ae-183">1 or more READ flags</span></span>  
</dl>

<span data-ttu-id="d14ae-184">Ресурсы можно повысить на основе общего состояния, основанного на следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d14ae-184">Resources can be promoted from the COMMON state based on the following table:</span></span>



| <span data-ttu-id="d14ae-185">Флаг состояния</span><span class="sxs-lookup"><span data-stu-id="d14ae-185">State flag</span></span>                    | <span data-ttu-id="d14ae-186">Буферы и текстуры Simultaneous-Access</span><span class="sxs-lookup"><span data-stu-id="d14ae-186">Buffers and Simultaneous-Access Textures</span></span>                             | <span data-ttu-id="d14ae-187">Текстуры без одновременного доступа</span><span class="sxs-lookup"><span data-stu-id="d14ae-187">Non-Simultaneous-Access Textures</span></span>                                     |
|-------------------------------|----------------------------------------------|--------------------------------------|
| <span data-ttu-id="d14ae-188">ВЕРШИНный \_ и \_ Постоянный \_ буфер</span><span class="sxs-lookup"><span data-stu-id="d14ae-188">VERTEX\_AND\_CONSTANT\_BUFFER</span></span> | <span data-ttu-id="d14ae-189">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-189">Yes</span></span>                                          | <span data-ttu-id="d14ae-190">Нет</span><span class="sxs-lookup"><span data-stu-id="d14ae-190">No</span></span>                                   |
| <span data-ttu-id="d14ae-191">буфер ИНДЕКСов \_</span><span class="sxs-lookup"><span data-stu-id="d14ae-191">INDEX\_BUFFER</span></span>                 | <span data-ttu-id="d14ae-192">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-192">Yes</span></span>                                          | <span data-ttu-id="d14ae-193">Нет</span><span class="sxs-lookup"><span data-stu-id="d14ae-193">No</span></span>                                   |
| <span data-ttu-id="d14ae-194">\_целевой объект прорисовки</span><span class="sxs-lookup"><span data-stu-id="d14ae-194">RENDER\_TARGET</span></span>                | <span data-ttu-id="d14ae-195">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-195">Yes</span></span>                                          | <span data-ttu-id="d14ae-196">Нет</span><span class="sxs-lookup"><span data-stu-id="d14ae-196">No</span></span>                                   |
| <span data-ttu-id="d14ae-197">неупорядоченный \_ доступ</span><span class="sxs-lookup"><span data-stu-id="d14ae-197">UNORDERED\_ACCESS</span></span>             | <span data-ttu-id="d14ae-198">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-198">Yes</span></span>                                          | <span data-ttu-id="d14ae-199">Нет</span><span class="sxs-lookup"><span data-stu-id="d14ae-199">No</span></span>                                   |
| <span data-ttu-id="d14ae-200">\_запись глубины</span><span class="sxs-lookup"><span data-stu-id="d14ae-200">DEPTH\_WRITE</span></span>                  | <span data-ttu-id="d14ae-201">Нет<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d14ae-201">No<sup>\*</sup></span></span>                              | <span data-ttu-id="d14ae-202">Нет</span><span class="sxs-lookup"><span data-stu-id="d14ae-202">No</span></span>                                   |
| <span data-ttu-id="d14ae-203">чтение с ГЛУБИНой \_</span><span class="sxs-lookup"><span data-stu-id="d14ae-203">DEPTH\_READ</span></span>                   | <span data-ttu-id="d14ae-204">Нет<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d14ae-204">No<sup>\*</sup></span></span>                              | <span data-ttu-id="d14ae-205">Нет</span><span class="sxs-lookup"><span data-stu-id="d14ae-205">No</span></span>                                   |
| <span data-ttu-id="d14ae-206">\_ \_ ресурс шейдера, не являющегося пиксельным \_</span><span class="sxs-lookup"><span data-stu-id="d14ae-206">NON\_PIXEL\_SHADER\_RESOURCE</span></span>  | <span data-ttu-id="d14ae-207">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-207">Yes</span></span>                                          | <span data-ttu-id="d14ae-208">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-208">Yes</span></span>                                  |
| <span data-ttu-id="d14ae-209">\_ресурс шейдера \_ пикселей</span><span class="sxs-lookup"><span data-stu-id="d14ae-209">PIXEL\_SHADER\_RESOURCE</span></span>       | <span data-ttu-id="d14ae-210">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-210">Yes</span></span>                                          | <span data-ttu-id="d14ae-211">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-211">Yes</span></span>                                  |
| <span data-ttu-id="d14ae-212">\_потоковая передача</span><span class="sxs-lookup"><span data-stu-id="d14ae-212">STREAM\_OUT</span></span>                   | <span data-ttu-id="d14ae-213">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-213">Yes</span></span>                                          | <span data-ttu-id="d14ae-214">Нет</span><span class="sxs-lookup"><span data-stu-id="d14ae-214">No</span></span>                                   |
| <span data-ttu-id="d14ae-215">непрямое \_ аргумент</span><span class="sxs-lookup"><span data-stu-id="d14ae-215">INDIRECT\_ARGUMENT</span></span>            | <span data-ttu-id="d14ae-216">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-216">Yes</span></span>                                          | <span data-ttu-id="d14ae-217">Нет</span><span class="sxs-lookup"><span data-stu-id="d14ae-217">No</span></span>                                   |
| <span data-ttu-id="d14ae-218">Копировать \_ конечный</span><span class="sxs-lookup"><span data-stu-id="d14ae-218">COPY\_DEST</span></span>                    | <span data-ttu-id="d14ae-219">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-219">Yes</span></span>                                          | <span data-ttu-id="d14ae-220">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-220">Yes</span></span>                                  |
| <span data-ttu-id="d14ae-221">Копировать \_ источник</span><span class="sxs-lookup"><span data-stu-id="d14ae-221">COPY\_SOURCE</span></span>                  | <span data-ttu-id="d14ae-222">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-222">Yes</span></span>                                          | <span data-ttu-id="d14ae-223">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-223">Yes</span></span>                                  |
| <span data-ttu-id="d14ae-224">Разрешить \_ конечный</span><span class="sxs-lookup"><span data-stu-id="d14ae-224">RESOLVE\_DEST</span></span>                 | <span data-ttu-id="d14ae-225">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-225">Yes</span></span>                                          | <span data-ttu-id="d14ae-226">Нет</span><span class="sxs-lookup"><span data-stu-id="d14ae-226">No</span></span>                                   |
| <span data-ttu-id="d14ae-227">Разрешить \_ источник</span><span class="sxs-lookup"><span data-stu-id="d14ae-227">RESOLVE\_SOURCE</span></span>               | <span data-ttu-id="d14ae-228">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-228">Yes</span></span>                                          | <span data-ttu-id="d14ae-229">Нет</span><span class="sxs-lookup"><span data-stu-id="d14ae-229">No</span></span>                                   |
| <span data-ttu-id="d14ae-230">ЗАТЕНЕНИЯ</span><span class="sxs-lookup"><span data-stu-id="d14ae-230">PREDICATION</span></span>                   | <span data-ttu-id="d14ae-231">Да</span><span class="sxs-lookup"><span data-stu-id="d14ae-231">Yes</span></span>                                          | <span data-ttu-id="d14ae-232">Нет</span><span class="sxs-lookup"><span data-stu-id="d14ae-232">No</span></span>                                   |



 

<span data-ttu-id="d14ae-233"><sup>\*</sup>Ресурсы шаблона глубины должны быть текстурами, не поддерживающими одновременный доступ, и поэтому никогда не могут быть косвенно выдвинуты.</span><span class="sxs-lookup"><span data-stu-id="d14ae-233"><sup>\*</sup>Depth-stencil resources must be non-simultaneous-access textures and thus can never be implicitly promoted.</span></span>

<span data-ttu-id="d14ae-234">Когда этот доступ происходит, повышение действует как неявный барьер ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d14ae-234">When this access occurs the promotion acts like an implicit resource barrier.</span></span> <span data-ttu-id="d14ae-235">Для последующих обращений к ресурсам при необходимости потребуется изменить состояние ресурса.</span><span class="sxs-lookup"><span data-stu-id="d14ae-235">For subsequent accesses, resource barriers will be required to change the resource state if necessary.</span></span> <span data-ttu-id="d14ae-236">Обратите внимание, что продвижение от одного уровня чтения до нескольких состояний чтения допустимо, но это не так для записи состояния.</span><span class="sxs-lookup"><span data-stu-id="d14ae-236">Note that promotion from one promoted read state into multiple read state is valid, but this is not the case for write states.</span></span>  
<span data-ttu-id="d14ae-237">Например, если ресурс в общем состоянии повышен до \_ ресурса шейдера пикселей \_ в вызове Draw, его все равно можно повысить до NON_PIXEL \_ ресурса шейдера \_ | \_Ресурс шейдера пикселей \_ в другом вызове Draw.</span><span class="sxs-lookup"><span data-stu-id="d14ae-237">For example, if a resource in the common state is promoted to PIXEL\_SHADER\_RESOURCE in a Draw call, it can still be promoted to NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE in another Draw call.</span></span> <span data-ttu-id="d14ae-238">Однако, если он используется в операции записи, такой как назначение копирования, барьер перехода состояния ресурса из Объединенных состояний чтения повышенного уровня, здесь NON_PIXEL \_ ресурс шейдера \_ | \_Требуется ресурс шейдера пикселей \_ для копирования \_ dest.</span><span class="sxs-lookup"><span data-stu-id="d14ae-238">However, if it is used in a write operation, such as a copy destination, a resource state transition barrier from the combined promoted read states, here NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE, to COPY\_DEST is needed.</span></span>  
<span data-ttu-id="d14ae-239">Аналогично, при повышении уровня общего \_ назначения для копирования конечного объекта барьер по-прежнему требуется для перехода от \_ приемника копирования к \_ ЦЕЛЕВому объекту рендеринга.</span><span class="sxs-lookup"><span data-stu-id="d14ae-239">Similarly, if promoted from COMMON to COPY\_DEST, a barrier is still required to transition from COPY\_DEST to RENDER\_TARGET.</span></span>

<span data-ttu-id="d14ae-240">Обратите внимание, что распространенное повышение состояния является "свободным", так что GPU не требуется для выполнения каких-либо ожиданий синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d14ae-240">Note that common state promotion is "free" in that there is no need for the GPU to perform any synchronization waits.</span></span> <span data-ttu-id="d14ae-241">Продвижение представляет тот факт, что ресурсы в общем состоянии не должны требовать дополнительного отслеживания GPU или драйверов для поддержки определенных операций доступа.</span><span class="sxs-lookup"><span data-stu-id="d14ae-241">The promotion represents the fact that resources in the COMMON state should not require additional GPU work or driver tracking to support certain accesses.</span></span>

### <a name="state-decay-to-common"></a><span data-ttu-id="d14ae-242">Decay состояния для общего</span><span class="sxs-lookup"><span data-stu-id="d14ae-242">State decay to common</span></span>

<span data-ttu-id="d14ae-243">Зеркальная сторона повышения общего состояния Decay обратно в D3D12ное \_ \_ состояние ресурса \_ .</span><span class="sxs-lookup"><span data-stu-id="d14ae-243">The flip-side of common state promotion is decay back to D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="d14ae-244">Ресурсы, соответствующие определенным требованиям, считаются без отслеживания состояния и фактически возвращаются в общее состояние, когда GPU завершает выполнение операции [**ексекутекоммандлистс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) .</span><span class="sxs-lookup"><span data-stu-id="d14ae-244">Resources that meet certain requirements are considered to be stateless and effectively return to the common state when the GPU finishes execution of an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation.</span></span> <span data-ttu-id="d14ae-245">Decay не происходит между списками команд, выполняемых вместе в одном вызове **ексекутекоммандлистс** .</span><span class="sxs-lookup"><span data-stu-id="d14ae-245">Decay does not occur between command lists executed together in the same **ExecuteCommandLists** call.</span></span>

<span data-ttu-id="d14ae-246">Следующие ресурсы будут Decay при завершении операции [**ексекутекоммандлистс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) на GPU:</span><span class="sxs-lookup"><span data-stu-id="d14ae-246">The following resources will decay when an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation is completed on the GPU:</span></span>

-   <span data-ttu-id="d14ae-247">Ресурсы, к которым осуществляется доступ в очереди копирования, *или*</span><span class="sxs-lookup"><span data-stu-id="d14ae-247">Resources being accessed on a Copy queue, *or*</span></span>
-   <span data-ttu-id="d14ae-248">Буферные ресурсы в любом типе очереди *или*</span><span class="sxs-lookup"><span data-stu-id="d14ae-248">Buffer resources on any queue type, *or*</span></span>
-   <span data-ttu-id="d14ae-249">Ресурсы текстуры в любом типе очереди, для которых установлен \_ флаг ресурса D3D12 \_ \_ Разрешить \_ одновременный \_ доступ, *или*</span><span class="sxs-lookup"><span data-stu-id="d14ae-249">Texture resources on any queue type that have the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set, *or*</span></span>
-   <span data-ttu-id="d14ae-250">Любой ресурс неявным образом повышается до состояния только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d14ae-250">Any resource implicitly promoted to a read-only state.</span></span>

<span data-ttu-id="d14ae-251">Как и при распространении состояния, Decay предоставляется бесплатно в том случае, если дополнительная синхронизация не требуется.</span><span class="sxs-lookup"><span data-stu-id="d14ae-251">Like common state promotion, the decay is free in that no additional synchronization is needed.</span></span> <span data-ttu-id="d14ae-252">Сочетание распространенного повышения состояния и Decay может помочь устранить множество ненужных переходов [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) .</span><span class="sxs-lookup"><span data-stu-id="d14ae-252">Combining common state promotion and decay can help to eliminate many unnecessary [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions.</span></span> <span data-ttu-id="d14ae-253">В некоторых случаях это может привести к значительному улучшению производительности.</span><span class="sxs-lookup"><span data-stu-id="d14ae-253">In some cases, this can provide significant performance improvements.</span></span>

<span data-ttu-id="d14ae-254">Буферы и Simultaneous-Access ресурсы будут Decay к общему состоянию независимо от того, были ли они явно перенесены с помощью барьеров ресурсов или неявно повышены.</span><span class="sxs-lookup"><span data-stu-id="d14ae-254">Buffers and Simultaneous-Access resources will decay to the common state regardless of whether they were explicitly transitioned using resource barriers or implicitly promoted.</span></span>

### <a name="performance-implications"></a><span data-ttu-id="d14ae-255">Влияние на производительность</span><span class="sxs-lookup"><span data-stu-id="d14ae-255">Performance implications</span></span>

<span data-ttu-id="d14ae-256">При записи явных [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) переходов для ресурсов в общем состоянии необходимо использовать \_ общее состояние ресурса D3D12 или любое переопределяющее \_ \_ состояние как значение *бефорестате* в \_ \_ \_ структуре барьера перехода ресурсов D3D12.</span><span class="sxs-lookup"><span data-stu-id="d14ae-256">When recording explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions on resources in the common state, it is correct to use either D3D12\_RESOURCE\_STATE\_COMMON or any promotable state as the *BeforeState* value in the D3D12\_RESOURCE\_TRANSITION\_BARRIER structure.</span></span> <span data-ttu-id="d14ae-257">Это обеспечивает традиционное управление состоянием, которое игнорирует автоматические Decay буферов и текстуры с одновременным доступом.</span><span class="sxs-lookup"><span data-stu-id="d14ae-257">This allows traditional state management that ignores automatic decay of buffers and simultaneous-access textures.</span></span> <span data-ttu-id="d14ae-258">Это может быть нежелательно, так как предотвращение **ресаурцебарриер** вызовов с ресурсами, которые находятся в общем состоянии, может значительно повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="d14ae-258">This may not be desirable though, as avoiding transition **ResourceBarrier** calls with resources known to be in the common state can significantly improve performance.</span></span> <span data-ttu-id="d14ae-259">Барьеры ресурсов могут быть дорогостоящими.</span><span class="sxs-lookup"><span data-stu-id="d14ae-259">Resource barriers can be expensive.</span></span> <span data-ttu-id="d14ae-260">Они предназначены для принудительного сброса кэша, изменения макета памяти и другие операции синхронизации, которые могут не потребоваться для ресурсов, которые уже находятся в общем состоянии.</span><span class="sxs-lookup"><span data-stu-id="d14ae-260">They are designed to force cache flushes, memory layout changes and other synchronization that may not be necessary for resources already in the common state.</span></span> <span data-ttu-id="d14ae-261">Список команд, использующий барьер ресурсов из нераспространенного состояния в другое необычное состояние для ресурса, находящегося в общем состоянии, может привести к ненужным издержкам.</span><span class="sxs-lookup"><span data-stu-id="d14ae-261">A command list that uses a resource barrier from a non-common state to another non-common state on a resource currently in the common state can introduce a lot of unneeded overhead.</span></span>

<span data-ttu-id="d14ae-262">Кроме того, следует избегать явного перехода [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) в D3D12ное \_ состояние ресурса, \_ \_ если это не обязательно (например, следующий доступ находится в очереди команд копирования, для которой требуется, чтобы ресурсы начали в общем состоянии).</span><span class="sxs-lookup"><span data-stu-id="d14ae-262">Also, avoid explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions to D3D12\_RESOURCE\_STATE\_COMMON unless absolutely necessary (e.g. the next access is on a COPY command queue which requires a resources begin in the common state).</span></span> <span data-ttu-id="d14ae-263">Чрезмерное число переходов к общему состоянию может значительно замедлить производительность GPU.</span><span class="sxs-lookup"><span data-stu-id="d14ae-263">Excessive transitions to the common state can dramatically slow down GPU performance.</span></span>

<span data-ttu-id="d14ae-264">В целом, постарайтесь полагаться на распространенное повышение состояния и Decay каждый раз, когда его семантика позволяет избежать выполнения вызовов [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) .</span><span class="sxs-lookup"><span data-stu-id="d14ae-264">In summary, try to rely on common state promotion and decay whenever its semantics let you get away without issuing [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) calls.</span></span>

## <a name="split-barriers"></a><span data-ttu-id="d14ae-265">Разделите барьеры</span><span class="sxs-lookup"><span data-stu-id="d14ae-265">Split Barriers</span></span>

<span data-ttu-id="d14ae-266">Барьер переключения ресурсов с \_ \_ флагом запуска D3D12а барьера ресурсов \_ \_ \_ начинает разбивать барьер, а барьер перехода считается ожидающим.</span><span class="sxs-lookup"><span data-stu-id="d14ae-266">A resource transition barrier with the D3D12\_RESOURCE\_BARRIER\_FLAG\_BEGIN\_ONLY flag begins a split barrier and the transition barrier is said to be pending.</span></span> <span data-ttu-id="d14ae-267">Пока барьер находится в состоянии ожидания, ресурс (подкласс) не может быть прочитан или записан с помощью GPU.</span><span class="sxs-lookup"><span data-stu-id="d14ae-267">While the barrier is pending the (sub)resource cannot be read or written by the GPU.</span></span> <span data-ttu-id="d14ae-268">Единственный допустимый барьер переходов, который можно применить к ресурсу (подзадаче) с ожидающим барьером, — это один из состояний *до* и *после* , а также флаг D3D12а \_ \_ барьера ресурсов \_ \_ \_ , который барьер завершает ожидание ожидающего перехода.</span><span class="sxs-lookup"><span data-stu-id="d14ae-268">The only legal transition barrier that can be applied to a (sub)resource with a pending barrier is one with the same *before* and *after* states and the D3D12\_RESOURCE\_BARRIER\_FLAG\_END\_ONLY flag, which barrier completes the pending transition.</span></span>

<span data-ttu-id="d14ae-269">Разделите барьеры предоставляют подсказки для GPU, которые ресурс в состоянии *а* затем будет использоваться в состоянии *б* позже.</span><span class="sxs-lookup"><span data-stu-id="d14ae-269">Split barriers provide hints to the GPU that a resource in state *A* will next be used in state *B* sometime later.</span></span> <span data-ttu-id="d14ae-270">Это дает GPU возможность оптимизировать рабочую нагрузку перехода, что может привести к сокращению или устранению ожидания выполнения.</span><span class="sxs-lookup"><span data-stu-id="d14ae-270">This gives the GPU the option to optimize the transition workload, possibly reducing or eliminating execution stalls.</span></span> <span data-ttu-id="d14ae-271">При выдаче конечного барьера гарантируется, что все операции перехода GPU завершаются до перехода к следующей команде.</span><span class="sxs-lookup"><span data-stu-id="d14ae-271">Issuing the end-only barrier guarantees that all GPU transition work is finished before moving onto the next command.</span></span>

<span data-ttu-id="d14ae-272">С помощью раздельных барьеров можно повысить производительность, особенно в сценариях с несколькими модулями или при том, что ресурсы, доступные для чтения и записи, распределены по всему одному или нескольким спискам команд.</span><span class="sxs-lookup"><span data-stu-id="d14ae-272">Using split barriers can help to improve performance, especially in multi-engine scenarios or where resources are read/write transitioned sparsely throughout one or more command lists.</span></span>

## <a name="resource-barrier-example-scenario"></a><span data-ttu-id="d14ae-273">Пример сценария барьера ресурсов</span><span class="sxs-lookup"><span data-stu-id="d14ae-273">Resource barrier example scenario</span></span>

<span data-ttu-id="d14ae-274">В следующих фрагментах кода показано использование метода [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) в примере многопоточности.</span><span class="sxs-lookup"><span data-stu-id="d14ae-274">The following snippets show the use of the [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) method in a multi-threading sample.</span></span>

<span data-ttu-id="d14ae-275">Создание представления трафарета глубины с переходом в состояние, доступное для записи.</span><span class="sxs-lookup"><span data-stu-id="d14ae-275">Creating the depth stencil view, transitioning it to a writeable state.</span></span>


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



<span data-ttu-id="d14ae-276">Создание представления буфера вершин, сначала изменение его из общего состояния на назначение, а затем из места назначения в общее доступное для чтения состояние.</span><span class="sxs-lookup"><span data-stu-id="d14ae-276">Creating the vertex buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



<span data-ttu-id="d14ae-277">Создание представления буфера индексов, сначала изменение его из общего состояния на назначение, а затем из места назначения в общее доступное для чтения состояние.</span><span class="sxs-lookup"><span data-stu-id="d14ae-277">Creating the index buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



<span data-ttu-id="d14ae-278">Создание текстур и представлений ресурсов шейдера.</span><span class="sxs-lookup"><span data-stu-id="d14ae-278">Creating textures and shader resource views.</span></span> <span data-ttu-id="d14ae-279">Текстура изменяется от общего состояния к назначению, а затем от назначения к ресурсу шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="d14ae-279">The texture is changed from a common state to a destination, and then from a destination to a pixel shader resource.</span></span>


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



<span data-ttu-id="d14ae-280">Начало кадра; Он не только использует [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) для указания того, что в качестве целевого объекта рендеринга используется буфер обмена, но также инициализируется ресурс кадра (который вызывает **ресаурцебарриер** в буфере трафарета глубины).</span><span class="sxs-lookup"><span data-stu-id="d14ae-280">Beginning a frame; this not only uses [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to indicate that the backbuffer is to be used as a render target, but also initializes the frame resource (which calls **ResourceBarrier** on the depth stencil buffer).</span></span>


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



<span data-ttu-id="d14ae-281">Завершение кадра с указанием заднего буфера, который теперь используется для представления.</span><span class="sxs-lookup"><span data-stu-id="d14ae-281">Ending a frame, indicating the back buffer is now used to present.</span></span>


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



<span data-ttu-id="d14ae-282">Инициализация ресурса фрейма, вызываемого при начале кадра, переводит буфер трафарета глубины в доступный для записи.</span><span class="sxs-lookup"><span data-stu-id="d14ae-282">Initializing a frame resource, called when beginning a frame, transitions the depth stencil buffer to writeable.</span></span>


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



<span data-ttu-id="d14ae-283">Барьеры направляются в середину фрейма, переходя к теневой карте с возможностью чтения.</span><span class="sxs-lookup"><span data-stu-id="d14ae-283">Barriers are swapped mid-frame, transitioning the shadow map from writeable to readable.</span></span>


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



<span data-ttu-id="d14ae-284">Метод Finish вызывается, когда кадр завершается, переключается на теневую карту в общее состояние.</span><span class="sxs-lookup"><span data-stu-id="d14ae-284">Finish is called when a frame is ended, transitioning the shadow map to a common state.</span></span>


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a><span data-ttu-id="d14ae-285">Пример повышения общего состояния и Decay</span><span class="sxs-lookup"><span data-stu-id="d14ae-285">Common state promotion and decay sample</span></span>

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a><span data-ttu-id="d14ae-286">Пример разделенных барьеров</span><span class="sxs-lookup"><span data-stu-id="d14ae-286">Example of split barriers</span></span>

<span data-ttu-id="d14ae-287">В следующем примере показано использование барьера разделения для уменьшения количества ожиданий конвейера.</span><span class="sxs-lookup"><span data-stu-id="d14ae-287">The following example shows how to use a split barrier to reduce pipeline stalls.</span></span> <span data-ttu-id="d14ae-288">Следующий код не использует барьеры разделения:</span><span class="sxs-lookup"><span data-stu-id="d14ae-288">The code that follows does not use split barriers:</span></span>

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

<span data-ttu-id="d14ae-289">В следующем коде используются барьеры разделения:</span><span class="sxs-lookup"><span data-stu-id="d14ae-289">The following code uses split barriers:</span></span>

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a><span data-ttu-id="d14ae-290">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d14ae-290">Related topics</span></span>

[<span data-ttu-id="d14ae-291">Учебные видеоматериалы по DirectX для расширенного обучения: барьеры ресурсов и отслеживание состояния</span><span class="sxs-lookup"><span data-stu-id="d14ae-291">DirectX advanced learning video tutorials : Resource Barriers and State Tracking</span></span>](https://www.youtube.com/watch?v=nmB2XMasz2o)

[<span data-ttu-id="d14ae-292">Синхронизация с несколькими движками</span><span class="sxs-lookup"><span data-stu-id="d14ae-292">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)

[<span data-ttu-id="d14ae-293">Отправка работы в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d14ae-293">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)

[<span data-ttu-id="d14ae-294">Взгляните на барьеры состояния ресурсов D3D12</span><span class="sxs-lookup"><span data-stu-id="d14ae-294">A Look Inside D3D12 Resource State Barriers</span></span>](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

