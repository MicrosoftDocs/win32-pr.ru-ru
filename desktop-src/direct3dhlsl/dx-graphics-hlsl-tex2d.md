---
title: tex2D (Справочник по HLSL)
description: Пример двухмерной текстуры.
ms.assetid: 9f4cbca8-c3de-42ed-89d9-5e86e47d12e5
keywords:
- tex2D HLSL
topic_type:
- apiref
api_name:
- tex2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ac8edb3bc4bb84c2259e193abda90dc32ef385d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793291"
---
# <a name="tex2d-hlsl-reference"></a><span data-ttu-id="006ad-104">tex2D (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="006ad-104">tex2D (HLSL reference)</span></span>

<span data-ttu-id="006ad-105">Пример двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="006ad-105">Samples a 2D texture.</span></span>



| <span data-ttu-id="006ad-106">RET tex2D (s, t)</span><span class="sxs-lookup"><span data-stu-id="006ad-106">ret tex2D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="006ad-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="006ad-107">Parameters</span></span>



| <span data-ttu-id="006ad-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="006ad-108">Item</span></span>                                                   | <span data-ttu-id="006ad-109">Описание</span><span class="sxs-lookup"><span data-stu-id="006ad-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="006ad-110"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="006ad-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="006ad-111">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="006ad-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="006ad-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="006ad-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="006ad-113">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="006ad-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="006ad-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="006ad-114">Return Value</span></span>

<span data-ttu-id="006ad-115">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="006ad-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="006ad-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="006ad-116">Type Description</span></span>



| <span data-ttu-id="006ad-117">Имя</span><span class="sxs-lookup"><span data-stu-id="006ad-117">Name</span></span> | <span data-ttu-id="006ad-118">В/Из</span><span class="sxs-lookup"><span data-stu-id="006ad-118">In/Out</span></span> | [<span data-ttu-id="006ad-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="006ad-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="006ad-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="006ad-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="006ad-121">Размер</span><span class="sxs-lookup"><span data-stu-id="006ad-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="006ad-122">s</span><span class="sxs-lookup"><span data-stu-id="006ad-122">s</span></span>    | <span data-ttu-id="006ad-123">in</span><span class="sxs-lookup"><span data-stu-id="006ad-123">in</span></span>     | [<span data-ttu-id="006ad-124">**объектами**</span><span class="sxs-lookup"><span data-stu-id="006ad-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="006ad-125">sampler2D</span><span class="sxs-lookup"><span data-stu-id="006ad-125">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="006ad-126">1</span><span class="sxs-lookup"><span data-stu-id="006ad-126">1</span></span>    |
| <span data-ttu-id="006ad-127">t</span><span class="sxs-lookup"><span data-stu-id="006ad-127">t</span></span>    | <span data-ttu-id="006ad-128">in</span><span class="sxs-lookup"><span data-stu-id="006ad-128">in</span></span>     | [<span data-ttu-id="006ad-129">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="006ad-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="006ad-130">**float**</span><span class="sxs-lookup"><span data-stu-id="006ad-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="006ad-131">2</span><span class="sxs-lookup"><span data-stu-id="006ad-131">2</span></span>    |
| <span data-ttu-id="006ad-132">обратно</span><span class="sxs-lookup"><span data-stu-id="006ad-132">ret</span></span>  | <span data-ttu-id="006ad-133">out</span><span class="sxs-lookup"><span data-stu-id="006ad-133">out</span></span>    | [<span data-ttu-id="006ad-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="006ad-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="006ad-135">**float**</span><span class="sxs-lookup"><span data-stu-id="006ad-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="006ad-136">4</span><span class="sxs-lookup"><span data-stu-id="006ad-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="006ad-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="006ad-137">Minimum Shader Model</span></span>

<span data-ttu-id="006ad-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="006ad-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="006ad-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="006ad-139">Shader Model</span></span>                                              | <span data-ttu-id="006ad-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="006ad-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="006ad-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="006ad-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="006ad-142">Да (только для шейдера Pixel), но при компиляции необходимо использовать [устаревший параметр Compile](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) .</span><span class="sxs-lookup"><span data-stu-id="006ad-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="006ad-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="006ad-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="006ad-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="006ad-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="006ad-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="006ad-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="006ad-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="006ad-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="006ad-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="006ad-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="006ad-148">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="006ad-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="006ad-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="006ad-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="006ad-150">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="006ad-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

