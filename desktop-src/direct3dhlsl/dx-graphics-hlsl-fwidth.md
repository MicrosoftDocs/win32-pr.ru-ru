---
title: фвидс
description: Возвращает абсолютное значение частичного производного указанного значения.
ms.assetid: 7184c3b4-1720-4176-a494-7f73322a918e
keywords:
- фвидс HLSL
topic_type:
- apiref
api_name:
- fwidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf2d5a34e1f387aadb3b044ddd1264616a61109b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134279"
---
# <a name="fwidth"></a><span data-ttu-id="349d6-104">фвидс</span><span class="sxs-lookup"><span data-stu-id="349d6-104">fwidth</span></span>

<span data-ttu-id="349d6-105">Возвращает абсолютное значение частичного производного указанного значения.</span><span class="sxs-lookup"><span data-stu-id="349d6-105">Returns the absolute value of the partial derivatives of the specified value.</span></span>



| <span data-ttu-id="349d6-106">*RET* фвидс (*x*)</span><span class="sxs-lookup"><span data-stu-id="349d6-106">*ret* fwidth(*x*)</span></span> |
|-------------------|



 

<span data-ttu-id="349d6-107">Эта функция вычислит следующее: [**ABS**](dx-graphics-hlsl-abs.md)([**DDX**](dx-graphics-hlsl-ddx.md)(*x*)) + [**ABS**](dx-graphics-hlsl-abs.md)([**ДДИ**](dx-graphics-hlsl-ddy.md)(*x*)).</span><span class="sxs-lookup"><span data-stu-id="349d6-107">This function computes the following: [**abs**](dx-graphics-hlsl-abs.md)([**ddx**](dx-graphics-hlsl-ddx.md)(*x*)) + [**abs**](dx-graphics-hlsl-abs.md)([**ddy**](dx-graphics-hlsl-ddy.md)(*x*)).</span></span>

<span data-ttu-id="349d6-108">Эта функция поддерживается только в шейдерах пикселей.</span><span class="sxs-lookup"><span data-stu-id="349d6-108">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="349d6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="349d6-109">Parameters</span></span>



| <span data-ttu-id="349d6-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="349d6-110">Item</span></span>                                                   | <span data-ttu-id="349d6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="349d6-111">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="349d6-112"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="349d6-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="349d6-113">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="349d6-113">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="349d6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="349d6-114">Return Value</span></span>

<span data-ttu-id="349d6-115">Абсолютное значение частичного производного параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="349d6-115">The absolute value of the partial derivatives of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="349d6-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="349d6-116">Type Description</span></span>



| <span data-ttu-id="349d6-117">Имя</span><span class="sxs-lookup"><span data-stu-id="349d6-117">Name</span></span>  | [<span data-ttu-id="349d6-118">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="349d6-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="349d6-119">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="349d6-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="349d6-120">Размер</span><span class="sxs-lookup"><span data-stu-id="349d6-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="349d6-121">*x*</span><span class="sxs-lookup"><span data-stu-id="349d6-121">*x*</span></span>   | <span data-ttu-id="349d6-122">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="349d6-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="349d6-123">**float**</span><span class="sxs-lookup"><span data-stu-id="349d6-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="349d6-124">any</span><span class="sxs-lookup"><span data-stu-id="349d6-124">any</span></span>                            |
| <span data-ttu-id="349d6-125">*обратно*</span><span class="sxs-lookup"><span data-stu-id="349d6-125">*ret*</span></span> | <span data-ttu-id="349d6-126">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="349d6-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="349d6-127">**float**</span><span class="sxs-lookup"><span data-stu-id="349d6-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="349d6-128">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="349d6-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="349d6-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="349d6-129">Minimum Shader Model</span></span>

<span data-ttu-id="349d6-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="349d6-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="349d6-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="349d6-131">Shader Model</span></span>                                                                       | <span data-ttu-id="349d6-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="349d6-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="349d6-133">[Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) и более высокие модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="349d6-133">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="349d6-134">да</span><span class="sxs-lookup"><span data-stu-id="349d6-134">yes</span></span>                 |
| [<span data-ttu-id="349d6-135">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="349d6-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="349d6-136">Да ( \_ только PS 2 \_ x)</span><span class="sxs-lookup"><span data-stu-id="349d6-136">yes (ps\_2\_x only)</span></span> |
| [<span data-ttu-id="349d6-137">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="349d6-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="349d6-138">Нет</span><span class="sxs-lookup"><span data-stu-id="349d6-138">no</span></span>                  |



 

## <a name="see-also"></a><span data-ttu-id="349d6-139">См. также</span><span class="sxs-lookup"><span data-stu-id="349d6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="349d6-140">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="349d6-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

