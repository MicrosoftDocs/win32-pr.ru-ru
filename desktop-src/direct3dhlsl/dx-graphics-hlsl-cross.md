---
title: перекрестные
description: Возвращает перекрестное произведение двух трехмерных векторов с плавающей точкой.
ms.assetid: 5f1832af-6bc5-49a7-956a-fd762f674f5f
keywords:
- перекрестное HLSL
topic_type:
- apiref
api_name:
- cross
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91959bf415c3e56edf370942de268523bf998743
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997158"
---
# <a name="cross"></a><span data-ttu-id="2db3a-104">перекрестные</span><span class="sxs-lookup"><span data-stu-id="2db3a-104">cross</span></span>

<span data-ttu-id="2db3a-105">Возвращает перекрестное произведение двух трехмерных векторов с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="2db3a-105">Returns the cross product of two floating-point, 3D vectors.</span></span>



| <span data-ttu-id="2db3a-106">*RET* перекрестие (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="2db3a-106">*ret* cross(*x*, *y*)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="2db3a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2db3a-107">Parameters</span></span>



| <span data-ttu-id="2db3a-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="2db3a-108">Item</span></span>                                                   | <span data-ttu-id="2db3a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2db3a-109">Description</span></span>                                             |
|--------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="2db3a-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="2db3a-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="2db3a-111">\[в \] первом трехмерном векторе с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="2db3a-111">\[in\] The first floating-point, 3D vector.</span></span><br/>  |
| <span data-ttu-id="2db3a-112"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="2db3a-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="2db3a-113">\[во \] втором трехмерном векторе с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="2db3a-113">\[in\] The second floating-point, 3D vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="2db3a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2db3a-114">Return Value</span></span>

<span data-ttu-id="2db3a-115">Перекрестное произведение параметра *x* и параметра *y* .</span><span class="sxs-lookup"><span data-stu-id="2db3a-115">The cross product of the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="2db3a-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="2db3a-116">Type Description</span></span>



| <span data-ttu-id="2db3a-117">Имя</span><span class="sxs-lookup"><span data-stu-id="2db3a-117">Name</span></span>  | [<span data-ttu-id="2db3a-118">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="2db3a-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="2db3a-119">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="2db3a-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="2db3a-120">Размер</span><span class="sxs-lookup"><span data-stu-id="2db3a-120">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="2db3a-121">*x*</span><span class="sxs-lookup"><span data-stu-id="2db3a-121">*x*</span></span>   | [<span data-ttu-id="2db3a-122">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="2db3a-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="2db3a-123">**float**</span><span class="sxs-lookup"><span data-stu-id="2db3a-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2db3a-124">3</span><span class="sxs-lookup"><span data-stu-id="2db3a-124">3</span></span>    |
| <span data-ttu-id="2db3a-125">*y*</span><span class="sxs-lookup"><span data-stu-id="2db3a-125">*y*</span></span>   | [<span data-ttu-id="2db3a-126">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="2db3a-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="2db3a-127">**float**</span><span class="sxs-lookup"><span data-stu-id="2db3a-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2db3a-128">3</span><span class="sxs-lookup"><span data-stu-id="2db3a-128">3</span></span>    |
| <span data-ttu-id="2db3a-129">*обратно*</span><span class="sxs-lookup"><span data-stu-id="2db3a-129">*ret*</span></span> | [<span data-ttu-id="2db3a-130">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="2db3a-130">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="2db3a-131">**float**</span><span class="sxs-lookup"><span data-stu-id="2db3a-131">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2db3a-132">3</span><span class="sxs-lookup"><span data-stu-id="2db3a-132">3</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2db3a-133">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2db3a-133">Minimum Shader Model</span></span>

<span data-ttu-id="2db3a-134">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="2db3a-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2db3a-135">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2db3a-135">Shader Model</span></span>                                                                       | <span data-ttu-id="2db3a-136">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="2db3a-136">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="2db3a-137">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="2db3a-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="2db3a-138">да</span><span class="sxs-lookup"><span data-stu-id="2db3a-138">yes</span></span>                   |
| [<span data-ttu-id="2db3a-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2db3a-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="2db3a-140">VS \_ 1 \_ 1 и PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="2db3a-140">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="2db3a-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2db3a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db3a-142">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="2db3a-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

