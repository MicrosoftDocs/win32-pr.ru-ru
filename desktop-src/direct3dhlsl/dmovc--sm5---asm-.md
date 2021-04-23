---
title: дмовк (SM5-ASM)
description: Условное перемещение на уровне компонентов. | дмовк (SM5-ASM)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e364e6340733c42ae69412db726851329eb2809d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424198"
---
# <a name="dmovc-sm5---asm"></a><span data-ttu-id="0f581-104">дмовк (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0f581-104">dmovc (sm5 - asm)</span></span>

<span data-ttu-id="0f581-105">Условное перемещение на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="0f581-105">Component-wise conditional move.</span></span>



| <span data-ttu-id="0f581-106">дмовк \[ \_ \] \[ . Mask \] , src0 \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src2 \[ \_ ABS \] \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="0f581-106">dmovc\[\_sat\] dest\[.mask\], src0\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\],</span></span> |
|-----------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="0f581-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="0f581-107">Item</span></span>                                                            | <span data-ttu-id="0f581-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0f581-108">Description</span></span>                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f581-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0f581-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0f581-110">\[в \] месте назначения перемещения.</span><span class="sxs-lookup"><span data-stu-id="0f581-110">\[in\] The move destination.</span></span><br/> <span data-ttu-id="0f581-111">Если *src0*, то укажите *dest*  =  *src1* else   =  *src2*.</span><span class="sxs-lookup"><span data-stu-id="0f581-111">If *src0*, then *dest* = *src1* else *dest* = *src2*.</span></span><br/> |
| <span data-ttu-id="0f581-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0f581-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0f581-113">\[в \] компонентах для проверки условия.</span><span class="sxs-lookup"><span data-stu-id="0f581-113">\[in\] The components to test the condition against.</span></span><br/>                                          |
| <span data-ttu-id="0f581-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="0f581-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="0f581-115">\[в \] компонентах для перемещения, если условие истинно.</span><span class="sxs-lookup"><span data-stu-id="0f581-115">\[in\] The components to move if the condition is true.</span></span><br/>                                       |
| <span data-ttu-id="0f581-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="0f581-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="0f581-117">\[в \] компонентах для перемещения, если условие имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="0f581-117">\[in\] The components to move if the condition is false.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="0f581-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="0f581-118">Remarks</span></span>

<span data-ttu-id="0f581-119">В следующем примере показано, как использовать эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="0f581-119">The following example shows how to use this instruction.</span></span>

``` syntax
                if(the dest mask contains .xy)
                {
                    if(the first 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the first double from src1 (post swizzle)
                        into dest.xy
                    }
                    else
                    {
                        copy the first double from src2 (post swizzle)
                        into dest.xy
                    }
                }
                if(the dest mask contains .zw)
                {
                    if(the second 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the second double from src1 (post swizzle)
                        into dest.zw
                    }
                    else
                    {
                        copy the second double from src2 (post swizzle)
                        into dest.zw
                    }
                }
```

<span data-ttu-id="0f581-120">Допустимыми масками для dest являются. XY,. ZW,. ксизв.</span><span class="sxs-lookup"><span data-stu-id="0f581-120">The valid masks for dest are .xy, .zw, .xyzw.</span></span>

<span data-ttu-id="0f581-121">Допустимыми свиззлес для *src0* являются все.</span><span class="sxs-lookup"><span data-stu-id="0f581-121">The valid swizzles for *src0* are anything.</span></span> <span data-ttu-id="0f581-122">Первые два компонента, выполняемые после свиззле, используются для определения 2 32-разрядных значений условий.</span><span class="sxs-lookup"><span data-stu-id="0f581-122">The first two components post-swizzle are used to indentify two 32-bit condition values.</span></span>

<span data-ttu-id="0f581-123">Допустимые свиззлес для *src1* и *src2* , содержащие Double, — это. ксизв,. ксикси,. звкси,. звзв.</span><span class="sxs-lookup"><span data-stu-id="0f581-123">The valid swizzles for *src1* and *src2* containing doubles are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="0f581-124">имеют вид. XY,. ZW и. ксизв.</span><span class="sxs-lookup"><span data-stu-id="0f581-124">are .xy, .zw, and .xyzw.</span></span>

