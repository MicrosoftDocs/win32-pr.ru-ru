---
title: tex3Dproj
description: Выберет трехмерную текстуру с помощью проектного деления; Координата текстуры делится на t. w до того, как происходит поиск.
ms.assetid: c7062ef0-3169-4cbe-b47b-4efc80944963
keywords:
- tex3Dproj HLSL
topic_type:
- apiref
api_name:
- tex3Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 519477b7dba4f746dc1720a08c2ce581ab7b7205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533416"
---
# <a name="tex3dproj"></a><span data-ttu-id="fdd87-104">tex3Dproj</span><span class="sxs-lookup"><span data-stu-id="fdd87-104">tex3Dproj</span></span>

<span data-ttu-id="fdd87-105">Выберет трехмерную текстуру с помощью проектного деления; Координата текстуры делится на t. w до того, как происходит поиск.</span><span class="sxs-lookup"><span data-stu-id="fdd87-105">Samples a 3D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="fdd87-106">RET tex3Dproj (s, t)</span><span class="sxs-lookup"><span data-stu-id="fdd87-106">ret tex3Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="fdd87-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fdd87-107">Parameters</span></span>



| <span data-ttu-id="fdd87-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="fdd87-108">Item</span></span>                                                   | <span data-ttu-id="fdd87-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fdd87-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="fdd87-110"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="fdd87-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="fdd87-111">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="fdd87-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="fdd87-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="fdd87-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="fdd87-113">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="fdd87-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="fdd87-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fdd87-114">Return Value</span></span>

<span data-ttu-id="fdd87-115">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="fdd87-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="fdd87-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="fdd87-116">Type Description</span></span>



| <span data-ttu-id="fdd87-117">Имя</span><span class="sxs-lookup"><span data-stu-id="fdd87-117">Name</span></span> | <span data-ttu-id="fdd87-118">В/Из</span><span class="sxs-lookup"><span data-stu-id="fdd87-118">In/Out</span></span> | [<span data-ttu-id="fdd87-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="fdd87-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="fdd87-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="fdd87-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="fdd87-121">Размер</span><span class="sxs-lookup"><span data-stu-id="fdd87-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="fdd87-122">s</span><span class="sxs-lookup"><span data-stu-id="fdd87-122">s</span></span>    | <span data-ttu-id="fdd87-123">in</span><span class="sxs-lookup"><span data-stu-id="fdd87-123">in</span></span>     | [<span data-ttu-id="fdd87-124">**объектами**</span><span class="sxs-lookup"><span data-stu-id="fdd87-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fdd87-125">sampler3D</span><span class="sxs-lookup"><span data-stu-id="fdd87-125">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="fdd87-126">1</span><span class="sxs-lookup"><span data-stu-id="fdd87-126">1</span></span>    |
| <span data-ttu-id="fdd87-127">t</span><span class="sxs-lookup"><span data-stu-id="fdd87-127">t</span></span>    | <span data-ttu-id="fdd87-128">in</span><span class="sxs-lookup"><span data-stu-id="fdd87-128">in</span></span>     | [<span data-ttu-id="fdd87-129">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="fdd87-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fdd87-130">**float**</span><span class="sxs-lookup"><span data-stu-id="fdd87-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fdd87-131">4</span><span class="sxs-lookup"><span data-stu-id="fdd87-131">4</span></span>    |
| <span data-ttu-id="fdd87-132">обратно</span><span class="sxs-lookup"><span data-stu-id="fdd87-132">ret</span></span>  | <span data-ttu-id="fdd87-133">out</span><span class="sxs-lookup"><span data-stu-id="fdd87-133">out</span></span>    | [<span data-ttu-id="fdd87-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="fdd87-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fdd87-135">**float**</span><span class="sxs-lookup"><span data-stu-id="fdd87-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fdd87-136">4</span><span class="sxs-lookup"><span data-stu-id="fdd87-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fdd87-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fdd87-137">Minimum Shader Model</span></span>

<span data-ttu-id="fdd87-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="fdd87-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fdd87-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fdd87-139">Shader Model</span></span>                                              | <span data-ttu-id="fdd87-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="fdd87-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="fdd87-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="fdd87-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fdd87-142">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="fdd87-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="fdd87-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdd87-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fdd87-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="fdd87-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="fdd87-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdd87-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fdd87-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="fdd87-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="fdd87-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdd87-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fdd87-148">Нет</span><span class="sxs-lookup"><span data-stu-id="fdd87-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="fdd87-149">См. также</span><span class="sxs-lookup"><span data-stu-id="fdd87-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd87-150">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="fdd87-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

