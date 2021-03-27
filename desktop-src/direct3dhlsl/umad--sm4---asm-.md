---
title: умад (SM4-ASM)
description: Целое число без знака умножается и добавляется.
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce52925622cb2f6f7cf53dec0e3f6f65d3fdcb58
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784929"
---
# <a name="umad-sm4---asm"></a><span data-ttu-id="e5b58-103">умад (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e5b58-103">umad (sm4 - asm)</span></span>

<span data-ttu-id="e5b58-104">Целое число без знака умножается и добавляется.</span><span class="sxs-lookup"><span data-stu-id="e5b58-104">Unsigned integer multiply and add.</span></span>



| <span data-ttu-id="e5b58-105">умад dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле \] , src2 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="e5b58-105">umad dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="e5b58-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="e5b58-106">Item</span></span>                                                            | <span data-ttu-id="e5b58-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e5b58-107">Description</span></span>                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e5b58-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e5b58-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e5b58-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="e5b58-109">\[in\] The address of the result of the operation.</span></span><br/>           |
| <span data-ttu-id="e5b58-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e5b58-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e5b58-111">\[в \] значении, умноженном на *src1*.</span><span class="sxs-lookup"><span data-stu-id="e5b58-111">\[in\] The value to multiply with *src1*.</span></span><br/>                    |
| <span data-ttu-id="e5b58-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="e5b58-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="e5b58-113">\[в \] значении, умноженном на *src1*.</span><span class="sxs-lookup"><span data-stu-id="e5b58-113">\[in\] The value to multiply with *src1*.</span></span><br/>                     |
| <span data-ttu-id="e5b58-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="e5b58-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="e5b58-115">\[в \] значение, добавляемое к продукту *src0* и *src1*.</span><span class="sxs-lookup"><span data-stu-id="e5b58-115">\[in\] The value to add to the product of *src0* and *src1*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e5b58-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5b58-116">Remarks</span></span>

<span data-ttu-id="e5b58-117">Компонентно-ориентированный [умул](umul--sm4---asm-.md) для 32-разрядных операндов *src0* и *src1* без знака, сохраняя низкий 32-бит на каждый компонент в результате.</span><span class="sxs-lookup"><span data-stu-id="e5b58-117">Component-wise [umul](umul--sm4---asm-.md) of 32-bit operands *src0* and *src1* unsigned, keeping the low 32-bits, per component, of the result.</span></span> <span data-ttu-id="e5b58-118">Затем эта инструкция выполняет [IAdd](iadd--sm4---asm-.md) из *src2*, создавая правильный младший 32-разрядный результат (на каждый компонент).</span><span class="sxs-lookup"><span data-stu-id="e5b58-118">This instruction then performs an [iadd](iadd--sm4---asm-.md) of *src2*, producing the correct low 32-bit (per component) result.</span></span> <span data-ttu-id="e5b58-119">32-разрядные результаты помещаются в *dest*.</span><span class="sxs-lookup"><span data-stu-id="e5b58-119">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="e5b58-120">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="e5b58-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e5b58-121">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="e5b58-121">Vertex Shader</span></span> | <span data-ttu-id="e5b58-122">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="e5b58-122">Geometry Shader</span></span> | <span data-ttu-id="e5b58-123">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="e5b58-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e5b58-124">x</span><span class="sxs-lookup"><span data-stu-id="e5b58-124">x</span></span>             | <span data-ttu-id="e5b58-125">x</span><span class="sxs-lookup"><span data-stu-id="e5b58-125">x</span></span>               | <span data-ttu-id="e5b58-126">x</span><span class="sxs-lookup"><span data-stu-id="e5b58-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e5b58-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e5b58-127">Minimum Shader Model</span></span>

<span data-ttu-id="e5b58-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="e5b58-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e5b58-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e5b58-129">Shader Model</span></span>                                              | <span data-ttu-id="e5b58-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e5b58-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e5b58-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="e5b58-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e5b58-132">да</span><span class="sxs-lookup"><span data-stu-id="e5b58-132">yes</span></span>       |
| [<span data-ttu-id="e5b58-133">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="e5b58-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e5b58-134">да</span><span class="sxs-lookup"><span data-stu-id="e5b58-134">yes</span></span>       |
| [<span data-ttu-id="e5b58-135">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="e5b58-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e5b58-136">да</span><span class="sxs-lookup"><span data-stu-id="e5b58-136">yes</span></span>       |
| [<span data-ttu-id="e5b58-137">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5b58-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e5b58-138">Нет</span><span class="sxs-lookup"><span data-stu-id="e5b58-138">no</span></span>        |
| [<span data-ttu-id="e5b58-139">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5b58-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e5b58-140">Нет</span><span class="sxs-lookup"><span data-stu-id="e5b58-140">no</span></span>        |
| [<span data-ttu-id="e5b58-141">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5b58-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e5b58-142">Нет</span><span class="sxs-lookup"><span data-stu-id="e5b58-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e5b58-143">См. также</span><span class="sxs-lookup"><span data-stu-id="e5b58-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5b58-144">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5b58-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





