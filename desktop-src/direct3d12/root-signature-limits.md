---
title: Ограничения корневой подписи
description: Корневая подпись — это простое недвижимость, и существуют ограничения и затраты, которые следует учитывать.
ms.assetid: 01121D3A-1926-4246-9C20-5E11F2E0B092
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25986da72cfcad7b714031e063341e1832d6ae68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104571"
---
# <a name="root-signature-limits"></a><span data-ttu-id="cbb2c-103">Ограничения корневой подписи</span><span class="sxs-lookup"><span data-stu-id="cbb2c-103">Root Signature Limits</span></span>

<span data-ttu-id="cbb2c-104">Корневая подпись — это простое недвижимость, и существуют ограничения и затраты, которые следует учитывать.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-104">The root signature is prime real estate, and there are strict limits and costs to consider.</span></span>

-   [<span data-ttu-id="cbb2c-105">Ограничения и затраты на память</span><span class="sxs-lookup"><span data-stu-id="cbb2c-105">Memory limits and costs</span></span>](#memory-limits-and-costs)
-   [<span data-ttu-id="cbb2c-106">Затраты на производительность</span><span class="sxs-lookup"><span data-stu-id="cbb2c-106">Performance costs</span></span>](#performance-costs)
-   [<span data-ttu-id="cbb2c-107">Статические пробы</span><span class="sxs-lookup"><span data-stu-id="cbb2c-107">Static samplers</span></span>](#static-samplers)
-   [<span data-ttu-id="cbb2c-108">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="cbb2c-108">Related topics</span></span>](#related-topics)

## <a name="memory-limits-and-costs"></a><span data-ttu-id="cbb2c-109">Ограничения и затраты на память</span><span class="sxs-lookup"><span data-stu-id="cbb2c-109">Memory limits and costs</span></span>

<span data-ttu-id="cbb2c-110">Максимальный размер корневой подписи — 64 DWORD.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-110">The maximum size of a root signature is 64 DWORDs.</span></span>

<span data-ttu-id="cbb2c-111">Этот максимальный размер выбирается, чтобы предотвратить нарушение подлинности корневой подписи в качестве способа хранения данных большого объема.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-111">This maximum size is chosen to prevent abuse of the root signature as a way of storing bulk data.</span></span> <span data-ttu-id="cbb2c-112">Каждая запись в корневой подписи имеет стоимость в 64 DWORD.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-112">Each entry in the root signature has a cost towards this 64 DWORD limit:</span></span>

-   <span data-ttu-id="cbb2c-113">Таблицы дескрипторов 1 DWORD каждый.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-113">Descriptor tables cost 1 DWORD each.</span></span>
-   <span data-ttu-id="cbb2c-114">Корневые константы имеют значение 1 DWORD, так как они представляют собой 32-битные значения.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-114">Root constants cost 1 DWORD each, since they are 32-bit values.</span></span>
-   <span data-ttu-id="cbb2c-115">Корневые дескрипторы (64-битные виртуальные адреса GPU) стоимость 2 DWORD каждого.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-115">Root descriptors (64-bit GPU virtual addresses) cost 2 DWORDs each.</span></span>

<span data-ttu-id="cbb2c-116">У статических пробных версий нет затрат на размер корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-116">Static samplers do not have any cost in the size of the root signature.</span></span>

## <a name="performance-costs"></a><span data-ttu-id="cbb2c-117">Затраты на производительность</span><span class="sxs-lookup"><span data-stu-id="cbb2c-117">Performance costs</span></span>

<span data-ttu-id="cbb2c-118">Затраты на производительность (с точки зрения уровней косвенного обращения) равны нулю для корневой константы, 1 — для корневого дескриптора и 2 — для таблицы дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-118">The performance cost (in terms of levels of indirection) are zero for a root constant, 1 for a root descriptor, and 2 for a descriptor table.</span></span> <span data-ttu-id="cbb2c-119">Если корневая подпись велика и выходит за пределы самой быстрой памяти на немного медленный объем памяти (что может произойти на определенном оборудовании), добавьте 1 к затратам на производительность для элементов, переходящих в конце корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-119">If a root signature is large and overflows out of the fastest memory into slightly slower memory (which can happen on some hardware), then add 1 to the performance cost for the overflowing items at the end of the root signature.</span></span>

<span data-ttu-id="cbb2c-120">Переполнение может произойти на оборудовании, которое может иметь, например, фиксированный размер в 16 DWORD для пространства корневого аргумента.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-120">An overflow can occur on hardware that might have, for example, a fixed size of 16 DWORDs for root argument space.</span></span> <span data-ttu-id="cbb2c-121">Это ограничение может быть дополнительно уменьшено на один, если используется входной ассемблер.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-121">This limit might be further reduced by one if the Input Assembler is used.</span></span> <span data-ttu-id="cbb2c-122">В этом случае переполнение немного замедляет память, если корневая подпись слишком велика для памяти в 15 или 16 DWORD.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-122">In this case there is overflow into slightly slower memory if the root signature is too large for the 15 or 16 DWORD native memory.</span></span> <span data-ttu-id="cbb2c-123">В другом оборудовании отсутствует фиксированная собственная память аргумента root (так что ситуация переполнения никогда не возникает).</span><span class="sxs-lookup"><span data-stu-id="cbb2c-123">In other hardware there is no fixed native root argument memory (so the overflow situation never occurs).</span></span>

<span data-ttu-id="cbb2c-124">Для всех устройств при изменении корневого аргумента драйвер должен поддерживать версию всех корневых аргументов (в отличие от других хранилищ, таких как кучи дескрипторов и буферные ресурсы, для которых драйвер не поддерживает управление версиями).</span><span class="sxs-lookup"><span data-stu-id="cbb2c-124">For all hardware, if any root argument changes, the driver must maintain a version of all the root arguments (unlike other storage such as descriptor heaps and buffer resources, which are not versioned by the driver).</span></span> <span data-ttu-id="cbb2c-125">На оборудовании возникает ситуация переполнения, в зависимости от того, где произошло изменение, необходимо иметь версию только для машинного кода или области переполнения.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-125">In hardware that an overflow situation occurs, only the native or overflow area needs to be versioned, depending on where the change occurred.</span></span> <span data-ttu-id="cbb2c-126">Необходимо, чтобы количество версий хранилось до необходимого минимума.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-126">The amount of versioning should obviously be kept to the necessary minimum.</span></span>

<span data-ttu-id="cbb2c-127">Как правило, учитывайте следующие рекомендации.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-127">Generally, consider the following guidelines:</span></span>

-   <span data-ttu-id="cbb2c-128">При необходимости используйте небольшой корневой сигнатуры, но следует сбалансировать это с гибкостью более крупной корневой сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-128">Use a small a root signature as necessary, though balance this with the flexibility of a larger root signature.</span></span>
-   <span data-ttu-id="cbb2c-129">Расположите параметры в большой корневой подписи таким образом, чтобы параметры, скорее всего, изменялись часто, или если важна низкая задержка доступа для данного параметра.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-129">Arrange parameters in a large root signature so that the parameters most likely to change often, or if low access latency for a given parameter is important, occur first.</span></span>
-   <span data-ttu-id="cbb2c-130">При использовании удобно использовать корневые константы или представления буфера корневых констант, помещая представления буфера констант в кучу дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-130">If convenient, use root constants or root constant buffer views over putting constant buffer views in a descriptor heap.</span></span>

## <a name="static-samplers"></a><span data-ttu-id="cbb2c-131">Статические пробы</span><span class="sxs-lookup"><span data-stu-id="cbb2c-131">Static samplers</span></span>

<span data-ttu-id="cbb2c-132">Статические пробы (пробы, в которых состояние полностью определено и неизменно) являются частью корневых подписей, но не учитываются при ограничении в 64 DWORD.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-132">Static samplers (samplers where the state is fully defined and immutable) are part of root signatures, but do not count towards the 64 DWORD limit.</span></span> <span data-ttu-id="cbb2c-133">Если выборка может быть определена как статическая, нет необходимости в том, чтобы образец был частью кучи дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-133">If a sampler can be defined as static, there is no need for the sampler to be part of a descriptor heap.</span></span>

<span data-ttu-id="cbb2c-134">Использование статических выборок не дает никаких затрат на производительность, а корневая подпись может содержать смесь статических выборок (хранящихся в корневой подписи или в зарезервированном пространстве на определенном оборудовании) и динамических проб (хранимых в куче дескрипторов образцов).</span><span class="sxs-lookup"><span data-stu-id="cbb2c-134">There is no performance cost to using static samplers, and a root signature can contain a mix of static samplers (stored in the root signature, or in reserved space on some hardware) and dynamic samplers (stored in a sampler descriptor heap).</span></span> <span data-ttu-id="cbb2c-135">Пробы в куче дескрипторов могут динамически назначаться и индексироваться, какие статические выборки не могут быть.</span><span class="sxs-lookup"><span data-stu-id="cbb2c-135">Samplers in a descriptor heap can be dynamically assigned and indexed, which static samplers cannot.</span></span>

<span data-ttu-id="cbb2c-136">Статические пробы можно записать как часть корневой подписи в HLSL шейдеров (см. раздел [Указание корневых сигнатур в HLSL](specifying-root-signatures-in-hlsl.md)).</span><span class="sxs-lookup"><span data-stu-id="cbb2c-136">Static samplers can be written as part of the root signature in HLSL shaders (refer to [Specifying Root Signatures in HLSL](specifying-root-signatures-in-hlsl.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbb2c-137">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="cbb2c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbb2c-138">Корневые подписи</span><span class="sxs-lookup"><span data-stu-id="cbb2c-138">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




