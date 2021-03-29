---
title: clip
description: Отменяет текущую точку, если указанное значение меньше нуля.
ms.assetid: c9f84a27-5572-45aa-a12f-4446614b7be5
keywords:
- обрезать HLSL
topic_type:
- apiref
api_name:
- clip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92a75f2839dbbb605d976e07fffa5c2f9b27fd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984020"
---
# <a name="clip"></a><span data-ttu-id="14b88-104">clip</span><span class="sxs-lookup"><span data-stu-id="14b88-104">clip</span></span>

<span data-ttu-id="14b88-105">Отменяет текущую точку, если указанное значение меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="14b88-105">Discards the current pixel if the specified value is less than zero.</span></span>



| <span data-ttu-id="14b88-106">клип (*x*)</span><span class="sxs-lookup"><span data-stu-id="14b88-106">clip(*x*)</span></span> |
|-----------|



 

## <a name="parameters"></a><span data-ttu-id="14b88-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="14b88-107">Parameters</span></span>



| <span data-ttu-id="14b88-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="14b88-108">Item</span></span>                                                   | <span data-ttu-id="14b88-109">Описание</span><span class="sxs-lookup"><span data-stu-id="14b88-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="14b88-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="14b88-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="14b88-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="14b88-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="14b88-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14b88-112">Return Value</span></span>

<span data-ttu-id="14b88-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="14b88-113">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b88-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="14b88-114">Remarks</span></span>

<span data-ttu-id="14b88-115">Используйте встроенную функцию **Clip** HLSL, чтобы имитировать обтравочные плоскости, если каждый компонент параметра *x* представляет расстояние от плоскости.</span><span class="sxs-lookup"><span data-stu-id="14b88-115">Use the **clip** HLSL intrinsic function to simulate clipping planes if each component of the *x* parameter represents the distance from a plane.</span></span>

<span data-ttu-id="14b88-116">Кроме того, используйте функцию **Clip** для проверки поведения альфа-канала, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="14b88-116">Also, use the **clip** function to test for alpha behavior, as shown in the following example:</span></span>


```
clip( Input.Color.A < 0.1f ? -1:1 );
```



## <a name="type-description"></a><span data-ttu-id="14b88-117">Описание типа</span><span class="sxs-lookup"><span data-stu-id="14b88-117">Type Description</span></span>



| <span data-ttu-id="14b88-118">Имя</span><span class="sxs-lookup"><span data-stu-id="14b88-118">Name</span></span> | [<span data-ttu-id="14b88-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="14b88-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="14b88-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="14b88-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="14b88-121">Размер</span><span class="sxs-lookup"><span data-stu-id="14b88-121">Size</span></span> |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="14b88-122">*x*</span><span class="sxs-lookup"><span data-stu-id="14b88-122">*x*</span></span>  | <span data-ttu-id="14b88-123">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="14b88-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="14b88-124">**float**</span><span class="sxs-lookup"><span data-stu-id="14b88-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="14b88-125">any</span><span class="sxs-lookup"><span data-stu-id="14b88-125">any</span></span>  |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="14b88-126">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="14b88-126">Minimum Shader Model</span></span>

<span data-ttu-id="14b88-127">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="14b88-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="14b88-128">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="14b88-128">Shader Model</span></span>                                              | <span data-ttu-id="14b88-129">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="14b88-129">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="14b88-130">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="14b88-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="14b88-131">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="14b88-131">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="14b88-132">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="14b88-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="14b88-133">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="14b88-133">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="14b88-134">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="14b88-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="14b88-135">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="14b88-135">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="14b88-136">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="14b88-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="14b88-137">Да (только для шейдера Pixel)</span><span class="sxs-lookup"><span data-stu-id="14b88-137">yes (pixel shader only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="14b88-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14b88-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b88-139">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="14b88-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

