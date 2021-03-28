---
title: tex1Dlod
description: Выборка одномерной текстуры с помощью MIP-карты. Лод mipmap указан в т.в.
ms.assetid: f1700ee6-2f79-4b8b-ad34-30561f319356
keywords:
- tex1Dlod HLSL
topic_type:
- apiref
api_name:
- tex1Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ca6379448290d027bba8a8b62f80cac39c84f25
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793020"
---
# <a name="tex1dlod"></a><span data-ttu-id="a5a04-105">tex1Dlod</span><span class="sxs-lookup"><span data-stu-id="a5a04-105">tex1Dlod</span></span>

<span data-ttu-id="a5a04-106">Выборка одномерной текстуры с помощью MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="a5a04-106">Samples a 1D texture with mipmaps.</span></span> <span data-ttu-id="a5a04-107">Лод mipmap указан в т.в.</span><span class="sxs-lookup"><span data-stu-id="a5a04-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="a5a04-108">RET tex1Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="a5a04-108">ret tex1Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="a5a04-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5a04-109">Parameters</span></span>



| <span data-ttu-id="a5a04-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="a5a04-110">Item</span></span>                                                   | <span data-ttu-id="a5a04-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a5a04-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="a5a04-112"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="a5a04-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="a5a04-113">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="a5a04-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="a5a04-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="a5a04-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="a5a04-115">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="a5a04-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a5a04-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5a04-116">Return Value</span></span>

<span data-ttu-id="a5a04-117">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="a5a04-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="a5a04-118">Описание типа</span><span class="sxs-lookup"><span data-stu-id="a5a04-118">Type Description</span></span>



| <span data-ttu-id="a5a04-119">Имя</span><span class="sxs-lookup"><span data-stu-id="a5a04-119">Name</span></span> | <span data-ttu-id="a5a04-120">В/Из</span><span class="sxs-lookup"><span data-stu-id="a5a04-120">In/Out</span></span> | [<span data-ttu-id="a5a04-121">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="a5a04-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="a5a04-122">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="a5a04-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="a5a04-123">Размер</span><span class="sxs-lookup"><span data-stu-id="a5a04-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="a5a04-124">s</span><span class="sxs-lookup"><span data-stu-id="a5a04-124">s</span></span>    | <span data-ttu-id="a5a04-125">in</span><span class="sxs-lookup"><span data-stu-id="a5a04-125">in</span></span>     | [<span data-ttu-id="a5a04-126">**объектами**</span><span class="sxs-lookup"><span data-stu-id="a5a04-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="a5a04-127">sampler1D</span><span class="sxs-lookup"><span data-stu-id="a5a04-127">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="a5a04-128">1</span><span class="sxs-lookup"><span data-stu-id="a5a04-128">1</span></span>    |
| <span data-ttu-id="a5a04-129">t</span><span class="sxs-lookup"><span data-stu-id="a5a04-129">t</span></span>    | <span data-ttu-id="a5a04-130">in</span><span class="sxs-lookup"><span data-stu-id="a5a04-130">in</span></span>     | [<span data-ttu-id="a5a04-131">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="a5a04-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="a5a04-132">**float**</span><span class="sxs-lookup"><span data-stu-id="a5a04-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a5a04-133">4</span><span class="sxs-lookup"><span data-stu-id="a5a04-133">4</span></span>    |
| <span data-ttu-id="a5a04-134">обратно</span><span class="sxs-lookup"><span data-stu-id="a5a04-134">ret</span></span>  | <span data-ttu-id="a5a04-135">out</span><span class="sxs-lookup"><span data-stu-id="a5a04-135">out</span></span>    | [<span data-ttu-id="a5a04-136">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="a5a04-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="a5a04-137">**float**</span><span class="sxs-lookup"><span data-stu-id="a5a04-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a5a04-138">4</span><span class="sxs-lookup"><span data-stu-id="a5a04-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a5a04-139">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a5a04-139">Minimum Shader Model</span></span>

<span data-ttu-id="a5a04-140">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a5a04-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a5a04-141">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a5a04-141">Shader Model</span></span>                                              | <span data-ttu-id="a5a04-142">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="a5a04-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="a5a04-143">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="a5a04-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a5a04-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="a5a04-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="a5a04-145">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5a04-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a5a04-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="a5a04-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="a5a04-147">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5a04-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a5a04-148">Нет</span><span class="sxs-lookup"><span data-stu-id="a5a04-148">no</span></span>                      |
| [<span data-ttu-id="a5a04-149">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5a04-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a5a04-150">Нет</span><span class="sxs-lookup"><span data-stu-id="a5a04-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="a5a04-151">См. также</span><span class="sxs-lookup"><span data-stu-id="a5a04-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5a04-152">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a5a04-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

