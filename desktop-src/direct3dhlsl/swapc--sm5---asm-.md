---
title: свапк (SM5-ASM)
description: Выполняет покомпонентную условную замену значений между двумя входными регистрами.
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d2ee674a1cb1067594b0e96c739ff8df73b152
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996911"
---
# <a name="swapc-sm5---asm"></a><span data-ttu-id="3abd7-103">свапк (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="3abd7-103">swapc (sm5 - asm)</span></span>

<span data-ttu-id="3abd7-104">Выполняет покомпонентную условную замену значений между двумя входными регистрами.</span><span class="sxs-lookup"><span data-stu-id="3abd7-104">Performs a component-wise conditional swap of the values between two input registers.</span></span>



| <span data-ttu-id="3abd7-105">свапк dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле \] , src2 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="3abd7-105">swapc dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="3abd7-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="3abd7-106">Item</span></span>                                                               | <span data-ttu-id="3abd7-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3abd7-107">Description</span></span>                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3abd7-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="3abd7-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="3abd7-109">\[\]Регистрация с произвольными непустыми масками записи.</span><span class="sxs-lookup"><span data-stu-id="3abd7-109">\[in\] Register with arbitrary nonempty write masks.</span></span> <span data-ttu-id="3abd7-110">Должно отличаться от *dest1*.</span><span class="sxs-lookup"><span data-stu-id="3abd7-110">Must be different than *dest1*.</span></span><br/> |
| <span data-ttu-id="3abd7-111"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="3abd7-111"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="3abd7-112">\[\]Регистрация с произвольными непустыми масками записи.</span><span class="sxs-lookup"><span data-stu-id="3abd7-112">\[in\] Register with arbitrary nonempty write masks.</span></span> <span data-ttu-id="3abd7-113">Должно отличаться от *dest0*.</span><span class="sxs-lookup"><span data-stu-id="3abd7-113">Must be different than *dest0*.</span></span><br/> |
| <span data-ttu-id="3abd7-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3abd7-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="3abd7-115">\[в \] предоставляет 4 условия.</span><span class="sxs-lookup"><span data-stu-id="3abd7-115">\[in\] Provides 4 conditions.</span></span> <span data-ttu-id="3abd7-116">Ненулевое целочисленное значение означает **true**.</span><span class="sxs-lookup"><span data-stu-id="3abd7-116">A nonzero integer value means **true**.</span></span> <br/>               |
| <span data-ttu-id="3abd7-117"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="3abd7-117"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="3abd7-118">\[в \] одно из значений, которые необходимо поменять местами.</span><span class="sxs-lookup"><span data-stu-id="3abd7-118">\[in\] One of the values to be swapped.</span></span><br/>                                              |
| <span data-ttu-id="3abd7-119"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="3abd7-119"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/>    | <span data-ttu-id="3abd7-120">\[в \] одно из значений, которые необходимо поменять местами.</span><span class="sxs-lookup"><span data-stu-id="3abd7-120">\[in\] One of the values to be swapped.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="3abd7-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="3abd7-121">Remarks</span></span>

<span data-ttu-id="3abd7-122">Кодировка этой инструкции пытается сжать несколько параллельных условных перестановок скалярных значений в регистрах 2 4 компонентов с незначительной гибкостью в порядке расположения пар чисел, участвующих в обмене данными.</span><span class="sxs-lookup"><span data-stu-id="3abd7-122">The encoding of this instruction attempts to compactly express multiple parallel conditional swaps of scalars across two 4-component registers, with minor flexibility in the arrangement of the pairs of numbers involved in swapping.</span></span>

