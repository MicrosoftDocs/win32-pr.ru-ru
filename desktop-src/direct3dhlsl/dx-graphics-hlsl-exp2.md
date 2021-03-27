---
title: EXP2 (Корекрт \_ Math. h)
description: Возвращает значение 2 экспоненциального или 2x указанного значения.
ms.assetid: 68b0057c-864d-440b-84f6-781d5fa3b019
keywords:
- EXP2 HLSL
topic_type:
- apiref
api_name:
- exp2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63aaf5ee7c29da49ca2e7b21d80af6967721058d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986861"
---
# <a name="exp2"></a><span data-ttu-id="2950f-104">EXP2</span><span class="sxs-lookup"><span data-stu-id="2950f-104">exp2</span></span>

<span data-ttu-id="2950f-105">Возвращает значение по основанию 2 экспоненциального или 2<sup>x</sup>указанного значения.</span><span class="sxs-lookup"><span data-stu-id="2950f-105">Returns the base 2 exponential, or 2<sup>x</sup>, of the specified value.</span></span>



| <span data-ttu-id="2950f-106">*RET* EXP2 (*x*)</span><span class="sxs-lookup"><span data-stu-id="2950f-106">*ret* exp2(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="2950f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2950f-107">Parameters</span></span>



| <span data-ttu-id="2950f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="2950f-108">Item</span></span>                                                   | <span data-ttu-id="2950f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2950f-109">Description</span></span>                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="2950f-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="2950f-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="2950f-111">\[в \] указанном значении с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="2950f-111">\[in\] The specified floating-point value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="2950f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2950f-112">Return Value</span></span>

<span data-ttu-id="2950f-113">Базовая экспонента параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="2950f-113">The base 2 exponential of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="2950f-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="2950f-114">Type Description</span></span>



| <span data-ttu-id="2950f-115">Имя</span><span class="sxs-lookup"><span data-stu-id="2950f-115">Name</span></span>  | [<span data-ttu-id="2950f-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="2950f-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="2950f-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="2950f-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="2950f-118">Размер</span><span class="sxs-lookup"><span data-stu-id="2950f-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="2950f-119">*x*</span><span class="sxs-lookup"><span data-stu-id="2950f-119">*x*</span></span>   | <span data-ttu-id="2950f-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="2950f-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="2950f-121">**float**</span><span class="sxs-lookup"><span data-stu-id="2950f-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2950f-122">any</span><span class="sxs-lookup"><span data-stu-id="2950f-122">any</span></span>                            |
| <span data-ttu-id="2950f-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="2950f-123">*ret*</span></span> | <span data-ttu-id="2950f-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="2950f-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="2950f-125">**float**</span><span class="sxs-lookup"><span data-stu-id="2950f-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2950f-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="2950f-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2950f-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2950f-127">Minimum Shader Model</span></span>

<span data-ttu-id="2950f-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="2950f-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2950f-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2950f-129">Shader Model</span></span>                                                                       | <span data-ttu-id="2950f-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="2950f-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="2950f-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="2950f-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="2950f-132">да</span><span class="sxs-lookup"><span data-stu-id="2950f-132">yes</span></span>       |
| [<span data-ttu-id="2950f-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2950f-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="2950f-134">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="2950f-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="2950f-135">Требования</span><span class="sxs-lookup"><span data-stu-id="2950f-135">Requirements</span></span>



| <span data-ttu-id="2950f-136">Требование</span><span class="sxs-lookup"><span data-stu-id="2950f-136">Requirement</span></span> | <span data-ttu-id="2950f-137">Значение</span><span class="sxs-lookup"><span data-stu-id="2950f-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2950f-138">Header</span><span class="sxs-lookup"><span data-stu-id="2950f-138">Header</span></span><br/> | <dl> <span data-ttu-id="2950f-139"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2950f-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2950f-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2950f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2950f-141">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="2950f-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

