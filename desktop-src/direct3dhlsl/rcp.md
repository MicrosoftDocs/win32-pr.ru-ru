---
title: rcp
description: Вычисляет быстрое и приближенное обратное значение для каждого компонента.
ms.assetid: c8d451e4-717e-45b3-a0fe-da55feb8f443
keywords:
- rcp HLSL
topic_type:
- apiref
api_name:
- rcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a857c897def08f31e18ef19466daa2b4584740a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792295"
---
# <a name="rcp"></a><span data-ttu-id="490bf-104">rcp</span><span class="sxs-lookup"><span data-stu-id="490bf-104">rcp</span></span>

<span data-ttu-id="490bf-105">Вычисляет быстрое и приближенное обратное значение для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="490bf-105">Calculates a fast, approximate, per-component reciprocal.</span></span>



| <span data-ttu-id="490bf-106">*RET* -RCP (*x*)</span><span class="sxs-lookup"><span data-stu-id="490bf-106">*ret* rcp(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="490bf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="490bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="490bf-108"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="490bf-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="490bf-109">\[во \] входном значении.</span><span class="sxs-lookup"><span data-stu-id="490bf-109">\[in\] The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="490bf-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="490bf-110">Return Value</span></span>

<span data-ttu-id="490bf-111">Обратная часть параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="490bf-111">The reciprocal of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="490bf-112">Описание типа</span><span class="sxs-lookup"><span data-stu-id="490bf-112">Type Description</span></span>



| <span data-ttu-id="490bf-113">Имя</span><span class="sxs-lookup"><span data-stu-id="490bf-113">Name</span></span>  | [<span data-ttu-id="490bf-114">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="490bf-114">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="490bf-115">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="490bf-115">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                      | <span data-ttu-id="490bf-116">Размер</span><span class="sxs-lookup"><span data-stu-id="490bf-116">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="490bf-117">*x*</span><span class="sxs-lookup"><span data-stu-id="490bf-117">*x*</span></span>   | <span data-ttu-id="490bf-118">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="490bf-118">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="490bf-119">[**float**](/windows/desktop/WinProg/windows-data-types) или [ **Double**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="490bf-119">[**float**](/windows/desktop/WinProg/windows-data-types) or [**double**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="490bf-120">any</span><span class="sxs-lookup"><span data-stu-id="490bf-120">any</span></span>                            |
| <span data-ttu-id="490bf-121">*обратно*</span><span class="sxs-lookup"><span data-stu-id="490bf-121">*ret*</span></span> | <span data-ttu-id="490bf-122">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="490bf-122">same as input *x*</span></span>                                                                                              | <span data-ttu-id="490bf-123">[**float**](/windows/desktop/WinProg/windows-data-types) или [ **Double**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="490bf-123">[**float**](/windows/desktop/WinProg/windows-data-types) or [**double**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="490bf-124">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="490bf-124">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="490bf-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="490bf-125">Minimum Shader Model</span></span>

<span data-ttu-id="490bf-126">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="490bf-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="490bf-127">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="490bf-127">Shader Model</span></span>                                                                | <span data-ttu-id="490bf-128">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="490bf-128">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="490bf-129">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="490bf-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="490bf-130">да</span><span class="sxs-lookup"><span data-stu-id="490bf-130">yes</span></span>       |



 

<span data-ttu-id="490bf-131">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="490bf-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="490bf-132">Вершина</span><span class="sxs-lookup"><span data-stu-id="490bf-132">Vertex</span></span> | <span data-ttu-id="490bf-133">Поверхности</span><span class="sxs-lookup"><span data-stu-id="490bf-133">Hull</span></span> | <span data-ttu-id="490bf-134">Домен</span><span class="sxs-lookup"><span data-stu-id="490bf-134">Domain</span></span> | <span data-ttu-id="490bf-135">Геометрия</span><span class="sxs-lookup"><span data-stu-id="490bf-135">Geometry</span></span> | <span data-ttu-id="490bf-136">Пиксель</span><span class="sxs-lookup"><span data-stu-id="490bf-136">Pixel</span></span> | <span data-ttu-id="490bf-137">Вычисления</span><span class="sxs-lookup"><span data-stu-id="490bf-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="490bf-138">x</span><span class="sxs-lookup"><span data-stu-id="490bf-138">x</span></span>      | <span data-ttu-id="490bf-139">x</span><span class="sxs-lookup"><span data-stu-id="490bf-139">x</span></span>    | <span data-ttu-id="490bf-140">x</span><span class="sxs-lookup"><span data-stu-id="490bf-140">x</span></span>      | <span data-ttu-id="490bf-141">x</span><span class="sxs-lookup"><span data-stu-id="490bf-141">x</span></span>        | <span data-ttu-id="490bf-142">x</span><span class="sxs-lookup"><span data-stu-id="490bf-142">x</span></span>     | <span data-ttu-id="490bf-143">x</span><span class="sxs-lookup"><span data-stu-id="490bf-143">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="490bf-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="490bf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="490bf-145">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="490bf-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="490bf-146">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="490bf-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 