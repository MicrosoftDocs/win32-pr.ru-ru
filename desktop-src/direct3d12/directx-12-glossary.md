---
title: Глоссарий Direct3D 12
description: Эти термины являются отличительными чертами Direct3D 12.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a84b4b2e5a993b33b4c322b91682c8f9b5499bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549023"
---
# <a name="direct3d-12-glossary"></a><span data-ttu-id="fdf88-103">Глоссарий Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fdf88-103">Direct3D 12 glossary</span></span>

<span data-ttu-id="fdf88-104">Эти термины являются отличительными чертами Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="fdf88-104">These terms are distinctive of Direct3D 12.</span></span>

<dl> <dt>

<span data-ttu-id="fdf88-105"><span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**вязывания**</span><span class="sxs-lookup"><span data-stu-id="fdf88-105"><span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-106">Процесс присоединения памяти к графическому конвейеру.</span><span class="sxs-lookup"><span data-stu-id="fdf88-106">The process of attaching memory to the graphics pipeline.</span></span> <span data-ttu-id="fdf88-107">Привязка ресурсов, например, включает в себя привязку ресурса, например текстуры к конвейеру, для использования при отрисовке объекта.</span><span class="sxs-lookup"><span data-stu-id="fdf88-107">Resource binding, for example, involves the binding of a resource such as a texture to the pipeline, for use in rendering an object.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-108"><span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**двойной**</span><span class="sxs-lookup"><span data-stu-id="fdf88-108"><span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**buffer**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-109">Тип ресурса D3D, который является синонимом непрерывного выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="fdf88-109">A type of D3D resource that is synonymous with a contiguous memory allocation.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-110"><span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**средство**</span><span class="sxs-lookup"><span data-stu-id="fdf88-110"><span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**bundle**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-111">Буфер команд, который модуль обработки графических процессоров может выполнять только непосредственно через *список прямых команд*.</span><span class="sxs-lookup"><span data-stu-id="fdf88-111">A command buffer that the graphics processing unit (GPU) can execute only directly via a *direct command list*.</span></span> <span data-ttu-id="fdf88-112">Пакет наследует все состояние GPU (за исключением заданного в настоящее время *объекта состояния конвейера* и топологии примитива).</span><span class="sxs-lookup"><span data-stu-id="fdf88-112">A bundle inherits all GPU state (except for the currently set *pipeline state object* and primitive topology).</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-113"><span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**распределитель команд**</span><span class="sxs-lookup"><span data-stu-id="fdf88-113"><span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**command allocator**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-114">Базовые выделения памяти, в которых хранятся команды GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-114">The underlying memory allocations in which GPU commands are stored.</span></span> <span data-ttu-id="fdf88-115">Объект распределителя команд применяется как к *прямым спискам команд* , так и к *пакетам*.</span><span class="sxs-lookup"><span data-stu-id="fdf88-115">The command allocator object applies to both *direct command lists* and *bundles*.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-116"><span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**Список команд**</span><span class="sxs-lookup"><span data-stu-id="fdf88-116"><span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**command list**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-117">Список команд соответствует набору команд, выполняемых GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-117">A command list corresponds to a set of commands which the GPU executes.</span></span> <span data-ttu-id="fdf88-118">К ним относятся такие команды, как установка состояния, рисование, очистка и копирование.</span><span class="sxs-lookup"><span data-stu-id="fdf88-118">These include commands such as to set state, draw, clear, and copy.</span></span> <span data-ttu-id="fdf88-119">Интерфейс списка команд D3D12 значительно отличается от интерфейса списка команд D3D11.</span><span class="sxs-lookup"><span data-stu-id="fdf88-119">The D3D12 command list interface is significantly different than the D3D11 command list interface.</span></span> <span data-ttu-id="fdf88-120">Интерфейс списка команд D3D12 содержит интерфейсы API, аналогичные интерфейсам API отрисовки контекста устройства D3D11.</span><span class="sxs-lookup"><span data-stu-id="fdf88-120">The D3D12 command list interface contains APIs similar to the D3D11 device context rendering APIs.</span></span>

<span data-ttu-id="fdf88-121">Список команд D3D12 не сопоставляет ресурсы и не отменяет их сопоставление, изменяет сопоставления плиток, меняет размер пулов плиток, получает данные запроса и не выполняет неявное пересылке команд GPU для выполнения.</span><span class="sxs-lookup"><span data-stu-id="fdf88-121">A D3D12 command list does not map or unmap resources, change tile mappings, resize tile pools, get query data, nor does it ever implicitly submit commands to the GPU for execution.</span></span>

