---
title: текскубепрож
description: Выберет текстуру Куба с помощью проектного деления; Координата текстуры делится на t. w до того, как происходит поиск.
ms.assetid: 86bdd1c3-0a8d-4d09-b70d-1ebcee32c866
keywords:
- Текскубепрож HLSL
topic_type:
- apiref
api_name:
- texCUBEproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d23a9b85034c1591cfe695759b29612a3674d436
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488205"
---
# <a name="texcubeproj"></a><span data-ttu-id="ecccf-104">текскубепрож</span><span class="sxs-lookup"><span data-stu-id="ecccf-104">texCUBEproj</span></span>

<span data-ttu-id="ecccf-105">Выберет текстуру Куба с помощью проектного деления; Координата текстуры делится на t. w до того, как происходит поиск.</span><span class="sxs-lookup"><span data-stu-id="ecccf-105">Samples a cube texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="ecccf-106">RET Текскубепрож (s, t)</span><span class="sxs-lookup"><span data-stu-id="ecccf-106">ret texCUBEproj(s, t)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="ecccf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ecccf-107">Parameters</span></span>



| <span data-ttu-id="ecccf-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="ecccf-108">Item</span></span>                                                   | <span data-ttu-id="ecccf-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ecccf-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="ecccf-110"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="ecccf-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="ecccf-111">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="ecccf-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="ecccf-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="ecccf-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="ecccf-113">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="ecccf-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ecccf-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ecccf-114">Return Value</span></span>

<span data-ttu-id="ecccf-115">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="ecccf-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="ecccf-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="ecccf-116">Type Description</span></span>



| <span data-ttu-id="ecccf-117">Имя</span><span class="sxs-lookup"><span data-stu-id="ecccf-117">Name</span></span> | <span data-ttu-id="ecccf-118">В/Из</span><span class="sxs-lookup"><span data-stu-id="ecccf-118">In/Out</span></span> | [<span data-ttu-id="ecccf-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="ecccf-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="ecccf-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="ecccf-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ecccf-121">Размер</span><span class="sxs-lookup"><span data-stu-id="ecccf-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="ecccf-122">s</span><span class="sxs-lookup"><span data-stu-id="ecccf-122">s</span></span>    | <span data-ttu-id="ecccf-123">in</span><span class="sxs-lookup"><span data-stu-id="ecccf-123">in</span></span>     | [<span data-ttu-id="ecccf-124">**объектами**</span><span class="sxs-lookup"><span data-stu-id="ecccf-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ecccf-125">самплеркубе</span><span class="sxs-lookup"><span data-stu-id="ecccf-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="ecccf-126">1</span><span class="sxs-lookup"><span data-stu-id="ecccf-126">1</span></span>    |
| <span data-ttu-id="ecccf-127">t</span><span class="sxs-lookup"><span data-stu-id="ecccf-127">t</span></span>    | <span data-ttu-id="ecccf-128">in</span><span class="sxs-lookup"><span data-stu-id="ecccf-128">in</span></span>     | [<span data-ttu-id="ecccf-129">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="ecccf-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ecccf-130">**float**</span><span class="sxs-lookup"><span data-stu-id="ecccf-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ecccf-131">4</span><span class="sxs-lookup"><span data-stu-id="ecccf-131">4</span></span>    |
| <span data-ttu-id="ecccf-132">обратно</span><span class="sxs-lookup"><span data-stu-id="ecccf-132">ret</span></span>  | <span data-ttu-id="ecccf-133">out</span><span class="sxs-lookup"><span data-stu-id="ecccf-133">out</span></span>    | [<span data-ttu-id="ecccf-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="ecccf-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ecccf-135">**float**</span><span class="sxs-lookup"><span data-stu-id="ecccf-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ecccf-136">4</span><span class="sxs-lookup"><span data-stu-id="ecccf-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ecccf-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ecccf-137">Minimum Shader Model</span></span>

<span data-ttu-id="ecccf-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ecccf-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ecccf-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ecccf-139">Shader Model</span></span>                                              | <span data-ttu-id="ecccf-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ecccf-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="ecccf-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ecccf-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ecccf-142">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="ecccf-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="ecccf-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecccf-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ecccf-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="ecccf-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="ecccf-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecccf-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ecccf-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="ecccf-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="ecccf-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecccf-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ecccf-148">Нет</span><span class="sxs-lookup"><span data-stu-id="ecccf-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="ecccf-149">См. также</span><span class="sxs-lookup"><span data-stu-id="ecccf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecccf-150">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ecccf-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

