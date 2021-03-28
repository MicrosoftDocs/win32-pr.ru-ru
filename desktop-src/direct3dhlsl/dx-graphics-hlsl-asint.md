---
title: ASIN
description: Интерпретирует битовый шаблон x как целое число.
ms.assetid: e17e0a11-ef52-4b23-94b8-5db0b18aff4d
keywords:
- ASIN HLSL
topic_type:
- apiref
api_name:
- asint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1b0ca7e1c7b3716be1a3029c5478f96e261ce5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070394"
---
# <a name="asint"></a><span data-ttu-id="1ac31-104">ASIN</span><span class="sxs-lookup"><span data-stu-id="1ac31-104">asint</span></span>

<span data-ttu-id="1ac31-105">Интерпретирует битовый шаблон *x* как целое число.</span><span class="sxs-lookup"><span data-stu-id="1ac31-105">Interprets the bit pattern of *x* as an integer.</span></span>



| <span data-ttu-id="1ac31-106">RET-ASIN (*x*)</span><span class="sxs-lookup"><span data-stu-id="1ac31-106">ret asint(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="1ac31-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ac31-107">Parameters</span></span>



| <span data-ttu-id="1ac31-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="1ac31-108">Item</span></span>                                                   | <span data-ttu-id="1ac31-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1ac31-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="1ac31-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="1ac31-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="1ac31-111">\[во \] входном значении.</span><span class="sxs-lookup"><span data-stu-id="1ac31-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="1ac31-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ac31-112">Return Value</span></span>

<span data-ttu-id="1ac31-113">Входные данные, интерпретируемые как целое число.</span><span class="sxs-lookup"><span data-stu-id="1ac31-113">The input interpreted as an integer.</span></span>

## <a name="type-description"></a><span data-ttu-id="1ac31-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="1ac31-114">Type Description</span></span>



| <span data-ttu-id="1ac31-115">Имя</span><span class="sxs-lookup"><span data-stu-id="1ac31-115">Name</span></span>  | [<span data-ttu-id="1ac31-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="1ac31-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="1ac31-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="1ac31-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                  | <span data-ttu-id="1ac31-118">Размер</span><span class="sxs-lookup"><span data-stu-id="1ac31-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="1ac31-119">*x*</span><span class="sxs-lookup"><span data-stu-id="1ac31-119">*x*</span></span>   | <span data-ttu-id="1ac31-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="1ac31-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="1ac31-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **uint**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="1ac31-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="1ac31-122">any</span><span class="sxs-lookup"><span data-stu-id="1ac31-122">any</span></span>                            |
| <span data-ttu-id="1ac31-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="1ac31-123">*ret*</span></span> | <span data-ttu-id="1ac31-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="1ac31-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="1ac31-125">**int**</span><span class="sxs-lookup"><span data-stu-id="1ac31-125">**int**</span></span>](/windows/desktop/WinProg/windows-data-types)                                           | <span data-ttu-id="1ac31-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="1ac31-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1ac31-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1ac31-127">Minimum Shader Model</span></span>

<span data-ttu-id="1ac31-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="1ac31-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1ac31-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1ac31-129">Shader Model</span></span>                                                        | <span data-ttu-id="1ac31-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1ac31-130">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="1ac31-131">[Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров</span><span class="sxs-lookup"><span data-stu-id="1ac31-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="1ac31-132">да</span><span class="sxs-lookup"><span data-stu-id="1ac31-132">yes</span></span>       |
| [<span data-ttu-id="1ac31-133">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1ac31-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="1ac31-134">Нет</span><span class="sxs-lookup"><span data-stu-id="1ac31-134">no</span></span>        |
| [<span data-ttu-id="1ac31-135">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1ac31-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="1ac31-136">Нет</span><span class="sxs-lookup"><span data-stu-id="1ac31-136">no</span></span>        |
| [<span data-ttu-id="1ac31-137">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1ac31-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="1ac31-138">Нет</span><span class="sxs-lookup"><span data-stu-id="1ac31-138">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="1ac31-139">См. также</span><span class="sxs-lookup"><span data-stu-id="1ac31-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ac31-140">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="1ac31-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

