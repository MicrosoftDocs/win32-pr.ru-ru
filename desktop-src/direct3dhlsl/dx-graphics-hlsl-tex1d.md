---
title: tex1D (Справочник по HLSL)
description: Выборка одномерной текстуры.
ms.assetid: 587be0fd-af12-4bf0-862b-84988435e90e
keywords:
- tex1D HLSL
topic_type:
- apiref
api_name:
- tex1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dec5cc8a35b18c35076f99443ad3c1166fcf410
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792301"
---
# <a name="tex1d-hlsl-reference"></a><span data-ttu-id="e63cd-104">tex1D (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="e63cd-104">tex1D (HLSL reference)</span></span>

<span data-ttu-id="e63cd-105">Выборка одномерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="e63cd-105">Samples a 1D texture.</span></span>



| <span data-ttu-id="e63cd-106">RET tex1D (s, t)</span><span class="sxs-lookup"><span data-stu-id="e63cd-106">ret tex1D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="e63cd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e63cd-107">Parameters</span></span>



| <span data-ttu-id="e63cd-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="e63cd-108">Item</span></span>                                                   | <span data-ttu-id="e63cd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e63cd-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="e63cd-110"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="e63cd-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="e63cd-111">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="e63cd-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="e63cd-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="e63cd-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="e63cd-113">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="e63cd-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e63cd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e63cd-114">Return Value</span></span>

<span data-ttu-id="e63cd-115">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="e63cd-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="e63cd-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="e63cd-116">Type Description</span></span>



| <span data-ttu-id="e63cd-117">Имя</span><span class="sxs-lookup"><span data-stu-id="e63cd-117">Name</span></span> | <span data-ttu-id="e63cd-118">В/Из</span><span class="sxs-lookup"><span data-stu-id="e63cd-118">In/Out</span></span> | [<span data-ttu-id="e63cd-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="e63cd-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="e63cd-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="e63cd-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e63cd-121">Размер</span><span class="sxs-lookup"><span data-stu-id="e63cd-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="e63cd-122">s</span><span class="sxs-lookup"><span data-stu-id="e63cd-122">s</span></span>    | <span data-ttu-id="e63cd-123">in</span><span class="sxs-lookup"><span data-stu-id="e63cd-123">in</span></span>     | [<span data-ttu-id="e63cd-124">**объектами**</span><span class="sxs-lookup"><span data-stu-id="e63cd-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e63cd-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="e63cd-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="e63cd-126">1</span><span class="sxs-lookup"><span data-stu-id="e63cd-126">1</span></span>    |
| <span data-ttu-id="e63cd-127">t</span><span class="sxs-lookup"><span data-stu-id="e63cd-127">t</span></span>    | <span data-ttu-id="e63cd-128">in</span><span class="sxs-lookup"><span data-stu-id="e63cd-128">in</span></span>     | [<span data-ttu-id="e63cd-129">**скаляр**</span><span class="sxs-lookup"><span data-stu-id="e63cd-129">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e63cd-130">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="e63cd-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e63cd-131">1</span><span class="sxs-lookup"><span data-stu-id="e63cd-131">1</span></span>    |
| <span data-ttu-id="e63cd-132">обратно</span><span class="sxs-lookup"><span data-stu-id="e63cd-132">ret</span></span>  | <span data-ttu-id="e63cd-133">out</span><span class="sxs-lookup"><span data-stu-id="e63cd-133">out</span></span>    | [<span data-ttu-id="e63cd-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="e63cd-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e63cd-135">**float**</span><span class="sxs-lookup"><span data-stu-id="e63cd-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e63cd-136">4</span><span class="sxs-lookup"><span data-stu-id="e63cd-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e63cd-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e63cd-137">Minimum Shader Model</span></span>

<span data-ttu-id="e63cd-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="e63cd-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e63cd-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e63cd-139">Shader Model</span></span>                                              | <span data-ttu-id="e63cd-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e63cd-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e63cd-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="e63cd-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e63cd-142">Да (только для шейдера Pixel), но при компиляции необходимо использовать [устаревший параметр Compile](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) .</span><span class="sxs-lookup"><span data-stu-id="e63cd-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="e63cd-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e63cd-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e63cd-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="e63cd-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="e63cd-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e63cd-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e63cd-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="e63cd-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="e63cd-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e63cd-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e63cd-148">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="e63cd-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="e63cd-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e63cd-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e63cd-150">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e63cd-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

