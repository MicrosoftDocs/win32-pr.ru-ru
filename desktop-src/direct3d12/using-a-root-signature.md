---
title: Использование корневой подписи
description: Корневая подпись является определением произвольно упорядоченной коллекции таблиц дескрипторов (включая их макет), корневых констант и корневых дескрипторов.
ms.assetid: 0131CDE4-02DB-440A-92B8-B0933C6414B0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3babe26dc06d4f85ce3d6fb771e18c78b54a3701
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104004"
---
# <a name="using-a-root-signature"></a><span data-ttu-id="20f11-103">Использование корневой подписи</span><span class="sxs-lookup"><span data-stu-id="20f11-103">Using a Root Signature</span></span>

<span data-ttu-id="20f11-104">Корневая подпись является определением произвольно упорядоченной коллекции таблиц дескрипторов (включая их макет), корневых констант и корневых дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="20f11-104">The root signature is the definition of an arbitrarily arranged collection of descriptor tables (including their layout), root constants and root descriptors.</span></span> <span data-ttu-id="20f11-105">Каждая запись имеет стоимость в сторону максимального ограничения, поэтому приложение может выплатить баланс между количеством записей каждого типа, которые будет содержать корневая подпись.</span><span class="sxs-lookup"><span data-stu-id="20f11-105">Each entry has a cost towards a maximum limit, so the application can trade off the balance between how many of each type of entry the root signature will contain.</span></span>

