---
title: tex2Dbias
description: Пример двухмерной текстуры после сдвига уровня MIP на т.в.
ms.assetid: adf2891a-732a-4953-875b-df315c19748b
keywords:
- tex2Dbias HLSL
topic_type:
- apiref
api_name:
- tex2Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cfaec24e1d188460d36a24d68b0fde8ddcb45c29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338844"
---
# <a name="tex2dbias"></a><span data-ttu-id="29d9e-104">tex2Dbias</span><span class="sxs-lookup"><span data-stu-id="29d9e-104">tex2Dbias</span></span>

<span data-ttu-id="29d9e-105">Пример двухмерной текстуры после сдвига уровня MIP на т.в.</span><span class="sxs-lookup"><span data-stu-id="29d9e-105">Samples a 2D texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="29d9e-106">RET tex2Dbias (s, t)</span><span class="sxs-lookup"><span data-stu-id="29d9e-106">ret tex2Dbias(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="29d9e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="29d9e-107">Parameters</span></span>



| <span data-ttu-id="29d9e-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="29d9e-108">Item</span></span>                                                   | <span data-ttu-id="29d9e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="29d9e-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="29d9e-110"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="29d9e-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="29d9e-111">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="29d9e-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="29d9e-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="29d9e-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="29d9e-113">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="29d9e-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="29d9e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29d9e-114">Return Value</span></span>

<span data-ttu-id="29d9e-115">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="29d9e-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="29d9e-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="29d9e-116">Type Description</span></span>



| <span data-ttu-id="29d9e-117">Имя</span><span class="sxs-lookup"><span data-stu-id="29d9e-117">Name</span></span> | <span data-ttu-id="29d9e-118">В/Из</span><span class="sxs-lookup"><span data-stu-id="29d9e-118">In/Out</span></span> | [<span data-ttu-id="29d9e-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="29d9e-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="29d9e-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="29d9e-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="29d9e-121">Размер</span><span class="sxs-lookup"><span data-stu-id="29d9e-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="29d9e-122">s</span><span class="sxs-lookup"><span data-stu-id="29d9e-122">s</span></span>    | <span data-ttu-id="29d9e-123">in</span><span class="sxs-lookup"><span data-stu-id="29d9e-123">in</span></span>     | [<span data-ttu-id="29d9e-124">**объектами**</span><span class="sxs-lookup"><span data-stu-id="29d9e-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="29d9e-125">sampler2D</span><span class="sxs-lookup"><span data-stu-id="29d9e-125">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="29d9e-126">1</span><span class="sxs-lookup"><span data-stu-id="29d9e-126">1</span></span>    |
| <span data-ttu-id="29d9e-127">t</span><span class="sxs-lookup"><span data-stu-id="29d9e-127">t</span></span>    | <span data-ttu-id="29d9e-128">in</span><span class="sxs-lookup"><span data-stu-id="29d9e-128">in</span></span>     | [<span data-ttu-id="29d9e-129">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="29d9e-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="29d9e-130">**float**</span><span class="sxs-lookup"><span data-stu-id="29d9e-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="29d9e-131">4</span><span class="sxs-lookup"><span data-stu-id="29d9e-131">4</span></span>    |
| <span data-ttu-id="29d9e-132">обратно</span><span class="sxs-lookup"><span data-stu-id="29d9e-132">ret</span></span>  | <span data-ttu-id="29d9e-133">out</span><span class="sxs-lookup"><span data-stu-id="29d9e-133">out</span></span>    | [<span data-ttu-id="29d9e-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="29d9e-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="29d9e-135">**float**</span><span class="sxs-lookup"><span data-stu-id="29d9e-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="29d9e-136">4</span><span class="sxs-lookup"><span data-stu-id="29d9e-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="29d9e-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="29d9e-137">Minimum Shader Model</span></span>

<span data-ttu-id="29d9e-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="29d9e-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="29d9e-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="29d9e-139">Shader Model</span></span>                                              | <span data-ttu-id="29d9e-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="29d9e-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="29d9e-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="29d9e-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="29d9e-142">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="29d9e-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="29d9e-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="29d9e-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="29d9e-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="29d9e-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="29d9e-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="29d9e-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="29d9e-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="29d9e-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="29d9e-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="29d9e-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="29d9e-148">Нет</span><span class="sxs-lookup"><span data-stu-id="29d9e-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="29d9e-149">См. также</span><span class="sxs-lookup"><span data-stu-id="29d9e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d9e-150">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="29d9e-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

