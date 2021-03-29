---
title: Floor (Корекрт \_ Math. h)
description: Возвращает максимальное целое число, которое меньше или равно указанному значению.
ms.assetid: f7193425-2448-4ae6-99d5-bb5e1aa74111
keywords:
- HLSL этажа
topic_type:
- apiref
api_name:
- floor
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ecb46719d5361ec9f7c36b21d94793bc9a67ffe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986858"
---
# <a name="floor"></a><span data-ttu-id="b677d-104">floor</span><span class="sxs-lookup"><span data-stu-id="b677d-104">floor</span></span>

<span data-ttu-id="b677d-105">Возвращает максимальное целое число, которое меньше или равно указанному значению.</span><span class="sxs-lookup"><span data-stu-id="b677d-105">Returns the largest integer that is less than or equal to the specified value.</span></span>



| <span data-ttu-id="b677d-106">*RET* -этаж (*x*)</span><span class="sxs-lookup"><span data-stu-id="b677d-106">*ret* floor(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="b677d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b677d-107">Parameters</span></span>



| <span data-ttu-id="b677d-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="b677d-108">Item</span></span>                                                   | <span data-ttu-id="b677d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b677d-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="b677d-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b677d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b677d-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="b677d-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b677d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b677d-112">Return Value</span></span>

<span data-ttu-id="b677d-113">Максимальное целочисленное значение (возвращаемое как тип с плавающей запятой), которое меньше или равно значению параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="b677d-113">The largest integer value (returned as a floating-point type) that is less than or equal to the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="b677d-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="b677d-114">Type Description</span></span>



| <span data-ttu-id="b677d-115">Имя</span><span class="sxs-lookup"><span data-stu-id="b677d-115">Name</span></span>  | [<span data-ttu-id="b677d-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="b677d-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b677d-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="b677d-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b677d-118">Размер</span><span class="sxs-lookup"><span data-stu-id="b677d-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b677d-119">*x*</span><span class="sxs-lookup"><span data-stu-id="b677d-119">*x*</span></span>   | <span data-ttu-id="b677d-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="b677d-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="b677d-121">**float**</span><span class="sxs-lookup"><span data-stu-id="b677d-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b677d-122">any</span><span class="sxs-lookup"><span data-stu-id="b677d-122">any</span></span>                            |
| <span data-ttu-id="b677d-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="b677d-123">*ret*</span></span> | <span data-ttu-id="b677d-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="b677d-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b677d-125">**float**</span><span class="sxs-lookup"><span data-stu-id="b677d-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b677d-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="b677d-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b677d-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b677d-127">Minimum Shader Model</span></span>

<span data-ttu-id="b677d-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="b677d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b677d-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b677d-129">Shader Model</span></span>                                                                       | <span data-ttu-id="b677d-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="b677d-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b677d-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="b677d-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b677d-132">да</span><span class="sxs-lookup"><span data-stu-id="b677d-132">yes</span></span>       |
| [<span data-ttu-id="b677d-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b677d-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b677d-134">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b677d-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="b677d-135">Требования</span><span class="sxs-lookup"><span data-stu-id="b677d-135">Requirements</span></span>



| <span data-ttu-id="b677d-136">Требование</span><span class="sxs-lookup"><span data-stu-id="b677d-136">Requirement</span></span> | <span data-ttu-id="b677d-137">Значение</span><span class="sxs-lookup"><span data-stu-id="b677d-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b677d-138">Header</span><span class="sxs-lookup"><span data-stu-id="b677d-138">Header</span></span><br/> | <dl> <span data-ttu-id="b677d-139"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b677d-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b677d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b677d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b677d-141">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b677d-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

