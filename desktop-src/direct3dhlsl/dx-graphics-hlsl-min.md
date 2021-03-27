---
title: мин
description: Выбирает меньшее из значений x и y.
ms.assetid: 4e10cfc2-d680-4d7f-81b2-fa52024f902d
keywords:
- min HLSL
topic_type:
- apiref
api_name:
- min
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 129c5cb641c2d69b6c1365d8221663e264060532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488212"
---
# <a name="min"></a><span data-ttu-id="418ec-104">мин</span><span class="sxs-lookup"><span data-stu-id="418ec-104">min</span></span>

<span data-ttu-id="418ec-105">Выбирает меньшее из значений x и y.</span><span class="sxs-lookup"><span data-stu-id="418ec-105">Selects the lesser of x and y.</span></span>



| <span data-ttu-id="418ec-106">RET-min (x, y)</span><span class="sxs-lookup"><span data-stu-id="418ec-106">ret min(x, y)</span></span> |
|---------------|



 

## <a name="parameters"></a><span data-ttu-id="418ec-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="418ec-107">Parameters</span></span>



| <span data-ttu-id="418ec-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="418ec-108">Item</span></span>                                                   | <span data-ttu-id="418ec-109">Описание</span><span class="sxs-lookup"><span data-stu-id="418ec-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="418ec-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="418ec-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="418ec-111">\[в \] входном значении x.</span><span class="sxs-lookup"><span data-stu-id="418ec-111">\[in\] The x input value.</span></span><br/> |
| <span data-ttu-id="418ec-112"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="418ec-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="418ec-113">\[во \] входном значении y.</span><span class="sxs-lookup"><span data-stu-id="418ec-113">\[in\] The y input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="418ec-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="418ec-114">Return Value</span></span>

<span data-ttu-id="418ec-115">Параметр *x* или *y* , в зависимости от наименьшего значения.</span><span class="sxs-lookup"><span data-stu-id="418ec-115">The *x* or *y* parameter, whichever is the smallest value.</span></span>


## <a name="remarks"></a><span data-ttu-id="418ec-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="418ec-116">Remarks</span></span>

<span data-ttu-id="418ec-117">Нормали обрабатываются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="418ec-117">Denormals are handled as follows:</span></span>

| <span data-ttu-id="418ec-118">src0 src1 — ></span><span class="sxs-lookup"><span data-stu-id="418ec-118">src0 src1-></span></span> | <span data-ttu-id="418ec-119">-inf</span><span class="sxs-lookup"><span data-stu-id="418ec-119">-inf</span></span> | <span data-ttu-id="418ec-120">C</span><span class="sxs-lookup"><span data-stu-id="418ec-120">F</span></span>             | <span data-ttu-id="418ec-121">+inf</span><span class="sxs-lookup"><span data-stu-id="418ec-121">+inf</span></span> | <span data-ttu-id="418ec-122">Не число</span><span class="sxs-lookup"><span data-stu-id="418ec-122">NAN</span></span>  |
|-------------|------|---------------|------|------|
| <span data-ttu-id="418ec-123">-inf</span><span class="sxs-lookup"><span data-stu-id="418ec-123">-inf</span></span>        | <span data-ttu-id="418ec-124">-inf</span><span class="sxs-lookup"><span data-stu-id="418ec-124">-inf</span></span> | <span data-ttu-id="418ec-125">-inf</span><span class="sxs-lookup"><span data-stu-id="418ec-125">-inf</span></span>          | <span data-ttu-id="418ec-126">-inf</span><span class="sxs-lookup"><span data-stu-id="418ec-126">-inf</span></span> | <span data-ttu-id="418ec-127">-inf</span><span class="sxs-lookup"><span data-stu-id="418ec-127">-inf</span></span> |
| <span data-ttu-id="418ec-128">C</span><span class="sxs-lookup"><span data-stu-id="418ec-128">F</span></span>           | <span data-ttu-id="418ec-129">-inf</span><span class="sxs-lookup"><span data-stu-id="418ec-129">-inf</span></span> | <span data-ttu-id="418ec-130">src0 или src1</span><span class="sxs-lookup"><span data-stu-id="418ec-130">src0 or src1</span></span>  | <span data-ttu-id="418ec-131">src0</span><span class="sxs-lookup"><span data-stu-id="418ec-131">src0</span></span> | <span data-ttu-id="418ec-132">src0</span><span class="sxs-lookup"><span data-stu-id="418ec-132">src0</span></span> |
| <span data-ttu-id="418ec-133">+inf</span><span class="sxs-lookup"><span data-stu-id="418ec-133">+inf</span></span>        | <span data-ttu-id="418ec-134">-inf</span><span class="sxs-lookup"><span data-stu-id="418ec-134">-inf</span></span> | <span data-ttu-id="418ec-135">src1</span><span class="sxs-lookup"><span data-stu-id="418ec-135">src1</span></span>          | <span data-ttu-id="418ec-136">+inf</span><span class="sxs-lookup"><span data-stu-id="418ec-136">+inf</span></span> | <span data-ttu-id="418ec-137">+inf</span><span class="sxs-lookup"><span data-stu-id="418ec-137">+inf</span></span> |
| <span data-ttu-id="418ec-138">не число</span><span class="sxs-lookup"><span data-stu-id="418ec-138">NaN</span></span>         | <span data-ttu-id="418ec-139">-inf</span><span class="sxs-lookup"><span data-stu-id="418ec-139">-inf</span></span> | <span data-ttu-id="418ec-140">src1</span><span class="sxs-lookup"><span data-stu-id="418ec-140">src1</span></span>          | <span data-ttu-id="418ec-141">+inf</span><span class="sxs-lookup"><span data-stu-id="418ec-141">+inf</span></span> | <span data-ttu-id="418ec-142">не число</span><span class="sxs-lookup"><span data-stu-id="418ec-142">NaN</span></span>  |