<span data-ttu-id="fdf88-122">В отличие от D3D11 отложенных контекстов, списки команд D3D12 поддерживают только два уровня косвенного обращения.</span><span class="sxs-lookup"><span data-stu-id="fdf88-122">Unlike D3D11 deferred contexts, D3D12 command lists only support two levels of indirection.</span></span> <span data-ttu-id="fdf88-123">*Прямой список команд* соответствует буферу команд, который может выполняться графическим процессором.</span><span class="sxs-lookup"><span data-stu-id="fdf88-123">A *direct command list* corresponds to a command buffer which the GPU can execute.</span></span> <span data-ttu-id="fdf88-124">*Пакет* может выполняться только непосредственно через список прямых команд.</span><span class="sxs-lookup"><span data-stu-id="fdf88-124">A *bundle* can be executed only directly via a direct command list.</span></span>

<span data-ttu-id="fdf88-125">Прямой список команд не наследует никаких состояний GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-125">A direct command list does not inherit any GPU state.</span></span> <span data-ttu-id="fdf88-126">Пакет наследует все состояние GPU (за исключением заданного в настоящее время объекта состояния конвейера и топологии примитива).</span><span class="sxs-lookup"><span data-stu-id="fdf88-126">A bundle inherits all GPU state (except for the currently set pipeline state object and primitive topology).</span></span>

<span data-ttu-id="fdf88-127">Память для списка команд задается *распределителем команд*.</span><span class="sxs-lookup"><span data-stu-id="fdf88-127">Memory for a command list is set by the *command allocator*.</span></span> <span data-ttu-id="fdf88-128">Назначение списков команд заключается в том, что их можно отправить в GPU в виде одного запроса на визуализацию.</span><span class="sxs-lookup"><span data-stu-id="fdf88-128">The purpose of command lists is that they can be submitted to a GPU as a single rendering request.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-129"><span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**очередь команд**</span><span class="sxs-lookup"><span data-stu-id="fdf88-129"><span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**command queue**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-130">Очередь *команд* , в которой выполняется выполнение GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-130">A queue of *command lists* that the GPU executes in succession.</span></span> <span data-ttu-id="fdf88-131">Приложения должны явно отправлять *списки команд* в очередь команд для выполнения.</span><span class="sxs-lookup"><span data-stu-id="fdf88-131">Applications must explicitly submit *command lists* to a command queue for execution.</span></span> <span data-ttu-id="fdf88-132">Обычно существует три командные очереди: трехмерная графика, вычисление и копирование, соответствующее конвейеру трехмерной графики, подсистеме вычислений и одному или нескольким обработчикам копирования на GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-132">Typically there are three command queues: 3D graphics, compute and copy, corresponding to the 3D graphics pipeline, the compute engine, and one or more copy engines, on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-133"><span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**консервативная растрирование**</span><span class="sxs-lookup"><span data-stu-id="fdf88-133"><span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**conservative rasterization**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-134">Консервативная растрирование — это режим работы для этапа растеризации графического конвейера Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fdf88-134">Conservative rasterization is a mode of operation for the rasterizer stage of the Direct3D graphics pipeline.</span></span> <span data-ttu-id="fdf88-135">Он отключает стандартную растрирование, основанную на образце, и вместо этого преобразует пиксел, покрываемый любой суммой, на примитив.</span><span class="sxs-lookup"><span data-stu-id="fdf88-135">It disables the standard sample-based rasterization, and will instead rasterize a pixel that is covered by any amount by a primitive.</span></span> <span data-ttu-id="fdf88-136">Одно важное отличие состоит в том, что, хотя любое покрытие на самом деле создает растровый пиксель, это покрытие не может быть характеризуется оборудованием, поэтому покрытие всегда отображается в виде двоичного шейдера пикселей: полностью охвачен или не охвачен.</span><span class="sxs-lookup"><span data-stu-id="fdf88-136">One important distinction is that, while any coverage at all produces a rasterized pixel, that coverage cannot be characterized by the hardware, so coverage always appears binary to a pixel shader: either fully covered or not covered.</span></span> <span data-ttu-id="fdf88-137">Он остается кодом шейдера пикселей для анализа фактического покрытия.</span><span class="sxs-lookup"><span data-stu-id="fdf88-137">It is left to the pixel shader code to analytically determine the actual coverage.</span></span>

