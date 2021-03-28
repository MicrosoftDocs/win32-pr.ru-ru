---
title: текскубелод
description: Пример текстуры Куба с MIP-карты. Лод mipmap указан в т.в.
ms.assetid: fa7b236d-2c52-42bd-9123-919541f9e675
keywords:
- Текскубелод HLSL
topic_type:
- apiref
api_name:
- texCUBElod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72635211263085f03b87c2e013ea57d1b6a21464
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984080"
---
# <a name="texcubelod"></a><span data-ttu-id="08ab5-105">текскубелод</span><span class="sxs-lookup"><span data-stu-id="08ab5-105">texCUBElod</span></span>

<span data-ttu-id="08ab5-106">Пример текстуры Куба с MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="08ab5-106">Samples a cube texture with mipmaps.</span></span> <span data-ttu-id="08ab5-107">Лод mipmap указан в т.в.</span><span class="sxs-lookup"><span data-stu-id="08ab5-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="08ab5-108">RET Текскубелод (s, t)</span><span class="sxs-lookup"><span data-stu-id="08ab5-108">ret texCUBElod(s, t)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="08ab5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="08ab5-109">Parameters</span></span>



| <span data-ttu-id="08ab5-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="08ab5-110">Item</span></span>                                                   | <span data-ttu-id="08ab5-111">Описание</span><span class="sxs-lookup"><span data-stu-id="08ab5-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="08ab5-112"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="08ab5-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="08ab5-113">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="08ab5-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="08ab5-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="08ab5-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="08ab5-115">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="08ab5-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="08ab5-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08ab5-116">Return Value</span></span>

<span data-ttu-id="08ab5-117">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="08ab5-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="08ab5-118">Описание типа</span><span class="sxs-lookup"><span data-stu-id="08ab5-118">Type Description</span></span>



| <span data-ttu-id="08ab5-119">Имя</span><span class="sxs-lookup"><span data-stu-id="08ab5-119">Name</span></span> | <span data-ttu-id="08ab5-120">В/Из</span><span class="sxs-lookup"><span data-stu-id="08ab5-120">In/Out</span></span> | [<span data-ttu-id="08ab5-121">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="08ab5-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="08ab5-122">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="08ab5-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="08ab5-123">Размер</span><span class="sxs-lookup"><span data-stu-id="08ab5-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="08ab5-124">s</span><span class="sxs-lookup"><span data-stu-id="08ab5-124">s</span></span>    | <span data-ttu-id="08ab5-125">in</span><span class="sxs-lookup"><span data-stu-id="08ab5-125">in</span></span>     | [<span data-ttu-id="08ab5-126">**объектами**</span><span class="sxs-lookup"><span data-stu-id="08ab5-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="08ab5-127">самплеркубе</span><span class="sxs-lookup"><span data-stu-id="08ab5-127">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="08ab5-128">1</span><span class="sxs-lookup"><span data-stu-id="08ab5-128">1</span></span>    |
| <span data-ttu-id="08ab5-129">t</span><span class="sxs-lookup"><span data-stu-id="08ab5-129">t</span></span>    | <span data-ttu-id="08ab5-130">in</span><span class="sxs-lookup"><span data-stu-id="08ab5-130">in</span></span>     | [<span data-ttu-id="08ab5-131">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="08ab5-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="08ab5-132">**float**</span><span class="sxs-lookup"><span data-stu-id="08ab5-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="08ab5-133">4</span><span class="sxs-lookup"><span data-stu-id="08ab5-133">4</span></span>    |
| <span data-ttu-id="08ab5-134">обратно</span><span class="sxs-lookup"><span data-stu-id="08ab5-134">ret</span></span>  | <span data-ttu-id="08ab5-135">out</span><span class="sxs-lookup"><span data-stu-id="08ab5-135">out</span></span>    | [<span data-ttu-id="08ab5-136">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="08ab5-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="08ab5-137">**float**</span><span class="sxs-lookup"><span data-stu-id="08ab5-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="08ab5-138">4</span><span class="sxs-lookup"><span data-stu-id="08ab5-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="08ab5-139">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="08ab5-139">Minimum Shader Model</span></span>

<span data-ttu-id="08ab5-140">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="08ab5-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="08ab5-141">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="08ab5-141">Shader Model</span></span>                                              | <span data-ttu-id="08ab5-142">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="08ab5-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="08ab5-143">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="08ab5-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="08ab5-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="08ab5-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="08ab5-145">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="08ab5-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="08ab5-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="08ab5-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="08ab5-147">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="08ab5-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="08ab5-148">Нет</span><span class="sxs-lookup"><span data-stu-id="08ab5-148">no</span></span>                      |
| [<span data-ttu-id="08ab5-149">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="08ab5-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="08ab5-150">Нет</span><span class="sxs-lookup"><span data-stu-id="08ab5-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="08ab5-151">См. также</span><span class="sxs-lookup"><span data-stu-id="08ab5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08ab5-152">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="08ab5-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

