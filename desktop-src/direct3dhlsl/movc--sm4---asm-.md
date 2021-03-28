---
title: МОВК (SM4-ASM)
description: Условное перемещение на уровне компонентов. | МОВК (SM4-ASM)
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91aa3116b7bc13102386c57c9b8c63d3534147a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998106"
---
# <a name="movc-sm4---asm"></a><span data-ttu-id="772b6-104">МОВК (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="772b6-104">movc (sm4 - asm)</span></span>

<span data-ttu-id="772b6-105">Условное перемещение на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="772b6-105">Component-wise conditional move.</span></span>



| <span data-ttu-id="772b6-106">МОВК \[ \_ \] \[ . Mask \] , src0 \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src2 \[ \_ ABS \] \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="772b6-106">movc\[\_sat\] dest\[.mask\], src0\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="772b6-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="772b6-107">Item</span></span>                                                            | <span data-ttu-id="772b6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="772b6-108">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772b6-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="772b6-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="772b6-110">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="772b6-110">\[in\] The address of the result of the operation.</span></span> <br/> <span data-ttu-id="772b6-111">Если *src0*, то укажите *dest*  =  *src1* else   =  *src2*</span><span class="sxs-lookup"><span data-stu-id="772b6-111">If *src0*, then *dest* = *src1* else *dest* = *src2*</span></span><br/> |
| <span data-ttu-id="772b6-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="772b6-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="772b6-113">\[в \] компонентах, для которых проверяется условие.</span><span class="sxs-lookup"><span data-stu-id="772b6-113">\[in\] The components on which to test the condition.</span></span><br/>                                                               |
| <span data-ttu-id="772b6-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="772b6-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="772b6-115">\[в \] перемещаемых компонентах.</span><span class="sxs-lookup"><span data-stu-id="772b6-115">\[in\] The components to move.</span></span> <br/>                                                                                     |
| <span data-ttu-id="772b6-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="772b6-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="772b6-117">\[в \] перемещаемых компонентах.</span><span class="sxs-lookup"><span data-stu-id="772b6-117">\[in\] The components to move.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="772b6-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="772b6-118">Remarks</span></span>

<span data-ttu-id="772b6-119">В следующем примере показано, как использовать эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="772b6-119">The following example shows how to use this instruction.</span></span>

``` syntax
                for each component in dest[.mask]
                    if the corresponding component in src0 (POS-swizzle)
                       has any bit set
                    {
                        copy this component (POS-swizzle) from src1 into dest
                    }
                    else
                    {
                        copy this component (POS-swizzle) from src2 into dest
                    }
                endfor
```

<span data-ttu-id="772b6-120">Модификаторы для *src1* и *src2*, кроме свиззле, предполагают, что данные являются плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="772b6-120">The modifiers on *src1* and *src2*, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="772b6-121">Отсутствие модификаторов просто перемещает данные без изменения битов.</span><span class="sxs-lookup"><span data-stu-id="772b6-121">The absence of modifiers just moves data without altering bits.</span></span>

<span data-ttu-id="772b6-122">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="772b6-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="772b6-123">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="772b6-123">Vertex Shader</span></span> | <span data-ttu-id="772b6-124">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="772b6-124">Geometry Shader</span></span> | <span data-ttu-id="772b6-125">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="772b6-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="772b6-126">x</span><span class="sxs-lookup"><span data-stu-id="772b6-126">x</span></span>             | <span data-ttu-id="772b6-127">x</span><span class="sxs-lookup"><span data-stu-id="772b6-127">x</span></span>               | <span data-ttu-id="772b6-128">x</span><span class="sxs-lookup"><span data-stu-id="772b6-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="772b6-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="772b6-129">Minimum Shader Model</span></span>

<span data-ttu-id="772b6-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="772b6-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="772b6-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="772b6-131">Shader Model</span></span>                                              | <span data-ttu-id="772b6-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="772b6-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="772b6-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="772b6-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="772b6-134">да</span><span class="sxs-lookup"><span data-stu-id="772b6-134">yes</span></span>       |
| [<span data-ttu-id="772b6-135">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="772b6-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="772b6-136">да</span><span class="sxs-lookup"><span data-stu-id="772b6-136">yes</span></span>       |
| [<span data-ttu-id="772b6-137">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="772b6-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="772b6-138">да</span><span class="sxs-lookup"><span data-stu-id="772b6-138">yes</span></span>       |
| [<span data-ttu-id="772b6-139">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="772b6-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="772b6-140">Нет</span><span class="sxs-lookup"><span data-stu-id="772b6-140">no</span></span>        |
| [<span data-ttu-id="772b6-141">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="772b6-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="772b6-142">Нет</span><span class="sxs-lookup"><span data-stu-id="772b6-142">no</span></span>        |
| [<span data-ttu-id="772b6-143">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="772b6-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="772b6-144">Нет</span><span class="sxs-lookup"><span data-stu-id="772b6-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="772b6-145">См. также</span><span class="sxs-lookup"><span data-stu-id="772b6-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="772b6-146">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="772b6-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





