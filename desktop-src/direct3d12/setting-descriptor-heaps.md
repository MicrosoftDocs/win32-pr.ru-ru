---
title: Задание и заполнение куч дескрипторов
description: Типы кучи дескрипторов, которые могут быть заданы в списке команд, — это те, которые содержат дескрипторы, для которых можно использовать таблицы (не более одного одновременно).
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e3a1b6c4863827e1d8e1bdfb33a0a64420211d
ms.sourcegitcommit: 584b35959515bc5e4a104e8cf5270513f146f590
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/03/2019
ms.locfileid: "104548957"
---
# <a name="setting-and-populating-descriptor-heaps"></a><span data-ttu-id="7abbc-103">Задание и заполнение куч дескрипторов</span><span class="sxs-lookup"><span data-stu-id="7abbc-103">Setting and Populating Descriptor Heaps</span></span>

<span data-ttu-id="7abbc-104">Типы кучи дескрипторов, которые могут быть заданы в списке команд, — это те, которые содержат дескрипторы, для которых можно использовать таблицы (не более одного одновременно).</span><span class="sxs-lookup"><span data-stu-id="7abbc-104">The descriptor heap types that can be set on a command list are those that contain descriptors for which descriptor tables can be used (at most one of each at a time).</span></span>

-   [<span data-ttu-id="7abbc-105">Задание куч дескриптора</span><span class="sxs-lookup"><span data-stu-id="7abbc-105">Setting descriptor heaps</span></span>](#setting-and-populating-descriptor-heaps)
-   [<span data-ttu-id="7abbc-106">Заполнение куч дескрипторов</span><span class="sxs-lookup"><span data-stu-id="7abbc-106">Populating descriptor heaps</span></span>](#populating-descriptor-heaps)
-   [<span data-ttu-id="7abbc-107">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="7abbc-107">Related topics</span></span>](#related-topics)

## <a name="setting-descriptor-heaps"></a><span data-ttu-id="7abbc-108">Задание куч дескриптора</span><span class="sxs-lookup"><span data-stu-id="7abbc-108">Setting descriptor heaps</span></span>

<span data-ttu-id="7abbc-109">В списке команд можно задать следующие типы кучи дескрипторов:</span><span class="sxs-lookup"><span data-stu-id="7abbc-109">The types of descriptor heap that can be set on a command list are:</span></span>

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

<span data-ttu-id="7abbc-110">Кучи, заданные в списке команд, также должны быть созданы как шейдеры видимыми.</span><span class="sxs-lookup"><span data-stu-id="7abbc-110">The heaps being set on the command list must also have been created as shader visible.</span></span> <span data-ttu-id="7abbc-111">Существует три типа списка команд: DIRECT, пакет и ВЫЧИСЛЕНие.</span><span class="sxs-lookup"><span data-stu-id="7abbc-111">There are three types of command list: DIRECT, BUNDLE, and COMPUTE.</span></span>

<span data-ttu-id="7abbc-112">После того как куча дескрипторов задана в списке команд, последующие вызовы, определяющие таблицы дескрипторов, ссылаются на текущую кучу дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="7abbc-112">After a descriptor heap is set on a command list, subsequent calls that define descriptor tables refer to the current descriptor heap.</span></span> <span data-ttu-id="7abbc-113">Состояние таблицы дескриптора не определено в начале списка команд, и после изменения куч дескриптора в списке команд.</span><span class="sxs-lookup"><span data-stu-id="7abbc-113">Descriptor table state is undefined at the beginning of a command list and after descriptor heaps are changed on a command list.</span></span> <span data-ttu-id="7abbc-114">Избыточная установка одной и той же кучи дескрипторов не приводит к тому, что параметры таблицы дескрипторов не будут определены.</span><span class="sxs-lookup"><span data-stu-id="7abbc-114">Redundantly setting the same descriptor heap does not cause descriptor table settings to be undefined.</span></span>

<span data-ttu-id="7abbc-115">В пакете, напротив, кучу дескрипторов можно задать только один раз (избыточные вызовы, устанавливающие одну и ту же кучу дважды, не создают ошибку); в противном случае поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="7abbc-115">In a bundle, by contrast, the descriptor heaps can only be set once (redundant calls setting the same heap twice do not produce an error); otherwise, the behavior is undefined.</span></span> <span data-ttu-id="7abbc-116">Заданные кучи дескрипторов должны соответствовать состоянию, когда любой список команд вызывает пакет; в противном случае поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="7abbc-116">The descriptor heaps that are set must match the state when any command list calls the bundle; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="7abbc-117">Это позволяет пакетам наследовать и изменять параметры таблицы дескрипторов в списке команд.</span><span class="sxs-lookup"><span data-stu-id="7abbc-117">This allows bundles to inherit and edit the command list’s descriptor table settings.</span></span> <span data-ttu-id="7abbc-118">В пакетах, которые не изменяют таблицы дескрипторов (наследуют их), не нужно задавать кучу дескрипторов и просто наследовать из списка вызывающей команды.</span><span class="sxs-lookup"><span data-stu-id="7abbc-118">Bundles that don’t change descriptor tables (only inherit them) don’t need to set a descriptor heap at all and will just inherit from the calling command list.</span></span>

<span data-ttu-id="7abbc-119">Если заданы кучи дескрипторов (с помощью [**ID3D12GraphicsCommandList:: сетдескрипторхеапс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), все используемые кучи задаются в одном вызове (и все ранее установленные кучи отменяются вызовом).</span><span class="sxs-lookup"><span data-stu-id="7abbc-119">When descriptor heaps are set (using [**ID3D12GraphicsCommandList::SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), all the heaps being used are set in a single call (and all previously set heaps are unset by the call).</span></span> <span data-ttu-id="7abbc-120">В вызове можно задать не более одной кучи для каждого типа, указанного выше.</span><span class="sxs-lookup"><span data-stu-id="7abbc-120">At most one heap of each type listed above can be set in the call.</span></span>

## <a name="populating-descriptor-heaps"></a><span data-ttu-id="7abbc-121">Заполнение куч дескрипторов</span><span class="sxs-lookup"><span data-stu-id="7abbc-121">Populating descriptor heaps</span></span>

<span data-ttu-id="7abbc-122">После того как приложение создало кучу дескрипторов, оно может использовать методы на устройстве для создания дескрипторов непосредственно в куче или копирования дескрипторов из одного места в другое.</span><span class="sxs-lookup"><span data-stu-id="7abbc-122">After an application has created a descriptor heap, it can then use methods on the device to either generate descriptors directly into the heap or copy descriptors from one place to another.</span></span>

<span data-ttu-id="7abbc-123">Начальное содержимое памяти кучи дескрипторов не определено, поэтому необходимо, чтобы графический процессор или драйвер, ссылающийся на неинициализированную память для подготовки к просмотру, мог вызвать неопределенные результаты, такие как сброс устройства.</span><span class="sxs-lookup"><span data-stu-id="7abbc-123">The initial contents of descriptor heap memory is undefined, so asking the GPU or driver to reference uninitialized memory for rendering can cause undefined results such as a device reset.</span></span>

<span data-ttu-id="7abbc-124">Если приложение настраивает кучу дескрипторов как видимую для ЦП, то ЦП может вызывать методы для создания дескрипторов в куче и копирования из места (в том числе между кучами) в немедленный, свободный потоковый способ.</span><span class="sxs-lookup"><span data-stu-id="7abbc-124">If the application configures a descriptor heap to be CPU visible, then the CPU can call methods to create descriptors into the heap and copy from place to place (including across heaps) in an immediate, free threaded manner.</span></span> <span data-ttu-id="7abbc-125">Если куча настроена как SHADER_VISIBLE, чтение ЦП не разрешено.</span><span class="sxs-lookup"><span data-stu-id="7abbc-125">If the heap has been configured as SHADER_VISIBLE, reading by the CPU is not permitted.</span></span>



## <a name="related-topics"></a><span data-ttu-id="7abbc-126">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="7abbc-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7abbc-127">Кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="7abbc-127">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




