---
title: Проектирование философии очередей команд и списков команд
description: Цели, позволяющие повторно использовать работу по отрисовке и многопоточное масштабирование, требуют фундаментальных изменений в том, как приложения Direct3D отправляют данные визуализации в GPU.
ms.assetid: C85C8C41-2306-4568-8FAE-F57EDA624298
keywords:
- Список команд
- bundle
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812275a630464dbe9137d587a672803f4d0c72f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104080"
---
# <a name="design-philosophy-of-command-queues-and-command-lists"></a><span data-ttu-id="1f6b7-105">Проектирование философии очередей команд и списков команд</span><span class="sxs-lookup"><span data-stu-id="1f6b7-105">Design Philosophy of Command Queues and Command Lists</span></span>

<span data-ttu-id="1f6b7-106">Цели, позволяющие повторно использовать работу по отрисовке и многопоточное масштабирование, требуют фундаментальных изменений в том, как приложения Direct3D отправляют данные визуализации в GPU.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-106">The goals of enabling reuse of rendering work and of multi-threaded scaling, required fundamental changes to how Direct3D apps submit rendering work to the GPU.</span></span> <span data-ttu-id="1f6b7-107">В Direct3D 12 процесс отправки работы по отрисовке отличается от более ранних версий тремя важными способами:</span><span class="sxs-lookup"><span data-stu-id="1f6b7-107">In Direct3D 12, the process of submitting rendering work differs from earlier versions in three important ways:</span></span>

<dl> 1. <span data-ttu-id="1f6b7-108">Исключение непосредственных контекстов.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-108">Elimination of the immediate context.</span></span> <span data-ttu-id="1f6b7-109">Это позволяет создавать многопоточность.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-109">This enables multi-threading.</span></span>  
2. <span data-ttu-id="1f6b7-110">Теперь приложения владеют тем, как вызовы отрисовки группируются в рабочие элементы графического процессора.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-110">Apps now own how rendering calls are grouped into graphics processing unit (GPU) work items.</span></span> <span data-ttu-id="1f6b7-111">Это позволяет повторно использовать.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-111">This enables re-use.</span></span>  
3. <span data-ttu-id="1f6b7-112">Теперь приложения явно управляют отправкой работы в GPU.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-112">Apps now explicitly control when work is submitted to the GPU .</span></span> <span data-ttu-id="1f6b7-113">Это позволяет элементам 1 и 2.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-113">This enables items 1 and 2.</span></span>  
</dl>

