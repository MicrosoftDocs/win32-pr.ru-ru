---
title: фрак
description: Возвращает дробную (или десятичную) часть x; значение больше или равно 0 и меньше 1.
ms.assetid: 4e85390f-2b1a-402b-b932-09b80097f7e6
keywords:
- фрак HLSL
topic_type:
- apiref
api_name:
- frac
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 468bddc34f22f9bb5f34871102678e1765148b11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488217"
---
# <a name="frac"></a><span data-ttu-id="77b02-104">фрак</span><span class="sxs-lookup"><span data-stu-id="77b02-104">frac</span></span>

<span data-ttu-id="77b02-105">Возвращает дробную (или десятичную) часть x; значение больше или равно 0 и меньше 1.</span><span class="sxs-lookup"><span data-stu-id="77b02-105">Returns the fractional (or decimal) part of x; which is greater than or equal to 0 and less than 1.</span></span>

<span data-ttu-id="77b02-106">См. также [TRUNC](./dx-graphics-hlsl-trunc.md).</span><span class="sxs-lookup"><span data-stu-id="77b02-106">Also see [trunc](./dx-graphics-hlsl-trunc.md).</span></span>

| <span data-ttu-id="77b02-107">*RET* фрак (*x*)</span><span class="sxs-lookup"><span data-stu-id="77b02-107">*ret* frac(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="77b02-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="77b02-108">Parameters</span></span>



| <span data-ttu-id="77b02-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="77b02-109">Item</span></span>                                                   | <span data-ttu-id="77b02-110">Описание</span><span class="sxs-lookup"><span data-stu-id="77b02-110">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="77b02-111"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="77b02-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="77b02-112">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="77b02-112">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="77b02-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77b02-113">Return Value</span></span>

<span data-ttu-id="77b02-114">Дробная часть параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="77b02-114">The fractional part of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="77b02-115">Описание типа</span><span class="sxs-lookup"><span data-stu-id="77b02-115">Type Description</span></span>



| <span data-ttu-id="77b02-116">Имя</span><span class="sxs-lookup"><span data-stu-id="77b02-116">Name</span></span>  | [<span data-ttu-id="77b02-117">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="77b02-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="77b02-118">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="77b02-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="77b02-119">Размер</span><span class="sxs-lookup"><span data-stu-id="77b02-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="77b02-120">*x*</span><span class="sxs-lookup"><span data-stu-id="77b02-120">*x*</span></span>   | <span data-ttu-id="77b02-121">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="77b02-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="77b02-122">**float**</span><span class="sxs-lookup"><span data-stu-id="77b02-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="77b02-123">any</span><span class="sxs-lookup"><span data-stu-id="77b02-123">any</span></span>                            |
| <span data-ttu-id="77b02-124">*обратно*</span><span class="sxs-lookup"><span data-stu-id="77b02-124">*ret*</span></span> | <span data-ttu-id="77b02-125">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="77b02-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="77b02-126">**float**</span><span class="sxs-lookup"><span data-stu-id="77b02-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="77b02-127">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="77b02-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="77b02-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="77b02-128">Minimum Shader Model</span></span>

<span data-ttu-id="77b02-129">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="77b02-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="77b02-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="77b02-130">Shader Model</span></span>                                                                       | <span data-ttu-id="77b02-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="77b02-131">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="77b02-132">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="77b02-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="77b02-133">да</span><span class="sxs-lookup"><span data-stu-id="77b02-133">yes</span></span>       |
| [<span data-ttu-id="77b02-134">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="77b02-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="77b02-135">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77b02-135">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="77b02-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77b02-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77b02-137">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="77b02-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