<span data-ttu-id="fdf88-138">Консервативная растрирование может помочь в таких проблемах, как конфликты и обнаружение попаданий, группирования и перекрытия, где цвет пикселя является более определенным, а граничные варианты можно исключить.</span><span class="sxs-lookup"><span data-stu-id="fdf88-138">Conservative rasterization can help with such problems as collision and hit detection, binning, and occlusion culling, where the color of a pixel is more certain and edge cases can be eliminated.</span></span> <span data-ttu-id="fdf88-139">См. раздел [консервативная растрирование](conservative-rasterization.md).</span><span class="sxs-lookup"><span data-stu-id="fdf88-139">See [Conservative Rasterization](conservative-rasterization.md).</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-140"><span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Представление буфера констант (CBV)**</span><span class="sxs-lookup"><span data-stu-id="fdf88-140"><span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Constant Buffer View (CBV)**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-141">Буферы констант содержат константные данные шейдера, такие как представление камеры, матрицы проекций и мировые матрицы.</span><span class="sxs-lookup"><span data-stu-id="fdf88-141">Constant buffers contain shader constant data, such as a camera view, projection matrices, and world matrices.</span></span> <span data-ttu-id="fdf88-142">"Представление буфера констант" — это представление буфера, зависящее от формата, которое отображается в графическом конвейере.</span><span class="sxs-lookup"><span data-stu-id="fdf88-142">A "constant buffer view" is the format-specific view of the buffer as seen by the graphics pipeline.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-143"><span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**куча по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="fdf88-143"><span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**default heap**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-144">Куча пользовательского режима, обеспечивающая поддержку постоянных типов ресурсов GPU, включая ресурсы, записанные GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-144">A user-mode heap that is focused on supporting persistent GPU resource types, including GPU-written resources.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-145"><span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**Descriptor**</span><span class="sxs-lookup"><span data-stu-id="fdf88-145"><span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**descriptor**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-146">Дескрипторы являются основной единицей привязки для одного ресурса в D3D12.</span><span class="sxs-lookup"><span data-stu-id="fdf88-146">Descriptors are the primary unit of binding for a single resource in D3D12.</span></span> <span data-ttu-id="fdf88-147">Дескриптор — это относительно небольшой блок данных, который полностью описывает объект для GPU в формате, характерном для GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-147">A descriptor is a relatively small block of data that fully describes an object to the GPU, in a GPU specific format.</span></span> <span data-ttu-id="fdf88-148">Существует множество различных типов дескрипторов: представления ресурсов шейдера (СРВС), неупорядоченные представления доступа (Уавс), представления постоянного буфера (КБВС) и пробы являются несколькими примерами.</span><span class="sxs-lookup"><span data-stu-id="fdf88-148">There are many different types of descriptors: Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers are a few examples.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-149"><span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**куча дескрипторов**</span><span class="sxs-lookup"><span data-stu-id="fdf88-149"><span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**descriptor heap**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-150">Куча дескрипторов — это набор смежных выделений дескрипторов, по одному выделению для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="fdf88-150">A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.</span></span> <span data-ttu-id="fdf88-151">Основной точкой кучи дескриптора является охватывающая часть памяти, необходимая для хранения спецификаций дескрипторов типов объектов, на которые ссылается шейдер, для того, чтобы большая часть окна отрисовки была как можно больше (в идеале это весь кадр отрисовки или более).</span><span class="sxs-lookup"><span data-stu-id="fdf88-151">The primary point of a descriptor heap is to encompass the bulk of memory allocation required for storing the descriptor specifications of object types that shaders reference for as large of a window of rendering as possible (ideally an entire frame of rendering or more).</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-152"><span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**Таблица дескрипторов**</span><span class="sxs-lookup"><span data-stu-id="fdf88-152"><span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**descriptor table**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-153">Таблица дескрипторов логически представляет собой набор дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="fdf88-153">A descriptor table is logically an array of descriptors.</span></span> <span data-ttu-id="fdf88-154">Каждая таблица дескрипторов хранит дескрипторы одного или нескольких типов, включая СРВС, уаве, КБВС и пробы.</span><span class="sxs-lookup"><span data-stu-id="fdf88-154">Each descriptor table stores descriptors of one or more types, including SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="fdf88-155">Таблица дескрипторов не является выделением памяти, это просто смещение и длина в куче дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="fdf88-155">A descriptor table is not an allocation of memory, it is simply an offset and length into a descriptor heap.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-156"><span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**список прямых команд**</span><span class="sxs-lookup"><span data-stu-id="fdf88-156"><span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**direct command list**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-157">Буфер команд, который может выполняться GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-157">A command buffer that the GPU can execute.</span></span> <span data-ttu-id="fdf88-158">Прямые списки команд не наследуют состояние GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-158">A direct command list doesn't inherit any GPU state.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-159"><span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**границе**</span><span class="sxs-lookup"><span data-stu-id="fdf88-159"><span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**fence**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-160">Механизм синхронизации GPU и ЦП.</span><span class="sxs-lookup"><span data-stu-id="fdf88-160">A mechanism to synchronize the GPU and CPU.</span></span> <span data-ttu-id="fdf88-161">Как GPU, так и ЦП могут быть настроены для ожидания ограждения, ожидая, как только другой процессор будет перехватываться.</span><span class="sxs-lookup"><span data-stu-id="fdf88-161">Both the GPU and CPU can be instructed to wait at a fence, waiting in effect for the other processor to catch up.</span></span> <span data-ttu-id="fdf88-162">См. раздел [Синхронизация с несколькими модулями](./user-mode-heap-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="fdf88-162">See [Multi-engine synchronization](./user-mode-heap-synchronization.md).</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-163"><span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**опасность, отслеживание опасности**</span><span class="sxs-lookup"><span data-stu-id="fdf88-163"><span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**hazard, hazard tracking**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-164">Опасность возникает, когда ресурс используется для одной цели, и приложение планирует повторно использовать его для другой цели.</span><span class="sxs-lookup"><span data-stu-id="fdf88-164">A hazard occurs when a resource has been used for one purpose, and the app intends to reuse it for another purpose.</span></span> <span data-ttu-id="fdf88-165">Для повторного использования ресурса промежуточные кэши должны быть сброшены или аннулированы, требования к сжатию должны соответствовать второму использованию, а ресурс должен находиться в нужном состоянии, чтобы избежать считывания ресурса после его записи в и сделать недействительными в целях назначения.</span><span class="sxs-lookup"><span data-stu-id="fdf88-165">In order to use the resource again, intermediate caches will need to be flushed or invalidated, compression requirements will need to be consistent with the second use, and the resource should be in the required state to avoid reading the resource after it has been written to and invalidated for the intended purpose.</span></span>

