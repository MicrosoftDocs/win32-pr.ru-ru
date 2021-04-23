---
title: tan
description: Возвращает тангенс указанного значения.
ms.assetid: ca03b184-9e1a-4152-9292-f8af38aa9423
keywords:
- светло HLSL
topic_type:
- apiref
api_name:
- tan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf9451a2bf1a5759470e87343f1b4a15583b470a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792306"
---
# <a name="tan"></a><span data-ttu-id="a44c2-104">tan</span><span class="sxs-lookup"><span data-stu-id="a44c2-104">tan</span></span>

<span data-ttu-id="a44c2-105">Возвращает тангенс указанного значения.</span><span class="sxs-lookup"><span data-stu-id="a44c2-105">Returns the tangent of the specified value.</span></span>



| <span data-ttu-id="a44c2-106">*RET* -коричневый (*x*)</span><span class="sxs-lookup"><span data-stu-id="a44c2-106">*ret* tan(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="a44c2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a44c2-107">Parameters</span></span>



| <span data-ttu-id="a44c2-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="a44c2-108">Item</span></span>                                                   | <span data-ttu-id="a44c2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a44c2-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="a44c2-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="a44c2-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="a44c2-111">\[в \] заданном значении в радианах.</span><span class="sxs-lookup"><span data-stu-id="a44c2-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a44c2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a44c2-112">Return Value</span></span>

<span data-ttu-id="a44c2-113">Тангенс параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="a44c2-113">The tangent of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="a44c2-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="a44c2-114">Type Description</span></span>



| <span data-ttu-id="a44c2-115">Имя</span><span class="sxs-lookup"><span data-stu-id="a44c2-115">Name</span></span>  | [<span data-ttu-id="a44c2-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="a44c2-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a44c2-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="a44c2-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="a44c2-118">Размер</span><span class="sxs-lookup"><span data-stu-id="a44c2-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="a44c2-119">*x*</span><span class="sxs-lookup"><span data-stu-id="a44c2-119">*x*</span></span>   | <span data-ttu-id="a44c2-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="a44c2-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="a44c2-121">**float**</span><span class="sxs-lookup"><span data-stu-id="a44c2-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a44c2-122">any</span><span class="sxs-lookup"><span data-stu-id="a44c2-122">any</span></span>                            |
| <span data-ttu-id="a44c2-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="a44c2-123">*ret*</span></span> | <span data-ttu-id="a44c2-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="a44c2-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="a44c2-125">**float**</span><span class="sxs-lookup"><span data-stu-id="a44c2-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a44c2-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="a44c2-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a44c2-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a44c2-127">Minimum Shader Model</span></span>

<span data-ttu-id="a44c2-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a44c2-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a44c2-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a44c2-129">Shader Model</span></span>                                                                       | <span data-ttu-id="a44c2-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="a44c2-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="a44c2-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="a44c2-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="a44c2-132">да</span><span class="sxs-lookup"><span data-stu-id="a44c2-132">yes</span></span>                 |
| [<span data-ttu-id="a44c2-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a44c2-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="a44c2-134">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="a44c2-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="a44c2-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a44c2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a44c2-136">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a44c2-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

