---
title: лерп
description: Выполняет линейную интерполяцию.
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- лерп HLSL
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c7a5251aaf410d7224b87b9ee9a8f0e8a0c947e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997083"
---
# <a name="lerp"></a><span data-ttu-id="d0156-104">лерп</span><span class="sxs-lookup"><span data-stu-id="d0156-104">lerp</span></span>

<span data-ttu-id="d0156-105">Выполняет линейную интерполяцию.</span><span class="sxs-lookup"><span data-stu-id="d0156-105">Performs a linear interpolation.</span></span>



| <span data-ttu-id="d0156-106">*RET* лерп (*x*, *y*, *s*)</span><span class="sxs-lookup"><span data-stu-id="d0156-106">*ret* lerp(*x*, *y*, *s*)</span></span> |
|---------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d0156-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0156-107">Parameters</span></span>



| <span data-ttu-id="d0156-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="d0156-108">Item</span></span>                                                   | <span data-ttu-id="d0156-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d0156-109">Description</span></span>                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0156-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="d0156-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d0156-111">\[в \] значении первого значения с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="d0156-111">\[in\] The first-floating point value.</span></span><br/>                                                     |
| <span data-ttu-id="d0156-112"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="d0156-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="d0156-113">\[во \] втором значении с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="d0156-113">\[in\] The second-floating point value.</span></span><br/>                                                    |
| <span data-ttu-id="d0156-114"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="d0156-114"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="d0156-115">\[в \] значении с линейной интерполяцией между параметром *x* и параметром *y* .</span><span class="sxs-lookup"><span data-stu-id="d0156-115">\[in\] A value that linearly interpolates between the *x* parameter and the *y* parameter.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d0156-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0156-116">Return Value</span></span>

<span data-ttu-id="d0156-117">Результат линейной интерполяции.</span><span class="sxs-lookup"><span data-stu-id="d0156-117">The result of the linear interpolation.</span></span>

## <a name="type-description"></a><span data-ttu-id="d0156-118">Описание типа</span><span class="sxs-lookup"><span data-stu-id="d0156-118">Type Description</span></span>



| <span data-ttu-id="d0156-119">Имя</span><span class="sxs-lookup"><span data-stu-id="d0156-119">Name</span></span>  | [<span data-ttu-id="d0156-120">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="d0156-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d0156-121">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="d0156-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d0156-122">Размер</span><span class="sxs-lookup"><span data-stu-id="d0156-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d0156-123">*x*</span><span class="sxs-lookup"><span data-stu-id="d0156-123">*x*</span></span>   | <span data-ttu-id="d0156-124">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="d0156-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="d0156-125">**float**</span><span class="sxs-lookup"><span data-stu-id="d0156-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d0156-126">any</span><span class="sxs-lookup"><span data-stu-id="d0156-126">any</span></span>                            |
| <span data-ttu-id="d0156-127">*y*</span><span class="sxs-lookup"><span data-stu-id="d0156-127">*y*</span></span>   | <span data-ttu-id="d0156-128">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="d0156-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d0156-129">**float**</span><span class="sxs-lookup"><span data-stu-id="d0156-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d0156-130">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="d0156-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="d0156-131">*s*</span><span class="sxs-lookup"><span data-stu-id="d0156-131">*s*</span></span>   | <span data-ttu-id="d0156-132">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="d0156-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d0156-133">**float**</span><span class="sxs-lookup"><span data-stu-id="d0156-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d0156-134">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="d0156-134">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="d0156-135">*обратно*</span><span class="sxs-lookup"><span data-stu-id="d0156-135">*ret*</span></span> | <span data-ttu-id="d0156-136">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="d0156-136">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d0156-137">**float**</span><span class="sxs-lookup"><span data-stu-id="d0156-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d0156-138">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="d0156-138">same dimension(s) as input *x*</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d0156-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="d0156-139">Remarks</span></span>

<span data-ttu-id="d0156-140">Линейная интерполяция основана на следующей формуле: x \* (1-s) + y \* , что может быть эквивалентно записано в виде x + s (y-x).</span><span class="sxs-lookup"><span data-stu-id="d0156-140">Linear interpolation is based on the following formula: x\*(1-s) + y\*s which can equivalently be written as x + s(y-x).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="d0156-141">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d0156-141">Minimum Shader Model</span></span>

<span data-ttu-id="d0156-142">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="d0156-142">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d0156-143">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d0156-143">Shader Model</span></span>                                                                       | <span data-ttu-id="d0156-144">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d0156-144">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="d0156-145">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="d0156-145">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d0156-146">да</span><span class="sxs-lookup"><span data-stu-id="d0156-146">yes</span></span>                         |
| [<span data-ttu-id="d0156-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d0156-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d0156-148">Да (VS 1 1 \_ \_ и PS \_ 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="d0156-148">yes (vs\_1\_1 and ps\_1\_1)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="d0156-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0156-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0156-150">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d0156-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