-   [<span data-ttu-id="20f11-106">Семантика списка команд</span><span class="sxs-lookup"><span data-stu-id="20f11-106">Command List Semantic</span></span>](#command-list-semantic)
-   [<span data-ttu-id="20f11-107">Семантика пакета</span><span class="sxs-lookup"><span data-stu-id="20f11-107">Bundle Semantics</span></span>](#bundle-semantics)
-   [<span data-ttu-id="20f11-108">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="20f11-108">Related topics</span></span>](#related-topics)

<span data-ttu-id="20f11-109">Корневая подпись — это объект, который можно создать с помощью ручного указания в API.</span><span class="sxs-lookup"><span data-stu-id="20f11-109">The root signature is an object that can be created by manual specification at the API.</span></span> <span data-ttu-id="20f11-110">Все шейдеры в PSO должны быть совместимы с корневым макетом, заданным в PSO, или, в противном случае отдельные шейдеры должны включать внедренные корневые макеты, которые соответствуют друг другу. в противном случае создание PSO завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="20f11-110">All shaders in a PSO must be compatible with the root layout specified with the PSO, or else the individual shaders must include embedded root layouts that match each other; otherwise, PSO creation will fail.</span></span> <span data-ttu-id="20f11-111">Одним из свойств корневой сигнатуры является то, что шейдеры не должны иметь сведений о них при создании, хотя при необходимости также могут быть созданы корневые подписи непосредственно в шейдере.</span><span class="sxs-lookup"><span data-stu-id="20f11-111">One property of the root signature is that shaders don't have to know about it when authored, although root signatures can also be authored directly in shaders if desired.</span></span> <span data-ttu-id="20f11-112">Для существующих ресурсов шейдера не требуется, чтобы изменения были совместимы с корневыми сигнатурами.</span><span class="sxs-lookup"><span data-stu-id="20f11-112">Existing shader assets do not require any changes to be compatible with root signatures.</span></span> <span data-ttu-id="20f11-113">Модель шейдера 5,1 введена для предоставления некоторой гибкости (динамическое индексирование дескрипторов из шейдеров) и может быть постепенно реализована начиная с существующих ресурсов шейдера по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="20f11-113">Shader Model 5.1 is introduced to provide some extra flexibility (dynamic indexing of descriptors from within shaders), and can be incrementally adopted starting from existing shader assets as desired.</span></span>

## <a name="command-list-semantic"></a><span data-ttu-id="20f11-114">Семантика списка команд</span><span class="sxs-lookup"><span data-stu-id="20f11-114">Command List Semantic</span></span>

<span data-ttu-id="20f11-115">В начале списка команд корневая подпись не определена.</span><span class="sxs-lookup"><span data-stu-id="20f11-115">At the beginning of a command list, the root signature is undefined.</span></span> <span data-ttu-id="20f11-116">Графические шейдеры имеют отдельную корневую подпись от COMPUTE Shader, каждый из которых задан отдельно в списке команд.</span><span class="sxs-lookup"><span data-stu-id="20f11-116">Graphics shaders have a separate root signature from the compute shader, each independently assigned on a command list.</span></span> <span data-ttu-id="20f11-117">Корневой набор сигнатур, заданный для списка команд или пакета, должен также совпадать с текущим набором PSO в Draw или Dispatch. в противном случае поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="20f11-117">The root signature set on a command list or bundle must also match the currently set PSO at Draw/Dispatch; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="20f11-118">Несоответствие временных корневых подписей перед настройкой или отправкой, например при установке несовместимого PSO перед переключением на совместимую корневую подпись (при условии, что они совместимы с вызовом времени или диспетчеризации).</span><span class="sxs-lookup"><span data-stu-id="20f11-118">Transient root signature mismatches before Draw/Dispatch are fine - such as setting an incompatible PSO before switching to a compatible root signature (as long as these are compatible by the time Draw/Dispatch is called).</span></span> <span data-ttu-id="20f11-119">При настройке PSO корневая подпись не изменяется.</span><span class="sxs-lookup"><span data-stu-id="20f11-119">Setting a PSO does not change the root signature.</span></span> <span data-ttu-id="20f11-120">Приложение должно вызывать выделенный API для установки корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="20f11-120">The application must call a dedicated API for setting the root signature.</span></span>

<span data-ttu-id="20f11-121">После установки корневой подписи в списке команд макет определяет набор привязок, которые предполагается предоставить приложению, и какие псос можно использовать (скомпилированные с тем же макетом) для следующих вызовов рисования/диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="20f11-121">Once a root signature has been set on a command list, the layout defines the set of bindings that the application is expected to provide, and which PSOs can be used (those compiled with the same layout) for the next draw/dispatch calls.</span></span> <span data-ttu-id="20f11-122">Например, корневая подпись может быть определена приложением для того, чтобы иметь следующие записи.</span><span class="sxs-lookup"><span data-stu-id="20f11-122">For example, a root signature could be defined by the application to have the following entries.</span></span> <span data-ttu-id="20f11-123">Каждая запись называется "слотом".</span><span class="sxs-lookup"><span data-stu-id="20f11-123">Each entry is referred to as a "slot".</span></span>

-   <span data-ttu-id="20f11-124">\[0 \] — встроенный дескриптор CBV (root)</span><span class="sxs-lookup"><span data-stu-id="20f11-124">\[0\] A CBV descriptor inline (root descriptors)</span></span>
-   <span data-ttu-id="20f11-125">\[1 \] Таблица дескрипторов, содержащая 2 СРВС, 1 КБВС и 1 UAV</span><span class="sxs-lookup"><span data-stu-id="20f11-125">\[1\] A descriptor table containing 2 SRVs, 1 CBVs, and 1 UAV</span></span>
-   <span data-ttu-id="20f11-126">\[2 \] Таблица дескрипторов, содержащая 1 образец</span><span class="sxs-lookup"><span data-stu-id="20f11-126">\[2\] A descriptor table containing 1 sampler</span></span>
-   <span data-ttu-id="20f11-127">\[3 \] 4x32-разрядная коллекция корневых констант</span><span class="sxs-lookup"><span data-stu-id="20f11-127">\[3\] A 4x32-bit collection of root constants</span></span>
-   <span data-ttu-id="20f11-128">\[4 \] Таблица дескрипторов, содержащая неуказанное число СРВС</span><span class="sxs-lookup"><span data-stu-id="20f11-128">\[4\] A descriptor table containing an unspecified number of SRVs</span></span>

<span data-ttu-id="20f11-129">В этом случае, прежде чем выдавать прорисовку или отправку, приложение должно установить соответствующую привязку для каждого из слотов \[ 0.. 4 \] , которое приложение определило с его текущей корневой подписью.</span><span class="sxs-lookup"><span data-stu-id="20f11-129">In this case, before being able to issue a Draw/Dispatch, the application is expected to set the appropriate binding to each of the slots \[0..4\] that the application defined with its current root signature.</span></span> <span data-ttu-id="20f11-130">Например, в слот \[ 1 \] Таблица дескрипторов должна быть привязана, то есть непрерывной областью в куче дескрипторов, которая содержит (или будет содержать при выполнении) 2 СРВС, 1 КБВС и 1 UAV.</span><span class="sxs-lookup"><span data-stu-id="20f11-130">For instance, at slot \[1\], a descriptor table must be bound, which is a contiguous region in a descriptor heap that contains (or will contain at execution) 2 SRVs, 1 CBVs, and 1 UAV.</span></span> <span data-ttu-id="20f11-131">Аналогичным образом необходимо задать таблицы дескрипторов в слотах \[ 2 \] и \[ 4 \] .</span><span class="sxs-lookup"><span data-stu-id="20f11-131">Similarly, descriptor tables must be set at slots \[2\] and \[4\].</span></span>

<span data-ttu-id="20f11-132">Приложение может изменить часть привязок корневой подписи за раз (остальное остается без изменений).</span><span class="sxs-lookup"><span data-stu-id="20f11-132">The application can change part of the root signature bindings at a time (the rest remain unchanged).</span></span> <span data-ttu-id="20f11-133">Например, если единственное, что необходимо изменить между операциями рисования, — одна из констант в слоте \[ 2 \] , то есть приложению нужно выполнить повторную привязку.</span><span class="sxs-lookup"><span data-stu-id="20f11-133">For example, if the only thing that needs to change between draws is one of the constants at slot \[2\], that is all the application needs to rebind.</span></span> <span data-ttu-id="20f11-134">Как обсуждалось ранее, версия драйвера или оборудования привязывает состояние привязки корневой подписи, так как оно изменяется автоматически.</span><span class="sxs-lookup"><span data-stu-id="20f11-134">As discussed previously, the driver/hardware versions all root signature bind state as it is modified automatically.</span></span> <span data-ttu-id="20f11-135">Если корневая сигнатура изменена в списке команд, все предыдущие привязки корневой сигнатуры устаревают и все вновь ожидаемые привязки должны быть установлены до рисования или диспетчеризации; в противном случае поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="20f11-135">If a root signature is changed on a command list, all previous root signature bindings become stale and all newly expected bindings must be set before Draw/Dispatch; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="20f11-136">Если корневая подпись настроена на то же значение, которая уже задана, существующие привязки корневой подписи не устаревают.</span><span class="sxs-lookup"><span data-stu-id="20f11-136">If the root signature is redundantly set to the same one currently set, existing root signature bindings do not become stale.</span></span>

## <a name="bundle-semantics"></a><span data-ttu-id="20f11-137">Семантика пакета</span><span class="sxs-lookup"><span data-stu-id="20f11-137">Bundle Semantics</span></span>

<span data-ttu-id="20f11-138">Пакеты наследуют привязки корневой подписи списка команд (привязки к различным слотам в приведенном выше примере списка команд).</span><span class="sxs-lookup"><span data-stu-id="20f11-138">Bundles inherit the command list's root signature bindings (the bindings to the various slots in the Command List example above).</span></span> <span data-ttu-id="20f11-139">Если пакету необходимо изменить некоторые из наследуемых корневых привязок сигнатур, сначала необходимо задать для корневой подписи то же значение, что и для вызывающего списка команд (унаследованные привязки не устаревают).</span><span class="sxs-lookup"><span data-stu-id="20f11-139">If a bundle needs to change some of the inherited root signature bindings, it must first set the root signature to be the same as the calling command list (the inherited bindings do not become stale).</span></span> <span data-ttu-id="20f11-140">Если пакет задает для корневой подписи значение, отличное от списка вызывающих команд, то оно имеет тот же результат, что и изменение корневой подписи в списке команд, описанном выше: все предыдущие привязки корневой сигнатуры устарели, и перед началом рисования или диспетчеризации должны быть установлены новые привязки. в противном случае поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="20f11-140">If the bundle sets the root signature to be different than the calling command list, that has the same effect as changing the root signature on the command list described above: all previous root signature bindings are stale and newly expected bindings must be set before Draw/Dispatch; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="20f11-141">Если пакету не требуется изменять привязки корневой подписи, не нужно задавать корневую подпись.</span><span class="sxs-lookup"><span data-stu-id="20f11-141">If a bundle does not need to change any root signature bindings, it does not need to set the root signature.</span></span>

<span data-ttu-id="20f11-142">В следующем коде показан пример потока вызовов в пакете.</span><span class="sxs-lookup"><span data-stu-id="20f11-142">The following code shows an example call flow into a bundle.</span></span>

``` syntax
// Command List
...
pCmdList->SetGraphicsRootSignature(pRootSig); // new parameter space
MyEngine_SetTextures(); // bundle inherits descriptor table setting
MyEngine_SetAnimationFactor(fTime); // bundle inherits root constant
pCmdList->ExecuteBundle(...);
...
// Bundle
pBundle->SetGraphicsRootSignature(pRootSig); // same as caller, in order to inherits bindings
pBundle->SetPipelineState(pPS); 
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,0,drawIDOffset);
pBundle->Draw(...); // using inherited textures / animation factor
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,1,drawIDOffset);
pBundle->Draw(...);
...
```

<span data-ttu-id="20f11-143">После выхода из пакета любые изменения в корневом макете и (или) привязки изменяются из пакета в список вызывающих команд после завершения выполнения пакета.</span><span class="sxs-lookup"><span data-stu-id="20f11-143">Coming out of a bundle, any root layout changes and/or binding changes a bundle makes are inherited back to the calling command list when a bundle finishes executing.</span></span>

<span data-ttu-id="20f11-144">Дополнительные сведения о наследовании см. в разделе **наследование состояния графического конвейера** статьи [Управление состоянием графического конвейера в Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="20f11-144">For more information on inheritance, refer to the **Graphics pipeline state inheritance** section of [Managing Graphics Pipeline State in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="20f11-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="20f11-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20f11-146">Корневые подписи</span><span class="sxs-lookup"><span data-stu-id="20f11-146">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




