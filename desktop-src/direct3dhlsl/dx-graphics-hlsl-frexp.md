---
title: frexp (Корекрт \_ Math. h)
description: Возвращает мантисса и экспоненту указанного значения с плавающей точкой.
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- frexp HLSL
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bddbcbbf9e97aff739bb06a0f0d0ddac12134463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000356"
---
# <a name="frexp"></a><span data-ttu-id="94fb2-104">frexp</span><span class="sxs-lookup"><span data-stu-id="94fb2-104">frexp</span></span>

<span data-ttu-id="94fb2-105">Возвращает мантисса и экспоненту указанного значения с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="94fb2-105">Returns the mantissa and exponent of the specified floating-point value.</span></span>



| <span data-ttu-id="94fb2-106">*RET* frexp (*x*, *exp*)</span><span class="sxs-lookup"><span data-stu-id="94fb2-106">*ret* frexp(*x*, *exp*)</span></span> |
|-------------------------|



 

<span data-ttu-id="94fb2-107">Возвращаемое значение — мантисса, а значение, возвращаемое параметром *exp* , — показатель степени.</span><span class="sxs-lookup"><span data-stu-id="94fb2-107">The return value is the mantissa, and the value returned by *exp* parameter is the exponent.</span></span>

## <a name="parameters"></a><span data-ttu-id="94fb2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="94fb2-108">Parameters</span></span>



| <span data-ttu-id="94fb2-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="94fb2-109">Item</span></span>                                                         | <span data-ttu-id="94fb2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="94fb2-110">Description</span></span>                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94fb2-111"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="94fb2-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="94fb2-112">\[в \] указанном значении с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="94fb2-112">\[in\] The specified floating-point value.</span></span> <span data-ttu-id="94fb2-113">Если параметр *x* равен 0, эта функция возвращает 0 для мантиссаа и экспоненты.</span><span class="sxs-lookup"><span data-stu-id="94fb2-113">If the *x* parameter is 0, this function returns 0 for both the mantissa and the exponent.</span></span><br/> |
| <span data-ttu-id="94fb2-114"><span id="exp"></span><span id="EXP"></span>*расширением*</span><span class="sxs-lookup"><span data-stu-id="94fb2-114"><span id="exp"></span><span id="EXP"></span>*exp*</span></span><br/> | <span data-ttu-id="94fb2-115">\[\]возвращаемый экспонента параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="94fb2-115">\[out\] The returned exponent of the *x* parameter.</span></span><br/>                                                                                   |



 

## <a name="return-value"></a><span data-ttu-id="94fb2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94fb2-116">Return Value</span></span>

<span data-ttu-id="94fb2-117">Мантисса параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="94fb2-117">The mantissa of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="94fb2-118">Описание типа</span><span class="sxs-lookup"><span data-stu-id="94fb2-118">Type Description</span></span>



| <span data-ttu-id="94fb2-119">Имя</span><span class="sxs-lookup"><span data-stu-id="94fb2-119">Name</span></span>  | [<span data-ttu-id="94fb2-120">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="94fb2-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="94fb2-121">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="94fb2-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="94fb2-122">Размер</span><span class="sxs-lookup"><span data-stu-id="94fb2-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="94fb2-123">*x*</span><span class="sxs-lookup"><span data-stu-id="94fb2-123">*x*</span></span>   | <span data-ttu-id="94fb2-124">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="94fb2-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="94fb2-125">**float**</span><span class="sxs-lookup"><span data-stu-id="94fb2-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="94fb2-126">any</span><span class="sxs-lookup"><span data-stu-id="94fb2-126">any</span></span>                            |
| <span data-ttu-id="94fb2-127">*exp*</span><span class="sxs-lookup"><span data-stu-id="94fb2-127">*exp*</span></span> | <span data-ttu-id="94fb2-128">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="94fb2-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="94fb2-129">**float**</span><span class="sxs-lookup"><span data-stu-id="94fb2-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="94fb2-130">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="94fb2-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="94fb2-131">*обратно*</span><span class="sxs-lookup"><span data-stu-id="94fb2-131">*ret*</span></span> | <span data-ttu-id="94fb2-132">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="94fb2-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="94fb2-133">**float**</span><span class="sxs-lookup"><span data-stu-id="94fb2-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="94fb2-134">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="94fb2-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="94fb2-135">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="94fb2-135">Minimum Shader Model</span></span>

<span data-ttu-id="94fb2-136">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="94fb2-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="94fb2-137">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="94fb2-137">Shader Model</span></span>                                                                       | <span data-ttu-id="94fb2-138">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="94fb2-138">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="94fb2-139">[Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) и более высокие модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="94fb2-139">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="94fb2-140">да</span><span class="sxs-lookup"><span data-stu-id="94fb2-140">yes</span></span>                 |
| [<span data-ttu-id="94fb2-141">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="94fb2-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="94fb2-142">Да ( \_ только PS 2 \_ x)</span><span class="sxs-lookup"><span data-stu-id="94fb2-142">yes (ps\_2\_x only)</span></span> |
| [<span data-ttu-id="94fb2-143">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="94fb2-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="94fb2-144">Нет</span><span class="sxs-lookup"><span data-stu-id="94fb2-144">no</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="94fb2-145">Remarks</span><span class="sxs-lookup"><span data-stu-id="94fb2-145">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="94fb2-146">Требования</span><span class="sxs-lookup"><span data-stu-id="94fb2-146">Requirements</span></span>



| <span data-ttu-id="94fb2-147">Требование</span><span class="sxs-lookup"><span data-stu-id="94fb2-147">Requirement</span></span> | <span data-ttu-id="94fb2-148">Значение</span><span class="sxs-lookup"><span data-stu-id="94fb2-148">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="94fb2-149">Header</span><span class="sxs-lookup"><span data-stu-id="94fb2-149">Header</span></span><br/> | <dl> <span data-ttu-id="94fb2-150"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="94fb2-150"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94fb2-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94fb2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94fb2-152">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="94fb2-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

