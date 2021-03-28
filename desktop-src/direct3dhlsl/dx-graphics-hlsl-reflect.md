---
title: характеризу
description: Возвращает вектор отражения с использованием лучей инцидента и нормали к поверхности.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- отражение HLSL
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46c981f636a797ecc4e0dd341ce44ed886c202cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793596"
---
# <a name="reflect"></a><span data-ttu-id="fbb0e-104">характеризу</span><span class="sxs-lookup"><span data-stu-id="fbb0e-104">reflect</span></span>

<span data-ttu-id="fbb0e-105">Возвращает вектор отражения с использованием лучей инцидента и нормали к поверхности.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-105">Returns a reflection vector using an incident ray and a surface normal.</span></span>



| <span data-ttu-id="fbb0e-106">отражение *RET* (*i*, *n*)</span><span class="sxs-lookup"><span data-stu-id="fbb0e-106">*ret* reflect(*i*, *n*)</span></span> |
|-------------------------|



 

## <a name="parameters"></a><span data-ttu-id="fbb0e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbb0e-107">Parameters</span></span>



| <span data-ttu-id="fbb0e-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="fbb0e-108">Item</span></span>                                                   | <span data-ttu-id="fbb0e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fbb0e-109">Description</span></span>                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fbb0e-110"><span id="i"></span><span id="I"></span>*сохранении*</span><span class="sxs-lookup"><span data-stu-id="fbb0e-110"><span id="i"></span><span id="I"></span>*i*</span></span><br/> | <span data-ttu-id="fbb0e-111">\[в \] векторе инцидента с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-111">\[in\] A floating-point, incident vector.</span></span><br/> |
| <span data-ttu-id="fbb0e-112"><span id="n"></span><span id="N"></span>*\n*</span><span class="sxs-lookup"><span data-stu-id="fbb0e-112"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="fbb0e-113">\[в \] векторе с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-113">\[in\] A floating-point, normal vector.</span></span><br/>   |



 

## <a name="return-value"></a><span data-ttu-id="fbb0e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fbb0e-114">Return Value</span></span>

<span data-ttu-id="fbb0e-115">Вектор отражения с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-115">A floating-point, reflection vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbb0e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="fbb0e-116">Remarks</span></span>

<span data-ttu-id="fbb0e-117">Эта функция вычисляет Вектор отражения, используя следующую формулу: v = i-2 \* n \* Dot (i n).</span><span class="sxs-lookup"><span data-stu-id="fbb0e-117">This function calculates the reflection vector using the following formula: v = i - 2 \* n \* dot(i n) .</span></span>

## <a name="type-description"></a><span data-ttu-id="fbb0e-118">Описание типа</span><span class="sxs-lookup"><span data-stu-id="fbb0e-118">Type Description</span></span>



| <span data-ttu-id="fbb0e-119">Имя</span><span class="sxs-lookup"><span data-stu-id="fbb0e-119">Name</span></span>  | [<span data-ttu-id="fbb0e-120">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="fbb0e-121">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="fbb0e-122">Размер</span><span class="sxs-lookup"><span data-stu-id="fbb0e-122">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="fbb0e-123">*i*</span><span class="sxs-lookup"><span data-stu-id="fbb0e-123">*i*</span></span>   | [<span data-ttu-id="fbb0e-124">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-124">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fbb0e-125">**float**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fbb0e-126">any</span><span class="sxs-lookup"><span data-stu-id="fbb0e-126">any</span></span>                            |
| <span data-ttu-id="fbb0e-127">*n*</span><span class="sxs-lookup"><span data-stu-id="fbb0e-127">*n*</span></span>   | [<span data-ttu-id="fbb0e-128">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-128">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fbb0e-129">**float**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fbb0e-130">те же измерения, что и входные данные *i*</span><span class="sxs-lookup"><span data-stu-id="fbb0e-130">same dimension(s) as input *i*</span></span> |
| <span data-ttu-id="fbb0e-131">*обратно*</span><span class="sxs-lookup"><span data-stu-id="fbb0e-131">*ret*</span></span> | [<span data-ttu-id="fbb0e-132">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-132">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fbb0e-133">**float**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fbb0e-134">те же измерения, что и входные данные *i*</span><span class="sxs-lookup"><span data-stu-id="fbb0e-134">same dimension(s) as input *i*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fbb0e-135">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fbb0e-135">Minimum Shader Model</span></span>

<span data-ttu-id="fbb0e-136">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fbb0e-137">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fbb0e-137">Shader Model</span></span>                                                                       | <span data-ttu-id="fbb0e-138">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="fbb0e-138">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="fbb0e-139">[Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) и более высокие модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="fbb0e-139">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="fbb0e-140">да</span><span class="sxs-lookup"><span data-stu-id="fbb0e-140">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fbb0e-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbb0e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbb0e-142">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

