---
title: tex3D (Справочник по HLSL) — выберите уровень MIP
description: Пример трехмерной текстуры с помощью градиента для выбора уровня MIP. | tex3D (Справочник по HLSL)
ms.assetid: b48a6791-61b7-4a13-9357-923910515164
keywords:
- tex3D HLSL
topic_type:
- apiref
api_name:
- tex3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 965c9229d4d54fafdb2da9a84119365075a3f903
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104273993"
---
# <a name="tex3d-hlsl-reference---select-the-mip-level"></a><span data-ttu-id="f86cf-105">tex3D (Справочник по HLSL) — выберите уровень MIP</span><span class="sxs-lookup"><span data-stu-id="f86cf-105">tex3D (HLSL reference) - Select the mip level</span></span>

<span data-ttu-id="f86cf-106">Пример трехмерной текстуры с помощью градиента для выбора уровня MIP.</span><span class="sxs-lookup"><span data-stu-id="f86cf-106">Samples a 3D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="f86cf-107">RET tex3D (s, t, DDX, дди)</span><span class="sxs-lookup"><span data-stu-id="f86cf-107">ret tex3D(s, t, ddx, ddy)</span></span> |
|---------------------------|



 

## <a name="parameters"></a><span data-ttu-id="f86cf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f86cf-108">Parameters</span></span>



| <span data-ttu-id="f86cf-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="f86cf-109">Item</span></span>                                                         | <span data-ttu-id="f86cf-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f86cf-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f86cf-111"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="f86cf-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="f86cf-112">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="f86cf-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="f86cf-113"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="f86cf-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="f86cf-114">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="f86cf-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="f86cf-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="f86cf-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="f86cf-116">\[\]интенсивность изменения геометрии поверхности в направлении x.</span><span class="sxs-lookup"><span data-stu-id="f86cf-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="f86cf-117"><span id="ddy"></span><span id="DDY"></span>*дди*</span><span class="sxs-lookup"><span data-stu-id="f86cf-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="f86cf-118">\[\]интенсивность изменения геометрии поверхности в направлении y.</span><span class="sxs-lookup"><span data-stu-id="f86cf-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="f86cf-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f86cf-119">Return Value</span></span>

<span data-ttu-id="f86cf-120">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="f86cf-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="f86cf-121">Описание типа</span><span class="sxs-lookup"><span data-stu-id="f86cf-121">Type Description</span></span>



