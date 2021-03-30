---
title: abs
description: Возвращает абсолютное значение указанного значения.
ms.assetid: 8c4cfd8f-8aac-4db3-8247-ce2bbf501e80
keywords:
- ABS HLSL
topic_type:
- apiref
api_name:
- abs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1acd1903e1a65a38f5af7549ab52577bc6cba51c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984057"
---
# <a name="abs"></a><span data-ttu-id="65903-104">abs</span><span class="sxs-lookup"><span data-stu-id="65903-104">abs</span></span>

<span data-ttu-id="65903-105">Возвращает абсолютное значение указанного значения.</span><span class="sxs-lookup"><span data-stu-id="65903-105">Returns the absolute value of the specified value.</span></span>



| <span data-ttu-id="65903-106">RET ABS (*x*)</span><span class="sxs-lookup"><span data-stu-id="65903-106">ret abs(*x*)</span></span> |
|--------------|



 

## <a name="parameters"></a><span data-ttu-id="65903-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="65903-107">Parameters</span></span>



| <span data-ttu-id="65903-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="65903-108">Item</span></span>                                                   | <span data-ttu-id="65903-109">Описание</span><span class="sxs-lookup"><span data-stu-id="65903-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="65903-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="65903-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="65903-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="65903-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="65903-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65903-112">Return Value</span></span>

<span data-ttu-id="65903-113">Абсолютное значение параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="65903-113">The absolute value of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="65903-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="65903-114">Type Description</span></span>



| <span data-ttu-id="65903-115">Имя</span><span class="sxs-lookup"><span data-stu-id="65903-115">Name</span></span>  | [<span data-ttu-id="65903-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="65903-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="65903-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="65903-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="65903-118">Размер</span><span class="sxs-lookup"><span data-stu-id="65903-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="65903-119">*x*</span><span class="sxs-lookup"><span data-stu-id="65903-119">*x*</span></span>   | <span data-ttu-id="65903-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="65903-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="65903-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="65903-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="65903-122">any</span><span class="sxs-lookup"><span data-stu-id="65903-122">any</span></span>                            |
| <span data-ttu-id="65903-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="65903-123">*ret*</span></span> | <span data-ttu-id="65903-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="65903-124">same as input *x*</span></span>                                                                                              | <span data-ttu-id="65903-125">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="65903-125">same as input *x*</span></span>                                                              | <span data-ttu-id="65903-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="65903-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="65903-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="65903-127">Minimum Shader Model</span></span>

<span data-ttu-id="65903-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="65903-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="65903-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="65903-129">Shader Model</span></span>                                                                       | <span data-ttu-id="65903-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="65903-130">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="65903-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="65903-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="65903-132">да</span><span class="sxs-lookup"><span data-stu-id="65903-132">yes</span></span>                   |
| [<span data-ttu-id="65903-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65903-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="65903-134">VS \_ 1 \_ 1 и PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="65903-134">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="65903-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65903-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65903-136">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="65903-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

