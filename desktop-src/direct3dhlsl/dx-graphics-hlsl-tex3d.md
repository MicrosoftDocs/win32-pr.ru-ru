---
title: tex3D (Справочник по HLSL)
description: Выберет трехмерную текстуру.
ms.assetid: 713eec24-bdf5-456e-98da-30e2c9d7e808
keywords:
- tex3D HLSL
topic_type:
- apiref
api_name:
- tex3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3a071d00dedabdff02bae302c71aa8ecece4ba2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793290"
---
# <a name="tex3d-hlsl-reference"></a><span data-ttu-id="efabc-104">tex3D (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="efabc-104">tex3D (HLSL reference)</span></span>

<span data-ttu-id="efabc-105">Выберет трехмерную текстуру.</span><span class="sxs-lookup"><span data-stu-id="efabc-105">Samples a 3D texture.</span></span>



| <span data-ttu-id="efabc-106">RET tex3D (s, t)</span><span class="sxs-lookup"><span data-stu-id="efabc-106">ret tex3D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="efabc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="efabc-107">Parameters</span></span>



| <span data-ttu-id="efabc-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="efabc-108">Item</span></span>                                                   | <span data-ttu-id="efabc-109">Описание</span><span class="sxs-lookup"><span data-stu-id="efabc-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="efabc-110"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="efabc-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="efabc-111">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="efabc-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="efabc-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="efabc-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="efabc-113">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="efabc-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="efabc-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efabc-114">Return Value</span></span>

<span data-ttu-id="efabc-115">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="efabc-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="efabc-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="efabc-116">Type Description</span></span>



| <span data-ttu-id="efabc-117">Имя</span><span class="sxs-lookup"><span data-stu-id="efabc-117">Name</span></span> | <span data-ttu-id="efabc-118">В/Из</span><span class="sxs-lookup"><span data-stu-id="efabc-118">In/Out</span></span> | [<span data-ttu-id="efabc-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="efabc-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="efabc-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="efabc-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="efabc-121">Размер</span><span class="sxs-lookup"><span data-stu-id="efabc-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="efabc-122">s</span><span class="sxs-lookup"><span data-stu-id="efabc-122">s</span></span>    | <span data-ttu-id="efabc-123">in</span><span class="sxs-lookup"><span data-stu-id="efabc-123">in</span></span>     | [<span data-ttu-id="efabc-124">**объектами**</span><span class="sxs-lookup"><span data-stu-id="efabc-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="efabc-125">sampler3D</span><span class="sxs-lookup"><span data-stu-id="efabc-125">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="efabc-126">1</span><span class="sxs-lookup"><span data-stu-id="efabc-126">1</span></span>    |
| <span data-ttu-id="efabc-127">t</span><span class="sxs-lookup"><span data-stu-id="efabc-127">t</span></span>    | <span data-ttu-id="efabc-128">in</span><span class="sxs-lookup"><span data-stu-id="efabc-128">in</span></span>     | [<span data-ttu-id="efabc-129">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="efabc-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="efabc-130">**float**</span><span class="sxs-lookup"><span data-stu-id="efabc-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="efabc-131">3</span><span class="sxs-lookup"><span data-stu-id="efabc-131">3</span></span>    |
| <span data-ttu-id="efabc-132">обратно</span><span class="sxs-lookup"><span data-stu-id="efabc-132">ret</span></span>  | <span data-ttu-id="efabc-133">out</span><span class="sxs-lookup"><span data-stu-id="efabc-133">out</span></span>    | [<span data-ttu-id="efabc-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="efabc-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="efabc-135">**float**</span><span class="sxs-lookup"><span data-stu-id="efabc-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="efabc-136">4</span><span class="sxs-lookup"><span data-stu-id="efabc-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="efabc-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="efabc-137">Minimum Shader Model</span></span>

<span data-ttu-id="efabc-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="efabc-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="efabc-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="efabc-139">Shader Model</span></span>                                              | <span data-ttu-id="efabc-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="efabc-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efabc-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="efabc-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="efabc-142">Да (только для шейдера Pixel), но при компиляции необходимо использовать [устаревший параметр Compile](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) .</span><span class="sxs-lookup"><span data-stu-id="efabc-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="efabc-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="efabc-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="efabc-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="efabc-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="efabc-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="efabc-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="efabc-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="efabc-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="efabc-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="efabc-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="efabc-148">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="efabc-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="efabc-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efabc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efabc-150">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="efabc-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

