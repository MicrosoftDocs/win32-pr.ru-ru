---
title: Текскубе (Справочник по HLSL)
description: Выбор текстуры Куба.
ms.assetid: 77943eb9-86e8-4ae4-8975-8f925e084ce4
keywords:
- Текскубе HLSL
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524ed44028372eeabf176c30da8b3a31a8ee7988
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070136"
---
# <a name="texcube-hlsl-reference"></a><span data-ttu-id="76151-104">Текскубе (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="76151-104">texCUBE (HLSL reference)</span></span>

<span data-ttu-id="76151-105">Выбор текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="76151-105">Samples a cube texture.</span></span>



| <span data-ttu-id="76151-106">RET Текскубе (s, t)</span><span class="sxs-lookup"><span data-stu-id="76151-106">ret texCUBE(s, t)</span></span> |
|-------------------|



 

## <a name="parameters"></a><span data-ttu-id="76151-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="76151-107">Parameters</span></span>



| <span data-ttu-id="76151-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="76151-108">Item</span></span>                                                   | <span data-ttu-id="76151-109">Описание</span><span class="sxs-lookup"><span data-stu-id="76151-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="76151-110"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="76151-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="76151-111">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="76151-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="76151-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="76151-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="76151-113">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="76151-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="76151-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76151-114">Return Value</span></span>

<span data-ttu-id="76151-115">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="76151-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="76151-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="76151-116">Type Description</span></span>



| <span data-ttu-id="76151-117">Имя</span><span class="sxs-lookup"><span data-stu-id="76151-117">Name</span></span> | <span data-ttu-id="76151-118">В/Из</span><span class="sxs-lookup"><span data-stu-id="76151-118">In/Out</span></span> | [<span data-ttu-id="76151-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="76151-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="76151-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="76151-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="76151-121">Размер</span><span class="sxs-lookup"><span data-stu-id="76151-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="76151-122">s</span><span class="sxs-lookup"><span data-stu-id="76151-122">s</span></span>    | <span data-ttu-id="76151-123">in</span><span class="sxs-lookup"><span data-stu-id="76151-123">in</span></span>     | [<span data-ttu-id="76151-124">**объектами**</span><span class="sxs-lookup"><span data-stu-id="76151-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="76151-125">самплеркубе</span><span class="sxs-lookup"><span data-stu-id="76151-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="76151-126">1</span><span class="sxs-lookup"><span data-stu-id="76151-126">1</span></span>    |
| <span data-ttu-id="76151-127">t</span><span class="sxs-lookup"><span data-stu-id="76151-127">t</span></span>    | <span data-ttu-id="76151-128">in</span><span class="sxs-lookup"><span data-stu-id="76151-128">in</span></span>     | [<span data-ttu-id="76151-129">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="76151-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="76151-130">**float**</span><span class="sxs-lookup"><span data-stu-id="76151-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="76151-131">3</span><span class="sxs-lookup"><span data-stu-id="76151-131">3</span></span>    |
| <span data-ttu-id="76151-132">обратно</span><span class="sxs-lookup"><span data-stu-id="76151-132">ret</span></span>  | <span data-ttu-id="76151-133">out</span><span class="sxs-lookup"><span data-stu-id="76151-133">out</span></span>    | [<span data-ttu-id="76151-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="76151-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="76151-135">**float**</span><span class="sxs-lookup"><span data-stu-id="76151-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="76151-136">4</span><span class="sxs-lookup"><span data-stu-id="76151-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="76151-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="76151-137">Minimum Shader Model</span></span>

<span data-ttu-id="76151-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="76151-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="76151-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="76151-139">Shader Model</span></span>                                              | <span data-ttu-id="76151-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="76151-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="76151-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="76151-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="76151-142">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="76151-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="76151-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76151-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="76151-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="76151-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="76151-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76151-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="76151-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="76151-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="76151-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76151-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="76151-148">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="76151-148">yes (pixel shader only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="76151-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76151-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76151-150">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="76151-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

