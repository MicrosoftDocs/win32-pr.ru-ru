---
title: max
description: Выбор большего числа x и y.
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- Максимальное HLSL
topic_type:
- apiref
api_name:
- max
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a40ccb32bb2c2fcd7ca7342b9d7d4d143688102
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413401"
---
# <a name="max"></a><span data-ttu-id="fe055-104">max</span><span class="sxs-lookup"><span data-stu-id="fe055-104">max</span></span>

<span data-ttu-id="fe055-105">Выбор большего числа x и y.</span><span class="sxs-lookup"><span data-stu-id="fe055-105">Selects the greater of x and y.</span></span>



| <span data-ttu-id="fe055-106">RET-Max (x, y)</span><span class="sxs-lookup"><span data-stu-id="fe055-106">ret max(x, y)</span></span> |
|---------------|



 

## <a name="parameters"></a><span data-ttu-id="fe055-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe055-107">Parameters</span></span>



| <span data-ttu-id="fe055-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="fe055-108">Item</span></span>                                                   | <span data-ttu-id="fe055-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fe055-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="fe055-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="fe055-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="fe055-111">\[в \] входном значении x.</span><span class="sxs-lookup"><span data-stu-id="fe055-111">\[in\] The x input value.</span></span><br/> |
| <span data-ttu-id="fe055-112"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="fe055-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="fe055-113">\[во \] входном значении y.</span><span class="sxs-lookup"><span data-stu-id="fe055-113">\[in\] The y input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="fe055-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe055-114">Return Value</span></span>

<span data-ttu-id="fe055-115">Параметр *x* или *y* , в зависимости от самого крупного значения.</span><span class="sxs-lookup"><span data-stu-id="fe055-115">The *x* or *y* parameter, whichever is the largest value.</span></span>


## <a name="remarks"></a><span data-ttu-id="fe055-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="fe055-116">Remarks</span></span>

<span data-ttu-id="fe055-117">Нормали обрабатываются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fe055-117">Denormals are handled as follows:</span></span>

| <span data-ttu-id="fe055-118">src0 src1 — ></span><span class="sxs-lookup"><span data-stu-id="fe055-118">src0 src1-></span></span> | <span data-ttu-id="fe055-119">-inf</span><span class="sxs-lookup"><span data-stu-id="fe055-119">-inf</span></span> | <span data-ttu-id="fe055-120">C</span><span class="sxs-lookup"><span data-stu-id="fe055-120">F</span></span>             | <span data-ttu-id="fe055-121">+inf</span><span class="sxs-lookup"><span data-stu-id="fe055-121">+inf</span></span> | <span data-ttu-id="fe055-122">Не число</span><span class="sxs-lookup"><span data-stu-id="fe055-122">NAN</span></span>  |
|-------------|------|---------------|------|------|
| <span data-ttu-id="fe055-123">-inf</span><span class="sxs-lookup"><span data-stu-id="fe055-123">-inf</span></span>        | <span data-ttu-id="fe055-124">-inf</span><span class="sxs-lookup"><span data-stu-id="fe055-124">-inf</span></span> | <span data-ttu-id="fe055-125">src1</span><span class="sxs-lookup"><span data-stu-id="fe055-125">src1</span></span>          | <span data-ttu-id="fe055-126">+inf</span><span class="sxs-lookup"><span data-stu-id="fe055-126">+inf</span></span> | <span data-ttu-id="fe055-127">-inf</span><span class="sxs-lookup"><span data-stu-id="fe055-127">-inf</span></span> |
| <span data-ttu-id="fe055-128">C</span><span class="sxs-lookup"><span data-stu-id="fe055-128">F</span></span>           | <span data-ttu-id="fe055-129">src0</span><span class="sxs-lookup"><span data-stu-id="fe055-129">src0</span></span> | <span data-ttu-id="fe055-130">src0 или src1</span><span class="sxs-lookup"><span data-stu-id="fe055-130">src0 or src1</span></span>  | <span data-ttu-id="fe055-131">+inf</span><span class="sxs-lookup"><span data-stu-id="fe055-131">+inf</span></span> | <span data-ttu-id="fe055-132">src0</span><span class="sxs-lookup"><span data-stu-id="fe055-132">src0</span></span> |
| <span data-ttu-id="fe055-133">+inf</span><span class="sxs-lookup"><span data-stu-id="fe055-133">+inf</span></span>        | <span data-ttu-id="fe055-134">+inf</span><span class="sxs-lookup"><span data-stu-id="fe055-134">+inf</span></span> | <span data-ttu-id="fe055-135">+inf</span><span class="sxs-lookup"><span data-stu-id="fe055-135">+inf</span></span>          | <span data-ttu-id="fe055-136">+inf</span><span class="sxs-lookup"><span data-stu-id="fe055-136">+inf</span></span> | <span data-ttu-id="fe055-137">+inf</span><span class="sxs-lookup"><span data-stu-id="fe055-137">+inf</span></span> |
| <span data-ttu-id="fe055-138">не число</span><span class="sxs-lookup"><span data-stu-id="fe055-138">NaN</span></span>         | <span data-ttu-id="fe055-139">-inf</span><span class="sxs-lookup"><span data-stu-id="fe055-139">-inf</span></span> | <span data-ttu-id="fe055-140">src1</span><span class="sxs-lookup"><span data-stu-id="fe055-140">src1</span></span>          | <span data-ttu-id="fe055-141">+inf</span><span class="sxs-lookup"><span data-stu-id="fe055-141">+inf</span></span> | <span data-ttu-id="fe055-142">не число</span><span class="sxs-lookup"><span data-stu-id="fe055-142">NaN</span></span>  |

