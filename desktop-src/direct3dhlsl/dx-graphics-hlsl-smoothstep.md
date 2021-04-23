---
title: смусстеп
description: Возвращает гладкую Хермите интерполяцию между 0 и 1, если x находится в диапазоне от \ min, Max \.
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- смусстеп HLSL
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104983996"
---
# <a name="smoothstep"></a><span data-ttu-id="d18c2-104">смусстеп</span><span class="sxs-lookup"><span data-stu-id="d18c2-104">smoothstep</span></span>

<span data-ttu-id="d18c2-105">Возвращает гладкую Хермите интерполяцию между 0 и 1, если *x* находится в диапазоне \[ *min*, *Max* \] .</span><span class="sxs-lookup"><span data-stu-id="d18c2-105">Returns a smooth Hermite interpolation between 0 and 1, if *x* is in the range \[*min*, *max*\].</span></span>



| <span data-ttu-id="d18c2-106">*RET* смусстеп (*min*, *Max*, *x*)</span><span class="sxs-lookup"><span data-stu-id="d18c2-106">*ret* smoothstep(*min*, *max*, *x*)</span></span> |
|-------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d18c2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d18c2-107">Parameters</span></span>



| <span data-ttu-id="d18c2-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="d18c2-108">Item</span></span>                                                         | <span data-ttu-id="d18c2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d18c2-109">Description</span></span>                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d18c2-110"><span id="min"></span><span id="MIN"></span>*минимум*</span><span class="sxs-lookup"><span data-stu-id="d18c2-110"><span id="min"></span><span id="MIN"></span>*min*</span></span><br/> | <span data-ttu-id="d18c2-111">\[в \] минимальном диапазоне параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="d18c2-111">\[in\] The minimum range of the *x* parameter.</span></span><br/> |
| <span data-ttu-id="d18c2-112"><span id="max"></span><span id="MAX"></span>*максимальной*</span><span class="sxs-lookup"><span data-stu-id="d18c2-112"><span id="max"></span><span id="MAX"></span>*max*</span></span><br/> | <span data-ttu-id="d18c2-113">\[в \] максимальном диапазоне параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="d18c2-113">\[in\] The maximum range of the *x* parameter.</span></span><br/> |
| <span data-ttu-id="d18c2-114"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="d18c2-114"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="d18c2-115">\[в \] указанном значении для интерполяции.</span><span class="sxs-lookup"><span data-stu-id="d18c2-115">\[in\] The specified value to be interpolated.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d18c2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d18c2-116">Return Value</span></span>

<span data-ttu-id="d18c2-117">Возвращает 0, если *x* меньше *min*; 1, если *x* больше *максимального*; в противном случае значение от 0 до 1, если *x* , находится в диапазоне \[ *min*, *Max* \] .</span><span class="sxs-lookup"><span data-stu-id="d18c2-117">Returns 0 if *x* is less than *min*; 1 if *x* is greater than *max*; otherwise, a value between 0 and 1 if *x* is in the range \[*min*, *max*\].</span></span>

## <a name="remarks"></a><span data-ttu-id="d18c2-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="d18c2-118">Remarks</span></span>

<span data-ttu-id="d18c2-119">Используйте встроенную функцию **смусстеп** HLSL, чтобы создать плавный переход между двумя значениями.</span><span class="sxs-lookup"><span data-stu-id="d18c2-119">Use the **smoothstep** HLSL intrinsic function to create a smooth transition between two values.</span></span> <span data-ttu-id="d18c2-120">Например, эту функцию можно использовать для плавного смешения двух цветов.</span><span class="sxs-lookup"><span data-stu-id="d18c2-120">For example, you can use this function to blend two colors smoothly.</span></span>

## <a name="type-description"></a><span data-ttu-id="d18c2-121">Описание типа</span><span class="sxs-lookup"><span data-stu-id="d18c2-121">Type Description</span></span>



| <span data-ttu-id="d18c2-122">Имя</span><span class="sxs-lookup"><span data-stu-id="d18c2-122">Name</span></span>  | [<span data-ttu-id="d18c2-123">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="d18c2-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d18c2-124">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="d18c2-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d18c2-125">Размер</span><span class="sxs-lookup"><span data-stu-id="d18c2-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d18c2-126">*x*</span><span class="sxs-lookup"><span data-stu-id="d18c2-126">*x*</span></span>   | <span data-ttu-id="d18c2-127">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="d18c2-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="d18c2-128">**float**</span><span class="sxs-lookup"><span data-stu-id="d18c2-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d18c2-129">any</span><span class="sxs-lookup"><span data-stu-id="d18c2-129">any</span></span>                            |
| <span data-ttu-id="d18c2-130">*min*</span><span class="sxs-lookup"><span data-stu-id="d18c2-130">*min*</span></span> | <span data-ttu-id="d18c2-131">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="d18c2-131">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d18c2-132">**float**</span><span class="sxs-lookup"><span data-stu-id="d18c2-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d18c2-133">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="d18c2-133">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="d18c2-134">*max*</span><span class="sxs-lookup"><span data-stu-id="d18c2-134">*max*</span></span> | <span data-ttu-id="d18c2-135">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="d18c2-135">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d18c2-136">**float**</span><span class="sxs-lookup"><span data-stu-id="d18c2-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d18c2-137">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="d18c2-137">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="d18c2-138">*обратно*</span><span class="sxs-lookup"><span data-stu-id="d18c2-138">*ret*</span></span> | <span data-ttu-id="d18c2-139">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="d18c2-139">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d18c2-140">**float**</span><span class="sxs-lookup"><span data-stu-id="d18c2-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d18c2-141">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="d18c2-141">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d18c2-142">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d18c2-142">Minimum Shader Model</span></span>

<span data-ttu-id="d18c2-143">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="d18c2-143">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d18c2-144">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d18c2-144">Shader Model</span></span>                                                                       | <span data-ttu-id="d18c2-145">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d18c2-145">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="d18c2-146">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="d18c2-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d18c2-147">да</span><span class="sxs-lookup"><span data-stu-id="d18c2-147">yes</span></span>                 |
| [<span data-ttu-id="d18c2-148">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d18c2-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d18c2-149">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="d18c2-149">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="d18c2-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d18c2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d18c2-151">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d18c2-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

