---
title: Текскубе (Справочник по HLSL) — выберите уровень MIP
description: Выберет текстуру Куба с помощью градиента, чтобы выбрать уровень MIP. | Текскубе (Справочник по HLSL)
ms.assetid: 5615f48b-eb0a-4de7-a441-51ec3cecf6fd
keywords:
- Текскубе HLSL
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6286b4fedb94b9fd5c84c76171e9478f06e16ce4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987296"
---
# <a name="texcube-hlsl-reference---select-the-mip-level"></a><span data-ttu-id="c6d7d-105">Текскубе (Справочник по HLSL) — выберите уровень MIP</span><span class="sxs-lookup"><span data-stu-id="c6d7d-105">texCUBE (HLSL reference) - Select the mip level</span></span>

<span data-ttu-id="c6d7d-106">Выберет текстуру Куба с помощью градиента, чтобы выбрать уровень MIP.</span><span class="sxs-lookup"><span data-stu-id="c6d7d-106">Samples a cube texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="c6d7d-107">RET Текскубе (s, t, DDX, дди)</span><span class="sxs-lookup"><span data-stu-id="c6d7d-107">ret texCUBE(s, t, ddx, ddy)</span></span> |
|-----------------------------|



 

## <a name="parameters"></a><span data-ttu-id="c6d7d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6d7d-108">Parameters</span></span>



| <span data-ttu-id="c6d7d-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="c6d7d-109">Item</span></span>                                                         | <span data-ttu-id="c6d7d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c6d7d-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c6d7d-111"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="c6d7d-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="c6d7d-112">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="c6d7d-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="c6d7d-113"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="c6d7d-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="c6d7d-114">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="c6d7d-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="c6d7d-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="c6d7d-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="c6d7d-116">\[\]интенсивность изменения геометрии поверхности в направлении x.</span><span class="sxs-lookup"><span data-stu-id="c6d7d-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="c6d7d-117"><span id="ddy"></span><span id="DDY"></span>*дди*</span><span class="sxs-lookup"><span data-stu-id="c6d7d-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="c6d7d-118">\[\]интенсивность изменения геометрии поверхности в направлении y.</span><span class="sxs-lookup"><span data-stu-id="c6d7d-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c6d7d-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6d7d-119">Return Value</span></span>

<span data-ttu-id="c6d7d-120">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="c6d7d-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="c6d7d-121">Описание типа</span><span class="sxs-lookup"><span data-stu-id="c6d7d-121">Type Description</span></span>



| <span data-ttu-id="c6d7d-122">Имя</span><span class="sxs-lookup"><span data-stu-id="c6d7d-122">Name</span></span> | <span data-ttu-id="c6d7d-123">В/Из</span><span class="sxs-lookup"><span data-stu-id="c6d7d-123">In/Out</span></span> | [<span data-ttu-id="c6d7d-124">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="c6d7d-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="c6d7d-125">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="c6d7d-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c6d7d-126">Размер</span><span class="sxs-lookup"><span data-stu-id="c6d7d-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="c6d7d-127">s</span><span class="sxs-lookup"><span data-stu-id="c6d7d-127">s</span></span>    | <span data-ttu-id="c6d7d-128">in</span><span class="sxs-lookup"><span data-stu-id="c6d7d-128">in</span></span>     | [<span data-ttu-id="c6d7d-129">**объектами**</span><span class="sxs-lookup"><span data-stu-id="c6d7d-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c6d7d-130">самплеркубе</span><span class="sxs-lookup"><span data-stu-id="c6d7d-130">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="c6d7d-131">1</span><span class="sxs-lookup"><span data-stu-id="c6d7d-131">1</span></span>    |
| <span data-ttu-id="c6d7d-132">t</span><span class="sxs-lookup"><span data-stu-id="c6d7d-132">t</span></span>    | <span data-ttu-id="c6d7d-133">in</span><span class="sxs-lookup"><span data-stu-id="c6d7d-133">in</span></span>     | [<span data-ttu-id="c6d7d-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="c6d7d-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c6d7d-135">**float**</span><span class="sxs-lookup"><span data-stu-id="c6d7d-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c6d7d-136">3</span><span class="sxs-lookup"><span data-stu-id="c6d7d-136">3</span></span>    |
| <span data-ttu-id="c6d7d-137">DDX</span><span class="sxs-lookup"><span data-stu-id="c6d7d-137">ddx</span></span>  | <span data-ttu-id="c6d7d-138">in</span><span class="sxs-lookup"><span data-stu-id="c6d7d-138">in</span></span>     | [<span data-ttu-id="c6d7d-139">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="c6d7d-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c6d7d-140">**float**</span><span class="sxs-lookup"><span data-stu-id="c6d7d-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c6d7d-141">3</span><span class="sxs-lookup"><span data-stu-id="c6d7d-141">3</span></span>    |
| <span data-ttu-id="c6d7d-142">дди</span><span class="sxs-lookup"><span data-stu-id="c6d7d-142">ddy</span></span>  | <span data-ttu-id="c6d7d-143">in</span><span class="sxs-lookup"><span data-stu-id="c6d7d-143">in</span></span>     | [<span data-ttu-id="c6d7d-144">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="c6d7d-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c6d7d-145">**float**</span><span class="sxs-lookup"><span data-stu-id="c6d7d-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c6d7d-146">3</span><span class="sxs-lookup"><span data-stu-id="c6d7d-146">3</span></span>    |
| <span data-ttu-id="c6d7d-147">обратно</span><span class="sxs-lookup"><span data-stu-id="c6d7d-147">ret</span></span>  | <span data-ttu-id="c6d7d-148">out</span><span class="sxs-lookup"><span data-stu-id="c6d7d-148">out</span></span>    | [<span data-ttu-id="c6d7d-149">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="c6d7d-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c6d7d-150">**float**</span><span class="sxs-lookup"><span data-stu-id="c6d7d-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c6d7d-151">4</span><span class="sxs-lookup"><span data-stu-id="c6d7d-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c6d7d-152">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c6d7d-152">Minimum Shader Model</span></span>

<span data-ttu-id="c6d7d-153">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="c6d7d-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c6d7d-154">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c6d7d-154">Shader Model</span></span>                                              | <span data-ttu-id="c6d7d-155">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="c6d7d-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="c6d7d-156">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="c6d7d-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c6d7d-157">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="c6d7d-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="c6d7d-158">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6d7d-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c6d7d-159">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="c6d7d-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="c6d7d-160">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6d7d-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c6d7d-161">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="c6d7d-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="c6d7d-162">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6d7d-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c6d7d-163">Нет</span><span class="sxs-lookup"><span data-stu-id="c6d7d-163">no</span></span>                       |



 

1.  <span data-ttu-id="c6d7d-164">Значительный Переупорядочение кода выполняется для перемещения вычислений градиента за пределы управления потоком.</span><span class="sxs-lookup"><span data-stu-id="c6d7d-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="c6d7d-165">Если для D3DPSHADERCAPS2 \_ 0 установлено значение D3DD3DPSHADERCAPS2 \_ 0 \_ градиентинструктионс, компилятор сопоставляет эту функцию с текслдд.</span><span class="sxs-lookup"><span data-stu-id="c6d7d-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6d7d-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6d7d-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d7d-167">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c6d7d-167">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

