---
description: Флаги возможностей шейдера пикселей.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2326b8f5066d34087fb543c7771a0cd547b98f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995271"
---
# <a name="d3dd3dpshadercaps2_0"></a><span data-ttu-id="c9ce0-103">D3DD3DPSHADERCAPS2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c9ce0-103">D3DD3DPSHADERCAPS2\_0</span></span>

<span data-ttu-id="c9ce0-104">Флаги возможностей шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="c9ce0-104">Pixel shader capability flags.</span></span>



| <span data-ttu-id="c9ce0-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="c9ce0-105">\#define</span></span>                                     | <span data-ttu-id="c9ce0-106">Значение</span><span class="sxs-lookup"><span data-stu-id="c9ce0-106">Value</span></span>          | <span data-ttu-id="c9ce0-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c9ce0-107">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ce0-108">D3DD3DPSHADERCAPS2 \_ 0 \_ арбитрарисвиззле</span><span class="sxs-lookup"><span data-stu-id="c9ce0-108">D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE</span></span>      | <span data-ttu-id="c9ce0-109">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="c9ce0-109">(1 << 0)</span></span> | <span data-ttu-id="c9ce0-110">Поддерживается произвольный группирующие.</span><span class="sxs-lookup"><span data-stu-id="c9ce0-110">Arbitrary swizzling is supported.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="c9ce0-111">D3DD3DPSHADERCAPS2 \_ 0 \_ градиентинструктионс</span><span class="sxs-lookup"><span data-stu-id="c9ce0-111">D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS</span></span>  | <span data-ttu-id="c9ce0-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="c9ce0-112">(1 << 1)</span></span> | <span data-ttu-id="c9ce0-113">Поддерживаются инструкции градиента.</span><span class="sxs-lookup"><span data-stu-id="c9ce0-113">Gradient instructions are supported.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="c9ce0-114">D3DD3DPSHADERCAPS2 \_ 0 \_ затенения</span><span class="sxs-lookup"><span data-stu-id="c9ce0-114">D3DD3DPSHADERCAPS2\_0\_PREDICATION</span></span>           | <span data-ttu-id="c9ce0-115">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="c9ce0-115">(1 << 2)</span></span> | <span data-ttu-id="c9ce0-116">Инструкция затенения поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c9ce0-116">Instruction predication is supported.</span></span> <span data-ttu-id="c9ce0-117">См. [сетп \_ comp-PS](../direct3dhlsl/setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="c9ce0-117">See [setp\_comp - ps](../direct3dhlsl/setp-comp---ps.md).</span></span>                                                                                                                         |
| <span data-ttu-id="c9ce0-118">D3DD3DPSHADERCAPS2 \_ 0 \_ нодепендентреадлимит</span><span class="sxs-lookup"><span data-stu-id="c9ce0-118">D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT</span></span>  | <span data-ttu-id="c9ce0-119">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="c9ce0-119">(1 << 3)</span></span> | <span data-ttu-id="c9ce0-120">Количество зависимых операций чтения для каждой инструкции не ограничено.</span><span class="sxs-lookup"><span data-stu-id="c9ce0-120">There is no limit on the number of dependent reads per instruction.</span></span>                                                                                                                                               |
| <span data-ttu-id="c9ce0-121">D3DD3DPSHADERCAPS2 \_ 0 \_ нотексинструктионлимит</span><span class="sxs-lookup"><span data-stu-id="c9ce0-121">D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT</span></span> | <span data-ttu-id="c9ce0-122">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="c9ce0-122">(1 << 4)</span></span> | <span data-ttu-id="c9ce0-123">Количество инструкций да не ограничено.</span><span class="sxs-lookup"><span data-stu-id="c9ce0-123">There is no limit on the number of tex instructions.</span></span>                                                                                                                                                              |
| <span data-ttu-id="c9ce0-124">D3DPS20 \_ Max \_ динамикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="c9ce0-124">D3DPS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="c9ce0-125">24</span><span class="sxs-lookup"><span data-stu-id="c9ce0-125">24</span></span>             | <span data-ttu-id="c9ce0-126">Максимальный уровень вложенности инструкций динамического управления потоком (break, бреакк, ИФК).</span><span class="sxs-lookup"><span data-stu-id="c9ce0-126">The maximum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="c9ce0-127">D3DPS20 \_ min \_ динамикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="c9ce0-127">D3DPS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="c9ce0-128">0</span><span class="sxs-lookup"><span data-stu-id="c9ce0-128">0</span></span>              | <span data-ttu-id="c9ce0-129">Минимальный уровень вложенности инструкций динамического управления потоком (break, бреакк, ИФК).</span><span class="sxs-lookup"><span data-stu-id="c9ce0-129">The minimum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="c9ce0-130">D3DPS20 \_ Max \_ нумтемпс</span><span class="sxs-lookup"><span data-stu-id="c9ce0-130">D3DPS20\_MAX\_NUMTEMPS</span></span>                       | <span data-ttu-id="c9ce0-131">32</span><span class="sxs-lookup"><span data-stu-id="c9ce0-131">32</span></span>             | <span data-ttu-id="c9ce0-132">Драйвер будет поддерживать не более этого количества временных регистров.</span><span class="sxs-lookup"><span data-stu-id="c9ce0-132">The driver will support at most this many temporary register.</span></span>                                                                                                                                                     |
| <span data-ttu-id="c9ce0-133">D3DPS20 \_ min \_ нумтемпс</span><span class="sxs-lookup"><span data-stu-id="c9ce0-133">D3DPS20\_MIN\_NUMTEMPS</span></span>                       | <span data-ttu-id="c9ce0-134">12</span><span class="sxs-lookup"><span data-stu-id="c9ce0-134">12</span></span>             | <span data-ttu-id="c9ce0-135">Драйвер будет поддерживать по крайней мере столько временных регистров.</span><span class="sxs-lookup"><span data-stu-id="c9ce0-135">The driver will support at least this many temporary register.</span></span>                                                                                                                                                    |
| <span data-ttu-id="c9ce0-136">D3DPS20 \_ Max \_ статикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="c9ce0-136">D3DPS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="c9ce0-137">4</span><span class="sxs-lookup"><span data-stu-id="c9ce0-137">4</span></span>              | <span data-ttu-id="c9ce0-138">Максимальная глубина вложенности инструкций « [цикл](../direct3dhlsl/loop---vs.md)-представителя-VS / [»](../direct3dhlsl/rep---vs.md) и « [Call-](../direct3dhlsl/call---vs.md)VS / [каллнз bool](../direct3dhlsl/callnz-bool---vs.md) -vs».</span><span class="sxs-lookup"><span data-stu-id="c9ce0-138">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="c9ce0-139">D3DPS20 \_ min \_ статикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="c9ce0-139">D3DPS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="c9ce0-140">1</span><span class="sxs-lookup"><span data-stu-id="c9ce0-140">1</span></span>              | <span data-ttu-id="c9ce0-141">Минимальная глубина вложенности инструкций «цикл- [](../direct3dhlsl/loop---vs.md) / [представителя-VS»](../direct3dhlsl/rep---vs.md) и « [Call-](../direct3dhlsl/call---vs.md)VS / [каллнз bool](../direct3dhlsl/callnz-bool---vs.md) -vs».</span><span class="sxs-lookup"><span data-stu-id="c9ce0-141">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="c9ce0-142">D3DPS20 \_ Max \_ нуминструктионслотс</span><span class="sxs-lookup"><span data-stu-id="c9ce0-142">D3DPS20\_MAX\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="c9ce0-143">512</span><span class="sxs-lookup"><span data-stu-id="c9ce0-143">512</span></span>            | <span data-ttu-id="c9ce0-144">Драйвер будет поддерживать не более этого числа инструкций.</span><span class="sxs-lookup"><span data-stu-id="c9ce0-144">The driver will support at most this many instructions.</span></span>                                                                                                                                                           |
| <span data-ttu-id="c9ce0-145">D3DPS20 \_ min \_ нуминструктионслотс</span><span class="sxs-lookup"><span data-stu-id="c9ce0-145">D3DPS20\_MIN\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="c9ce0-146">96</span><span class="sxs-lookup"><span data-stu-id="c9ce0-146">96</span></span>             | <span data-ttu-id="c9ce0-147">Драйвер будет поддерживать по крайней мере столько инструкций.</span><span class="sxs-lookup"><span data-stu-id="c9ce0-147">The driver will support at least this many instructions.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="c9ce0-148">Эти константы используются \_ членом D3DPSHADERCAPS2 0 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="c9ce0-148">These constants are used by the D3DPSHADERCAPS2\_0 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="c9ce0-149">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="c9ce0-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="c9ce0-150">Header</span><span class="sxs-lookup"><span data-stu-id="c9ce0-150">Header</span></span>                   | <span data-ttu-id="c9ce0-151">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="c9ce0-151">d3d9caps.h</span></span> |
| <span data-ttu-id="c9ce0-152">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="c9ce0-152">Minimum operating system</span></span> | <span data-ttu-id="c9ce0-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c9ce0-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c9ce0-154">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c9ce0-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9ce0-155">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="c9ce0-155">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="c9ce0-156">**D3DPSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="c9ce0-156">**D3DPSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
