---
title: индикатор
description: Возвращает вектор коэффициента освещения.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- освещенный HLSL
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dbf6f1e53218355ba1ee9ccf58dac6176007218
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890664"
---
# <a name="lit"></a><span data-ttu-id="199d5-104">индикатор</span><span class="sxs-lookup"><span data-stu-id="199d5-104">lit</span></span>

<span data-ttu-id="199d5-105">Возвращает вектор коэффициента освещения.</span><span class="sxs-lookup"><span data-stu-id="199d5-105">Returns a lighting coefficient vector.</span></span>



| <span data-ttu-id="199d5-106">*RET* -горит (*n \_ точек \_ l*, *n \_ точек \_ h*, *m*)</span><span class="sxs-lookup"><span data-stu-id="199d5-106">*ret* lit(*n\_dot\_l*, *n\_dot\_h*, *m*)</span></span> |
|------------------------------------------|



 

<span data-ttu-id="199d5-107">Эта функция возвращает вектор коэффициента освещения (внешние, диффузные, блики, 1), где:</span><span class="sxs-lookup"><span data-stu-id="199d5-107">This function returns a lighting coefficient vector (ambient, diffuse, specular, 1) where:</span></span>

-   <span data-ttu-id="199d5-108">окружение = 1</span><span class="sxs-lookup"><span data-stu-id="199d5-108">ambient = 1</span></span>
-   <span data-ttu-id="199d5-109">Диффузная = n · l < 0?</span><span class="sxs-lookup"><span data-stu-id="199d5-109">diffuse = n · l < 0 ?</span></span> <span data-ttu-id="199d5-110">0: n · н</span><span class="sxs-lookup"><span data-stu-id="199d5-110">0 : n · l</span></span>
-   <span data-ttu-id="199d5-111">отражающий = n · l < 0 \| \| n · h < 0?</span><span class="sxs-lookup"><span data-stu-id="199d5-111">specular = n · l < 0 \|\| n · h < 0 ?</span></span> <span data-ttu-id="199d5-112">0: (n · h) ^ m</span><span class="sxs-lookup"><span data-stu-id="199d5-112">0 : (n · h) ^ m</span></span>

<span data-ttu-id="199d5-113">Где Vector n является нормальным вектором, l — это направление падения, а h — половина вектора.</span><span class="sxs-lookup"><span data-stu-id="199d5-113">Where the vector n is the normal vector, l is the direction to light and h is the half vector.</span></span>

## <a name="parameters"></a><span data-ttu-id="199d5-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="199d5-114">Parameters</span></span>



| <span data-ttu-id="199d5-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="199d5-115">Item</span></span>                                                                       | <span data-ttu-id="199d5-116">Описание</span><span class="sxs-lookup"><span data-stu-id="199d5-116">Description</span></span>                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="199d5-117"><span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ точек \_ l*</span><span class="sxs-lookup"><span data-stu-id="199d5-117"><span id="n_dot_l"></span><span id="N_DOT_L"></span>*n\_dot\_l*</span></span><br/> | <span data-ttu-id="199d5-118">\[в виде \] скалярного произведения нормализованной поверхности и светлой вектор.</span><span class="sxs-lookup"><span data-stu-id="199d5-118">\[in\] The dot product of the normalized surface normal and the light vector.</span></span><br/> |
| <span data-ttu-id="199d5-119"><span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ точек \_ h*</span><span class="sxs-lookup"><span data-stu-id="199d5-119"><span id="n_dot_h"></span><span id="N_DOT_H"></span>*n\_dot\_h*</span></span><br/> | <span data-ttu-id="199d5-120">\[в \] скалярном продукте для вектора половины углов и нормали к поверхности.</span><span class="sxs-lookup"><span data-stu-id="199d5-120">\[in\] The dot product of the half-angle vector and the surface normal.</span></span><br/>       |
| <span data-ttu-id="199d5-121"><span id="m"></span><span id="M"></span>*Пн*</span><span class="sxs-lookup"><span data-stu-id="199d5-121"><span id="m"></span><span id="M"></span>*m*</span></span><br/>                     | <span data-ttu-id="199d5-122">\[в \] отраженном экспоненте.</span><span class="sxs-lookup"><span data-stu-id="199d5-122">\[in\] A specular exponent.</span></span><br/>                                                   |



 

## <a name="return-value"></a><span data-ttu-id="199d5-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="199d5-123">Return Value</span></span>

<span data-ttu-id="199d5-124">Вектор коэффициента освещения.</span><span class="sxs-lookup"><span data-stu-id="199d5-124">The lighting coefficient vector.</span></span>

## <a name="type-description"></a><span data-ttu-id="199d5-125">Описание типа</span><span class="sxs-lookup"><span data-stu-id="199d5-125">Type Description</span></span>



| <span data-ttu-id="199d5-126">Имя</span><span class="sxs-lookup"><span data-stu-id="199d5-126">Name</span></span>        | [<span data-ttu-id="199d5-127">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="199d5-127">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="199d5-128">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="199d5-128">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="199d5-129">Размер</span><span class="sxs-lookup"><span data-stu-id="199d5-129">Size</span></span> |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="199d5-130">*n \_ точек \_ l*</span><span class="sxs-lookup"><span data-stu-id="199d5-130">*n\_dot\_l*</span></span> | [<span data-ttu-id="199d5-131">**скаляр**</span><span class="sxs-lookup"><span data-stu-id="199d5-131">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="199d5-132">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="199d5-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="199d5-133">1</span><span class="sxs-lookup"><span data-stu-id="199d5-133">1</span></span>    |
| <span data-ttu-id="199d5-134">*n \_ точек \_ h*</span><span class="sxs-lookup"><span data-stu-id="199d5-134">*n\_dot\_h*</span></span> | [<span data-ttu-id="199d5-135">**скаляр**</span><span class="sxs-lookup"><span data-stu-id="199d5-135">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="199d5-136">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="199d5-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="199d5-137">1</span><span class="sxs-lookup"><span data-stu-id="199d5-137">1</span></span>    |
| <span data-ttu-id="199d5-138">*m*</span><span class="sxs-lookup"><span data-stu-id="199d5-138">*m*</span></span>         | [<span data-ttu-id="199d5-139">**скаляр**</span><span class="sxs-lookup"><span data-stu-id="199d5-139">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="199d5-140">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="199d5-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="199d5-141">1</span><span class="sxs-lookup"><span data-stu-id="199d5-141">1</span></span>    |
| <span data-ttu-id="199d5-142">*обратно*</span><span class="sxs-lookup"><span data-stu-id="199d5-142">*ret*</span></span>       | [<span data-ttu-id="199d5-143">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="199d5-143">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="199d5-144">**float**</span><span class="sxs-lookup"><span data-stu-id="199d5-144">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="199d5-145">4</span><span class="sxs-lookup"><span data-stu-id="199d5-145">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="199d5-146">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="199d5-146">Minimum Shader Model</span></span>

<span data-ttu-id="199d5-147">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="199d5-147">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="199d5-148">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="199d5-148">Shader Model</span></span>                                                                       | <span data-ttu-id="199d5-149">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="199d5-149">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="199d5-150">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="199d5-150">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="199d5-151">да</span><span class="sxs-lookup"><span data-stu-id="199d5-151">yes</span></span>                 |
| [<span data-ttu-id="199d5-152">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="199d5-152">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="199d5-153">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="199d5-153">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="199d5-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="199d5-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="199d5-155">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="199d5-155">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

