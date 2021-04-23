---
title: log
description: Возвращает логарифм по базовому e указанного значения.
ms.assetid: 443e7aa7-7219-40ad-aafc-4bce09c8f596
keywords:
- HLSL журнала
topic_type:
- apiref
api_name:
- log
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdd08fe178925406145476b3250e8d256b263c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793021"
---
# <a name="log"></a><span data-ttu-id="77b47-104">log</span><span class="sxs-lookup"><span data-stu-id="77b47-104">log</span></span>

<span data-ttu-id="77b47-105">Возвращает логарифм по базовому e указанного значения.</span><span class="sxs-lookup"><span data-stu-id="77b47-105">Returns the base-e logarithm of the specified value.</span></span>



| <span data-ttu-id="77b47-106">Журнал *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="77b47-106">*ret* log(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="77b47-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="77b47-107">Parameters</span></span>



| <span data-ttu-id="77b47-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="77b47-108">Item</span></span>                                                   | <span data-ttu-id="77b47-109">Описание</span><span class="sxs-lookup"><span data-stu-id="77b47-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="77b47-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="77b47-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="77b47-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="77b47-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="77b47-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77b47-112">Return Value</span></span>

<span data-ttu-id="77b47-113">Логарифм по основанию e параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="77b47-113">The base-e logarithm of the *x* parameter.</span></span> <span data-ttu-id="77b47-114">Если параметр *x* отрицательный, эта функция возвращает неопределенное значение.</span><span class="sxs-lookup"><span data-stu-id="77b47-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="77b47-115">Если параметр *x* равен 0, эта функция ВОЗВРАЩАЕТ-INF.</span><span class="sxs-lookup"><span data-stu-id="77b47-115">If the *x* parameter is 0, this function returns -INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="77b47-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="77b47-116">Type Description</span></span>



| <span data-ttu-id="77b47-117">Имя</span><span class="sxs-lookup"><span data-stu-id="77b47-117">Name</span></span>  | [<span data-ttu-id="77b47-118">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="77b47-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="77b47-119">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="77b47-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="77b47-120">Размер</span><span class="sxs-lookup"><span data-stu-id="77b47-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="77b47-121">*x*</span><span class="sxs-lookup"><span data-stu-id="77b47-121">*x*</span></span>   | <span data-ttu-id="77b47-122">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="77b47-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="77b47-123">**float**</span><span class="sxs-lookup"><span data-stu-id="77b47-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="77b47-124">any</span><span class="sxs-lookup"><span data-stu-id="77b47-124">any</span></span>                            |
| <span data-ttu-id="77b47-125">*обратно*</span><span class="sxs-lookup"><span data-stu-id="77b47-125">*ret*</span></span> | <span data-ttu-id="77b47-126">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="77b47-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="77b47-127">**float**</span><span class="sxs-lookup"><span data-stu-id="77b47-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="77b47-128">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="77b47-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="77b47-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="77b47-129">Minimum Shader Model</span></span>

<span data-ttu-id="77b47-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="77b47-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="77b47-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="77b47-131">Shader Model</span></span>                                                                       | <span data-ttu-id="77b47-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="77b47-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="77b47-133">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="77b47-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="77b47-134">да</span><span class="sxs-lookup"><span data-stu-id="77b47-134">yes</span></span>                 |
| [<span data-ttu-id="77b47-135">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="77b47-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="77b47-136">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="77b47-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="77b47-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77b47-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77b47-138">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="77b47-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

