---
title: log10
description: Возвращает десятичный логарифм указанного значения.
ms.assetid: a94f8438-8153-4a31-bde3-98831edf99e5
keywords:
- LOG10 HLSL
topic_type:
- apiref
api_name:
- log10
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d226dcc33da1aee6d55e21c6d97febc23577503
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338601"
---
# <a name="log10"></a><span data-ttu-id="b84fc-104">log10</span><span class="sxs-lookup"><span data-stu-id="b84fc-104">log10</span></span>

<span data-ttu-id="b84fc-105">Возвращает десятичный логарифм указанного значения.</span><span class="sxs-lookup"><span data-stu-id="b84fc-105">Returns the base-10 logarithm of the specified value.</span></span>



| <span data-ttu-id="b84fc-106">*RET* log10 (*x*)</span><span class="sxs-lookup"><span data-stu-id="b84fc-106">*ret* log10(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="b84fc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b84fc-107">Parameters</span></span>



| <span data-ttu-id="b84fc-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="b84fc-108">Item</span></span>                                                   | <span data-ttu-id="b84fc-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b84fc-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="b84fc-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b84fc-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b84fc-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="b84fc-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b84fc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b84fc-112">Return Value</span></span>

<span data-ttu-id="b84fc-113">Десятичный логарифм параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="b84fc-113">The base-10 logarithm of the *x* parameter.</span></span> <span data-ttu-id="b84fc-114">Если параметр *x* отрицательный, эта функция возвращает неопределенное значение.</span><span class="sxs-lookup"><span data-stu-id="b84fc-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="b84fc-115">Если значение *x* равно 0, эта функция ВОЗВРАЩАЕТ-INF.</span><span class="sxs-lookup"><span data-stu-id="b84fc-115">If the *x* is 0, this function returns -INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="b84fc-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="b84fc-116">Type Description</span></span>



| <span data-ttu-id="b84fc-117">Имя</span><span class="sxs-lookup"><span data-stu-id="b84fc-117">Name</span></span>  | [<span data-ttu-id="b84fc-118">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="b84fc-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b84fc-119">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="b84fc-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b84fc-120">Размер</span><span class="sxs-lookup"><span data-stu-id="b84fc-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b84fc-121">*x*</span><span class="sxs-lookup"><span data-stu-id="b84fc-121">*x*</span></span>   | <span data-ttu-id="b84fc-122">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="b84fc-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="b84fc-123">**float**</span><span class="sxs-lookup"><span data-stu-id="b84fc-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b84fc-124">any</span><span class="sxs-lookup"><span data-stu-id="b84fc-124">any</span></span>                            |
| <span data-ttu-id="b84fc-125">*обратно*</span><span class="sxs-lookup"><span data-stu-id="b84fc-125">*ret*</span></span> | <span data-ttu-id="b84fc-126">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="b84fc-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b84fc-127">**float**</span><span class="sxs-lookup"><span data-stu-id="b84fc-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b84fc-128">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="b84fc-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b84fc-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b84fc-129">Minimum Shader Model</span></span>

<span data-ttu-id="b84fc-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="b84fc-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b84fc-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b84fc-131">Shader Model</span></span>                                                                       | <span data-ttu-id="b84fc-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="b84fc-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="b84fc-133">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="b84fc-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b84fc-134">да</span><span class="sxs-lookup"><span data-stu-id="b84fc-134">yes</span></span>                 |
| [<span data-ttu-id="b84fc-135">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b84fc-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b84fc-136">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="b84fc-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="b84fc-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b84fc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b84fc-138">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b84fc-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

