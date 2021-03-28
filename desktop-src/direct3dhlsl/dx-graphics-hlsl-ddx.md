---
title: DDX
description: Возвращает частичный производный от указанного значения по отношению к координате x пространства экрана.
ms.assetid: a21c2d2a-7c62-4dc6-8521-273690be1104
keywords:
- DDX HLSL
topic_type:
- apiref
api_name:
- ddx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc82f41e8968ccfadaf5d87a8058d332f04ce3a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413154"
---
# <a name="ddx"></a><span data-ttu-id="4e84d-104">DDX</span><span class="sxs-lookup"><span data-stu-id="4e84d-104">ddx</span></span>

<span data-ttu-id="4e84d-105">Возвращает частичный производный от указанного значения по отношению к координате x пространства экрана.</span><span class="sxs-lookup"><span data-stu-id="4e84d-105">Returns the partial derivative of the specified value with respect to the screen-space x-coordinate.</span></span>



| <span data-ttu-id="4e84d-106">*RET* -DDX (*x*)</span><span class="sxs-lookup"><span data-stu-id="4e84d-106">*ret* ddx(*x*)</span></span> |
|----------------|



 

<span data-ttu-id="4e84d-107">Эта функция рассчитывает частичный производный объект относительно координаты x пространства экрана.</span><span class="sxs-lookup"><span data-stu-id="4e84d-107">This function computes the partial derivative with respect to the screen-space x-coordinate.</span></span> <span data-ttu-id="4e84d-108">Чтобы вычислить частичный производный по отношению к y-координате экранного пространства, используйте функцию [**ДДИ**](dx-graphics-hlsl-ddy.md) .</span><span class="sxs-lookup"><span data-stu-id="4e84d-108">To compute the partial derivative with respect to the screen-space y-coordinate, use the [**ddy**](dx-graphics-hlsl-ddy.md) function.</span></span>

<span data-ttu-id="4e84d-109">Эта функция поддерживается только в шейдерах пикселей.</span><span class="sxs-lookup"><span data-stu-id="4e84d-109">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e84d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e84d-110">Parameters</span></span>



| <span data-ttu-id="4e84d-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="4e84d-111">Item</span></span>                                                   | <span data-ttu-id="4e84d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4e84d-112">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="4e84d-113"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="4e84d-113"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="4e84d-114">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="4e84d-114">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4e84d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e84d-115">Return Value</span></span>

<span data-ttu-id="4e84d-116">Частичная производная от параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="4e84d-116">The partial derivative of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="4e84d-117">Описание типа</span><span class="sxs-lookup"><span data-stu-id="4e84d-117">Type Description</span></span>



| <span data-ttu-id="4e84d-118">Имя</span><span class="sxs-lookup"><span data-stu-id="4e84d-118">Name</span></span>  | [<span data-ttu-id="4e84d-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="4e84d-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="4e84d-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="4e84d-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="4e84d-121">Размер</span><span class="sxs-lookup"><span data-stu-id="4e84d-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="4e84d-122">*x*</span><span class="sxs-lookup"><span data-stu-id="4e84d-122">*x*</span></span>   | <span data-ttu-id="4e84d-123">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="4e84d-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="4e84d-124">**float**</span><span class="sxs-lookup"><span data-stu-id="4e84d-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4e84d-125">any</span><span class="sxs-lookup"><span data-stu-id="4e84d-125">any</span></span>                            |
| <span data-ttu-id="4e84d-126">*обратно*</span><span class="sxs-lookup"><span data-stu-id="4e84d-126">*ret*</span></span> | <span data-ttu-id="4e84d-127">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="4e84d-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="4e84d-128">**float**</span><span class="sxs-lookup"><span data-stu-id="4e84d-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4e84d-129">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="4e84d-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4e84d-130">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4e84d-130">Minimum Shader Model</span></span>

<span data-ttu-id="4e84d-131">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="4e84d-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4e84d-132">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4e84d-132">Shader Model</span></span>                                                                | <span data-ttu-id="4e84d-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="4e84d-133">Supported</span></span>                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="4e84d-134">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="4e84d-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="4e84d-135">да</span><span class="sxs-lookup"><span data-stu-id="4e84d-135">yes</span></span>                                       |
| [<span data-ttu-id="4e84d-136">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="4e84d-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                                  | <span data-ttu-id="4e84d-137">да</span><span class="sxs-lookup"><span data-stu-id="4e84d-137">yes</span></span>                                       |
| [<span data-ttu-id="4e84d-138">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e84d-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)                   | <span data-ttu-id="4e84d-139">да</span><span class="sxs-lookup"><span data-stu-id="4e84d-139">yes</span></span>                                       |
| [<span data-ttu-id="4e84d-140">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e84d-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                   | <span data-ttu-id="4e84d-141">Да в PS \_ 2 \_ x; не поддерживается в PS \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="4e84d-141">yes in ps\_2\_x; unsupported in ps\_2\_0.</span></span> |
| [<span data-ttu-id="4e84d-142">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e84d-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                   | <span data-ttu-id="4e84d-143">Нет</span><span class="sxs-lookup"><span data-stu-id="4e84d-143">no</span></span>                                        |



 

<span data-ttu-id="4e84d-144">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="4e84d-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4e84d-145">Вершина</span><span class="sxs-lookup"><span data-stu-id="4e84d-145">Vertex</span></span> | <span data-ttu-id="4e84d-146">Поверхности</span><span class="sxs-lookup"><span data-stu-id="4e84d-146">Hull</span></span> | <span data-ttu-id="4e84d-147">Домен</span><span class="sxs-lookup"><span data-stu-id="4e84d-147">Domain</span></span> | <span data-ttu-id="4e84d-148">Геометрия</span><span class="sxs-lookup"><span data-stu-id="4e84d-148">Geometry</span></span> | <span data-ttu-id="4e84d-149">Пиксель</span><span class="sxs-lookup"><span data-stu-id="4e84d-149">Pixel</span></span> | <span data-ttu-id="4e84d-150">Вычисления</span><span class="sxs-lookup"><span data-stu-id="4e84d-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4e84d-151">x</span><span class="sxs-lookup"><span data-stu-id="4e84d-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="4e84d-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e84d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e84d-153">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4e84d-153">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

