---
title: fmod (Корекрт \_ Math. h)
description: Возвращает остаток от деления x/y на число с плавающей запятой.
ms.assetid: bb940548-c4c5-4109-a488-4ea7295c7213
keywords:
- FMOD HLSL
topic_type:
- apiref
api_name:
- fmod
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9dc4367e3aa80484098e88926567953fc8e9a90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354740"
---
# <a name="fmod"></a><span data-ttu-id="81213-104">fmod</span><span class="sxs-lookup"><span data-stu-id="81213-104">fmod</span></span>

<span data-ttu-id="81213-105">Возвращает остаток от деления x/y на число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="81213-105">Returns the floating-point remainder of x/y.</span></span>



| <span data-ttu-id="81213-106">*RET* fmod (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="81213-106">*ret* fmod(*x*, *y*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="81213-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="81213-107">Parameters</span></span>



| <span data-ttu-id="81213-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="81213-108">Item</span></span>                                                   | <span data-ttu-id="81213-109">Описание</span><span class="sxs-lookup"><span data-stu-id="81213-109">Description</span></span>                                    |
|--------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="81213-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="81213-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="81213-111">\[в \] делимом с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="81213-111">\[in\] The floating-point dividend.</span></span><br/> |
| <span data-ttu-id="81213-112"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="81213-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="81213-113">\[в \] делителье с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="81213-113">\[in\] The floating-point divisor.</span></span><br/>  |



 

## <a name="return-value"></a><span data-ttu-id="81213-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81213-114">Return Value</span></span>

<span data-ttu-id="81213-115">Остаток числа с плавающей запятой параметра *x* , деленный на параметр *y* .</span><span class="sxs-lookup"><span data-stu-id="81213-115">The floating-point remainder of the *x* parameter divided by the *y* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="81213-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="81213-116">Remarks</span></span>

<span data-ttu-id="81213-117">Остаток с плавающей запятой вычисляется таким образом, что x = i \* y + f, где i является целым числом, f имеет тот же знак, что и x, а абсолютное значение f меньше, чем абсолютное значение y.</span><span class="sxs-lookup"><span data-stu-id="81213-117">The floating-point remainder is calculated such that x = i \* y + f, where i is an integer, f has the same sign as x, and the absolute value of f is less than the absolute value of y.</span></span>

## <a name="type-description"></a><span data-ttu-id="81213-118">Описание типа</span><span class="sxs-lookup"><span data-stu-id="81213-118">Type Description</span></span>



| <span data-ttu-id="81213-119">Имя</span><span class="sxs-lookup"><span data-stu-id="81213-119">Name</span></span>  | [<span data-ttu-id="81213-120">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="81213-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="81213-121">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="81213-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="81213-122">Размер</span><span class="sxs-lookup"><span data-stu-id="81213-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="81213-123">*x*</span><span class="sxs-lookup"><span data-stu-id="81213-123">*x*</span></span>   | <span data-ttu-id="81213-124">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="81213-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="81213-125">**float**</span><span class="sxs-lookup"><span data-stu-id="81213-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="81213-126">any</span><span class="sxs-lookup"><span data-stu-id="81213-126">any</span></span>                            |
| <span data-ttu-id="81213-127">*y*</span><span class="sxs-lookup"><span data-stu-id="81213-127">*y*</span></span>   | <span data-ttu-id="81213-128">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="81213-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="81213-129">**float**</span><span class="sxs-lookup"><span data-stu-id="81213-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="81213-130">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="81213-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="81213-131">*обратно*</span><span class="sxs-lookup"><span data-stu-id="81213-131">*ret*</span></span> | <span data-ttu-id="81213-132">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="81213-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="81213-133">**float**</span><span class="sxs-lookup"><span data-stu-id="81213-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="81213-134">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="81213-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="81213-135">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="81213-135">Minimum Shader Model</span></span>

<span data-ttu-id="81213-136">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="81213-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="81213-137">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="81213-137">Shader Model</span></span>                                                                       | <span data-ttu-id="81213-138">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="81213-138">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="81213-139">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="81213-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="81213-140">да</span><span class="sxs-lookup"><span data-stu-id="81213-140">yes</span></span>       |
| [<span data-ttu-id="81213-141">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="81213-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="81213-142">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="81213-142">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="81213-143">Требования</span><span class="sxs-lookup"><span data-stu-id="81213-143">Requirements</span></span>



| <span data-ttu-id="81213-144">Требование</span><span class="sxs-lookup"><span data-stu-id="81213-144">Requirement</span></span> | <span data-ttu-id="81213-145">Значение</span><span class="sxs-lookup"><span data-stu-id="81213-145">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="81213-146">Header</span><span class="sxs-lookup"><span data-stu-id="81213-146">Header</span></span><br/> | <dl> <span data-ttu-id="81213-147"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="81213-147"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81213-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81213-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81213-149">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="81213-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

