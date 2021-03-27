---
title: pow
description: Возвращает указанное значение, возведенное в указанную степень.
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- Pow HLSL
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f190c374b6c0ac42d41862eb918f0c0482b6d785
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488209"
---
# <a name="pow"></a><span data-ttu-id="5b025-104">pow</span><span class="sxs-lookup"><span data-stu-id="5b025-104">pow</span></span>

<span data-ttu-id="5b025-105">Возвращает указанное значение, возведенное в указанную степень.</span><span class="sxs-lookup"><span data-stu-id="5b025-105">Returns the specified value raised to the specified power.</span></span>



| <span data-ttu-id="5b025-106">*RET* Pow (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="5b025-106">*ret* pow(*x*, *y*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="5b025-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b025-107">Parameters</span></span>



| <span data-ttu-id="5b025-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="5b025-108">Item</span></span>                                                   | <span data-ttu-id="5b025-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5b025-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="5b025-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="5b025-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="5b025-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="5b025-111">\[in\] The specified value.</span></span><br/> |
| <span data-ttu-id="5b025-112"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="5b025-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="5b025-113">\[в \] заданной степени.</span><span class="sxs-lookup"><span data-stu-id="5b025-113">\[in\] The specified power.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="5b025-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b025-114">Return Value</span></span>

<span data-ttu-id="5b025-115">Параметр *x* , возведенный в степень параметра *y* .</span><span class="sxs-lookup"><span data-stu-id="5b025-115">The *x* parameter raised to the power of the *y* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b025-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="5b025-116">Remarks</span></span>

<span data-ttu-id="5b025-117">Встроенная функция **Pow** HLSL вычисляет *x*<sup>y</sup>.</span><span class="sxs-lookup"><span data-stu-id="5b025-117">The **pow** HLSL intrinsic function calculates *x*<sup>y</sup>.</span></span>



| <span data-ttu-id="5b025-118">X</span><span class="sxs-lookup"><span data-stu-id="5b025-118">X</span></span>      | <span data-ttu-id="5b025-119">Y</span><span class="sxs-lookup"><span data-stu-id="5b025-119">Y</span></span>      | <span data-ttu-id="5b025-120">Результат</span><span class="sxs-lookup"><span data-stu-id="5b025-120">Result</span></span>                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5b025-121">< 0</span><span class="sxs-lookup"><span data-stu-id="5b025-121">< 0</span></span> | <span data-ttu-id="5b025-122">any</span><span class="sxs-lookup"><span data-stu-id="5b025-122">any</span></span>    | <span data-ttu-id="5b025-123">Не число</span><span class="sxs-lookup"><span data-stu-id="5b025-123">NAN</span></span>                                                                         |
| <span data-ttu-id="5b025-124">> 0</span><span class="sxs-lookup"><span data-stu-id="5b025-124">> 0</span></span> | <span data-ttu-id="5b025-125">= = 0</span><span class="sxs-lookup"><span data-stu-id="5b025-125">== 0</span></span>   | <span data-ttu-id="5b025-126">1</span><span class="sxs-lookup"><span data-stu-id="5b025-126">1</span></span>                                                                           |
| <span data-ttu-id="5b025-127">= = 0</span><span class="sxs-lookup"><span data-stu-id="5b025-127">== 0</span></span>   | <span data-ttu-id="5b025-128">> 0</span><span class="sxs-lookup"><span data-stu-id="5b025-128">> 0</span></span> | <span data-ttu-id="5b025-129">0</span><span class="sxs-lookup"><span data-stu-id="5b025-129">0</span></span>                                                                           |
| <span data-ttu-id="5b025-130">= = 0</span><span class="sxs-lookup"><span data-stu-id="5b025-130">== 0</span></span>   | <span data-ttu-id="5b025-131">< 0</span><span class="sxs-lookup"><span data-stu-id="5b025-131">< 0</span></span> | <span data-ttu-id="5b025-132">файлу</span><span class="sxs-lookup"><span data-stu-id="5b025-132">inf</span></span>                                                                         |
| <span data-ttu-id="5b025-133">> 0</span><span class="sxs-lookup"><span data-stu-id="5b025-133">> 0</span></span> | <span data-ttu-id="5b025-134">< 0</span><span class="sxs-lookup"><span data-stu-id="5b025-134">< 0</span></span> | <span data-ttu-id="5b025-135">1/X<sup>-Y</sup></span><span class="sxs-lookup"><span data-stu-id="5b025-135">1/X<sup>-Y</sup></span></span>                                                            |
| <span data-ttu-id="5b025-136">= = 0</span><span class="sxs-lookup"><span data-stu-id="5b025-136">== 0</span></span>   | <span data-ttu-id="5b025-137">= = 0</span><span class="sxs-lookup"><span data-stu-id="5b025-137">== 0</span></span>   | <span data-ttu-id="5b025-138">Зависит от конкретного графического процессора</span><span class="sxs-lookup"><span data-stu-id="5b025-138">Depends on the particular graphics processor</span></span><br/> <span data-ttu-id="5b025-139">0, 1 или NAN</span><span class="sxs-lookup"><span data-stu-id="5b025-139">0, or 1, or NAN</span></span><br/> |



 

## <a name="type-description"></a><span data-ttu-id="5b025-140">Описание типа</span><span class="sxs-lookup"><span data-stu-id="5b025-140">Type Description</span></span>



| <span data-ttu-id="5b025-141">Имя</span><span class="sxs-lookup"><span data-stu-id="5b025-141">Name</span></span>  | [<span data-ttu-id="5b025-142">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="5b025-142">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="5b025-143">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="5b025-143">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="5b025-144">Размер</span><span class="sxs-lookup"><span data-stu-id="5b025-144">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="5b025-145">*x*</span><span class="sxs-lookup"><span data-stu-id="5b025-145">*x*</span></span>   | <span data-ttu-id="5b025-146">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="5b025-146">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="5b025-147">**float**</span><span class="sxs-lookup"><span data-stu-id="5b025-147">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5b025-148">any</span><span class="sxs-lookup"><span data-stu-id="5b025-148">any</span></span>                            |
| <span data-ttu-id="5b025-149">*y*</span><span class="sxs-lookup"><span data-stu-id="5b025-149">*y*</span></span>   | <span data-ttu-id="5b025-150">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="5b025-150">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="5b025-151">**float**</span><span class="sxs-lookup"><span data-stu-id="5b025-151">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5b025-152">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="5b025-152">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="5b025-153">*обратно*</span><span class="sxs-lookup"><span data-stu-id="5b025-153">*ret*</span></span> | <span data-ttu-id="5b025-154">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="5b025-154">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="5b025-155">**float**</span><span class="sxs-lookup"><span data-stu-id="5b025-155">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5b025-156">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="5b025-156">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5b025-157">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5b025-157">Minimum Shader Model</span></span>

<span data-ttu-id="5b025-158">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="5b025-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5b025-159">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5b025-159">Shader Model</span></span>                                                                       | <span data-ttu-id="5b025-160">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="5b025-160">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="5b025-161">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="5b025-161">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="5b025-162">да</span><span class="sxs-lookup"><span data-stu-id="5b025-162">yes</span></span>                 |
| [<span data-ttu-id="5b025-163">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5b025-163">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="5b025-164">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="5b025-164">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="5b025-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b025-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b025-166">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="5b025-166">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

