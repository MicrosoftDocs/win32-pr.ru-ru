---
title: ceil (Корекрт \_ Math. h)
description: Возвращает наименьшее целочисленное значение, которое больше или равно указанному значению.
ms.assetid: 9823f321-14c3-4b27-9a4b-7a885cece39b
keywords:
- ceil HLSL
topic_type:
- apiref
api_name:
- ceil
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec86db320119b7f162ed48a748c1d1ff4335b6f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998360"
---
# <a name="ceil"></a><span data-ttu-id="11f56-104">ceil</span><span class="sxs-lookup"><span data-stu-id="11f56-104">ceil</span></span>

<span data-ttu-id="11f56-105">Возвращает наименьшее целочисленное значение, которое больше или равно указанному значению.</span><span class="sxs-lookup"><span data-stu-id="11f56-105">Returns the smallest integer value that is greater than or equal to the specified value.</span></span>



| <span data-ttu-id="11f56-106">*RET* ceil (*x*)</span><span class="sxs-lookup"><span data-stu-id="11f56-106">*ret* ceil(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="11f56-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="11f56-107">Parameters</span></span>



| <span data-ttu-id="11f56-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="11f56-108">Item</span></span>                                                   | <span data-ttu-id="11f56-109">Описание</span><span class="sxs-lookup"><span data-stu-id="11f56-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="11f56-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="11f56-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="11f56-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="11f56-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="11f56-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11f56-112">Return Value</span></span>

<span data-ttu-id="11f56-113">Наименьшее целочисленное значение (возвращаемое как тип с плавающей запятой), которое больше или равно значению параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="11f56-113">The smallest integer value (returned as a floating-point type) that is greater than or equal to the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="11f56-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="11f56-114">Type Description</span></span>



| <span data-ttu-id="11f56-115">Имя</span><span class="sxs-lookup"><span data-stu-id="11f56-115">Name</span></span>  | [<span data-ttu-id="11f56-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="11f56-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="11f56-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="11f56-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="11f56-118">Размер</span><span class="sxs-lookup"><span data-stu-id="11f56-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="11f56-119">*x*</span><span class="sxs-lookup"><span data-stu-id="11f56-119">*x*</span></span>   | <span data-ttu-id="11f56-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="11f56-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="11f56-121">**float**</span><span class="sxs-lookup"><span data-stu-id="11f56-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="11f56-122">any</span><span class="sxs-lookup"><span data-stu-id="11f56-122">any</span></span>                            |
| <span data-ttu-id="11f56-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="11f56-123">*ret*</span></span> | <span data-ttu-id="11f56-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="11f56-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="11f56-125">**float**</span><span class="sxs-lookup"><span data-stu-id="11f56-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="11f56-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="11f56-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="11f56-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="11f56-127">Minimum Shader Model</span></span>

<span data-ttu-id="11f56-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="11f56-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="11f56-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="11f56-129">Shader Model</span></span>                                                                       | <span data-ttu-id="11f56-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="11f56-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="11f56-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="11f56-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="11f56-132">да</span><span class="sxs-lookup"><span data-stu-id="11f56-132">yes</span></span>       |
| [<span data-ttu-id="11f56-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11f56-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="11f56-134">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="11f56-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="11f56-135">Требования</span><span class="sxs-lookup"><span data-stu-id="11f56-135">Requirements</span></span>



| <span data-ttu-id="11f56-136">Требование</span><span class="sxs-lookup"><span data-stu-id="11f56-136">Requirement</span></span> | <span data-ttu-id="11f56-137">Значение</span><span class="sxs-lookup"><span data-stu-id="11f56-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f56-138">Header</span><span class="sxs-lookup"><span data-stu-id="11f56-138">Header</span></span><br/> | <dl> <span data-ttu-id="11f56-139"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="11f56-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11f56-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11f56-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f56-141">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="11f56-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

