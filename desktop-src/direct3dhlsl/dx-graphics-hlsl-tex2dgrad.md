---
title: tex2Dgrad
description: Пример двухмерной текстуры с помощью градиента для выбора уровня MIP. | tex2Dgrad
ms.assetid: a9ab7972-3480-4b37-aa10-c5cf811bdd0e
keywords:
- tex2Dgrad HLSL
topic_type:
- apiref
api_name:
- tex2Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74b20f1cf1f6f5d3b2873f4546dd57ef73b23dbb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986220"
---
# <a name="tex2dgrad"></a><span data-ttu-id="44cbe-105">tex2Dgrad</span><span class="sxs-lookup"><span data-stu-id="44cbe-105">tex2Dgrad</span></span>

<span data-ttu-id="44cbe-106">Пример двухмерной текстуры с помощью градиента для выбора уровня MIP.</span><span class="sxs-lookup"><span data-stu-id="44cbe-106">Samples a 2D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="44cbe-107">RET tex2Dgrad (s, t, DDX, дди)</span><span class="sxs-lookup"><span data-stu-id="44cbe-107">ret tex2Dgrad(s, t, ddx, ddy)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="44cbe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="44cbe-108">Parameters</span></span>



| <span data-ttu-id="44cbe-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="44cbe-109">Item</span></span>                                                         | <span data-ttu-id="44cbe-110">Описание</span><span class="sxs-lookup"><span data-stu-id="44cbe-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="44cbe-111"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="44cbe-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="44cbe-112">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="44cbe-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="44cbe-113"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="44cbe-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="44cbe-114">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="44cbe-114">\[in\] The texture coordinates.</span></span><br/>                                   |
| <span data-ttu-id="44cbe-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="44cbe-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="44cbe-116">\[\]интенсивность изменения геометрии поверхности в направлении x.</span><span class="sxs-lookup"><span data-stu-id="44cbe-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="44cbe-117"><span id="ddy"></span><span id="DDY"></span>*дди*</span><span class="sxs-lookup"><span data-stu-id="44cbe-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="44cbe-118">\[\]интенсивность изменения геометрии поверхности в направлении y.</span><span class="sxs-lookup"><span data-stu-id="44cbe-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="44cbe-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44cbe-119">Return Value</span></span>

<span data-ttu-id="44cbe-120">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="44cbe-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="44cbe-121">Описание типа</span><span class="sxs-lookup"><span data-stu-id="44cbe-121">Type Description</span></span>