<span data-ttu-id="fdf88-166">Процесс поддержания ресурсов и предотвращения этих проблем синхронизации называется отслеживанием опасности.</span><span class="sxs-lookup"><span data-stu-id="fdf88-166">The process of maintaining resources and avoiding these sync issues is known as hazard tracking.</span></span> <span data-ttu-id="fdf88-167">Если драйвер не отслеживает опасности, приложение несет ответственность за это.</span><span class="sxs-lookup"><span data-stu-id="fdf88-167">If there is no hazard tracking by the driver, then the app is responsible for this.</span></span> <span data-ttu-id="fdf88-168">В большинстве предыдущих версий DirectX отслеживание опасности было обработано драйвером.</span><span class="sxs-lookup"><span data-stu-id="fdf88-168">In most earlier versions of DirectX, hazard tracking was handled by the driver.</span></span> <span data-ttu-id="fdf88-169">Для повышения производительности в DirectX 12 доступны методы без отслеживания опасности.</span><span class="sxs-lookup"><span data-stu-id="fdf88-169">To improve performance, methods without hazard tracking are available in DirectX 12.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-170"><span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**Язык шейдера высокого уровня (HLSL)**</span><span class="sxs-lookup"><span data-stu-id="fdf88-170"><span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**High-Level Shader Language (HLSL)**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-171">Язык компьютера, аналогичный, но отличающийся различными способами от C, который используется для написания кода шейдера.</span><span class="sxs-lookup"><span data-stu-id="fdf88-171">A computer language, similar but distinct in many ways from C, that is used to write shader code.</span></span> <span data-ttu-id="fdf88-172">Шейдеры вершин, пиксельных, геометрических, вычислений, доменов и поверхности записываются с помощью HLSL.</span><span class="sxs-lookup"><span data-stu-id="fdf88-172">Vertex, pixel, geometry, compute, domain, and hull shaders are all written using HLSL.</span></span> <span data-ttu-id="fdf88-173">Компилятор преобразует источник HLSL в двоичный формат для использования GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-173">A compiler converts the HLSL source into a binary format for the GPU to consume.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-174"><span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**Многомодульная система**</span><span class="sxs-lookup"><span data-stu-id="fdf88-174"><span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-175">Различные экземпляры и типы ядер в одном GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-175">The different instances and types of engines in a single GPU.</span></span> <span data-ttu-id="fdf88-176">К типам модулей относятся: графические, COMPUTE и Copy.</span><span class="sxs-lookup"><span data-stu-id="fdf88-176">The types of engines include: graphics, compute, and copy.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-177"><span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**мултигпу**</span><span class="sxs-lookup"><span data-stu-id="fdf88-177"><span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-178">Конфигурация оборудования, в которой имеется более одного графического адаптера.</span><span class="sxs-lookup"><span data-stu-id="fdf88-178">A hardware configuration where there is more than one graphics adapter.</span></span> <span data-ttu-id="fdf88-179">Отдельные адаптеры иногда называют узлами.</span><span class="sxs-lookup"><span data-stu-id="fdf88-179">The separate adapters are sometimes referred to as nodes.</span></span> <span data-ttu-id="fdf88-180">Наличие нескольких графических процессоров может заставить задачу синхронизировать их с ЦП, а другое — значительно сложнее, чем с помощью одного GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-180">Having multiple GPUs can make the task of synchronizing them with the CPU, and each other, considerably more complex than with a single GPU.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-181"><span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Объект состояния конвейера (PSO)**</span><span class="sxs-lookup"><span data-stu-id="fdf88-181"><span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Pipeline State object (PSO)**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-182">Значительная часть состояния GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-182">A significant portion of the state of the GPU.</span></span> <span data-ttu-id="fdf88-183">Это состояние включает все заданные в данный момент шейдеры и определенные объекты состояния фиксированной функции.</span><span class="sxs-lookup"><span data-stu-id="fdf88-183">This state includes all currently set shaders and certain fixed-function state objects.</span></span> <span data-ttu-id="fdf88-184">Единственный способ изменить состояния, содержащиеся в объекте конвейера, — изменить объект конвейера, привязанный к текущему объекту.</span><span class="sxs-lookup"><span data-stu-id="fdf88-184">The only way to change states contained within the pipeline object is to change the currently bound pipeline object.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-185"><span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**затенения**</span><span class="sxs-lookup"><span data-stu-id="fdf88-185"><span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**predication**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-186">Затенения — это функция, которая позволяет GPU, а не ЦП определять, что не может рисовать, копировать или отправлять объект.</span><span class="sxs-lookup"><span data-stu-id="fdf88-186">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy or dispatch an object.</span></span> <span data-ttu-id="fdf88-187">Например, если ограничивающий прямоугольник объекта полностью перекрыто другим объектом или перспективой, размер объекта уменьшился до меньшего размера пикселя, то, возможно, нет никакой точки в попытке рисования скрытого объекта.</span><span class="sxs-lookup"><span data-stu-id="fdf88-187">For example, if a bounding box of an object is totally occluded by another object or perspective has reduced the object to less than the size of a pixel, there may be no point in attempting to draw the hidden object at all.</span></span> <span data-ttu-id="fdf88-188">См. [затенения](predication.md).</span><span class="sxs-lookup"><span data-stu-id="fdf88-188">See [Predication](predication.md).</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-189"><span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Представление порядка средства отображения программной прорисовки (ров)**</span><span class="sxs-lookup"><span data-stu-id="fdf88-189"><span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Rasterizer Order View (ROV)**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-190">В стандартных графических конвейерах могут возникнуть проблемы с правильной компоновкой нескольких текстур, содержащих прозрачность.</span><span class="sxs-lookup"><span data-stu-id="fdf88-190">Standard graphics pipelines may have trouble correctly compositing together multiple textures that contain transparency.</span></span> <span data-ttu-id="fdf88-191">Для получения желаемого эффекта объекты, такие как провода, растительности и цветные границы, используют прозрачность.</span><span class="sxs-lookup"><span data-stu-id="fdf88-191">Objects such as wire fences, smoke, fire, vegetation, and colored glass use transparency to get the desired effect.</span></span> <span data-ttu-id="fdf88-192">Проблемы возникают, когда несколько текстур, содержащих прозрачность, расположены друг с другом (в качестве примера это повышена ограждение перед созданием стекла, содержащим растительности).</span><span class="sxs-lookup"><span data-stu-id="fdf88-192">Problems arise when multiple textures that contain transparency are in line with each other (smoke in front of a fence in front of a glass building containing vegetation, as an example).</span></span> <span data-ttu-id="fdf88-193">В упорядоченных представлениях средства растеризации (РОВС) для базового порядка можно использовать функции оборудования, чтобы правильно разрешить порядок прозрачности.</span><span class="sxs-lookup"><span data-stu-id="fdf88-193">Rasterizer ordered views (ROVs) enable the underlying Order Independent Transparency (OIT) algorithms to use features of the hardware to try to resolve the transparency order correctly.</span></span> <span data-ttu-id="fdf88-194">Прозрачность обрабатывается шейдером пикселей.</span><span class="sxs-lookup"><span data-stu-id="fdf88-194">Transparency is handled by the pixel shader.</span></span>

