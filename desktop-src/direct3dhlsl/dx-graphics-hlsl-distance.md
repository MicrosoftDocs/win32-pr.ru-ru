---
title: distance
description: Возвращает скалярное расстояние между двумя векторами.
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- Расстояние HLSL
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0f3a64778666ac8f7de16b91eed202e36e90ed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338076"
---
# <a name="distance"></a><span data-ttu-id="6b16f-104">distance</span><span class="sxs-lookup"><span data-stu-id="6b16f-104">distance</span></span>

<span data-ttu-id="6b16f-105">Возвращает скалярное расстояние между двумя векторами.</span><span class="sxs-lookup"><span data-stu-id="6b16f-105">Returns a distance scalar between two vectors.</span></span>



| <span data-ttu-id="6b16f-106">Расстояние *RET* (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="6b16f-106">*ret* distance(*x*, *y*)</span></span> |
|--------------------------|



 

## <a name="parameters"></a><span data-ttu-id="6b16f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b16f-107">Parameters</span></span>



| <span data-ttu-id="6b16f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="6b16f-108">Item</span></span>                                                   | <span data-ttu-id="6b16f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6b16f-109">Description</span></span>                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="6b16f-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="6b16f-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="6b16f-111">\[в \] первом сравниваемом векторе с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="6b16f-111">\[in\] The first floating-point vector to compare.</span></span><br/>  |
| <span data-ttu-id="6b16f-112"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="6b16f-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="6b16f-113">\[во \] втором сравниваемом векторе с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="6b16f-113">\[in\] The second floating-point vector to compare.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="6b16f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b16f-114">Return Value</span></span>

<span data-ttu-id="6b16f-115">Скалярное значение с плавающей запятой, представляющее расстояние между параметром *x* и параметром *y* .</span><span class="sxs-lookup"><span data-stu-id="6b16f-115">A floating-point, scalar value that represents the distance between the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="6b16f-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="6b16f-116">Type Description</span></span>



| <span data-ttu-id="6b16f-117">Имя</span><span class="sxs-lookup"><span data-stu-id="6b16f-117">Name</span></span>  | [<span data-ttu-id="6b16f-118">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="6b16f-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="6b16f-119">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="6b16f-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6b16f-120">Размер</span><span class="sxs-lookup"><span data-stu-id="6b16f-120">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="6b16f-121">*x*</span><span class="sxs-lookup"><span data-stu-id="6b16f-121">*x*</span></span>   | [<span data-ttu-id="6b16f-122">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="6b16f-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6b16f-123">**float**</span><span class="sxs-lookup"><span data-stu-id="6b16f-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6b16f-124">any</span><span class="sxs-lookup"><span data-stu-id="6b16f-124">any</span></span>                            |
| <span data-ttu-id="6b16f-125">*y*</span><span class="sxs-lookup"><span data-stu-id="6b16f-125">*y*</span></span>   | [<span data-ttu-id="6b16f-126">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="6b16f-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6b16f-127">**float**</span><span class="sxs-lookup"><span data-stu-id="6b16f-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6b16f-128">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="6b16f-128">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="6b16f-129">*обратно*</span><span class="sxs-lookup"><span data-stu-id="6b16f-129">*ret*</span></span> | [<span data-ttu-id="6b16f-130">**скаляр**</span><span class="sxs-lookup"><span data-stu-id="6b16f-130">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6b16f-131">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="6b16f-131">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6b16f-132">1</span><span class="sxs-lookup"><span data-stu-id="6b16f-132">1</span></span>                              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6b16f-133">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6b16f-133">Minimum Shader Model</span></span>

<span data-ttu-id="6b16f-134">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="6b16f-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6b16f-135">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6b16f-135">Shader Model</span></span>                                                                       | <span data-ttu-id="6b16f-136">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="6b16f-136">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6b16f-137">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="6b16f-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="6b16f-138">да</span><span class="sxs-lookup"><span data-stu-id="6b16f-138">yes</span></span>       |
| [<span data-ttu-id="6b16f-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b16f-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="6b16f-140">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="6b16f-140">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="6b16f-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b16f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b16f-142">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="6b16f-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

