---
title: tex1Dproj
description: Выборка одномерной текстуры с помощью проектного деления; Координата текстуры делится на t. w до того, как происходит поиск.
ms.assetid: 7cfe996d-3967-40da-b0e7-e03938478594
keywords:
- tex1Dproj HLSL
topic_type:
- apiref
api_name:
- tex1Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34fc1c019ab5479fe8a23446c94073e19ca68de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984052"
---
# <a name="tex1dproj"></a><span data-ttu-id="7ed3a-104">tex1Dproj</span><span class="sxs-lookup"><span data-stu-id="7ed3a-104">tex1Dproj</span></span>

<span data-ttu-id="7ed3a-105">Выборка одномерной текстуры с помощью проектного деления; Координата текстуры делится на t. w до того, как происходит поиск.</span><span class="sxs-lookup"><span data-stu-id="7ed3a-105">Samples a 1D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="7ed3a-106">RET tex1Dproj (s, t)</span><span class="sxs-lookup"><span data-stu-id="7ed3a-106">ret tex1Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="7ed3a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ed3a-107">Parameters</span></span>



| <span data-ttu-id="7ed3a-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="7ed3a-108">Item</span></span>                                                   | <span data-ttu-id="7ed3a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7ed3a-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="7ed3a-110"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="7ed3a-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="7ed3a-111">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="7ed3a-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="7ed3a-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="7ed3a-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="7ed3a-113">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="7ed3a-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7ed3a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ed3a-114">Return Value</span></span>

<span data-ttu-id="7ed3a-115">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="7ed3a-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="7ed3a-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="7ed3a-116">Type Description</span></span>



| <span data-ttu-id="7ed3a-117">Имя</span><span class="sxs-lookup"><span data-stu-id="7ed3a-117">Name</span></span> | <span data-ttu-id="7ed3a-118">В/Из</span><span class="sxs-lookup"><span data-stu-id="7ed3a-118">In/Out</span></span> | [<span data-ttu-id="7ed3a-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="7ed3a-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="7ed3a-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="7ed3a-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="7ed3a-121">Размер</span><span class="sxs-lookup"><span data-stu-id="7ed3a-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="7ed3a-122">s</span><span class="sxs-lookup"><span data-stu-id="7ed3a-122">s</span></span>    | <span data-ttu-id="7ed3a-123">in</span><span class="sxs-lookup"><span data-stu-id="7ed3a-123">in</span></span>     | [<span data-ttu-id="7ed3a-124">**объектами**</span><span class="sxs-lookup"><span data-stu-id="7ed3a-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="7ed3a-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="7ed3a-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="7ed3a-126">1</span><span class="sxs-lookup"><span data-stu-id="7ed3a-126">1</span></span>    |
| <span data-ttu-id="7ed3a-127">t</span><span class="sxs-lookup"><span data-stu-id="7ed3a-127">t</span></span>    | <span data-ttu-id="7ed3a-128">in</span><span class="sxs-lookup"><span data-stu-id="7ed3a-128">in</span></span>     | [<span data-ttu-id="7ed3a-129">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="7ed3a-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="7ed3a-130">**float**</span><span class="sxs-lookup"><span data-stu-id="7ed3a-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7ed3a-131">4</span><span class="sxs-lookup"><span data-stu-id="7ed3a-131">4</span></span>    |
| <span data-ttu-id="7ed3a-132">обратно</span><span class="sxs-lookup"><span data-stu-id="7ed3a-132">ret</span></span>  | <span data-ttu-id="7ed3a-133">out</span><span class="sxs-lookup"><span data-stu-id="7ed3a-133">out</span></span>    | [<span data-ttu-id="7ed3a-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="7ed3a-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="7ed3a-135">**float**</span><span class="sxs-lookup"><span data-stu-id="7ed3a-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7ed3a-136">4</span><span class="sxs-lookup"><span data-stu-id="7ed3a-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7ed3a-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7ed3a-137">Minimum Shader Model</span></span>

<span data-ttu-id="7ed3a-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="7ed3a-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7ed3a-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7ed3a-139">Shader Model</span></span>                                              | <span data-ttu-id="7ed3a-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="7ed3a-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="7ed3a-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="7ed3a-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7ed3a-142">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="7ed3a-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="7ed3a-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ed3a-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7ed3a-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="7ed3a-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="7ed3a-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ed3a-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7ed3a-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="7ed3a-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="7ed3a-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ed3a-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7ed3a-148">Нет</span><span class="sxs-lookup"><span data-stu-id="7ed3a-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="7ed3a-149">См. также</span><span class="sxs-lookup"><span data-stu-id="7ed3a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed3a-150">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7ed3a-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

