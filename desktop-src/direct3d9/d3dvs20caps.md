---
description: Константы шейдера вершин. Эти константы используются членом VS20Caps объекта D3DCAPS9.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caccdebe3dc67b6299c038935e26c0dbac2be6d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710751"
---
# <a name="d3dvs20caps"></a><span data-ttu-id="42d89-104">D3DVS20CAPS</span><span class="sxs-lookup"><span data-stu-id="42d89-104">D3DVS20CAPS</span></span>

<span data-ttu-id="42d89-105">Константы шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="42d89-105">Vertex shader caps constants.</span></span> <span data-ttu-id="42d89-106">Эти константы используются членом VS20Caps объекта [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="42d89-106">These constants are used by the VS20Caps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>



| <span data-ttu-id="42d89-107">\#определенно</span><span class="sxs-lookup"><span data-stu-id="42d89-107">\#define</span></span>                              | <span data-ttu-id="42d89-108">Значение</span><span class="sxs-lookup"><span data-stu-id="42d89-108">Value</span></span>          | <span data-ttu-id="42d89-109">Описание</span><span class="sxs-lookup"><span data-stu-id="42d89-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42d89-110">D3DVS20CAPS \_ затенения</span><span class="sxs-lookup"><span data-stu-id="42d89-110">D3DVS20CAPS\_PREDICATION</span></span>              | <span data-ttu-id="42d89-111">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="42d89-111">(1 << 0)</span></span> | <span data-ttu-id="42d89-112">Инструкция затенения поддерживается.</span><span class="sxs-lookup"><span data-stu-id="42d89-112">Instruction predication is supported.</span></span> <span data-ttu-id="42d89-113">См. раздел [сетп \_ comp-VS](../direct3dhlsl/setp-comp---vs.md).</span><span class="sxs-lookup"><span data-stu-id="42d89-113">See [setp\_comp - vs](../direct3dhlsl/setp-comp---vs.md).</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="42d89-114">D3DVS20 \_ Max \_ динамикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="42d89-114">D3DVS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="42d89-115">24</span><span class="sxs-lookup"><span data-stu-id="42d89-115">24</span></span>             | <span data-ttu-id="42d89-116">Максимальный уровень вложенности инструкций динамического управления потоками ([break-VS](../direct3dhlsl/break---vs.md)и [break \_ -VS](../direct3dhlsl/break-comp---vs.md), [бреакп-VS](../direct3dhlsl/breakp---vs.md), [Если \_ comp-](../direct3dhlsl/if-comp---vs.md)VS, if-VS, если \_ " [пред](../direct3dhlsl/if-pred---vs.md)-VS").</span><span class="sxs-lookup"><span data-stu-id="42d89-116">The maximum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="42d89-117">D3DVS20 \_ min \_ динамикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="42d89-117">D3DVS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="42d89-118">0</span><span class="sxs-lookup"><span data-stu-id="42d89-118">0</span></span>              | <span data-ttu-id="42d89-119">Минимальный уровень вложенности инструкций динамического управления потоками ([break-VS](../direct3dhlsl/break---vs.md)и [break \_ -VS](../direct3dhlsl/break-comp---vs.md), [бреакп-VS](../direct3dhlsl/breakp---vs.md), [Если \_ comp-](../direct3dhlsl/if-comp---vs.md)VS, if-VS, если \_ " [пред](../direct3dhlsl/if-pred---vs.md)-VS").</span><span class="sxs-lookup"><span data-stu-id="42d89-119">The minimum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="42d89-120">D3DVS20 \_ Max \_ нумтемпс</span><span class="sxs-lookup"><span data-stu-id="42d89-120">D3DVS20\_MAX\_NUMTEMPS</span></span>                | <span data-ttu-id="42d89-121">32</span><span class="sxs-lookup"><span data-stu-id="42d89-121">32</span></span>             | <span data-ttu-id="42d89-122">Максимальное число поддерживаемых временных регистров.</span><span class="sxs-lookup"><span data-stu-id="42d89-122">The maximum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="42d89-123">D3DVS20 \_ min \_ нумтемпс</span><span class="sxs-lookup"><span data-stu-id="42d89-123">D3DVS20\_MIN\_NUMTEMPS</span></span>                | <span data-ttu-id="42d89-124">12</span><span class="sxs-lookup"><span data-stu-id="42d89-124">12</span></span>             | <span data-ttu-id="42d89-125">Поддерживаемое минимальное количество временных регистров.</span><span class="sxs-lookup"><span data-stu-id="42d89-125">The minimum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="42d89-126">D3DVS20 \_ Max \_ статикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="42d89-126">D3DVS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="42d89-127">4</span><span class="sxs-lookup"><span data-stu-id="42d89-127">4</span></span>              | <span data-ttu-id="42d89-128">Максимальная глубина вложенности инструкций « [цикл](../direct3dhlsl/loop---vs.md)-представителя-VS / [»](../direct3dhlsl/rep---vs.md) и « [Call-](../direct3dhlsl/call---vs.md)VS / [каллнз bool](../direct3dhlsl/callnz-bool---vs.md) -vs».</span><span class="sxs-lookup"><span data-stu-id="42d89-128">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |
| <span data-ttu-id="42d89-129">D3DVS20 \_ min \_ статикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="42d89-129">D3DVS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="42d89-130">1</span><span class="sxs-lookup"><span data-stu-id="42d89-130">1</span></span>              | <span data-ttu-id="42d89-131">Минимальная глубина вложенности инструкций «цикл- [](../direct3dhlsl/loop---vs.md) / [представителя-VS»](../direct3dhlsl/rep---vs.md) и « [Call-](../direct3dhlsl/call---vs.md)VS / [каллнз bool](../direct3dhlsl/callnz-bool---vs.md) -vs».</span><span class="sxs-lookup"><span data-stu-id="42d89-131">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |



 

## <a name="constant-information"></a><span data-ttu-id="42d89-132">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="42d89-132">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="42d89-133">Header</span><span class="sxs-lookup"><span data-stu-id="42d89-133">Header</span></span>                   | <span data-ttu-id="42d89-134">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="42d89-134">d3d9caps.h</span></span> |
| <span data-ttu-id="42d89-135">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="42d89-135">Minimum operating system</span></span> | <span data-ttu-id="42d89-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="42d89-136">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="42d89-137">См. также</span><span class="sxs-lookup"><span data-stu-id="42d89-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42d89-138">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="42d89-138">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="42d89-139">**D3DVSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="42d89-139">**D3DVSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
