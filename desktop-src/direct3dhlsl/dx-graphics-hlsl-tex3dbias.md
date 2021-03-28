---
title: tex3Dbias
description: Пример трехмерной текстуры после сдвига уровня MIP на т.в.
ms.assetid: 6a506036-90d1-420c-a712-a373068c8c16
keywords:
- tex3Dbias HLSL
topic_type:
- apiref
api_name:
- tex3Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53fb0a196831a9dd9d7f7cbe7c34c56259f9a0e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413617"
---
# <a name="tex3dbias"></a><span data-ttu-id="385a8-104">tex3Dbias</span><span class="sxs-lookup"><span data-stu-id="385a8-104">tex3Dbias</span></span>

<span data-ttu-id="385a8-105">Пример трехмерной текстуры после сдвига уровня MIP на т.в.</span><span class="sxs-lookup"><span data-stu-id="385a8-105">Samples a 3D texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="385a8-106">RET tex3Dbias (s, t)</span><span class="sxs-lookup"><span data-stu-id="385a8-106">ret tex3Dbias(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="385a8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="385a8-107">Parameters</span></span>



| <span data-ttu-id="385a8-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="385a8-108">Item</span></span>                                                   | <span data-ttu-id="385a8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="385a8-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="385a8-110"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="385a8-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="385a8-111">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="385a8-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="385a8-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="385a8-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="385a8-113">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="385a8-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="385a8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="385a8-114">Return Value</span></span>

<span data-ttu-id="385a8-115">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="385a8-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="385a8-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="385a8-116">Type Description</span></span>



| <span data-ttu-id="385a8-117">Имя</span><span class="sxs-lookup"><span data-stu-id="385a8-117">Name</span></span> | <span data-ttu-id="385a8-118">В/Из</span><span class="sxs-lookup"><span data-stu-id="385a8-118">In/Out</span></span> | [<span data-ttu-id="385a8-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="385a8-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="385a8-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="385a8-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="385a8-121">Размер</span><span class="sxs-lookup"><span data-stu-id="385a8-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="385a8-122">s</span><span class="sxs-lookup"><span data-stu-id="385a8-122">s</span></span>    | <span data-ttu-id="385a8-123">in</span><span class="sxs-lookup"><span data-stu-id="385a8-123">in</span></span>     | [<span data-ttu-id="385a8-124">**объектами**</span><span class="sxs-lookup"><span data-stu-id="385a8-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="385a8-125">sampler3D</span><span class="sxs-lookup"><span data-stu-id="385a8-125">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="385a8-126">1</span><span class="sxs-lookup"><span data-stu-id="385a8-126">1</span></span>    |
| <span data-ttu-id="385a8-127">t</span><span class="sxs-lookup"><span data-stu-id="385a8-127">t</span></span>    | <span data-ttu-id="385a8-128">in</span><span class="sxs-lookup"><span data-stu-id="385a8-128">in</span></span>     | [<span data-ttu-id="385a8-129">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="385a8-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="385a8-130">**float**</span><span class="sxs-lookup"><span data-stu-id="385a8-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="385a8-131">4</span><span class="sxs-lookup"><span data-stu-id="385a8-131">4</span></span>    |
| <span data-ttu-id="385a8-132">обратно</span><span class="sxs-lookup"><span data-stu-id="385a8-132">ret</span></span>  | <span data-ttu-id="385a8-133">out</span><span class="sxs-lookup"><span data-stu-id="385a8-133">out</span></span>    | [<span data-ttu-id="385a8-134">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="385a8-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="385a8-135">**float**</span><span class="sxs-lookup"><span data-stu-id="385a8-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="385a8-136">4</span><span class="sxs-lookup"><span data-stu-id="385a8-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="385a8-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="385a8-137">Minimum Shader Model</span></span>

<span data-ttu-id="385a8-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="385a8-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="385a8-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="385a8-139">Shader Model</span></span>                                              | <span data-ttu-id="385a8-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="385a8-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="385a8-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="385a8-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="385a8-142">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="385a8-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="385a8-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="385a8-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="385a8-144">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="385a8-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="385a8-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="385a8-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="385a8-146">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="385a8-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="385a8-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="385a8-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="385a8-148">Нет</span><span class="sxs-lookup"><span data-stu-id="385a8-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="385a8-149">См. также</span><span class="sxs-lookup"><span data-stu-id="385a8-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="385a8-150">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="385a8-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