<span data-ttu-id="3abd7-123">Возможность выбора регистра и значения для *src0*, *src1* и *src2* не ограничена каким бы то ни было способом, как [МОВК](movc--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="3abd7-123">The choice of register and value for *src0*, *src1*, and *src2* are unconstrained in any way, like [movc](movc--sm4---asm-.md).</span></span>

<span data-ttu-id="3abd7-124">Семантика этой инструкции может быть описана в эквивалентных операциях с инструкцией **МОВК** .</span><span class="sxs-lookup"><span data-stu-id="3abd7-124">The semantics of this instruction can be described by the equivalent operations with the **movc** instruction.</span></span> <span data-ttu-id="3abd7-125">Наихудший случай показан в следующем примере: Убедитесь, что регистры места назначения не обновляются до конца.</span><span class="sxs-lookup"><span data-stu-id="3abd7-125">The worst case is shown in the following example, making sure destination registers are not updated until the end.</span></span>

``` syntax
                swapc dest0[.mask], 
                      dest1[.mask],
                      src0[.swizzle],
                      src1[.swizzle],
                      src2[.swizzle]

                expands to:

                movc temp[dest0 s mask], 
                     src0[.swizzle], 
                     src2[.swizzle], src1[.swizzle]

                movc dest1[.mask], 
                     src0[.swizzle], 
                     src1[.swizzle], src2[.swizzle]

                mov  dest0.mask, temp
```

<span data-ttu-id="3abd7-126">Можно выбрать способ решения задачи, если он не напрямую.</span><span class="sxs-lookup"><span data-stu-id="3abd7-126">You can choose how to tackle the task, if not directly.</span></span> <span data-ttu-id="3abd7-127">Например, один и тот же результат может быть достигнут последовательностью до 4 простых скалярных условных переключений или двух инструкций векторного **МОВКА** , а также с любыми издержками, чтобы гарантировать, что исходные значения не затертся более ранними операциями в процессе расширения.</span><span class="sxs-lookup"><span data-stu-id="3abd7-127">For example, the same effect can be achieved by a sequence of up to 4 simple scalar conditional swaps, or as above, two vector **movc** instructions, plus any overhead to make sure the source values are not clobbered by earlier operations in the midst of the expansion.</span></span>

<span data-ttu-id="3abd7-128">Используйте эту инструкцию для сортировки.</span><span class="sxs-lookup"><span data-stu-id="3abd7-128">Use this instruction for sorting.</span></span>

<span data-ttu-id="3abd7-129">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="3abd7-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3abd7-130">Вершина</span><span class="sxs-lookup"><span data-stu-id="3abd7-130">Vertex</span></span> | <span data-ttu-id="3abd7-131">Поверхности</span><span class="sxs-lookup"><span data-stu-id="3abd7-131">Hull</span></span> | <span data-ttu-id="3abd7-132">Домен</span><span class="sxs-lookup"><span data-stu-id="3abd7-132">Domain</span></span> | <span data-ttu-id="3abd7-133">Геометрия</span><span class="sxs-lookup"><span data-stu-id="3abd7-133">Geometry</span></span> | <span data-ttu-id="3abd7-134">Пиксель</span><span class="sxs-lookup"><span data-stu-id="3abd7-134">Pixel</span></span> | <span data-ttu-id="3abd7-135">Вычисления</span><span class="sxs-lookup"><span data-stu-id="3abd7-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3abd7-136">X</span><span class="sxs-lookup"><span data-stu-id="3abd7-136">X</span></span>      | <span data-ttu-id="3abd7-137">X</span><span class="sxs-lookup"><span data-stu-id="3abd7-137">X</span></span>    | <span data-ttu-id="3abd7-138">X</span><span class="sxs-lookup"><span data-stu-id="3abd7-138">X</span></span>      | <span data-ttu-id="3abd7-139">X</span><span class="sxs-lookup"><span data-stu-id="3abd7-139">X</span></span>        | <span data-ttu-id="3abd7-140">X</span><span class="sxs-lookup"><span data-stu-id="3abd7-140">X</span></span>     | <span data-ttu-id="3abd7-141">X</span><span class="sxs-lookup"><span data-stu-id="3abd7-141">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3abd7-142">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3abd7-142">Minimum Shader Model</span></span>

<span data-ttu-id="3abd7-143">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="3abd7-143">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="3abd7-144">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3abd7-144">Shader Model</span></span>                                              | <span data-ttu-id="3abd7-145">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="3abd7-145">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3abd7-146">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="3abd7-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3abd7-147">да</span><span class="sxs-lookup"><span data-stu-id="3abd7-147">yes</span></span>       |
| [<span data-ttu-id="3abd7-148">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="3abd7-148">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3abd7-149">Нет</span><span class="sxs-lookup"><span data-stu-id="3abd7-149">no</span></span>        |
| [<span data-ttu-id="3abd7-150">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="3abd7-150">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3abd7-151">Нет</span><span class="sxs-lookup"><span data-stu-id="3abd7-151">no</span></span>        |
| [<span data-ttu-id="3abd7-152">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3abd7-152">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3abd7-153">Нет</span><span class="sxs-lookup"><span data-stu-id="3abd7-153">no</span></span>        |
| [<span data-ttu-id="3abd7-154">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3abd7-154">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3abd7-155">Нет</span><span class="sxs-lookup"><span data-stu-id="3abd7-155">no</span></span>        |
| [<span data-ttu-id="3abd7-156">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3abd7-156">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3abd7-157">Нет</span><span class="sxs-lookup"><span data-stu-id="3abd7-157">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3abd7-158">См. также</span><span class="sxs-lookup"><span data-stu-id="3abd7-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3abd7-159">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3abd7-159">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





