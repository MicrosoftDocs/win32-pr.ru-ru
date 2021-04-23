---
title: фиксаци
description: Отменяет указанное значение до указанного минимального и максимального диапазона.
ms.assetid: bcfafcec-3f9c-4b65-950c-da34184d5cdb
keywords:
- HLSL среза
topic_type:
- apiref
api_name:
- clamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d6b0a3e83c0b1a5e511aba96df03b828b90c11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793308"
---
# <a name="clamp"></a><span data-ttu-id="0bcab-104">фиксаци</span><span class="sxs-lookup"><span data-stu-id="0bcab-104">clamp</span></span>

<span data-ttu-id="0bcab-105">Отменяет указанное значение до указанного минимального и максимального диапазона.</span><span class="sxs-lookup"><span data-stu-id="0bcab-105">Clamps the specified value to the specified minimum and maximum range.</span></span>



| <span data-ttu-id="0bcab-106">*RET* -зажим (*x*, *min*, *Max*)</span><span class="sxs-lookup"><span data-stu-id="0bcab-106">*ret* clamp(*x*, *min*, *max*)</span></span> |
|--------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="0bcab-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bcab-107">Parameters</span></span>



| <span data-ttu-id="0bcab-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="0bcab-108">Item</span></span>                                                         | <span data-ttu-id="0bcab-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0bcab-109">Description</span></span>                                    |
|--------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="0bcab-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="0bcab-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="0bcab-111">\[в \] значении для среза.</span><span class="sxs-lookup"><span data-stu-id="0bcab-111">\[in\] A value to clamp.</span></span><br/>            |
| <span data-ttu-id="0bcab-112"><span id="min"></span><span id="MIN"></span>*минимум*</span><span class="sxs-lookup"><span data-stu-id="0bcab-112"><span id="min"></span><span id="MIN"></span>*min*</span></span><br/> | <span data-ttu-id="0bcab-113">\[в \] указанном минимальном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="0bcab-113">\[in\] The specified minimum range.</span></span><br/> |
| <span data-ttu-id="0bcab-114"><span id="max"></span><span id="MAX"></span>*максимальной*</span><span class="sxs-lookup"><span data-stu-id="0bcab-114"><span id="max"></span><span id="MAX"></span>*max*</span></span><br/> | <span data-ttu-id="0bcab-115">\[в \] указанном максимальном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="0bcab-115">\[in\] The specified maximum range.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0bcab-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0bcab-116">Return Value</span></span>

<span data-ttu-id="0bcab-117">Значение среза для параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="0bcab-117">The clamped value for the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bcab-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="0bcab-118">Remarks</span></span>

<span data-ttu-id="0bcab-119">Для значений параметра-INF или INF будет вести себя так, как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="0bcab-119">For values of -INF or INF, clamp will behave as expected.</span></span> <span data-ttu-id="0bcab-120">Однако для значений NaN результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="0bcab-120">However for values of NaN, the results are undefined.</span></span>

## <a name="type-description"></a><span data-ttu-id="0bcab-121">Описание типа</span><span class="sxs-lookup"><span data-stu-id="0bcab-121">Type Description</span></span>



| <span data-ttu-id="0bcab-122">Имя</span><span class="sxs-lookup"><span data-stu-id="0bcab-122">Name</span></span>  | [<span data-ttu-id="0bcab-123">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="0bcab-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="0bcab-124">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="0bcab-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="0bcab-125">Размер</span><span class="sxs-lookup"><span data-stu-id="0bcab-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="0bcab-126">*x*</span><span class="sxs-lookup"><span data-stu-id="0bcab-126">*x*</span></span>   | <span data-ttu-id="0bcab-127">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="0bcab-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="0bcab-128">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="0bcab-128">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="0bcab-129">any</span><span class="sxs-lookup"><span data-stu-id="0bcab-129">any</span></span>                            |
| <span data-ttu-id="0bcab-130">*min*</span><span class="sxs-lookup"><span data-stu-id="0bcab-130">*min*</span></span> | <span data-ttu-id="0bcab-131">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="0bcab-131">same as input *x*</span></span>                                                                                              | <span data-ttu-id="0bcab-132">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="0bcab-132">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="0bcab-133">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="0bcab-133">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="0bcab-134">*max*</span><span class="sxs-lookup"><span data-stu-id="0bcab-134">*max*</span></span> | <span data-ttu-id="0bcab-135">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="0bcab-135">same as input *x*</span></span>                                                                                              | <span data-ttu-id="0bcab-136">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="0bcab-136">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="0bcab-137">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="0bcab-137">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="0bcab-138">*обратно*</span><span class="sxs-lookup"><span data-stu-id="0bcab-138">*ret*</span></span> | <span data-ttu-id="0bcab-139">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="0bcab-139">same as input *x*</span></span>                                                                                              | <span data-ttu-id="0bcab-140">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="0bcab-140">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="0bcab-141">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="0bcab-141">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0bcab-142">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0bcab-142">Minimum Shader Model</span></span>

<span data-ttu-id="0bcab-143">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="0bcab-143">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0bcab-144">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0bcab-144">Shader Model</span></span>                                                                       | <span data-ttu-id="0bcab-145">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="0bcab-145">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="0bcab-146">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="0bcab-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="0bcab-147">да</span><span class="sxs-lookup"><span data-stu-id="0bcab-147">yes</span></span>                   |
| [<span data-ttu-id="0bcab-148">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bcab-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="0bcab-149">VS \_ 1 \_ 1 и PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="0bcab-149">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="0bcab-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0bcab-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bcab-151">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0bcab-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

