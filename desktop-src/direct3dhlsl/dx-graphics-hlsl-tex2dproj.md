---
title: tex2Dproj
description: Выполняет выборку двухмерной текстуры с помощью проектного деления; Координата текстуры делится на t. w до того, как происходит поиск.
ms.assetid: c6b79360-3737-4b74-bdf3-6d46323e8e54
keywords:
- tex2Dproj HLSL
topic_type:
- apiref
api_name:
- tex2Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 365401e4e4eca8703207ffb5c7676748f4a06d30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533251"
---
# <a name="tex2dproj"></a><span data-ttu-id="43417-104">tex2Dproj</span><span class="sxs-lookup"><span data-stu-id="43417-104">tex2Dproj</span></span>

<span data-ttu-id="43417-105">Выполняет выборку двухмерной текстуры с помощью проектного деления; Координата текстуры делится на t. w до того, как происходит поиск.</span><span class="sxs-lookup"><span data-stu-id="43417-105">Samples a 2D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="43417-106">RET tex2Dproj (s, t)</span><span class="sxs-lookup"><span data-stu-id="43417-106">ret tex2Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="43417-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="43417-107">Parameters</span></span>



| <span data-ttu-id="43417-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="43417-108">Item</span></span>                                                   | <span data-ttu-id="43417-109">Описание</span><span class="sxs-lookup"><span data-stu-id="43417-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="43417-110"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="43417-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="43417-111">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="43417-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="43417-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="43417-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="43417-113">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="43417-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="43417-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43417-114">Return Value</span></span>

<span data-ttu-id="43417-115">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="43417-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="43417-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="43417-116">Type Description</span></span>



| <span data-ttu-id="43417-117">Имя</span><span class="sxs-lookup"><span data-stu-id="43417-117">Name</span></span> | <span data-ttu-id="43417-118">В/Из</span><span class="sxs-lookup"><span data-stu-id="43417-118">In/Out</span></span> | [<span data-ttu-id="43417-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="43417-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="43417-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="43417-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="43417-121">Размер</span><span class="sxs-lookup"><span data-stu-id="43417-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="43417-122">s</span><span class="sxs-lookup"><span data-stu-id="43417-122">s</span></span>    | <span data-ttu-id="43417-123">in</span><span class="sxs-lookup"><span data-stu-id="43417-123">in</span></span>     | [<span data-ttu-id="43417-124">**объектами**</span><span class="sxs-lookup"><span data-stu-id="43417-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="43417-125">sampler2D</span><span class="sxs-lookup"><span data-stu-id="43417-125">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="43417-126">1</span><span class="sxs-lookup"><span data-stu-id="43417-126">1</span></span>    |
| <span data-ttu-id="43417-127">t</span><span class="sxs-lookup"><span data-stu-id="43417-127">t</span></span>    | <span data-ttu-id="43417-128">in</span><span class="sxs-lookup"><span data-stu-id="43417-128">in</span></span>     | [<span data-ttu-id="43417-129">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="43417-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="43417-130">**float**</span><span class="sxs-lookup"><span data-stu-id="43417-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="43417-131">4</span><span class="sxs-lookup"><span data-stu-id="43417-131">4</span></span>    |
| <span data-ttu-id="43417-132">обратно</span><span class="sxs-lookup"><span data-stu-id="43417-132">ret</span></span>  | <span data-ttu-id="43417-133">out</span><span class="sxs-lookup"><span data-stu-id="43417-133">out</span></span>    | [<span data-ttu-id="43417-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="43417-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="43417-135">**float**</span><span class="sxs-lookup"><span data-stu-id="43417-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="43417-136">4</span><span class="sxs-lookup"><span data-stu-id="43417-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="43417-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="43417-137">Minimum Shader Model</span></span>

<span data-ttu-id="43417-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="43417-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="43417-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="43417-139">Shader Model</span></span>                                              | <span data-ttu-id="43417-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="43417-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="43417-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="43417-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="43417-142">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="43417-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="43417-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="43417-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="43417-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="43417-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="43417-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="43417-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="43417-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="43417-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="43417-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="43417-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="43417-148">Нет</span><span class="sxs-lookup"><span data-stu-id="43417-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="43417-149">См. также</span><span class="sxs-lookup"><span data-stu-id="43417-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43417-150">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="43417-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