| <span data-ttu-id="44cbe-122">Имя</span><span class="sxs-lookup"><span data-stu-id="44cbe-122">Name</span></span> | <span data-ttu-id="44cbe-123">В/Из</span><span class="sxs-lookup"><span data-stu-id="44cbe-123">In/Out</span></span> | [<span data-ttu-id="44cbe-124">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="44cbe-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="44cbe-125">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="44cbe-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="44cbe-126">Размер</span><span class="sxs-lookup"><span data-stu-id="44cbe-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="44cbe-127">s</span><span class="sxs-lookup"><span data-stu-id="44cbe-127">s</span></span>    | <span data-ttu-id="44cbe-128">in</span><span class="sxs-lookup"><span data-stu-id="44cbe-128">in</span></span>     | [<span data-ttu-id="44cbe-129">**объектами**</span><span class="sxs-lookup"><span data-stu-id="44cbe-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="44cbe-130">sampler2D</span><span class="sxs-lookup"><span data-stu-id="44cbe-130">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="44cbe-131">1</span><span class="sxs-lookup"><span data-stu-id="44cbe-131">1</span></span>    |
| <span data-ttu-id="44cbe-132">t</span><span class="sxs-lookup"><span data-stu-id="44cbe-132">t</span></span>    | <span data-ttu-id="44cbe-133">in</span><span class="sxs-lookup"><span data-stu-id="44cbe-133">in</span></span>     | [<span data-ttu-id="44cbe-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="44cbe-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="44cbe-135">**float**</span><span class="sxs-lookup"><span data-stu-id="44cbe-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="44cbe-136">2</span><span class="sxs-lookup"><span data-stu-id="44cbe-136">2</span></span>    |
| <span data-ttu-id="44cbe-137">DDX</span><span class="sxs-lookup"><span data-stu-id="44cbe-137">ddx</span></span>  | <span data-ttu-id="44cbe-138">in</span><span class="sxs-lookup"><span data-stu-id="44cbe-138">in</span></span>     | [<span data-ttu-id="44cbe-139">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="44cbe-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="44cbe-140">**float**</span><span class="sxs-lookup"><span data-stu-id="44cbe-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="44cbe-141">2</span><span class="sxs-lookup"><span data-stu-id="44cbe-141">2</span></span>    |
| <span data-ttu-id="44cbe-142">дди</span><span class="sxs-lookup"><span data-stu-id="44cbe-142">ddy</span></span>  | <span data-ttu-id="44cbe-143">in</span><span class="sxs-lookup"><span data-stu-id="44cbe-143">in</span></span>     | [<span data-ttu-id="44cbe-144">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="44cbe-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="44cbe-145">**float**</span><span class="sxs-lookup"><span data-stu-id="44cbe-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="44cbe-146">2</span><span class="sxs-lookup"><span data-stu-id="44cbe-146">2</span></span>    |
| <span data-ttu-id="44cbe-147">обратно</span><span class="sxs-lookup"><span data-stu-id="44cbe-147">ret</span></span>  | <span data-ttu-id="44cbe-148">out</span><span class="sxs-lookup"><span data-stu-id="44cbe-148">out</span></span>    | [<span data-ttu-id="44cbe-149">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="44cbe-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="44cbe-150">**float**</span><span class="sxs-lookup"><span data-stu-id="44cbe-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="44cbe-151">4</span><span class="sxs-lookup"><span data-stu-id="44cbe-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="44cbe-152">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="44cbe-152">Minimum Shader Model</span></span>

<span data-ttu-id="44cbe-153">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="44cbe-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="44cbe-154">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="44cbe-154">Shader Model</span></span>                                              | <span data-ttu-id="44cbe-155">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="44cbe-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="44cbe-156">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="44cbe-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="44cbe-157">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="44cbe-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="44cbe-158">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44cbe-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="44cbe-159">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="44cbe-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="44cbe-160">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44cbe-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="44cbe-161">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="44cbe-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="44cbe-162">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44cbe-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="44cbe-163">Нет</span><span class="sxs-lookup"><span data-stu-id="44cbe-163">no</span></span>                       |



 

1.  <span data-ttu-id="44cbe-164">Значительный Переупорядочение кода выполняется для перемещения вычислений градиента за пределы управления потоком.</span><span class="sxs-lookup"><span data-stu-id="44cbe-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="44cbe-165">Если для D3DPSHADERCAPS2 \_ 0 установлено значение D3DD3DPSHADERCAPS2 \_ 0 \_ градиентинструктионс, компилятор сопоставляет эту функцию с текслдд.</span><span class="sxs-lookup"><span data-stu-id="44cbe-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="44cbe-166">Примечания</span><span class="sxs-lookup"><span data-stu-id="44cbe-166">Remarks</span></span>

<span data-ttu-id="44cbe-167">Когда управление потоком представлено в шейдере, результат вычисления градиента в заданном пути к ветви неоднозначен, если смежные Пиксели могут находиться в разных путях управления потоком.</span><span class="sxs-lookup"><span data-stu-id="44cbe-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="44cbe-168">Поэтому считается недопустимым использование любой операции шейдера пикселей, запрашивающей вычисление градиента в расположении, находящегося внутри конструкции управления потоком, которая может меняться в пикселях для растрирования данного примитива.</span><span class="sxs-lookup"><span data-stu-id="44cbe-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="44cbe-169">Если любая из сторон инструкции **If** с атрибутом Branch использует функцию градиента, может возникать ошибка компилятора.</span><span class="sxs-lookup"><span data-stu-id="44cbe-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="44cbe-170">См. [инструкции if (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="44cbe-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="44cbe-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44cbe-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44cbe-172">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="44cbe-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

