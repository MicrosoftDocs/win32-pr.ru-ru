---
title: убфе (SM5-ASM)
description: При наличии диапазона битов в числе сдвигают эти биты в ЛСБ и устанавливает оставшиеся биты в 0.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ebbe853ec1b53b452f32d79c9c2ec120e826b8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103890004"
---
# <a name="ubfe-sm5---asm"></a><span data-ttu-id="8cf45-103">убфе (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8cf45-103">ubfe (sm5 - asm)</span></span>

<span data-ttu-id="8cf45-104">При наличии диапазона битов в числе сдвигают эти биты в ЛСБ и устанавливает оставшиеся биты в 0.</span><span class="sxs-lookup"><span data-stu-id="8cf45-104">Given a range of bits in a number, shift those bits to the LSB and set remaining bits to 0.</span></span>



| <span data-ttu-id="8cf45-105">убфе dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле \] , src2 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="8cf45-105">ubfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="8cf45-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="8cf45-106">Item</span></span>                                                            | <span data-ttu-id="8cf45-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8cf45-107">Description</span></span>                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="8cf45-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="8cf45-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="8cf45-109">\[в \] содержит результаты выполнения инструкции.</span><span class="sxs-lookup"><span data-stu-id="8cf45-109">\[in\] Contains the results of the instruction.</span></span><br/>                     |
| <span data-ttu-id="8cf45-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8cf45-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="8cf45-111">\[в \] ЛСБ 5 бит обеспечивает ширину битовых разрядов (0-31).</span><span class="sxs-lookup"><span data-stu-id="8cf45-111">\[in\] The LSB 5 bits provide the bitfield width (0-31).</span></span><br/>            |
| <span data-ttu-id="8cf45-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="8cf45-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="8cf45-113">\[в \] ЛСБ 5 бит *src1* предоставляет смещение битового смещения (0-31).</span><span class="sxs-lookup"><span data-stu-id="8cf45-113">\[in\] The LSB 5 bits of *src1* provide the bitfield offset (0-31).</span></span><br/> |
| <span data-ttu-id="8cf45-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="8cf45-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="8cf45-115">\[\]число для сдвига.</span><span class="sxs-lookup"><span data-stu-id="8cf45-115">\[in\] The number to shift.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="8cf45-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="8cf45-116">Remarks</span></span>

``` syntax
 
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ushr dest, dest, 32-width
                }
                else
                {
                    ushr dest, src2, offset
                }
```

<span data-ttu-id="8cf45-117">Используйте эту инструкцию для распаковки целых чисел без знака или флагов.</span><span class="sxs-lookup"><span data-stu-id="8cf45-117">Use this instruction to unpack unsigned integers or flags.</span></span>

<span data-ttu-id="8cf45-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="8cf45-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8cf45-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="8cf45-119">Vertex</span></span> | <span data-ttu-id="8cf45-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="8cf45-120">Hull</span></span> | <span data-ttu-id="8cf45-121">Домен</span><span class="sxs-lookup"><span data-stu-id="8cf45-121">Domain</span></span> | <span data-ttu-id="8cf45-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="8cf45-122">Geometry</span></span> | <span data-ttu-id="8cf45-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="8cf45-123">Pixel</span></span> | <span data-ttu-id="8cf45-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="8cf45-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8cf45-125">X</span><span class="sxs-lookup"><span data-stu-id="8cf45-125">X</span></span>      | <span data-ttu-id="8cf45-126">X</span><span class="sxs-lookup"><span data-stu-id="8cf45-126">X</span></span>    | <span data-ttu-id="8cf45-127">X</span><span class="sxs-lookup"><span data-stu-id="8cf45-127">X</span></span>      | <span data-ttu-id="8cf45-128">X</span><span class="sxs-lookup"><span data-stu-id="8cf45-128">X</span></span>        | <span data-ttu-id="8cf45-129">X</span><span class="sxs-lookup"><span data-stu-id="8cf45-129">X</span></span>     | <span data-ttu-id="8cf45-130">X</span><span class="sxs-lookup"><span data-stu-id="8cf45-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8cf45-131">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8cf45-131">Minimum Shader Model</span></span>

<span data-ttu-id="8cf45-132">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="8cf45-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8cf45-133">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8cf45-133">Shader Model</span></span>                                              | <span data-ttu-id="8cf45-134">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8cf45-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8cf45-135">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="8cf45-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8cf45-136">да</span><span class="sxs-lookup"><span data-stu-id="8cf45-136">yes</span></span>       |
| [<span data-ttu-id="8cf45-137">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="8cf45-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8cf45-138">Нет</span><span class="sxs-lookup"><span data-stu-id="8cf45-138">no</span></span>        |
| [<span data-ttu-id="8cf45-139">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="8cf45-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8cf45-140">Нет</span><span class="sxs-lookup"><span data-stu-id="8cf45-140">no</span></span>        |
| [<span data-ttu-id="8cf45-141">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8cf45-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8cf45-142">Нет</span><span class="sxs-lookup"><span data-stu-id="8cf45-142">no</span></span>        |
| [<span data-ttu-id="8cf45-143">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8cf45-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8cf45-144">Нет</span><span class="sxs-lookup"><span data-stu-id="8cf45-144">no</span></span>        |
| [<span data-ttu-id="8cf45-145">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8cf45-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8cf45-146">Нет</span><span class="sxs-lookup"><span data-stu-id="8cf45-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8cf45-147">См. также</span><span class="sxs-lookup"><span data-stu-id="8cf45-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cf45-148">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8cf45-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





