---
title: текскубебиас
description: Выберет текстуру Куба после сдвига уровня MIP на т.в.
ms.assetid: dad27cff-6b10-45db-b70f-c4ad78c64e76
keywords:
- Текскубебиас HLSL
topic_type:
- apiref
api_name:
- texCUBEbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0129c20db1da320e9cb85aacfc4490124be28f8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133958"
---
# <a name="texcubebias"></a><span data-ttu-id="d8474-104">текскубебиас</span><span class="sxs-lookup"><span data-stu-id="d8474-104">texCUBEbias</span></span>

<span data-ttu-id="d8474-105">Выберет текстуру Куба после сдвига уровня MIP на т.в.</span><span class="sxs-lookup"><span data-stu-id="d8474-105">Samples a cube texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="d8474-106">RET Текскубебиас (s, t)</span><span class="sxs-lookup"><span data-stu-id="d8474-106">ret texCUBEbias(s, t)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="d8474-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8474-107">Parameters</span></span>



| <span data-ttu-id="d8474-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="d8474-108">Item</span></span>                                                   | <span data-ttu-id="d8474-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d8474-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="d8474-110"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="d8474-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="d8474-111">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="d8474-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="d8474-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="d8474-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="d8474-113">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="d8474-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d8474-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8474-114">Return Value</span></span>

<span data-ttu-id="d8474-115">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="d8474-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="d8474-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="d8474-116">Type Description</span></span>



| <span data-ttu-id="d8474-117">Имя</span><span class="sxs-lookup"><span data-stu-id="d8474-117">Name</span></span> | <span data-ttu-id="d8474-118">В/Из</span><span class="sxs-lookup"><span data-stu-id="d8474-118">In/Out</span></span> | [<span data-ttu-id="d8474-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="d8474-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="d8474-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="d8474-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d8474-121">Размер</span><span class="sxs-lookup"><span data-stu-id="d8474-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="d8474-122">s</span><span class="sxs-lookup"><span data-stu-id="d8474-122">s</span></span>    | <span data-ttu-id="d8474-123">in</span><span class="sxs-lookup"><span data-stu-id="d8474-123">in</span></span>     | [<span data-ttu-id="d8474-124">**объектами**</span><span class="sxs-lookup"><span data-stu-id="d8474-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d8474-125">самплеркубе</span><span class="sxs-lookup"><span data-stu-id="d8474-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="d8474-126">1</span><span class="sxs-lookup"><span data-stu-id="d8474-126">1</span></span>    |
| <span data-ttu-id="d8474-127">t</span><span class="sxs-lookup"><span data-stu-id="d8474-127">t</span></span>    | <span data-ttu-id="d8474-128">in</span><span class="sxs-lookup"><span data-stu-id="d8474-128">in</span></span>     | [<span data-ttu-id="d8474-129">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="d8474-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d8474-130">**float**</span><span class="sxs-lookup"><span data-stu-id="d8474-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d8474-131">4</span><span class="sxs-lookup"><span data-stu-id="d8474-131">4</span></span>    |
| <span data-ttu-id="d8474-132">обратно</span><span class="sxs-lookup"><span data-stu-id="d8474-132">ret</span></span>  | <span data-ttu-id="d8474-133">out</span><span class="sxs-lookup"><span data-stu-id="d8474-133">out</span></span>    | [<span data-ttu-id="d8474-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="d8474-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d8474-135">**float**</span><span class="sxs-lookup"><span data-stu-id="d8474-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d8474-136">4</span><span class="sxs-lookup"><span data-stu-id="d8474-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d8474-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d8474-137">Minimum Shader Model</span></span>

<span data-ttu-id="d8474-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="d8474-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d8474-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d8474-139">Shader Model</span></span>                                              | <span data-ttu-id="d8474-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d8474-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="d8474-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="d8474-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d8474-142">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="d8474-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="d8474-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8474-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d8474-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="d8474-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="d8474-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8474-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d8474-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="d8474-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="d8474-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8474-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d8474-148">Нет</span><span class="sxs-lookup"><span data-stu-id="d8474-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="d8474-149">См. также</span><span class="sxs-lookup"><span data-stu-id="d8474-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8474-150">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d8474-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

