---
title: tex3Dlod
description: Пример трехмерной текстуры с помощью MIP-карты. Лод mipmap указан в т.в.
ms.assetid: 9bdd8fa1-8c02-4765-8f4d-61ceb532354e
keywords:
- tex3Dlod HLSL
topic_type:
- apiref
api_name:
- tex3Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bc25af449f7f32e94d4ca344bf5ef3a4d09b376c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104983993"
---
# <a name="tex3dlod"></a><span data-ttu-id="7cd13-105">tex3Dlod</span><span class="sxs-lookup"><span data-stu-id="7cd13-105">tex3Dlod</span></span>

<span data-ttu-id="7cd13-106">Пример трехмерной текстуры с помощью MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="7cd13-106">Samples a 3D texture with mipmaps.</span></span> <span data-ttu-id="7cd13-107">Лод mipmap указан в т.в.</span><span class="sxs-lookup"><span data-stu-id="7cd13-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="7cd13-108">RET tex3Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="7cd13-108">ret tex3Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="7cd13-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cd13-109">Parameters</span></span>



| <span data-ttu-id="7cd13-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="7cd13-110">Item</span></span>                                                   | <span data-ttu-id="7cd13-111">Описание</span><span class="sxs-lookup"><span data-stu-id="7cd13-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="7cd13-112"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="7cd13-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="7cd13-113">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="7cd13-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="7cd13-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="7cd13-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="7cd13-115">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="7cd13-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7cd13-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cd13-116">Return Value</span></span>

<span data-ttu-id="7cd13-117">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="7cd13-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="7cd13-118">Описание типа</span><span class="sxs-lookup"><span data-stu-id="7cd13-118">Type Description</span></span>



| <span data-ttu-id="7cd13-119">Имя</span><span class="sxs-lookup"><span data-stu-id="7cd13-119">Name</span></span> | <span data-ttu-id="7cd13-120">В/Из</span><span class="sxs-lookup"><span data-stu-id="7cd13-120">In/Out</span></span> | [<span data-ttu-id="7cd13-121">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="7cd13-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="7cd13-122">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="7cd13-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="7cd13-123">Размер</span><span class="sxs-lookup"><span data-stu-id="7cd13-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="7cd13-124">s</span><span class="sxs-lookup"><span data-stu-id="7cd13-124">s</span></span>    | <span data-ttu-id="7cd13-125">in</span><span class="sxs-lookup"><span data-stu-id="7cd13-125">in</span></span>     | [<span data-ttu-id="7cd13-126">**объектами**</span><span class="sxs-lookup"><span data-stu-id="7cd13-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="7cd13-127">sampler3D</span><span class="sxs-lookup"><span data-stu-id="7cd13-127">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="7cd13-128">1</span><span class="sxs-lookup"><span data-stu-id="7cd13-128">1</span></span>    |
| <span data-ttu-id="7cd13-129">t</span><span class="sxs-lookup"><span data-stu-id="7cd13-129">t</span></span>    | <span data-ttu-id="7cd13-130">in</span><span class="sxs-lookup"><span data-stu-id="7cd13-130">in</span></span>     | [<span data-ttu-id="7cd13-131">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="7cd13-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="7cd13-132">**float**</span><span class="sxs-lookup"><span data-stu-id="7cd13-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7cd13-133">4</span><span class="sxs-lookup"><span data-stu-id="7cd13-133">4</span></span>    |
| <span data-ttu-id="7cd13-134">обратно</span><span class="sxs-lookup"><span data-stu-id="7cd13-134">ret</span></span>  | <span data-ttu-id="7cd13-135">out</span><span class="sxs-lookup"><span data-stu-id="7cd13-135">out</span></span>    | [<span data-ttu-id="7cd13-136">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="7cd13-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="7cd13-137">**float**</span><span class="sxs-lookup"><span data-stu-id="7cd13-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7cd13-138">4</span><span class="sxs-lookup"><span data-stu-id="7cd13-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7cd13-139">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7cd13-139">Minimum Shader Model</span></span>

<span data-ttu-id="7cd13-140">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="7cd13-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7cd13-141">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7cd13-141">Shader Model</span></span>                                              | <span data-ttu-id="7cd13-142">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="7cd13-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="7cd13-143">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="7cd13-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7cd13-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="7cd13-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="7cd13-145">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7cd13-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7cd13-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="7cd13-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="7cd13-147">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7cd13-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7cd13-148">Нет</span><span class="sxs-lookup"><span data-stu-id="7cd13-148">no</span></span>                      |
| [<span data-ttu-id="7cd13-149">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7cd13-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7cd13-150">Нет</span><span class="sxs-lookup"><span data-stu-id="7cd13-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="7cd13-151">См. также</span><span class="sxs-lookup"><span data-stu-id="7cd13-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd13-152">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7cd13-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