<span data-ttu-id="fe055-143">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="fe055-143">F means finite-real number.</span></span>


## <a name="type-description"></a><span data-ttu-id="fe055-144">Описание типа</span><span class="sxs-lookup"><span data-stu-id="fe055-144">Type Description</span></span>

| <span data-ttu-id="fe055-145">Имя</span><span class="sxs-lookup"><span data-stu-id="fe055-145">Name</span></span> | <span data-ttu-id="fe055-146">В/Из</span><span class="sxs-lookup"><span data-stu-id="fe055-146">In/Out</span></span>      | [<span data-ttu-id="fe055-147">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="fe055-147">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="fe055-148">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="fe055-148">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="fe055-149">Размер</span><span class="sxs-lookup"><span data-stu-id="fe055-149">Size</span></span>                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="fe055-150">x</span><span class="sxs-lookup"><span data-stu-id="fe055-150">x</span></span>    | <span data-ttu-id="fe055-151">in</span><span class="sxs-lookup"><span data-stu-id="fe055-151">in</span></span>          | <span data-ttu-id="fe055-152">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="fe055-152">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="fe055-153">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="fe055-153">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="fe055-154">any</span><span class="sxs-lookup"><span data-stu-id="fe055-154">any</span></span>                          |
| <span data-ttu-id="fe055-155">да</span><span class="sxs-lookup"><span data-stu-id="fe055-155">y</span></span>    | <span data-ttu-id="fe055-156">in</span><span class="sxs-lookup"><span data-stu-id="fe055-156">in</span></span>          | <span data-ttu-id="fe055-157">то же, что входные данные x</span><span class="sxs-lookup"><span data-stu-id="fe055-157">same as input x</span></span>                                                                                                | <span data-ttu-id="fe055-158">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="fe055-158">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="fe055-159">те же измерения, что и входные x</span><span class="sxs-lookup"><span data-stu-id="fe055-159">same dimension(s) as input x</span></span> |
| <span data-ttu-id="fe055-160">обратно</span><span class="sxs-lookup"><span data-stu-id="fe055-160">ret</span></span>  | <span data-ttu-id="fe055-161">тип возвращаемого значения;</span><span class="sxs-lookup"><span data-stu-id="fe055-161">return type</span></span> | <span data-ttu-id="fe055-162">то же, что входные данные x</span><span class="sxs-lookup"><span data-stu-id="fe055-162">same as input x</span></span>                                                                                                | <span data-ttu-id="fe055-163">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="fe055-163">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="fe055-164">те же измерения, что и входные x</span><span class="sxs-lookup"><span data-stu-id="fe055-164">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fe055-165">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fe055-165">Minimum Shader Model</span></span>

<span data-ttu-id="fe055-166">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="fe055-166">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fe055-167">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fe055-167">Shader Model</span></span>                                                                       | <span data-ttu-id="fe055-168">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="fe055-168">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="fe055-169">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="fe055-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="fe055-170">да</span><span class="sxs-lookup"><span data-stu-id="fe055-170">yes</span></span>                         |
| [<span data-ttu-id="fe055-171">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe055-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="fe055-172">Да (VS \_ 1 \_ 1 и PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="fe055-172">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="fe055-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe055-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe055-174">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="fe055-174">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[<span data-ttu-id="fe055-175">**Функциональная спецификация DirectX**</span><span class="sxs-lookup"><span data-stu-id="fe055-175">**DirectX Functional Specification**</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
