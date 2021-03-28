---
title: радианах
description: Преобразует указанное значение из градусов в радианы.
ms.assetid: 6fc6b1f8-b686-49ba-93ea-2b2470b3fc72
keywords:
- HLSL в радианах
topic_type:
- apiref
api_name:
- radians
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 029c0ffe2838cdcc997e47cae4e0adafede4411d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413620"
---
# <a name="radians"></a><span data-ttu-id="ab4f5-104">радианах</span><span class="sxs-lookup"><span data-stu-id="ab4f5-104">radians</span></span>

<span data-ttu-id="ab4f5-105">Преобразует указанное значение из градусов в радианы.</span><span class="sxs-lookup"><span data-stu-id="ab4f5-105">Converts the specified value from degrees to radians.</span></span>



| <span data-ttu-id="ab4f5-106">*RET* радианы (*x*)</span><span class="sxs-lookup"><span data-stu-id="ab4f5-106">*ret* radians(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="ab4f5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab4f5-107">Parameters</span></span>



| <span data-ttu-id="ab4f5-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="ab4f5-108">Item</span></span>                                                   | <span data-ttu-id="ab4f5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ab4f5-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="ab4f5-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="ab4f5-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ab4f5-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="ab4f5-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ab4f5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab4f5-112">Return Value</span></span>

<span data-ttu-id="ab4f5-113">Параметр *x* , преобразованный из градусов в радианы.</span><span class="sxs-lookup"><span data-stu-id="ab4f5-113">The *x* parameter converted from degrees to radians.</span></span>

## <a name="type-description"></a><span data-ttu-id="ab4f5-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="ab4f5-114">Type Description</span></span>



| <span data-ttu-id="ab4f5-115">Имя</span><span class="sxs-lookup"><span data-stu-id="ab4f5-115">Name</span></span>  | [<span data-ttu-id="ab4f5-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="ab4f5-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ab4f5-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="ab4f5-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ab4f5-118">Размер</span><span class="sxs-lookup"><span data-stu-id="ab4f5-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ab4f5-119">*x*</span><span class="sxs-lookup"><span data-stu-id="ab4f5-119">*x*</span></span>   | <span data-ttu-id="ab4f5-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="ab4f5-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ab4f5-121">**float**</span><span class="sxs-lookup"><span data-stu-id="ab4f5-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ab4f5-122">any</span><span class="sxs-lookup"><span data-stu-id="ab4f5-122">any</span></span>                            |
| <span data-ttu-id="ab4f5-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="ab4f5-123">*ret*</span></span> | <span data-ttu-id="ab4f5-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="ab4f5-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ab4f5-125">**float**</span><span class="sxs-lookup"><span data-stu-id="ab4f5-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ab4f5-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="ab4f5-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ab4f5-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ab4f5-127">Minimum Shader Model</span></span>

<span data-ttu-id="ab4f5-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ab4f5-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ab4f5-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ab4f5-129">Shader Model</span></span>                                                                       | <span data-ttu-id="ab4f5-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ab4f5-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ab4f5-131">[Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) и более высокие модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="ab4f5-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="ab4f5-132">да</span><span class="sxs-lookup"><span data-stu-id="ab4f5-132">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ab4f5-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab4f5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab4f5-134">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ab4f5-134">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

