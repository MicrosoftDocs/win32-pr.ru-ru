---
description: Константы шейдера вершин. Эти константы используются членом VS20Caps объекта D3DCAPS9.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bd0905a0996e2dc9df77adb0896c9397a93450
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342949"
---
# <a name="d3dvs20caps"></a><span data-ttu-id="1c6b4-104">D3DVS20CAPS</span><span class="sxs-lookup"><span data-stu-id="1c6b4-104">D3DVS20CAPS</span></span>

<span data-ttu-id="1c6b4-105">Константы шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="1c6b4-105">Vertex shader caps constants.</span></span> <span data-ttu-id="1c6b4-106">Эти константы используются членом VS20Caps объекта [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="1c6b4-106">These constants are used by the VS20Caps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>



| <span data-ttu-id="1c6b4-107">\#определенно</span><span class="sxs-lookup"><span data-stu-id="1c6b4-107">\#define</span></span>                              | <span data-ttu-id="1c6b4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1c6b4-108">Value</span></span>          | <span data-ttu-id="1c6b4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1c6b4-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c6b4-110">D3DVS20CAPS \_ затенения</span><span class="sxs-lookup"><span data-stu-id="1c6b4-110">D3DVS20CAPS\_PREDICATION</span></span>              | <span data-ttu-id="1c6b4-111">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="1c6b4-111">(1 << 0)</span></span> | <span data-ttu-id="1c6b4-112">Инструкция затенения поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1c6b4-112">Instruction predication is supported.</span></span> <span data-ttu-id="1c6b4-113">См. раздел [сетп \_ comp-VS](../direct3dhlsl/setp-comp---vs.md).</span><span class="sxs-lookup"><span data-stu-id="1c6b4-113">See [setp\_comp - vs](../direct3dhlsl/setp-comp---vs.md).</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="1c6b4-114">D3DVS20 \_ Max \_ динамикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="1c6b4-114">D3DVS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="1c6b4-115">24</span><span class="sxs-lookup"><span data-stu-id="1c6b4-115">24</span></span>             | <span data-ttu-id="1c6b4-116">Максимальный уровень вложенности инструкций динамического управления потоками ([break-VS](../direct3dhlsl/break---vs.md)и [break \_ -VS](../direct3dhlsl/break-comp---vs.md), [бреакп-VS](../direct3dhlsl/breakp---vs.md), [Если \_ comp-](../direct3dhlsl/if-comp---vs.md)VS, if-VS, если \_ " [пред](../direct3dhlsl/if-pred---vs.md)-VS").</span><span class="sxs-lookup"><span data-stu-id="1c6b4-116">The maximum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="1c6b4-117">D3DVS20 \_ min \_ динамикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="1c6b4-117">D3DVS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="1c6b4-118">0</span><span class="sxs-lookup"><span data-stu-id="1c6b4-118">0</span></span>              | <span data-ttu-id="1c6b4-119">Минимальный уровень вложенности инструкций динамического управления потоками ([break-VS](../direct3dhlsl/break---vs.md)и [break \_ -VS](../direct3dhlsl/break-comp---vs.md), [бреакп-VS](../direct3dhlsl/breakp---vs.md), [Если \_ comp-](../direct3dhlsl/if-comp---vs.md)VS, if-VS, если \_ " [пред](../direct3dhlsl/if-pred---vs.md)-VS").</span><span class="sxs-lookup"><span data-stu-id="1c6b4-119">The minimum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="1c6b4-120">D3DVS20 \_ Max \_ нумтемпс</span><span class="sxs-lookup"><span data-stu-id="1c6b4-120">D3DVS20\_MAX\_NUMTEMPS</span></span>                | <span data-ttu-id="1c6b4-121">32</span><span class="sxs-lookup"><span data-stu-id="1c6b4-121">32</span></span>             | <span data-ttu-id="1c6b4-122">Максимальное число поддерживаемых временных регистров.</span><span class="sxs-lookup"><span data-stu-id="1c6b4-122">The maximum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1c6b4-123">D3DVS20 \_ min \_ нумтемпс</span><span class="sxs-lookup"><span data-stu-id="1c6b4-123">D3DVS20\_MIN\_NUMTEMPS</span></span>                | <span data-ttu-id="1c6b4-124">12</span><span class="sxs-lookup"><span data-stu-id="1c6b4-124">12</span></span>             | <span data-ttu-id="1c6b4-125">Поддерживаемое минимальное количество временных регистров.</span><span class="sxs-lookup"><span data-stu-id="1c6b4-125">The minimum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1c6b4-126">D3DVS20 \_ Max \_ статикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="1c6b4-126">D3DVS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="1c6b4-127">4</span><span class="sxs-lookup"><span data-stu-id="1c6b4-127">4</span></span>              | <span data-ttu-id="1c6b4-128">Максимальная глубина вложенности инструкций « [цикл](../direct3dhlsl/loop---vs.md)-представителя-VS / [»](../direct3dhlsl/rep---vs.md) и « [Call-](../direct3dhlsl/call---vs.md)VS / [каллнз bool](../direct3dhlsl/callnz-bool---vs.md) -vs».</span><span class="sxs-lookup"><span data-stu-id="1c6b4-128">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |
| <span data-ttu-id="1c6b4-129">D3DVS20 \_ min \_ статикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="1c6b4-129">D3DVS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="1c6b4-130">1</span><span class="sxs-lookup"><span data-stu-id="1c6b4-130">1</span></span>              | <span data-ttu-id="1c6b4-131">Минимальная глубина вложенности инструкций «цикл- [](../direct3dhlsl/loop---vs.md) / [представителя-VS»](../direct3dhlsl/rep---vs.md) и « [Call-](../direct3dhlsl/call---vs.md)VS / [каллнз bool](../direct3dhlsl/callnz-bool---vs.md) -vs».</span><span class="sxs-lookup"><span data-stu-id="1c6b4-131">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |



 

## <a name="constant-information"></a><span data-ttu-id="1c6b4-132">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="1c6b4-132">Constant Information</span></span>



| <span data-ttu-id="1c6b4-133">Требование</span><span class="sxs-lookup"><span data-stu-id="1c6b4-133">Requirement</span></span>                         | <span data-ttu-id="1c6b4-134">Значение</span><span class="sxs-lookup"><span data-stu-id="1c6b4-134">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="1c6b4-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1c6b4-135">Header</span></span>                   | <span data-ttu-id="1c6b4-136">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="1c6b4-136">d3d9caps.h</span></span> |
| <span data-ttu-id="1c6b4-137">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="1c6b4-137">Minimum operating system</span></span> | <span data-ttu-id="1c6b4-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="1c6b4-138">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1c6b4-139">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1c6b4-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c6b4-140">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="1c6b4-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="1c6b4-141">**D3DVSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="1c6b4-141">**D3DVSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
