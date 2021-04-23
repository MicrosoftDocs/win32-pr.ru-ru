---
title: modf (Корекрт \_ Math. h)
description: Разделяет значение x на дробные и целые части, каждый из которых имеет тот же знак, что и x.
ms.assetid: 0cac1cf3-f0da-4b0a-ba30-4af5d65b04b2
keywords:
- modf HLSL
topic_type:
- apiref
api_name:
- modf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5079549e70414f8237fd33a5e263dd8f17dcb9e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000405"
---
# <a name="modf"></a><span data-ttu-id="fdd23-104">modf</span><span class="sxs-lookup"><span data-stu-id="fdd23-104">modf</span></span>

<span data-ttu-id="fdd23-105">Разделяет значение x на дробные и целые части, каждый из которых имеет тот же знак, что и x.</span><span class="sxs-lookup"><span data-stu-id="fdd23-105">Splits the value x into fractional and integer parts, each of which has the same sign as x.</span></span>



| <span data-ttu-id="fdd23-106">RET modf (x, out IP)</span><span class="sxs-lookup"><span data-stu-id="fdd23-106">ret modf(x, out ip)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="fdd23-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fdd23-107">Parameters</span></span>



| <span data-ttu-id="fdd23-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="fdd23-108">Item</span></span>                                                      | <span data-ttu-id="fdd23-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fdd23-109">Description</span></span>                                    |
|-----------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="fdd23-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="fdd23-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/>    | <span data-ttu-id="fdd23-111">\[в \] входном значении x.</span><span class="sxs-lookup"><span data-stu-id="fdd23-111">\[in\] The x input value.</span></span><br/>           |
| <span data-ttu-id="fdd23-112"><span id="ip"></span><span id="IP"></span>*см*</span><span class="sxs-lookup"><span data-stu-id="fdd23-112"><span id="ip"></span><span id="IP"></span>*ip*</span></span><br/> | <span data-ttu-id="fdd23-113">\[\]вычислить целую часть *x*.</span><span class="sxs-lookup"><span data-stu-id="fdd23-113">\[out\] The integer portion of *x*.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="fdd23-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fdd23-114">Return Value</span></span>

<span data-ttu-id="fdd23-115">Дробная часть x.</span><span class="sxs-lookup"><span data-stu-id="fdd23-115">The signed-fractional portion of x.</span></span>

## <a name="type-description"></a><span data-ttu-id="fdd23-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="fdd23-116">Type Description</span></span>



| <span data-ttu-id="fdd23-117">Имя</span><span class="sxs-lookup"><span data-stu-id="fdd23-117">Name</span></span> | <span data-ttu-id="fdd23-118">В/Из</span><span class="sxs-lookup"><span data-stu-id="fdd23-118">In/Out</span></span> | [<span data-ttu-id="fdd23-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="fdd23-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="fdd23-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="fdd23-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="fdd23-121">Размер</span><span class="sxs-lookup"><span data-stu-id="fdd23-121">Size</span></span>                         |
|------|--------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="fdd23-122">x</span><span class="sxs-lookup"><span data-stu-id="fdd23-122">x</span></span>    | <span data-ttu-id="fdd23-123">in</span><span class="sxs-lookup"><span data-stu-id="fdd23-123">in</span></span>     | <span data-ttu-id="fdd23-124">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="fdd23-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="fdd23-125">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="fdd23-125">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="fdd23-126">any</span><span class="sxs-lookup"><span data-stu-id="fdd23-126">any</span></span>                          |
| <span data-ttu-id="fdd23-127">см</span><span class="sxs-lookup"><span data-stu-id="fdd23-127">ip</span></span>   | <span data-ttu-id="fdd23-128">out</span><span class="sxs-lookup"><span data-stu-id="fdd23-128">out</span></span>    | <span data-ttu-id="fdd23-129">то же, что входные данные x</span><span class="sxs-lookup"><span data-stu-id="fdd23-129">same as input x</span></span>                                                                                                | <span data-ttu-id="fdd23-130">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="fdd23-130">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="fdd23-131">те же измерения, что и входные x</span><span class="sxs-lookup"><span data-stu-id="fdd23-131">same dimension(s) as input x</span></span> |
| <span data-ttu-id="fdd23-132">обратно</span><span class="sxs-lookup"><span data-stu-id="fdd23-132">ret</span></span>  | <span data-ttu-id="fdd23-133">out</span><span class="sxs-lookup"><span data-stu-id="fdd23-133">out</span></span>    | <span data-ttu-id="fdd23-134">то же, что входные данные x</span><span class="sxs-lookup"><span data-stu-id="fdd23-134">same as input x</span></span>                                                                                                | <span data-ttu-id="fdd23-135">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="fdd23-135">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="fdd23-136">те же измерения, что и входные x</span><span class="sxs-lookup"><span data-stu-id="fdd23-136">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fdd23-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fdd23-137">Minimum Shader Model</span></span>

<span data-ttu-id="fdd23-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="fdd23-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fdd23-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fdd23-139">Shader Model</span></span>                                                                       | <span data-ttu-id="fdd23-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="fdd23-140">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="fdd23-141">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="fdd23-141">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="fdd23-142">да</span><span class="sxs-lookup"><span data-stu-id="fdd23-142">yes</span></span>                 |
| [<span data-ttu-id="fdd23-143">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdd23-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="fdd23-144">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="fdd23-144">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="fdd23-145">Требования</span><span class="sxs-lookup"><span data-stu-id="fdd23-145">Requirements</span></span>



| <span data-ttu-id="fdd23-146">Требование</span><span class="sxs-lookup"><span data-stu-id="fdd23-146">Requirement</span></span> | <span data-ttu-id="fdd23-147">Значение</span><span class="sxs-lookup"><span data-stu-id="fdd23-147">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd23-148">Header</span><span class="sxs-lookup"><span data-stu-id="fdd23-148">Header</span></span><br/> | <dl> <span data-ttu-id="fdd23-149"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdd23-149"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdd23-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fdd23-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd23-151">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="fdd23-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

