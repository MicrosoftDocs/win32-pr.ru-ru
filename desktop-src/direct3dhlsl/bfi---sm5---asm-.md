---
title: БФИ (SM5-ASM)
description: Учитывая диапазон битов от ЛСБ числа, поместите это число битов в другое число в любом смещении.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14f8b9f6ef126ec3c6a31bf330dfd89cf0770c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069358"
---
# <a name="bfi-sm5---asm"></a><span data-ttu-id="05ff2-103">БФИ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="05ff2-103">bfi (sm5 - asm)</span></span>

<span data-ttu-id="05ff2-104">Учитывая диапазон битов от ЛСБ числа, поместите это число битов в другое число в любом смещении.</span><span class="sxs-lookup"><span data-stu-id="05ff2-104">Given a bit range from the LSB of a number, place that number of bits in another number at any offset.</span></span>



| <span data-ttu-id="05ff2-105">БФИ dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле \] , src2 \[ . свиззле \] , src3 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="05ff2-105">bfi dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\], src3\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="05ff2-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="05ff2-106">Item</span></span>                                                            | <span data-ttu-id="05ff2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="05ff2-107">Description</span></span>                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="05ff2-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="05ff2-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="05ff2-109">\[в \] адресе результатов.</span><span class="sxs-lookup"><span data-stu-id="05ff2-109">\[in\] The address of the results.</span></span><br/>                       |
| <span data-ttu-id="05ff2-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="05ff2-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="05ff2-111">\[в \] битовой области для получения из *src2*.</span><span class="sxs-lookup"><span data-stu-id="05ff2-111">\[in\] The bitfield width to take from *src2*.</span></span><br/>           |
| <span data-ttu-id="05ff2-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="05ff2-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="05ff2-113">\[в \] битовом смещении для замены битов в *src3*.</span><span class="sxs-lookup"><span data-stu-id="05ff2-113">\[in\] The bitfield offset for replacing bits in *src3*.</span></span><br/> |
| <span data-ttu-id="05ff2-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="05ff2-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="05ff2-115">\[\]число, из которого берутся биты.</span><span class="sxs-lookup"><span data-stu-id="05ff2-115">\[in\] The number the bits are taken from.</span></span> <br/>              |
| <span data-ttu-id="05ff2-116"><span id="src3"></span><span id="SRC3"></span>*src3*</span><span class="sxs-lookup"><span data-stu-id="05ff2-116"><span id="src3"></span><span id="SRC3"></span>*src3*</span></span><br/> | <span data-ttu-id="05ff2-117">\[число, в \] котором заменяются биты.</span><span class="sxs-lookup"><span data-stu-id="05ff2-117">\[in\] The number with bits to be replaced.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="05ff2-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="05ff2-118">Remarks</span></span>

<span data-ttu-id="05ff2-119">ЛСБ 5 разрядов *src0* предоставляют ширину битовой панели (0-31), которую следует взять из *src2*.</span><span class="sxs-lookup"><span data-stu-id="05ff2-119">The LSB 5 bits of *src0* provide the bitfield width (0-31) to take from *src2*.</span></span>

<span data-ttu-id="05ff2-120">ЛСБ 5 бит *src1* предоставляет смещение битовых разрядов (0-31) для начала замены битов числа, считанного из *src3*.</span><span class="sxs-lookup"><span data-stu-id="05ff2-120">The LSB 5 bits of *src1* provide the bitfield offset (0-31) to start replacing bits in the number read from *src3*.</span></span>

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

<span data-ttu-id="05ff2-121">Эта инструкция используется для упаковки целых чисел или флагов.</span><span class="sxs-lookup"><span data-stu-id="05ff2-121">This instruction is used for packing integers or flags.</span></span>

<span data-ttu-id="05ff2-122">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="05ff2-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="05ff2-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="05ff2-123">Vertex</span></span> | <span data-ttu-id="05ff2-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="05ff2-124">Hull</span></span> | <span data-ttu-id="05ff2-125">Домен</span><span class="sxs-lookup"><span data-stu-id="05ff2-125">Domain</span></span> | <span data-ttu-id="05ff2-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="05ff2-126">Geometry</span></span> | <span data-ttu-id="05ff2-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="05ff2-127">Pixel</span></span> | <span data-ttu-id="05ff2-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="05ff2-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="05ff2-129">X</span><span class="sxs-lookup"><span data-stu-id="05ff2-129">X</span></span>      | <span data-ttu-id="05ff2-130">X</span><span class="sxs-lookup"><span data-stu-id="05ff2-130">X</span></span>    | <span data-ttu-id="05ff2-131">X</span><span class="sxs-lookup"><span data-stu-id="05ff2-131">X</span></span>      | <span data-ttu-id="05ff2-132">X</span><span class="sxs-lookup"><span data-stu-id="05ff2-132">X</span></span>        | <span data-ttu-id="05ff2-133">X</span><span class="sxs-lookup"><span data-stu-id="05ff2-133">X</span></span>     | <span data-ttu-id="05ff2-134">X</span><span class="sxs-lookup"><span data-stu-id="05ff2-134">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="05ff2-135">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="05ff2-135">Minimum Shader Model</span></span>

<span data-ttu-id="05ff2-136">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="05ff2-136">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="05ff2-137">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="05ff2-137">Shader Model</span></span>                                              | <span data-ttu-id="05ff2-138">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="05ff2-138">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="05ff2-139">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="05ff2-139">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="05ff2-140">да</span><span class="sxs-lookup"><span data-stu-id="05ff2-140">yes</span></span>       |
| [<span data-ttu-id="05ff2-141">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="05ff2-141">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="05ff2-142">Нет</span><span class="sxs-lookup"><span data-stu-id="05ff2-142">no</span></span>        |
| [<span data-ttu-id="05ff2-143">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="05ff2-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="05ff2-144">Нет</span><span class="sxs-lookup"><span data-stu-id="05ff2-144">no</span></span>        |
| [<span data-ttu-id="05ff2-145">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="05ff2-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="05ff2-146">Нет</span><span class="sxs-lookup"><span data-stu-id="05ff2-146">no</span></span>        |
| [<span data-ttu-id="05ff2-147">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="05ff2-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="05ff2-148">Нет</span><span class="sxs-lookup"><span data-stu-id="05ff2-148">no</span></span>        |
| [<span data-ttu-id="05ff2-149">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="05ff2-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="05ff2-150">Нет</span><span class="sxs-lookup"><span data-stu-id="05ff2-150">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="05ff2-151">См. также</span><span class="sxs-lookup"><span data-stu-id="05ff2-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05ff2-152">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="05ff2-152">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





