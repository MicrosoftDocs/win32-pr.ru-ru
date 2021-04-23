---
title: ибфе (SM5-ASM)
description: При наличии диапазона битов в числе сдвигают эти биты в ЛСБ и знак, расширяя диапазон в диапазоне.
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 805d5c1137e25d8b8fa560588b9e876ccc5c8748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784905"
---
# <a name="ibfe-sm5---asm"></a><span data-ttu-id="af6a5-103">ибфе (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="af6a5-103">ibfe (sm5 - asm)</span></span>

<span data-ttu-id="af6a5-104">При наличии диапазона битов в числе сдвигают эти биты в ЛСБ и знак, расширяя диапазон в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="af6a5-104">Given a range of bits in a number, shift those bits to the LSB and sign extend the MSB of the range.</span></span>



| <span data-ttu-id="af6a5-105">ибфе dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле \] , src2 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="af6a5-105">ibfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="af6a5-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="af6a5-106">Item</span></span>                                                            | <span data-ttu-id="af6a5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="af6a5-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="af6a5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="af6a5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="af6a5-109">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="af6a5-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="af6a5-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="af6a5-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="af6a5-111">\[в \] битовой ширине.</span><span class="sxs-lookup"><span data-stu-id="af6a5-111">\[in\] The bitfield width.</span></span><br/>                          |
| <span data-ttu-id="af6a5-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="af6a5-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="af6a5-113">\[в \] битовом смещении.</span><span class="sxs-lookup"><span data-stu-id="af6a5-113">\[in\] The bitfield offset.</span></span><br/>                         |
| <span data-ttu-id="af6a5-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="af6a5-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="af6a5-115">\[в \] поле значение для сдвига.</span><span class="sxs-lookup"><span data-stu-id="af6a5-115">\[in\] The value to shift.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="af6a5-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="af6a5-116">Remarks</span></span>

<span data-ttu-id="af6a5-117">ЛСБ 5 бит src0 (0-31) обеспечивает ширину битовых разрядов.</span><span class="sxs-lookup"><span data-stu-id="af6a5-117">The LSB 5 bits of src0 provide the bitfield width (0-31).</span></span>

<span data-ttu-id="af6a5-118">ЛСБ 5 бит src1 предоставляет смещение битовых разрядов (0-31).</span><span class="sxs-lookup"><span data-stu-id="af6a5-118">The LSB 5 bits of src1 provide the bitfield offset (0-31).</span></span>

<span data-ttu-id="af6a5-119">В следующем примере показано, как использовать эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="af6a5-119">The following example shows how to use this instruction.</span></span>

``` syntax
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ishr dest, dest, 32-width
                }
                else
                {
                    ishr dest, src2, offset
                }
```

<span data-ttu-id="af6a5-120">Используйте эту инструкцию для распаковки целых чисел со знаком или флагов.</span><span class="sxs-lookup"><span data-stu-id="af6a5-120">Use this instruction to unpack signed integers or flags.</span></span>

<span data-ttu-id="af6a5-121">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="af6a5-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="af6a5-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="af6a5-122">Vertex</span></span> | <span data-ttu-id="af6a5-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="af6a5-123">Hull</span></span> | <span data-ttu-id="af6a5-124">Домен</span><span class="sxs-lookup"><span data-stu-id="af6a5-124">Domain</span></span> | <span data-ttu-id="af6a5-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="af6a5-125">Geometry</span></span> | <span data-ttu-id="af6a5-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="af6a5-126">Pixel</span></span> | <span data-ttu-id="af6a5-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="af6a5-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="af6a5-128">X</span><span class="sxs-lookup"><span data-stu-id="af6a5-128">X</span></span>      | <span data-ttu-id="af6a5-129">X</span><span class="sxs-lookup"><span data-stu-id="af6a5-129">X</span></span>    | <span data-ttu-id="af6a5-130">X</span><span class="sxs-lookup"><span data-stu-id="af6a5-130">X</span></span>      | <span data-ttu-id="af6a5-131">X</span><span class="sxs-lookup"><span data-stu-id="af6a5-131">X</span></span>        | <span data-ttu-id="af6a5-132">X</span><span class="sxs-lookup"><span data-stu-id="af6a5-132">X</span></span>     | <span data-ttu-id="af6a5-133">X</span><span class="sxs-lookup"><span data-stu-id="af6a5-133">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="af6a5-134">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="af6a5-134">Minimum Shader Model</span></span>

<span data-ttu-id="af6a5-135">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="af6a5-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="af6a5-136">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="af6a5-136">Shader Model</span></span>                                              | <span data-ttu-id="af6a5-137">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="af6a5-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="af6a5-138">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="af6a5-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="af6a5-139">да</span><span class="sxs-lookup"><span data-stu-id="af6a5-139">yes</span></span>       |
| [<span data-ttu-id="af6a5-140">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="af6a5-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="af6a5-141">Нет</span><span class="sxs-lookup"><span data-stu-id="af6a5-141">no</span></span>        |
| [<span data-ttu-id="af6a5-142">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="af6a5-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="af6a5-143">Нет</span><span class="sxs-lookup"><span data-stu-id="af6a5-143">no</span></span>        |
| [<span data-ttu-id="af6a5-144">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af6a5-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="af6a5-145">Нет</span><span class="sxs-lookup"><span data-stu-id="af6a5-145">no</span></span>        |
| [<span data-ttu-id="af6a5-146">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af6a5-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="af6a5-147">Нет</span><span class="sxs-lookup"><span data-stu-id="af6a5-147">no</span></span>        |
| [<span data-ttu-id="af6a5-148">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af6a5-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="af6a5-149">Нет</span><span class="sxs-lookup"><span data-stu-id="af6a5-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="af6a5-150">См. также</span><span class="sxs-lookup"><span data-stu-id="af6a5-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af6a5-151">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af6a5-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