-   [<span data-ttu-id="1f6b7-114">Удаление непосредственных контекстов</span><span class="sxs-lookup"><span data-stu-id="1f6b7-114">Removal of the immediate context</span></span>](#removal-of-the-immediate-context)
-   [<span data-ttu-id="1f6b7-115">Группирование рабочих элементов GPU</span><span class="sxs-lookup"><span data-stu-id="1f6b7-115">Grouping of GPU work items</span></span>](#grouping-of-gpu-work-items)
-   [<span data-ttu-id="1f6b7-116">Отправка работы GPU</span><span class="sxs-lookup"><span data-stu-id="1f6b7-116">GPU work submission</span></span>](#gpu-work-submission)
-   [<span data-ttu-id="1f6b7-117">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1f6b7-117">Related topics</span></span>](#related-topics)

## <a name="removal-of-the-immediate-context"></a><span data-ttu-id="1f6b7-118">Удаление непосредственных контекстов</span><span class="sxs-lookup"><span data-stu-id="1f6b7-118">Removal of the immediate context</span></span>

<span data-ttu-id="1f6b7-119">Самым большим изменением с Microsoft Direct3D 11 до Microsoft Direct3D 12 является отсутствие единственного немедленного контекста, связанного с устройством.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-119">The largest change from Microsoft Direct3D 11 to Microsoft Direct3D 12 is that there is no longer a single, immediate context associated with a device.</span></span> <span data-ttu-id="1f6b7-120">Вместо этого для подготовки к просмотру приложения создают списки команд, в которых можно вызывать традиционные API-интерфейсы отрисовки.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-120">Instead, to render, apps create command lists in which traditional rendering APIs can be called.</span></span> <span data-ttu-id="1f6b7-121">Список команд выглядит аналогично методу Render приложения Direct3D 11, который использовал непосредственный контекст в том, что он содержит вызовы, которые рисуют примитивы или меняют состояние отрисовки.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-121">A command list looks similar to the render method of a Direct3D 11 app that used the immediate context in that it contains calls that draw primitives or change the rendering state.</span></span> <span data-ttu-id="1f6b7-122">Как и в случае с непосредственными контекстами, каждый список команд не является потокобезопасным. Однако несколько списков команд можно записать одновременно, что позволяет использовать современные, многоядерные процессоры.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-122">Like immediate contexts, each command list is not free-threaded; however, multiple command lists can be recorded concurrently, which takes advantage of modern, multi-core processors.</span></span>

<span data-ttu-id="1f6b7-123">Списки команд обычно выполняются один раз.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-123">Command lists are typically executed once.</span></span> <span data-ttu-id="1f6b7-124">Однако список команд может быть выполнен несколько раз, если приложение гарантирует завершение предыдущих выполнений перед отправкой новых выполнений.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-124">However, a command list can be executed multiple times if the application ensures that the previous executions are complete before submitting new executions.</span></span> <span data-ttu-id="1f6b7-125">Дополнительные сведения о синхронизации списка команд см. в разделе [исполнение и синхронизация списков команд](executing-and-synchronizing-command-lists.md).</span><span class="sxs-lookup"><span data-stu-id="1f6b7-125">For more information about command list synchronization, see [Executing and synchronizing command lists](executing-and-synchronizing-command-lists.md).</span></span>

## <a name="grouping-of-gpu-work-items"></a><span data-ttu-id="1f6b7-126">Группирование рабочих элементов GPU</span><span class="sxs-lookup"><span data-stu-id="1f6b7-126">Grouping of GPU work items</span></span>

<span data-ttu-id="1f6b7-127">В дополнение к спискам команд Direct3D 12 использует преимущества функций, имеющихся на всех устройствах, за счет добавления второго уровня списков команд, называемых *пакетами*.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-127">In addition to command lists, Direct3D 12 takes advantage of functionality present in all hardware today by adding a second level of command lists, which are called *bundles*.</span></span> <span data-ttu-id="1f6b7-128">Чтобы отличить эти два типа, списки команд первого уровня могут называться *прямыми списками команд*.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-128">To help to distinguish these two types, the first-level command lists can be referred to as *direct command lists*.</span></span> <span data-ttu-id="1f6b7-129">Назначение пакетов состоит в том, чтобы разрешить приложениям группировать небольшое количество команд API для последующего повторного выполнения в списках прямых команд.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-129">The purpose of bundles is to allow apps to group a small number of API commands together for later, repeated execution from within direct command lists.</span></span> <span data-ttu-id="1f6b7-130">Во время создания пакета драйвер выполняет как можно более предварительную обработку, чтобы повысить эффективность выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-130">At the time of creating a bundle, the driver will perform as much pre-processing as possible to make later execution efficient.</span></span> <span data-ttu-id="1f6b7-131">Пакеты могут быть выполнены из нескольких списков команд и несколько раз в одном списке команд.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-131">Bundles can then be executed from within multiple command lists and multiple times within the same command list.</span></span>

<span data-ttu-id="1f6b7-132">Повторное использование пакетов — это большой фактор повышения эффективности работы с одними потоками ЦП.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-132">The re-use of bundles is a large driver of improved efficiency with single CPU threads.</span></span> <span data-ttu-id="1f6b7-133">Поскольку пакеты предварительно обрабатываются и могут быть отправлены несколько раз, существуют определенные ограничения на операции, которые могут быть выполнены в пакете.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-133">Because bundles are pre-processed and can be submitted multiple times, there are certain restrictions on what operations can be performed within a bundle.</span></span> <span data-ttu-id="1f6b7-134">Дополнительные сведения см. в разделе [Создание и запись списков команд и пакетов](recording-command-lists-and-bundles.md).</span><span class="sxs-lookup"><span data-stu-id="1f6b7-134">For more information, see [Creating and recording command lists and bundles](recording-command-lists-and-bundles.md).</span></span>

## <a name="gpu-work-submission"></a><span data-ttu-id="1f6b7-135">Отправка работы GPU</span><span class="sxs-lookup"><span data-stu-id="1f6b7-135">GPU work submission</span></span>

<span data-ttu-id="1f6b7-136">Для выполнения работы с GPU приложение должно явно отправить список команд в очередь команд, связанную с устройством Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-136">To execute work on the GPU, an app must explicitly submit a command list to a command queue associated with the Direct3D device.</span></span> <span data-ttu-id="1f6b7-137">Прямой список команд может быть отправлен для выполнения несколько раз, но приложение несет ответственность за проверку того, что список прямых команд завершил выполнение на GPU, прежде чем отправлять его снова.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-137">A direct command list can be submitted for execution multiple times, but the app is responsible for ensuring that the direct command list has finished executing on the GPU before submitting it again.</span></span> <span data-ttu-id="1f6b7-138">Пакеты не имеют ограничений на параллельное использование и могут выполняться несколько раз в нескольких списках команд, но пакеты не могут быть непосредственно переданы в очередь команд для выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-138">Bundles have no concurrent-use restrictions and can be executed multiple times in multiple command lists, but bundles cannot be directly submitted to a command queue for execution.</span></span>

<span data-ttu-id="1f6b7-139">Любой поток может отправить список команд в любую очередь команд в любое время, и среда выполнения будет автоматически выполнять сериализацию списка команд в очередь команд при сохранении порядка отправки.</span><span class="sxs-lookup"><span data-stu-id="1f6b7-139">Any thread may submit a command list to any command queue at any time, and the runtime will automatically serialize submission of the command list in the command queue while preserving the submission order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f6b7-140">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1f6b7-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f6b7-141">Отправка рабочих заданий в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1f6b7-141">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)
</dt> </dl>

 

 