| <span data-ttu-id="f86cf-122">Имя</span><span class="sxs-lookup"><span data-stu-id="f86cf-122">Name</span></span> | <span data-ttu-id="f86cf-123">В/Из</span><span class="sxs-lookup"><span data-stu-id="f86cf-123">In/Out</span></span> | [<span data-ttu-id="f86cf-124">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="f86cf-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="f86cf-125">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="f86cf-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f86cf-126">Размер</span><span class="sxs-lookup"><span data-stu-id="f86cf-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="f86cf-127">s</span><span class="sxs-lookup"><span data-stu-id="f86cf-127">s</span></span>    | <span data-ttu-id="f86cf-128">in</span><span class="sxs-lookup"><span data-stu-id="f86cf-128">in</span></span>     | [<span data-ttu-id="f86cf-129">**объектами**</span><span class="sxs-lookup"><span data-stu-id="f86cf-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f86cf-130">sampler3D</span><span class="sxs-lookup"><span data-stu-id="f86cf-130">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="f86cf-131">1</span><span class="sxs-lookup"><span data-stu-id="f86cf-131">1</span></span>    |
| <span data-ttu-id="f86cf-132">t</span><span class="sxs-lookup"><span data-stu-id="f86cf-132">t</span></span>    | <span data-ttu-id="f86cf-133">in</span><span class="sxs-lookup"><span data-stu-id="f86cf-133">in</span></span>     | [<span data-ttu-id="f86cf-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="f86cf-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f86cf-135">**float**</span><span class="sxs-lookup"><span data-stu-id="f86cf-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f86cf-136">3</span><span class="sxs-lookup"><span data-stu-id="f86cf-136">3</span></span>    |
| <span data-ttu-id="f86cf-137">DDX</span><span class="sxs-lookup"><span data-stu-id="f86cf-137">ddx</span></span>  | <span data-ttu-id="f86cf-138">in</span><span class="sxs-lookup"><span data-stu-id="f86cf-138">in</span></span>     | [<span data-ttu-id="f86cf-139">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="f86cf-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f86cf-140">**float**</span><span class="sxs-lookup"><span data-stu-id="f86cf-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f86cf-141">3</span><span class="sxs-lookup"><span data-stu-id="f86cf-141">3</span></span>    |
| <span data-ttu-id="f86cf-142">дди</span><span class="sxs-lookup"><span data-stu-id="f86cf-142">ddy</span></span>  | <span data-ttu-id="f86cf-143">in</span><span class="sxs-lookup"><span data-stu-id="f86cf-143">in</span></span>     | [<span data-ttu-id="f86cf-144">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="f86cf-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f86cf-145">**float**</span><span class="sxs-lookup"><span data-stu-id="f86cf-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f86cf-146">3</span><span class="sxs-lookup"><span data-stu-id="f86cf-146">3</span></span>    |
| <span data-ttu-id="f86cf-147">обратно</span><span class="sxs-lookup"><span data-stu-id="f86cf-147">ret</span></span>  | <span data-ttu-id="f86cf-148">out</span><span class="sxs-lookup"><span data-stu-id="f86cf-148">out</span></span>    | [<span data-ttu-id="f86cf-149">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="f86cf-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f86cf-150">**float**</span><span class="sxs-lookup"><span data-stu-id="f86cf-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f86cf-151">4</span><span class="sxs-lookup"><span data-stu-id="f86cf-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f86cf-152">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f86cf-152">Minimum Shader Model</span></span>

<span data-ttu-id="f86cf-153">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="f86cf-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f86cf-154">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f86cf-154">Shader Model</span></span>                                              | <span data-ttu-id="f86cf-155">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="f86cf-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="f86cf-156">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="f86cf-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f86cf-157">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="f86cf-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="f86cf-158">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f86cf-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f86cf-159">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="f86cf-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="f86cf-160">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f86cf-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f86cf-161">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="f86cf-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="f86cf-162">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f86cf-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f86cf-163">Нет</span><span class="sxs-lookup"><span data-stu-id="f86cf-163">no</span></span>                       |



 

1.  <span data-ttu-id="f86cf-164">Значительный Переупорядочение кода выполняется для перемещения вычислений градиента за пределы управления потоком.</span><span class="sxs-lookup"><span data-stu-id="f86cf-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="f86cf-165">Если для D3DPSHADERCAPS2 \_ 0 установлено значение D3DD3DPSHADERCAPS2 \_ 0 \_ градиентинструктионс, компилятор сопоставляет эту функцию с текслдд.</span><span class="sxs-lookup"><span data-stu-id="f86cf-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="f86cf-166">Примечания</span><span class="sxs-lookup"><span data-stu-id="f86cf-166">Remarks</span></span>

<span data-ttu-id="f86cf-167">Когда управление потоком представлено в шейдере, результат вычисления градиента в заданном пути к ветви неоднозначен, если смежные Пиксели могут находиться в разных путях управления потоком.</span><span class="sxs-lookup"><span data-stu-id="f86cf-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="f86cf-168">Поэтому считается недопустимым использование любой операции шейдера пикселей, запрашивающей вычисление градиента в расположении, находящегося внутри конструкции управления потоком, которая может меняться в пикселях для растрирования данного примитива.</span><span class="sxs-lookup"><span data-stu-id="f86cf-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="f86cf-169">Если любая из сторон инструкции **If** с атрибутом Branch использует функцию градиента, может возникать ошибка компилятора.</span><span class="sxs-lookup"><span data-stu-id="f86cf-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="f86cf-170">См. [инструкции if (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="f86cf-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f86cf-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f86cf-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f86cf-172">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="f86cf-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

