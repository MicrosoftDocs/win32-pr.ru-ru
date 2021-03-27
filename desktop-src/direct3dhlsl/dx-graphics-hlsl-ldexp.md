---
title: ldexp (Корекрт \_ Math. h)
description: Возвращает результат умножения указанного значения на два, возведенное в степень указанного показателя степени.
ms.assetid: 6d6fee96-f952-4058-a1ac-3abb98dbd540
keywords:
- ldexp HLSL
topic_type:
- apiref
api_name:
- ldexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731cb5cbf933ea3f8754a7d70b9ef0b7a54e783b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914756"
---
# <a name="ldexp"></a><span data-ttu-id="b2b0b-104">ldexp</span><span class="sxs-lookup"><span data-stu-id="b2b0b-104">ldexp</span></span>

<span data-ttu-id="b2b0b-105">Возвращает результат умножения указанного значения на два, возведенное в степень указанного показателя степени.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-105">Returns the result of multiplying the specified value by two, raised to the power of the specified exponent.</span></span>



| <span data-ttu-id="b2b0b-106">*RET* ldexp (*x*, *exp*)</span><span class="sxs-lookup"><span data-stu-id="b2b0b-106">*ret* ldexp(*x*, *exp*)</span></span> |
|-------------------------|



 

<span data-ttu-id="b2b0b-107">Эта функция использует следующую формулу: *x* \* 2 <sup>exp</sup></span><span class="sxs-lookup"><span data-stu-id="b2b0b-107">This function uses the following formula: *x* \* 2<sup>exp</sup></span></span>

## <a name="parameters"></a><span data-ttu-id="b2b0b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2b0b-108">Parameters</span></span>



| <span data-ttu-id="b2b0b-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="b2b0b-109">Item</span></span>                                                         | <span data-ttu-id="b2b0b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b2b0b-110">Description</span></span>                               |
|--------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="b2b0b-111"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b2b0b-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="b2b0b-112">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-112">\[in\] The specified value.</span></span><br/>    |
| <span data-ttu-id="b2b0b-113"><span id="exp"></span><span id="EXP"></span>*расширением*</span><span class="sxs-lookup"><span data-stu-id="b2b0b-113"><span id="exp"></span><span id="EXP"></span>*exp*</span></span><br/> | <span data-ttu-id="b2b0b-114">\[в \] указанном экспоненте.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-114">\[in\] The specified exponent.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b2b0b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2b0b-115">Return Value</span></span>

<span data-ttu-id="b2b0b-116">Результат умножения параметра *x* на два, возведенный в степень параметра *exp* .</span><span class="sxs-lookup"><span data-stu-id="b2b0b-116">The result of multiplying the *x* parameter by two, raised to the power of the *exp* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="b2b0b-117">Описание типа</span><span class="sxs-lookup"><span data-stu-id="b2b0b-117">Type Description</span></span>



| <span data-ttu-id="b2b0b-118">Имя</span><span class="sxs-lookup"><span data-stu-id="b2b0b-118">Name</span></span>  | [<span data-ttu-id="b2b0b-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="b2b0b-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b2b0b-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="b2b0b-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b2b0b-121">Размер</span><span class="sxs-lookup"><span data-stu-id="b2b0b-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b2b0b-122">*x*</span><span class="sxs-lookup"><span data-stu-id="b2b0b-122">*x*</span></span>   | <span data-ttu-id="b2b0b-123">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="b2b0b-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="b2b0b-124">**float**</span><span class="sxs-lookup"><span data-stu-id="b2b0b-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b2b0b-125">any</span><span class="sxs-lookup"><span data-stu-id="b2b0b-125">any</span></span>                            |
| <span data-ttu-id="b2b0b-126">*exp*</span><span class="sxs-lookup"><span data-stu-id="b2b0b-126">*exp*</span></span> | <span data-ttu-id="b2b0b-127">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="b2b0b-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b2b0b-128">**float**</span><span class="sxs-lookup"><span data-stu-id="b2b0b-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b2b0b-129">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="b2b0b-129">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="b2b0b-130">*обратно*</span><span class="sxs-lookup"><span data-stu-id="b2b0b-130">*ret*</span></span> | <span data-ttu-id="b2b0b-131">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="b2b0b-131">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b2b0b-132">**float**</span><span class="sxs-lookup"><span data-stu-id="b2b0b-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b2b0b-133">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="b2b0b-133">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b2b0b-134">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b2b0b-134">Minimum Shader Model</span></span>

<span data-ttu-id="b2b0b-135">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-135">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b2b0b-136">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b2b0b-136">Shader Model</span></span>                                                                       | <span data-ttu-id="b2b0b-137">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="b2b0b-137">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="b2b0b-138">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="b2b0b-138">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b2b0b-139">да</span><span class="sxs-lookup"><span data-stu-id="b2b0b-139">yes</span></span>                 |
| [<span data-ttu-id="b2b0b-140">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b2b0b-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b2b0b-141">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="b2b0b-141">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b2b0b-142">Требования</span><span class="sxs-lookup"><span data-stu-id="b2b0b-142">Requirements</span></span>



| <span data-ttu-id="b2b0b-143">Требование</span><span class="sxs-lookup"><span data-stu-id="b2b0b-143">Requirement</span></span> | <span data-ttu-id="b2b0b-144">Значение</span><span class="sxs-lookup"><span data-stu-id="b2b0b-144">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b0b-145">Header</span><span class="sxs-lookup"><span data-stu-id="b2b0b-145">Header</span></span><br/> | <dl> <span data-ttu-id="b2b0b-146"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2b0b-146"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2b0b-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2b0b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b0b-148">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b2b0b-148">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

