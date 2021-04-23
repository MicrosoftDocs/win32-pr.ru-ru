---
title: Конвейеры и шейдеры с Direct3D 12
description: Программируемый конвейер Direct3D 12 значительно увеличивает производительность отрисовки по сравнению с интерфейсами программирования графики предыдущих поколений.
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c392b3915443da2f287a5511f3959cbb7179f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "104548959"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a><span data-ttu-id="fa772-103">Конвейеры и шейдеры с Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fa772-103">Pipelines and Shaders with Direct3D 12</span></span>

<span data-ttu-id="fa772-104">Программируемый конвейер Direct3D 12 значительно увеличивает производительность отрисовки по сравнению с интерфейсами программирования графики предыдущих поколений.</span><span class="sxs-lookup"><span data-stu-id="fa772-104">The Direct3D 12 programmable pipeline significantly increases rendering performance compared to previous generation graphics programming interfaces.</span></span>

-   [<span data-ttu-id="fa772-105">Графический конвейер Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fa772-105">Direct3D 12 graphics pipeline</span></span>](#direct3d-12-graphics-pipeline)
-   [<span data-ttu-id="fa772-106">Объекты состояния конвейера</span><span class="sxs-lookup"><span data-stu-id="fa772-106">Pipeline state objects</span></span>](#pipeline-state-objects)
-   [<span data-ttu-id="fa772-107">Конвейер вычислений Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fa772-107">Direct3D 12 compute pipeline</span></span>](#direct3d-12-compute-pipeline)
-   [<span data-ttu-id="fa772-108">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="fa772-108">Related topics</span></span>](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a><span data-ttu-id="fa772-109">Графический конвейер Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fa772-109">Direct3D 12 graphics pipeline</span></span>

<span data-ttu-id="fa772-110">На следующей схеме показан конвейер и состояние графического процесса Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="fa772-110">The following diagram illustrates the Direct3D 12 graphics pipeline and state.</span></span>

![Схема, иллюстрирующая конвейер и состояние Direct3D 12](images/pipeline.png)

<span data-ttu-id="fa772-112">Графический конвейер — это последовательный поток входных и выходных данных, когда GPU визуализирует кадры.</span><span class="sxs-lookup"><span data-stu-id="fa772-112">A graphics pipeline is the sequential flow of data inputs and outputs as the GPU renders frames.</span></span> <span data-ttu-id="fa772-113">Учитывая состояние конвейера и входные данные, GPU выполняет ряд операций для создания результирующих изображений.</span><span class="sxs-lookup"><span data-stu-id="fa772-113">Given the pipeline state and inputs, the GPU performs a series of operations to create the resulting images.</span></span> <span data-ttu-id="fa772-114">Графический конвейер содержит шейдеры, которые выполняют программируемые эффекты отрисовки и вычисления, а операции с фиксированной функцией.</span><span class="sxs-lookup"><span data-stu-id="fa772-114">A graphics pipeline contains shaders, which perform programmable rendering effects and calculations, and fixed function operations.</span></span>

<span data-ttu-id="fa772-115">При обращении к схеме состояния конвейера Обратите внимание на следующее:</span><span class="sxs-lookup"><span data-stu-id="fa772-115">Note the following when referring to the pipeline state diagram:</span></span>

-   <span data-ttu-id="fa772-116">Таблицы дескрипторов и кучи могут быть произвольно упорядочены: СРВС, КБВС и Уавс могут ссылаться и выделяться в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="fa772-116">The descriptor tables and heaps can be arbitrarily arranged: SRVs, CBVs and UAVs can be referenced and allocated in any order.</span></span>
-   <span data-ttu-id="fa772-117">Некоторые операции конвейера можно настроить.</span><span class="sxs-lookup"><span data-stu-id="fa772-117">Some operations of the pipeline are configurable.</span></span> <span data-ttu-id="fa772-118">Например, выходное слияние, как правило, работает с целью чтения, изменения и записи с помощью целевого объекта прорисовки и представлений трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="fa772-118">For example, the output merger typically operates on a read-modify-write basis with the render target and depth stencil views.</span></span> <span data-ttu-id="fa772-119">Однако конвейер можно настроить таким образом, чтобы любое из этих представлений было доступно только для чтения или только для записи.</span><span class="sxs-lookup"><span data-stu-id="fa772-119">However the pipeline can be configured so that either of these views are read-only or write-only.</span></span>
-   <span data-ttu-id="fa772-120">Статические пробы не являются частью корневых аргументов, так как они являются статическими.</span><span class="sxs-lookup"><span data-stu-id="fa772-120">Static samplers are not part of the root arguments since they are static.</span></span>

## <a name="pipeline-state-objects"></a><span data-ttu-id="fa772-121">Объекты состояния конвейера</span><span class="sxs-lookup"><span data-stu-id="fa772-121">Pipeline state objects</span></span>

<span data-ttu-id="fa772-122">В Direct3D 12 появился объект состояния конвейера (PSO).</span><span class="sxs-lookup"><span data-stu-id="fa772-122">Direct3D 12 introduces the pipeline state object (PSO).</span></span> <span data-ttu-id="fa772-123">Вместо того чтобы хранить и представлять состояние конвейера в большом количестве объектов высокого уровня, состояния компонентов конвейера, таких как входной ассемблер, средство прорисовки, шейдер пикселей и слияние выходных данных, хранятся в PSO.</span><span class="sxs-lookup"><span data-stu-id="fa772-123">Rather than storing and representing pipeline state across a large number of high-level objects, the states of pipeline components like the input assembler, rasterizer, pixel shader, and output merger are stored in a PSO.</span></span> <span data-ttu-id="fa772-124">PSO — это унифицированный объект состояния конвейера, который не является изменяемым после создания.</span><span class="sxs-lookup"><span data-stu-id="fa772-124">A PSO is a unified pipeline state object that is immutable after creation.</span></span> <span data-ttu-id="fa772-125">Выбранные в настоящее время PSO можно быстро и динамически изменить, а оборудование и драйверы могут напрямую преобразовывать PSO в собственные аппаратные инструкции и состояния, подготавливая графический процессор для обработки графики.</span><span class="sxs-lookup"><span data-stu-id="fa772-125">The currently selected PSO can be changed quickly and dynamically, and the hardware and drivers can directly convert a PSO into native hardware instructions and state, readying the GPU for graphics processing.</span></span> <span data-ttu-id="fa772-126">Чтобы применить PSO, оборудование копирует минимальный объем предварительно вычисленного состояния непосредственно в реестры оборудования.</span><span class="sxs-lookup"><span data-stu-id="fa772-126">To apply a PSO, the hardware copies a minimal amount of pre-computed state directly to the hardware registers.</span></span> <span data-ttu-id="fa772-127">Это устраняет издержки, вызванные тем, что драйвер графики постоянно пересматривает состояние оборудования, учитывая все применимые параметры отрисовки и конвейера.</span><span class="sxs-lookup"><span data-stu-id="fa772-127">This removes the overhead caused by the graphics driver continually recomputing hardware state based on all currently applicable rendering and pipeline settings.</span></span> <span data-ttu-id="fa772-128">В результате значительно уменьшается нагрузка на вызовы рисования, повышенная производительность и число вызовов рисования на кадр.</span><span class="sxs-lookup"><span data-stu-id="fa772-128">The result is significantly reduced draw call overhead, increased performance, and more draw calls per frame.</span></span>

<span data-ttu-id="fa772-129">В настоящее время примененные PSO определяют и соединяют все используемые шейдеры в конвейере отрисовки.</span><span class="sxs-lookup"><span data-stu-id="fa772-129">The currently applied PSO defines and connects all of the shaders being used in the rendering pipeline.</span></span> <span data-ttu-id="fa772-130">[Язык шейдеров высокого уровня (Майкрософт) (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) предварительно скомпилирован в объекты шейдера, которые затем используются во время выполнения в качестве входных для объектов состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="fa772-130">[Microsoft High Level Shader Language (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) is pre-compiled into shader objects, which are then used at run time as input for pipeline state objects.</span></span> <span data-ttu-id="fa772-131">Дополнительные сведения о функциях PSO в графическом конвейере см. в разделе [Управление состоянием графического конвейера в Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="fa772-131">For more information about how the PSO functions within the graphics pipeline, see [Managing graphics pipeline state in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span></span>

## <a name="direct3d-12-compute-pipeline"></a><span data-ttu-id="fa772-132">Конвейер вычислений Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fa772-132">Direct3D 12 compute pipeline</span></span>

<span data-ttu-id="fa772-133">На следующей схеме показан конвейер вычислений Direct3D 12 и его состояние.</span><span class="sxs-lookup"><span data-stu-id="fa772-133">The following diagram illustrates the Direct3D 12 compute pipeline and state.</span></span>

![Схема, на которой показан конвейер вычислений Direct3D 12.](images/compute-pipeline.png)

<span data-ttu-id="fa772-135">В этом конвейере нет единиц фиксированных функций, однако кучи дескрипторов, кучи образцов и статические пробы по-прежнему доступны в средах выполнения вычислений.</span><span class="sxs-lookup"><span data-stu-id="fa772-135">There are no fixed function units in this pipeline, however descriptor heaps, sampler heaps and static samplers are still available in compute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa772-136">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="fa772-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa772-137">Отправка рабочих заданий в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fa772-137">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)
</dt> </dl>

 

 