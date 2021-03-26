---
title: синкос
description: Возвращает синус и косинус x.
ms.assetid: 2ef9e84e-4539-47f5-9966-d8e02ca15d36
keywords:
- синкос HLSL
topic_type:
- apiref
api_name:
- sincos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8391c2fcecc939db1d7044fe56fbd281fe3e79fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997138"
---
# <a name="sincos"></a><span data-ttu-id="20ed8-104">синкос</span><span class="sxs-lookup"><span data-stu-id="20ed8-104">sincos</span></span>

<span data-ttu-id="20ed8-105">Возвращает синус и косинус x.</span><span class="sxs-lookup"><span data-stu-id="20ed8-105">Returns the sine and cosine of x.</span></span>



| <span data-ttu-id="20ed8-106">синкос (*x*, out *s*, out *c*)</span><span class="sxs-lookup"><span data-stu-id="20ed8-106">sincos(*x*, out *s*, out *c*)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="20ed8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="20ed8-107">Parameters</span></span>



| <span data-ttu-id="20ed8-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="20ed8-108">Item</span></span>                                                   | <span data-ttu-id="20ed8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="20ed8-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="20ed8-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="20ed8-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="20ed8-111">\[в \] заданном значении в радианах.</span><span class="sxs-lookup"><span data-stu-id="20ed8-111">\[in\] The specified value, in radians.</span></span><br/> |
| <span data-ttu-id="20ed8-112"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="20ed8-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="20ed8-113">\[out \] возвращает синус x.</span><span class="sxs-lookup"><span data-stu-id="20ed8-113">\[out\] Returns the sine of x.</span></span><br/>          |
| <span data-ttu-id="20ed8-114"><span id="c"></span><span id="C"></span>*ц*</span><span class="sxs-lookup"><span data-stu-id="20ed8-114"><span id="c"></span><span id="C"></span>*c*</span></span><br/> | <span data-ttu-id="20ed8-115">\[out \] возвращает косинус x.</span><span class="sxs-lookup"><span data-stu-id="20ed8-115">\[out\] Returns the cosine of x.</span></span><br/>        |



 

## <a name="return-value"></a><span data-ttu-id="20ed8-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20ed8-116">Return Value</span></span>

<span data-ttu-id="20ed8-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="20ed8-117">None.</span></span>

## <a name="type-description"></a><span data-ttu-id="20ed8-118">Описание типа</span><span class="sxs-lookup"><span data-stu-id="20ed8-118">Type Description</span></span>



| <span data-ttu-id="20ed8-119">Имя</span><span class="sxs-lookup"><span data-stu-id="20ed8-119">Name</span></span> | [<span data-ttu-id="20ed8-120">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="20ed8-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="20ed8-121">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="20ed8-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="20ed8-122">Размер</span><span class="sxs-lookup"><span data-stu-id="20ed8-122">Size</span></span>                           |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="20ed8-123">*x*</span><span class="sxs-lookup"><span data-stu-id="20ed8-123">*x*</span></span>  | <span data-ttu-id="20ed8-124">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="20ed8-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="20ed8-125">**float**</span><span class="sxs-lookup"><span data-stu-id="20ed8-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="20ed8-126">any</span><span class="sxs-lookup"><span data-stu-id="20ed8-126">any</span></span>                            |
| <span data-ttu-id="20ed8-127">*s*</span><span class="sxs-lookup"><span data-stu-id="20ed8-127">*s*</span></span>  | <span data-ttu-id="20ed8-128">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="20ed8-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="20ed8-129">**float**</span><span class="sxs-lookup"><span data-stu-id="20ed8-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="20ed8-130">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="20ed8-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="20ed8-131">c</span><span class="sxs-lookup"><span data-stu-id="20ed8-131">c</span></span>    | <span data-ttu-id="20ed8-132">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="20ed8-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="20ed8-133">**float**</span><span class="sxs-lookup"><span data-stu-id="20ed8-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="20ed8-134">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="20ed8-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="20ed8-135">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="20ed8-135">Minimum Shader Model</span></span>

<span data-ttu-id="20ed8-136">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="20ed8-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="20ed8-137">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="20ed8-137">Shader Model</span></span>                                                                       | <span data-ttu-id="20ed8-138">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="20ed8-138">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="20ed8-139">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="20ed8-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="20ed8-140">да</span><span class="sxs-lookup"><span data-stu-id="20ed8-140">yes</span></span>                 |
| [<span data-ttu-id="20ed8-141">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20ed8-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="20ed8-142">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="20ed8-142">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="20ed8-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20ed8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ed8-144">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="20ed8-144">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

