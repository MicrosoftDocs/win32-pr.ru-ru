---
title: cosh
description: Возвращает гиперболический косинус указанного значения.
ms.assetid: ed68c461-de91-4ce4-a424-8ab28ee43f23
keywords:
- cosh HLSL
topic_type:
- apiref
api_name:
- cosh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3bd6cad2b79e849d8f20bbaf5baa6cfc7db0b702
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997159"
---
# <a name="cosh"></a><span data-ttu-id="4c855-104">cosh</span><span class="sxs-lookup"><span data-stu-id="4c855-104">cosh</span></span>

<span data-ttu-id="4c855-105">Возвращает гиперболический косинус указанного значения.</span><span class="sxs-lookup"><span data-stu-id="4c855-105">Returns the hyperbolic cosine of the specified value.</span></span>



| <span data-ttu-id="4c855-106">*RET* cosh (*x*)</span><span class="sxs-lookup"><span data-stu-id="4c855-106">*ret* cosh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="4c855-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c855-107">Parameters</span></span>



| <span data-ttu-id="4c855-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="4c855-108">Item</span></span>                                                   | <span data-ttu-id="4c855-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4c855-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="4c855-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="4c855-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="4c855-111">\[в \] заданном значении в радианах.</span><span class="sxs-lookup"><span data-stu-id="4c855-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4c855-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c855-112">Return Value</span></span>

<span data-ttu-id="4c855-113">Гиперболический косинус параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="4c855-113">The hyperbolic cosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="4c855-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="4c855-114">Type Description</span></span>



| <span data-ttu-id="4c855-115">Имя</span><span class="sxs-lookup"><span data-stu-id="4c855-115">Name</span></span>  | [<span data-ttu-id="4c855-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="4c855-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="4c855-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="4c855-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="4c855-118">Размер</span><span class="sxs-lookup"><span data-stu-id="4c855-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="4c855-119">*x*</span><span class="sxs-lookup"><span data-stu-id="4c855-119">*x*</span></span>   | <span data-ttu-id="4c855-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="4c855-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="4c855-121">**float**</span><span class="sxs-lookup"><span data-stu-id="4c855-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4c855-122">any</span><span class="sxs-lookup"><span data-stu-id="4c855-122">any</span></span>                            |
| <span data-ttu-id="4c855-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="4c855-123">*ret*</span></span> | <span data-ttu-id="4c855-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="4c855-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="4c855-125">**float**</span><span class="sxs-lookup"><span data-stu-id="4c855-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4c855-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="4c855-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4c855-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4c855-127">Minimum Shader Model</span></span>

<span data-ttu-id="4c855-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="4c855-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4c855-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4c855-129">Shader Model</span></span>                                                                       | <span data-ttu-id="4c855-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="4c855-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4c855-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="4c855-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="4c855-132">да</span><span class="sxs-lookup"><span data-stu-id="4c855-132">yes</span></span>       |
| [<span data-ttu-id="4c855-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c855-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="4c855-134">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="4c855-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="4c855-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c855-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c855-136">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4c855-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

