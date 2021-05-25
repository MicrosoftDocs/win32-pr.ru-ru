---
description: Флаги возможностей шейдера пикселей.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4eed8fb6c7a5c4c4da31185dc4cc8c1661f7109
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343119"
---
# <a name="d3dd3dpshadercaps2_0"></a><span data-ttu-id="a0f04-103">D3DD3DPSHADERCAPS2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0f04-103">D3DD3DPSHADERCAPS2\_0</span></span>

<span data-ttu-id="a0f04-104">Флаги возможностей шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="a0f04-104">Pixel shader capability flags.</span></span>



| <span data-ttu-id="a0f04-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="a0f04-105">\#define</span></span>                                     | <span data-ttu-id="a0f04-106">Значение</span><span class="sxs-lookup"><span data-stu-id="a0f04-106">Value</span></span>          | <span data-ttu-id="a0f04-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a0f04-107">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f04-108">D3DD3DPSHADERCAPS2 \_ 0 \_ арбитрарисвиззле</span><span class="sxs-lookup"><span data-stu-id="a0f04-108">D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE</span></span>      | <span data-ttu-id="a0f04-109">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="a0f04-109">(1 << 0)</span></span> | <span data-ttu-id="a0f04-110">Поддерживается произвольный группирующие.</span><span class="sxs-lookup"><span data-stu-id="a0f04-110">Arbitrary swizzling is supported.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="a0f04-111">D3DD3DPSHADERCAPS2 \_ 0 \_ градиентинструктионс</span><span class="sxs-lookup"><span data-stu-id="a0f04-111">D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS</span></span>  | <span data-ttu-id="a0f04-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="a0f04-112">(1 << 1)</span></span> | <span data-ttu-id="a0f04-113">Поддерживаются инструкции градиента.</span><span class="sxs-lookup"><span data-stu-id="a0f04-113">Gradient instructions are supported.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="a0f04-114">D3DD3DPSHADERCAPS2 \_ 0 \_ затенения</span><span class="sxs-lookup"><span data-stu-id="a0f04-114">D3DD3DPSHADERCAPS2\_0\_PREDICATION</span></span>           | <span data-ttu-id="a0f04-115">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="a0f04-115">(1 << 2)</span></span> | <span data-ttu-id="a0f04-116">Инструкция затенения поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a0f04-116">Instruction predication is supported.</span></span> <span data-ttu-id="a0f04-117">См. [сетп \_ comp-PS](../direct3dhlsl/setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="a0f04-117">See [setp\_comp - ps](../direct3dhlsl/setp-comp---ps.md).</span></span>                                                                                                                         |
| <span data-ttu-id="a0f04-118">D3DD3DPSHADERCAPS2 \_ 0 \_ нодепендентреадлимит</span><span class="sxs-lookup"><span data-stu-id="a0f04-118">D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT</span></span>  | <span data-ttu-id="a0f04-119">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="a0f04-119">(1 << 3)</span></span> | <span data-ttu-id="a0f04-120">Количество зависимых операций чтения для каждой инструкции не ограничено.</span><span class="sxs-lookup"><span data-stu-id="a0f04-120">There is no limit on the number of dependent reads per instruction.</span></span>                                                                                                                                               |
| <span data-ttu-id="a0f04-121">D3DD3DPSHADERCAPS2 \_ 0 \_ нотексинструктионлимит</span><span class="sxs-lookup"><span data-stu-id="a0f04-121">D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT</span></span> | <span data-ttu-id="a0f04-122">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="a0f04-122">(1 << 4)</span></span> | <span data-ttu-id="a0f04-123">Количество инструкций да не ограничено.</span><span class="sxs-lookup"><span data-stu-id="a0f04-123">There is no limit on the number of tex instructions.</span></span>                                                                                                                                                              |
| <span data-ttu-id="a0f04-124">D3DPS20 \_ Max \_ динамикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="a0f04-124">D3DPS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="a0f04-125">24</span><span class="sxs-lookup"><span data-stu-id="a0f04-125">24</span></span>             | <span data-ttu-id="a0f04-126">Максимальный уровень вложенности инструкций динамического управления потоком (break, бреакк, ИФК).</span><span class="sxs-lookup"><span data-stu-id="a0f04-126">The maximum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="a0f04-127">D3DPS20 \_ min \_ динамикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="a0f04-127">D3DPS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="a0f04-128">0</span><span class="sxs-lookup"><span data-stu-id="a0f04-128">0</span></span>              | <span data-ttu-id="a0f04-129">Минимальный уровень вложенности инструкций динамического управления потоком (break, бреакк, ИФК).</span><span class="sxs-lookup"><span data-stu-id="a0f04-129">The minimum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="a0f04-130">D3DPS20 \_ Max \_ нумтемпс</span><span class="sxs-lookup"><span data-stu-id="a0f04-130">D3DPS20\_MAX\_NUMTEMPS</span></span>                       | <span data-ttu-id="a0f04-131">32</span><span class="sxs-lookup"><span data-stu-id="a0f04-131">32</span></span>             | <span data-ttu-id="a0f04-132">Драйвер будет поддерживать не более этого количества временных регистров.</span><span class="sxs-lookup"><span data-stu-id="a0f04-132">The driver will support at most this many temporary register.</span></span>                                                                                                                                                     |
| <span data-ttu-id="a0f04-133">D3DPS20 \_ min \_ нумтемпс</span><span class="sxs-lookup"><span data-stu-id="a0f04-133">D3DPS20\_MIN\_NUMTEMPS</span></span>                       | <span data-ttu-id="a0f04-134">12</span><span class="sxs-lookup"><span data-stu-id="a0f04-134">12</span></span>             | <span data-ttu-id="a0f04-135">Драйвер будет поддерживать по крайней мере столько временных регистров.</span><span class="sxs-lookup"><span data-stu-id="a0f04-135">The driver will support at least this many temporary register.</span></span>                                                                                                                                                    |
| <span data-ttu-id="a0f04-136">D3DPS20 \_ Max \_ статикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="a0f04-136">D3DPS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="a0f04-137">4</span><span class="sxs-lookup"><span data-stu-id="a0f04-137">4</span></span>              | <span data-ttu-id="a0f04-138">Максимальная глубина вложенности инструкций « [цикл](../direct3dhlsl/loop---vs.md)-представителя-VS / [»](../direct3dhlsl/rep---vs.md) и « [Call-](../direct3dhlsl/call---vs.md)VS / [каллнз bool](../direct3dhlsl/callnz-bool---vs.md) -vs».</span><span class="sxs-lookup"><span data-stu-id="a0f04-138">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="a0f04-139">D3DPS20 \_ min \_ статикфловконтролдепс</span><span class="sxs-lookup"><span data-stu-id="a0f04-139">D3DPS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="a0f04-140">1</span><span class="sxs-lookup"><span data-stu-id="a0f04-140">1</span></span>              | <span data-ttu-id="a0f04-141">Минимальная глубина вложенности инструкций «цикл- [](../direct3dhlsl/loop---vs.md) / [представителя-VS»](../direct3dhlsl/rep---vs.md) и « [Call-](../direct3dhlsl/call---vs.md)VS / [каллнз bool](../direct3dhlsl/callnz-bool---vs.md) -vs».</span><span class="sxs-lookup"><span data-stu-id="a0f04-141">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="a0f04-142">D3DPS20 \_ Max \_ нуминструктионслотс</span><span class="sxs-lookup"><span data-stu-id="a0f04-142">D3DPS20\_MAX\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="a0f04-143">512</span><span class="sxs-lookup"><span data-stu-id="a0f04-143">512</span></span>            | <span data-ttu-id="a0f04-144">Драйвер будет поддерживать не более этого числа инструкций.</span><span class="sxs-lookup"><span data-stu-id="a0f04-144">The driver will support at most this many instructions.</span></span>                                                                                                                                                           |
| <span data-ttu-id="a0f04-145">D3DPS20 \_ min \_ нуминструктионслотс</span><span class="sxs-lookup"><span data-stu-id="a0f04-145">D3DPS20\_MIN\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="a0f04-146">96</span><span class="sxs-lookup"><span data-stu-id="a0f04-146">96</span></span>             | <span data-ttu-id="a0f04-147">Драйвер будет поддерживать по крайней мере столько инструкций.</span><span class="sxs-lookup"><span data-stu-id="a0f04-147">The driver will support at least this many instructions.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="a0f04-148">Эти константы используются \_ членом D3DPSHADERCAPS2 0 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="a0f04-148">These constants are used by the D3DPSHADERCAPS2\_0 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="a0f04-149">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="a0f04-149">Constant Information</span></span>



|  <span data-ttu-id="a0f04-150">Требование</span><span class="sxs-lookup"><span data-stu-id="a0f04-150">Requirement</span></span>                        | <span data-ttu-id="a0f04-151">Значение</span><span class="sxs-lookup"><span data-stu-id="a0f04-151">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="a0f04-152">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a0f04-152">Header</span></span>                   | <span data-ttu-id="a0f04-153">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="a0f04-153">d3d9caps.h</span></span> |
| <span data-ttu-id="a0f04-154">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="a0f04-154">Minimum operating system</span></span> | <span data-ttu-id="a0f04-155">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a0f04-155">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a0f04-156">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a0f04-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0f04-157">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="a0f04-157">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="a0f04-158">**D3DPSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="a0f04-158">**D3DPSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
