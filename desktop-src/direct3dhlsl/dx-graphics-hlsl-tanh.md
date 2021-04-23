---
title: tanh
description: Возвращает гиперболический тангенс указанного значения.
ms.assetid: e2d27aa0-5e03-4f2f-a29c-884711710c8d
keywords:
- tanh HLSL
topic_type:
- apiref
api_name:
- tanh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c5312aaac6d6f164e940f99183e61688b393fbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070200"
---
# <a name="tanh"></a><span data-ttu-id="406de-104">tanh</span><span class="sxs-lookup"><span data-stu-id="406de-104">tanh</span></span>

<span data-ttu-id="406de-105">Возвращает гиперболический тангенс указанного значения.</span><span class="sxs-lookup"><span data-stu-id="406de-105">Returns the hyperbolic tangent of the specified value.</span></span>



| <span data-ttu-id="406de-106">*RET* tanh (*x*)</span><span class="sxs-lookup"><span data-stu-id="406de-106">*ret* tanh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="406de-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="406de-107">Parameters</span></span>



| <span data-ttu-id="406de-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="406de-108">Item</span></span>                                                   | <span data-ttu-id="406de-109">Описание</span><span class="sxs-lookup"><span data-stu-id="406de-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="406de-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="406de-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="406de-111">\[в \] заданном значении в радианах.</span><span class="sxs-lookup"><span data-stu-id="406de-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="406de-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="406de-112">Return Value</span></span>

<span data-ttu-id="406de-113">Гиперболический тангенс параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="406de-113">The hyperbolic tangent of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="406de-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="406de-114">Type Description</span></span>



| <span data-ttu-id="406de-115">Имя</span><span class="sxs-lookup"><span data-stu-id="406de-115">Name</span></span>  | [<span data-ttu-id="406de-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="406de-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="406de-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="406de-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="406de-118">Размер</span><span class="sxs-lookup"><span data-stu-id="406de-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="406de-119">*x*</span><span class="sxs-lookup"><span data-stu-id="406de-119">*x*</span></span>   | <span data-ttu-id="406de-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="406de-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="406de-121">**float**</span><span class="sxs-lookup"><span data-stu-id="406de-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="406de-122">any</span><span class="sxs-lookup"><span data-stu-id="406de-122">any</span></span>                            |
| <span data-ttu-id="406de-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="406de-123">*ret*</span></span> | <span data-ttu-id="406de-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="406de-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="406de-125">**float**</span><span class="sxs-lookup"><span data-stu-id="406de-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="406de-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="406de-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="406de-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="406de-127">Minimum Shader Model</span></span>

<span data-ttu-id="406de-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="406de-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="406de-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="406de-129">Shader Model</span></span>                                                                       | <span data-ttu-id="406de-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="406de-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="406de-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="406de-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="406de-132">да</span><span class="sxs-lookup"><span data-stu-id="406de-132">yes</span></span>                 |
| [<span data-ttu-id="406de-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="406de-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="406de-134">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="406de-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="406de-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="406de-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="406de-136">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="406de-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