<span data-ttu-id="0f581-125">Следующие сопоставления *src* ниже являются свиззле.</span><span class="sxs-lookup"><span data-stu-id="0f581-125">The following *src* mappings below are post-swizzle:</span></span>

-   <span data-ttu-id="0f581-126">*dest* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="0f581-126">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="0f581-127">*src0* — это 32-разрядный или компонентный vec2 по осям x и y (ZW игнорируется).</span><span class="sxs-lookup"><span data-stu-id="0f581-127">*src0* is a 32bit/component vec2 across x and y (zw ignored).</span></span>
-   <span data-ttu-id="0f581-128">*src1* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="0f581-128">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="0f581-129">*src2* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="0f581-129">*src2* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="0f581-130">Модификаторы для *src1* и *src2*, кроме свиззле, предполагают, что данные являются двойными.</span><span class="sxs-lookup"><span data-stu-id="0f581-130">The modifiers on *src1* and *src2*, other than swizzle, assume the data is double.</span></span> <span data-ttu-id="0f581-131">Отсутствие модификаторов перемещает данные без изменения битов.</span><span class="sxs-lookup"><span data-stu-id="0f581-131">The absence of modifiers moves data without altering bits.</span></span>

<span data-ttu-id="0f581-132">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="0f581-132">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0f581-133">Вершина</span><span class="sxs-lookup"><span data-stu-id="0f581-133">Vertex</span></span> | <span data-ttu-id="0f581-134">Поверхности</span><span class="sxs-lookup"><span data-stu-id="0f581-134">Hull</span></span> | <span data-ttu-id="0f581-135">Домен</span><span class="sxs-lookup"><span data-stu-id="0f581-135">Domain</span></span> | <span data-ttu-id="0f581-136">Геометрия</span><span class="sxs-lookup"><span data-stu-id="0f581-136">Geometry</span></span> | <span data-ttu-id="0f581-137">Пиксель</span><span class="sxs-lookup"><span data-stu-id="0f581-137">Pixel</span></span> | <span data-ttu-id="0f581-138">Вычисления</span><span class="sxs-lookup"><span data-stu-id="0f581-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0f581-139">X</span><span class="sxs-lookup"><span data-stu-id="0f581-139">X</span></span>      | <span data-ttu-id="0f581-140">X</span><span class="sxs-lookup"><span data-stu-id="0f581-140">X</span></span>    | <span data-ttu-id="0f581-141">X</span><span class="sxs-lookup"><span data-stu-id="0f581-141">X</span></span>      | <span data-ttu-id="0f581-142">X</span><span class="sxs-lookup"><span data-stu-id="0f581-142">X</span></span>        | <span data-ttu-id="0f581-143">X</span><span class="sxs-lookup"><span data-stu-id="0f581-143">X</span></span>     | <span data-ttu-id="0f581-144">X</span><span class="sxs-lookup"><span data-stu-id="0f581-144">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0f581-145">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0f581-145">Minimum Shader Model</span></span>

<span data-ttu-id="0f581-146">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="0f581-146">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0f581-147">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0f581-147">Shader Model</span></span>                                              | <span data-ttu-id="0f581-148">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="0f581-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0f581-149">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="0f581-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0f581-150">да</span><span class="sxs-lookup"><span data-stu-id="0f581-150">yes</span></span>       |
| [<span data-ttu-id="0f581-151">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="0f581-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0f581-152">Нет</span><span class="sxs-lookup"><span data-stu-id="0f581-152">no</span></span>        |
| [<span data-ttu-id="0f581-153">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="0f581-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0f581-154">Нет</span><span class="sxs-lookup"><span data-stu-id="0f581-154">no</span></span>        |
| [<span data-ttu-id="0f581-155">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f581-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0f581-156">Нет</span><span class="sxs-lookup"><span data-stu-id="0f581-156">no</span></span>        |
| [<span data-ttu-id="0f581-157">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f581-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0f581-158">Нет</span><span class="sxs-lookup"><span data-stu-id="0f581-158">no</span></span>        |
| [<span data-ttu-id="0f581-159">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f581-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0f581-160">Нет</span><span class="sxs-lookup"><span data-stu-id="0f581-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0f581-161">См. также</span><span class="sxs-lookup"><span data-stu-id="0f581-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f581-162">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f581-162">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