<span data-ttu-id="418ec-143">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="418ec-143">F means finite-real number.</span></span>


## <a name="type-description"></a><span data-ttu-id="418ec-144">Описание типа</span><span class="sxs-lookup"><span data-stu-id="418ec-144">Type Description</span></span>

| <span data-ttu-id="418ec-145">Имя</span><span class="sxs-lookup"><span data-stu-id="418ec-145">Name</span></span> | <span data-ttu-id="418ec-146">В/Из</span><span class="sxs-lookup"><span data-stu-id="418ec-146">In/Out</span></span>      | [<span data-ttu-id="418ec-147">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="418ec-147">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="418ec-148">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="418ec-148">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="418ec-149">Размер</span><span class="sxs-lookup"><span data-stu-id="418ec-149">Size</span></span>                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="418ec-150">x</span><span class="sxs-lookup"><span data-stu-id="418ec-150">x</span></span>    | <span data-ttu-id="418ec-151">in</span><span class="sxs-lookup"><span data-stu-id="418ec-151">in</span></span>          | <span data-ttu-id="418ec-152">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="418ec-152">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="418ec-153">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="418ec-153">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="418ec-154">any</span><span class="sxs-lookup"><span data-stu-id="418ec-154">any</span></span>                          |
| <span data-ttu-id="418ec-155">да</span><span class="sxs-lookup"><span data-stu-id="418ec-155">y</span></span>    | <span data-ttu-id="418ec-156">in</span><span class="sxs-lookup"><span data-stu-id="418ec-156">in</span></span>          | <span data-ttu-id="418ec-157">то же, что входные данные x</span><span class="sxs-lookup"><span data-stu-id="418ec-157">same as input x</span></span>                                                                                                | <span data-ttu-id="418ec-158">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="418ec-158">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="418ec-159">те же измерения, что и входные x</span><span class="sxs-lookup"><span data-stu-id="418ec-159">same dimension(s) as input x</span></span> |
| <span data-ttu-id="418ec-160">обратно</span><span class="sxs-lookup"><span data-stu-id="418ec-160">ret</span></span>  | <span data-ttu-id="418ec-161">тип возвращаемого значения;</span><span class="sxs-lookup"><span data-stu-id="418ec-161">return type</span></span> | <span data-ttu-id="418ec-162">то же, что входные данные x</span><span class="sxs-lookup"><span data-stu-id="418ec-162">same as input x</span></span>                                                                                                | <span data-ttu-id="418ec-163">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="418ec-163">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="418ec-164">те же измерения, что и входные x</span><span class="sxs-lookup"><span data-stu-id="418ec-164">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="418ec-165">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="418ec-165">Minimum Shader Model</span></span>

<span data-ttu-id="418ec-166">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="418ec-166">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="418ec-167">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="418ec-167">Shader Model</span></span>                                                                       | <span data-ttu-id="418ec-168">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="418ec-168">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="418ec-169">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="418ec-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="418ec-170">да</span><span class="sxs-lookup"><span data-stu-id="418ec-170">yes</span></span>                         |
| [<span data-ttu-id="418ec-171">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="418ec-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="418ec-172">Да (VS \_ 1 \_ 1 и PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="418ec-172">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="418ec-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="418ec-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="418ec-174">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="418ec-174">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[<span data-ttu-id="418ec-175">**Функциональная спецификация DirectX**</span><span class="sxs-lookup"><span data-stu-id="418ec-175">**DirectX Functional Specification**</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MIN)