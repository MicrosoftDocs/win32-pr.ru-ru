---
title: tex1Dbias
description: Выборка текстуры 1D после сдвига уровня MIP на т.в.
ms.assetid: 2619ae23-e4b2-4699-b2ac-5ee711f9569a
keywords:
- tex1Dbias HLSL
topic_type:
- apiref
api_name:
- tex1Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0328b9328a1406177fa26bd566c0fbf7d384db63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134054"
---
# <a name="tex1dbias"></a><span data-ttu-id="95ca5-104">tex1Dbias</span><span class="sxs-lookup"><span data-stu-id="95ca5-104">tex1Dbias</span></span>

<span data-ttu-id="95ca5-105">Выборка текстуры 1D после сдвига уровня MIP на т.в.</span><span class="sxs-lookup"><span data-stu-id="95ca5-105">Samples a 1D texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="95ca5-106">RET tex1Dbias (s, t)</span><span class="sxs-lookup"><span data-stu-id="95ca5-106">ret tex1Dbias(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="95ca5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="95ca5-107">Parameters</span></span>



| <span data-ttu-id="95ca5-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="95ca5-108">Item</span></span>                                                   | <span data-ttu-id="95ca5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="95ca5-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="95ca5-110"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="95ca5-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="95ca5-111">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="95ca5-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="95ca5-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="95ca5-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="95ca5-113">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="95ca5-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="95ca5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95ca5-114">Return Value</span></span>

<span data-ttu-id="95ca5-115">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="95ca5-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="95ca5-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="95ca5-116">Type Description</span></span>



| <span data-ttu-id="95ca5-117">Имя</span><span class="sxs-lookup"><span data-stu-id="95ca5-117">Name</span></span> | <span data-ttu-id="95ca5-118">В/Из</span><span class="sxs-lookup"><span data-stu-id="95ca5-118">In/Out</span></span> | [<span data-ttu-id="95ca5-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="95ca5-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="95ca5-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="95ca5-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="95ca5-121">Размер</span><span class="sxs-lookup"><span data-stu-id="95ca5-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="95ca5-122">s</span><span class="sxs-lookup"><span data-stu-id="95ca5-122">s</span></span>    | <span data-ttu-id="95ca5-123">in</span><span class="sxs-lookup"><span data-stu-id="95ca5-123">in</span></span>     | [<span data-ttu-id="95ca5-124">**объектами**</span><span class="sxs-lookup"><span data-stu-id="95ca5-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="95ca5-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="95ca5-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="95ca5-126">1</span><span class="sxs-lookup"><span data-stu-id="95ca5-126">1</span></span>    |
| <span data-ttu-id="95ca5-127">t</span><span class="sxs-lookup"><span data-stu-id="95ca5-127">t</span></span>    | <span data-ttu-id="95ca5-128">in</span><span class="sxs-lookup"><span data-stu-id="95ca5-128">in</span></span>     | [<span data-ttu-id="95ca5-129">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="95ca5-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="95ca5-130">**float**</span><span class="sxs-lookup"><span data-stu-id="95ca5-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="95ca5-131">4</span><span class="sxs-lookup"><span data-stu-id="95ca5-131">4</span></span>    |
| <span data-ttu-id="95ca5-132">обратно</span><span class="sxs-lookup"><span data-stu-id="95ca5-132">ret</span></span>  | <span data-ttu-id="95ca5-133">out</span><span class="sxs-lookup"><span data-stu-id="95ca5-133">out</span></span>    | [<span data-ttu-id="95ca5-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="95ca5-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="95ca5-135">**float**</span><span class="sxs-lookup"><span data-stu-id="95ca5-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="95ca5-136">4</span><span class="sxs-lookup"><span data-stu-id="95ca5-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="95ca5-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="95ca5-137">Minimum Shader Model</span></span>

<span data-ttu-id="95ca5-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="95ca5-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="95ca5-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="95ca5-139">Shader Model</span></span>                                              | <span data-ttu-id="95ca5-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="95ca5-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="95ca5-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="95ca5-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="95ca5-142">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="95ca5-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="95ca5-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95ca5-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="95ca5-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="95ca5-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="95ca5-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95ca5-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="95ca5-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="95ca5-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="95ca5-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95ca5-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="95ca5-148">Нет</span><span class="sxs-lookup"><span data-stu-id="95ca5-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="95ca5-149">См. также</span><span class="sxs-lookup"><span data-stu-id="95ca5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95ca5-150">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="95ca5-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

