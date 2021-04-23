---
title: sin
description: Возвращает синус указанного значения.
ms.assetid: e1c3ead8-73dd-4798-8553-1a42dbaefe8e
keywords:
- Sin HLSL
topic_type:
- apiref
api_name:
- sin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d48332d35052a893dcb348a70e4d464a6bbfe0c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413506"
---
# <a name="sin"></a><span data-ttu-id="d6008-104">sin</span><span class="sxs-lookup"><span data-stu-id="d6008-104">sin</span></span>

<span data-ttu-id="d6008-105">Возвращает синус указанного значения.</span><span class="sxs-lookup"><span data-stu-id="d6008-105">Returns the sine of the specified value.</span></span>



| <span data-ttu-id="d6008-106">*RET* Sin (*x*)</span><span class="sxs-lookup"><span data-stu-id="d6008-106">*ret* sin(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="d6008-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6008-107">Parameters</span></span>



| <span data-ttu-id="d6008-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="d6008-108">Item</span></span>                                                   | <span data-ttu-id="d6008-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d6008-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="d6008-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="d6008-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d6008-111">\[в \] заданном значении в радианах.</span><span class="sxs-lookup"><span data-stu-id="d6008-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d6008-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6008-112">Return Value</span></span>

<span data-ttu-id="d6008-113">Синус параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="d6008-113">The sine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="d6008-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="d6008-114">Type Description</span></span>



| <span data-ttu-id="d6008-115">Имя</span><span class="sxs-lookup"><span data-stu-id="d6008-115">Name</span></span>  | [<span data-ttu-id="d6008-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="d6008-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d6008-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="d6008-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d6008-118">Размер</span><span class="sxs-lookup"><span data-stu-id="d6008-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d6008-119">*x*</span><span class="sxs-lookup"><span data-stu-id="d6008-119">*x*</span></span>   | <span data-ttu-id="d6008-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="d6008-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="d6008-121">**float**</span><span class="sxs-lookup"><span data-stu-id="d6008-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d6008-122">any</span><span class="sxs-lookup"><span data-stu-id="d6008-122">any</span></span>                            |
| <span data-ttu-id="d6008-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="d6008-123">*ret*</span></span> | <span data-ttu-id="d6008-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="d6008-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d6008-125">**float**</span><span class="sxs-lookup"><span data-stu-id="d6008-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d6008-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="d6008-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d6008-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d6008-127">Minimum Shader Model</span></span>

<span data-ttu-id="d6008-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="d6008-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d6008-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d6008-129">Shader Model</span></span>                                                                       | <span data-ttu-id="d6008-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d6008-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="d6008-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="d6008-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d6008-132">да</span><span class="sxs-lookup"><span data-stu-id="d6008-132">yes</span></span>                 |
| [<span data-ttu-id="d6008-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6008-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d6008-134">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="d6008-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="d6008-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6008-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6008-136">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d6008-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