<span data-ttu-id="fdf88-195">В упорядоченных представлениях средства растеризации изображений (РОВС) разрешить коду шейдера пикселей пометить неупорядоченные привязки представлений доступа (UAV) с объявлением, изменяющим нормальные требования к порядку результатов графического конвейера для Уавс.</span><span class="sxs-lookup"><span data-stu-id="fdf88-195">Rasterizer Ordered Views (ROVs) allow pixel shader code to mark Unordered Access View (UAV) bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-196"><span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**куча реадбакк**</span><span class="sxs-lookup"><span data-stu-id="fdf88-196"><span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**readback heap**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-197">Куча пользовательского режима, которая передает данные из GPU обратно в ЦП.</span><span class="sxs-lookup"><span data-stu-id="fdf88-197">A user-mode heap that is focused on data transfer from the GPU back to the CPU.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-198"><span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**ресурсов**</span><span class="sxs-lookup"><span data-stu-id="fdf88-198"><span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**resource**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-199">Сущность, которая предоставляет данные конвейеру и определяет, что отображается во время сцены.</span><span class="sxs-lookup"><span data-stu-id="fdf88-199">An entity that provides data to the pipeline and defines what is rendered during your scene.</span></span> <span data-ttu-id="fdf88-200">Ресурсы могут загружаться из мультимедиа вашей игры или создаваться динамически во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="fdf88-200">Resources can be loaded from your game media or created dynamically at run time.</span></span> <span data-ttu-id="fdf88-201">Обычно ресурсы включают данные текстуры, данные вершин и данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="fdf88-201">Typically, resources include texture data, vertex data, and shader data.</span></span> <span data-ttu-id="fdf88-202">Большинство приложений Direct3D создают и уничтожают ресурсы в течение всего времени существования.</span><span class="sxs-lookup"><span data-stu-id="fdf88-202">Most Direct3D applications create and destroy resources extensively throughout their lifespan.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-203"><span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**барьер ресурсов**</span><span class="sxs-lookup"><span data-stu-id="fdf88-203"><span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**resource barrier**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-204">Барьер ресурсов уведомляет драйвер о том, что может потребоваться синхронизация нескольких обращений к одному ресурсу, например чтение и запись в ту же текстуру.</span><span class="sxs-lookup"><span data-stu-id="fdf88-204">A resource barrier notifies the driver that synchronization of multiple accesses to a single resource may be required, for example, reading and writing to the same texture.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-205"><span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**Привязка ресурсов**</span><span class="sxs-lookup"><span data-stu-id="fdf88-205"><span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**resource binding**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-206">Привязка ресурсов — это процесс связывания ресурсов (текстур, буферы вершин, буферы индексов и т. д.) с графическим конвейером, что позволяет шейдерам конвейера обрабатывать правильный ресурс.</span><span class="sxs-lookup"><span data-stu-id="fdf88-206">Resource binding is the process of linking resources (textures, vertex buffers, index buffers, and so on), to the graphics pipeline, enabling the shaders of the pipeline to process the correct resource.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-207"><span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**кучи ресурсов**</span><span class="sxs-lookup"><span data-stu-id="fdf88-207"><span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**resource heaps**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-208">Кучи ресурсов — это универсальный термин для куч, которые представляют собой буферы памяти, настроенные для хранения ресурсов по мере их передачи в графический процессор и из него.</span><span class="sxs-lookup"><span data-stu-id="fdf88-208">Resource heaps is a generic term for the heaps that are memory buffers set aside to hold resources as they are transferred to and from the GPU.</span></span> <span data-ttu-id="fdf88-209">Для передачи в GPU требуется куча передачи, от GPU до ЦП требуется куча Реадбакк, а постоянная куча для поддержки GPU в нескольких кадрах отрисовки называется кучей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fdf88-209">A transfer to the GPU requires an Upload Heap, from the GPU to the CPU requires a Readback Heap, and a persistent heap for the GPU to maintain over multiple rendering frames is called a Default Heap.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-210"><span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**Корневая подпись**</span><span class="sxs-lookup"><span data-stu-id="fdf88-210"><span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**root signature**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-211">Корневые подписи определяют все ресурсы, которые должны быть привязаны к графическим или вычисленным конвейерам.</span><span class="sxs-lookup"><span data-stu-id="fdf88-211">Root signatures define all the resources that are to be bound to the graphics, or compute, pipelines.</span></span> <span data-ttu-id="fdf88-212">Корневая подпись настраивается приложением и связывает списки команд с ресурсами, которые требуются шейдеру, как правило, одна графика и одна Графическая подпись для каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="fdf88-212">A root signature is configured by the app and links command lists to the resources that the shaders require Typically, there is one graphics and one compute root signature per app.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-213"><span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**образец**</span><span class="sxs-lookup"><span data-stu-id="fdf88-213"><span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**sampler**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-214">Образец — это код, считывающий данные из текстуры.</span><span class="sxs-lookup"><span data-stu-id="fdf88-214">A sampler is code that reads from a texture.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-215"><span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Представление ресурсов шейдера (SRV)**</span><span class="sxs-lookup"><span data-stu-id="fdf88-215"><span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Shader Resource View (SRV)**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-216">Способ просмотра данных в ресурсе шейдера, такой как текстура, зависит от формата.</span><span class="sxs-lookup"><span data-stu-id="fdf88-216">A format-specific way to look at the data in a shader resource, such as a texture.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-217"><span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**Статическая куча**</span><span class="sxs-lookup"><span data-stu-id="fdf88-217"><span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**static heap**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-218">Куча пользовательского режима, которая ориентирована на несколько ресурсов GPU-только для чтения, которые обычно используются одновременно и не меняются часто.</span><span class="sxs-lookup"><span data-stu-id="fdf88-218">A user-mode heap that is focused on multiple GPU-read-only resources that are typically used at the same time and are not changed frequently.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-219"><span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**цепочка подкачки**</span><span class="sxs-lookup"><span data-stu-id="fdf88-219"><span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-220">Цепи переключения управляют поворотом заднего буфера, формируя основание графической анимации.</span><span class="sxs-lookup"><span data-stu-id="fdf88-220">Swap chains control the back buffer rotation, forming the basis of graphics animation.</span></span> <span data-ttu-id="fdf88-221">Цепочки подкачки обрабатываются с помощью функции DXGI API нижнего уровня (см. [Общие сведения о DXGI](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).</span><span class="sxs-lookup"><span data-stu-id="fdf88-221">Swap chains are handled by the low level API set DXGI (see [DXGI Overview](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-222"><span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**свиззле**</span><span class="sxs-lookup"><span data-stu-id="fdf88-222"><span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-223">Метод обнаружения многомерных данных в памяти, в котором данные о расположении близлежащих элементов обычно имеют близлежащие адреса.</span><span class="sxs-lookup"><span data-stu-id="fdf88-223">A technique of locating multidimensional data in memory such that data of nearby dimensionality tends to have nearby addresses.</span></span> <span data-ttu-id="fdf88-224">В частности, все данные одной строки не располагаются непрерывно перед данными для следующей строки.</span><span class="sxs-lookup"><span data-stu-id="fdf88-224">In particular, all the data for one row is not located contiguously before the data for the next row.</span></span> <span data-ttu-id="fdf88-225">"Параметризованный Свиззле" описывает стандартизированный способ описания свиззле шаблонов.</span><span class="sxs-lookup"><span data-stu-id="fdf88-225">A "Parameterized Swizzle" describes a standardized way to describe swizzle patterns.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-226"><span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**поддержки**</span><span class="sxs-lookup"><span data-stu-id="fdf88-226"><span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**texture**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-227">Тип ресурса D3D, который является многомерным и имеет макет памяти, оптимизированный для многомерного доступа из GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-227">A type of D3D resource that is multi-dimensional and has a memory layout that is optimized for multi-dimensional access from the GPU.</span></span> <span data-ttu-id="fdf88-228">Текстуры часто содержат необработанный образ, необходимый для отображения на поверхности, перед освещением и наложением, но может содержать другие формы данных, такие как цветовые градиенты и эталонные цвета.</span><span class="sxs-lookup"><span data-stu-id="fdf88-228">Textures often contain the raw image required to render onto a surface, before lighting and blending takes place, but can contain other forms of data such as color gradients and reference colors.</span></span> <span data-ttu-id="fdf88-229">Direct3D 12 поддерживает одну, две и трехмерные текстуры.</span><span class="sxs-lookup"><span data-stu-id="fdf88-229">Direct3D 12 supports one, two, and three dimensional textures.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-230"><span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**Tile**</span><span class="sxs-lookup"><span data-stu-id="fdf88-230"><span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**tile**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-231">Страница видеопамяти, аналогичная системной памяти.</span><span class="sxs-lookup"><span data-stu-id="fdf88-231">A page of video memory, similar to a CPU/System page of memory.</span></span> <span data-ttu-id="fdf88-232">Нотация плитки позволяет отличать подсистему виртуальной памяти GPU от подсистемы виртуальной памяти ЦП.</span><span class="sxs-lookup"><span data-stu-id="fdf88-232">The tile notation helps to distinguish the GPU virtual memory subsystem from the CPU virtual memory subsystem.</span></span> <span data-ttu-id="fdf88-233">Графические процессоры предоставляют аналогичные возможности виртуальной памяти в качестве системной виртуальной памяти.</span><span class="sxs-lookup"><span data-stu-id="fdf88-233">GPUs provide similar virtual memory capabilities as system virtual memory.</span></span> <span data-ttu-id="fdf88-234">Некоторые GPU имеют общие возможности виртуальной памяти, которые позволяют совместно использовать некоторые страницы виртуальной памяти с ЦП и GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-234">Some GPUs have shared virtual memory capabilities, which allow for the sharing of some pages of the virtual memory subsystem with both the CPU and GPU.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-235"><span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**Мозаичные ресурсы**</span><span class="sxs-lookup"><span data-stu-id="fdf88-235"><span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**tiled resources**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-236">Ресурсы мозаичного заполнения необходимы, поэтому меньше памяти GPU тратится на хранение областей поверхностей, к которым приложение не будет обращаться, и оборудование может понять, как выполнять фильтрацию по смежным плиткам.</span><span class="sxs-lookup"><span data-stu-id="fdf88-236">Tiled resources are needed so less GPU memory is wasted storing regions of surfaces that the application knows will not be accessed, and the hardware can understand how to filter across adjacent tiles.</span></span> <span data-ttu-id="fdf88-237">Мозаичные ресурсы — это большие логические ресурсы, но для них требуются небольшие объемы физической памяти.</span><span class="sxs-lookup"><span data-stu-id="fdf88-237">Tiled resources are large logical resources, but requiring small amounts of physical memory.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-238"><span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Представление неупорядоченного доступа (UAV)**</span><span class="sxs-lookup"><span data-stu-id="fdf88-238"><span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Unordered Access View (UAV)**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-239">Неупорядоченное представление доступа к ресурсу (которое включает буферы, текстуры и массивы текстур без множественной выборки) позволяет временно неупорядоченный доступ на чтение и запись из нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="fdf88-239">An unordered access view into a resource (which includes buffers, textures, and texture arrays - without multi-sampling), allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="fdf88-240">Это означает, что этот тип ресурса может быть считан и записан одновременно несколькими потоками без создания конфликтов памяти.</span><span class="sxs-lookup"><span data-stu-id="fdf88-240">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-241"><span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**отправить кучу**</span><span class="sxs-lookup"><span data-stu-id="fdf88-241"><span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**upload heap**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-242">Куча пользовательского режима, которая посвящена переносу данных с ЦП на GPU.</span><span class="sxs-lookup"><span data-stu-id="fdf88-242">A user-mode heap that is focused on data transfer from the CPU to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-243"><span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**куча пользовательского режима**</span><span class="sxs-lookup"><span data-stu-id="fdf88-243"><span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**user-mode heap**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-244">Коллекция больших непрерывных выделений памяти, которые перезапускаются без поддержки какого-либо компонента ядра: методы выделения и уничтожения не вызывают методы выделения и уничтожения ядра в стабильном состоянии.</span><span class="sxs-lookup"><span data-stu-id="fdf88-244">A collection of large, contiguous memory allocations that are recycled without any kernel component's awareness: the allocation and destruction methods do not call kernel allocation and destruction methods during steady state.</span></span> <span data-ttu-id="fdf88-245">Данные о кучах передачи, Реадбакк и по умолчанию являются вариантами куч пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="fdf88-245">Upload, Readback, and Default heaps are variants of user mode heaps.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-246"><span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**ресурсы для мозаичного заполнения тома**</span><span class="sxs-lookup"><span data-stu-id="fdf88-246"><span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**volume tiled resources**</span></span>
</dt> <dd>

<span data-ttu-id="fdf88-247">Объемные [мозаичные ресурсы](/windows).</span><span class="sxs-lookup"><span data-stu-id="fdf88-247">Three-dimensional [tiled resources](/windows).</span></span>

</dd> </dl>

 

 