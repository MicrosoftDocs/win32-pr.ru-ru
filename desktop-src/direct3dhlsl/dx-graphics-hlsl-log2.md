---
title: log2 (Корекрт \_ Math. h)
description: Возвращает логарифм по основанию 2 указанного значения.
ms.assetid: 0bc75697-92c0-4de5-89bd-2ce824baa03e
keywords:
- log2 HLSL
topic_type:
- apiref
api_name:
- log2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81692071b7886fa3e3096d785bccf80c7eff937a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000508"
---
# <a name="log2"></a><span data-ttu-id="7ff2d-104">log2</span><span class="sxs-lookup"><span data-stu-id="7ff2d-104">log2</span></span>

<span data-ttu-id="7ff2d-105">Возвращает логарифм по основанию 2 указанного значения.</span><span class="sxs-lookup"><span data-stu-id="7ff2d-105">Returns the base-2 logarithm of the specified value.</span></span>



| <span data-ttu-id="7ff2d-106">*RET* log2 (*x*)</span><span class="sxs-lookup"><span data-stu-id="7ff2d-106">*ret* log2(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="7ff2d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ff2d-107">Parameters</span></span>



| <span data-ttu-id="7ff2d-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="7ff2d-108">Item</span></span>                                                   | <span data-ttu-id="7ff2d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7ff2d-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="7ff2d-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="7ff2d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="7ff2d-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="7ff2d-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7ff2d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ff2d-112">Return Value</span></span>

<span data-ttu-id="7ff2d-113">Логарифм по основанию 2 параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="7ff2d-113">The base-2 logarithm of the *x* parameter.</span></span> <span data-ttu-id="7ff2d-114">Если параметр *x* отрицательный, эта функция возвращает неопределенное значение.</span><span class="sxs-lookup"><span data-stu-id="7ff2d-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="7ff2d-115">Если параметр *x* равен 0, эта функция ВОЗВРАЩАЕТ + INF.</span><span class="sxs-lookup"><span data-stu-id="7ff2d-115">If the *x* parameter is 0, this function returns +INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="7ff2d-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="7ff2d-116">Type Description</span></span>



| <span data-ttu-id="7ff2d-117">Имя</span><span class="sxs-lookup"><span data-stu-id="7ff2d-117">Name</span></span>  | [<span data-ttu-id="7ff2d-118">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="7ff2d-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="7ff2d-119">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="7ff2d-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="7ff2d-120">Размер</span><span class="sxs-lookup"><span data-stu-id="7ff2d-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="7ff2d-121">*x*</span><span class="sxs-lookup"><span data-stu-id="7ff2d-121">*x*</span></span>   | <span data-ttu-id="7ff2d-122">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="7ff2d-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="7ff2d-123">**float**</span><span class="sxs-lookup"><span data-stu-id="7ff2d-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7ff2d-124">any</span><span class="sxs-lookup"><span data-stu-id="7ff2d-124">any</span></span>                            |
| <span data-ttu-id="7ff2d-125">*обратно*</span><span class="sxs-lookup"><span data-stu-id="7ff2d-125">*ret*</span></span> | <span data-ttu-id="7ff2d-126">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="7ff2d-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="7ff2d-127">**float**</span><span class="sxs-lookup"><span data-stu-id="7ff2d-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7ff2d-128">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="7ff2d-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7ff2d-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7ff2d-129">Minimum Shader Model</span></span>

<span data-ttu-id="7ff2d-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="7ff2d-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7ff2d-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7ff2d-131">Shader Model</span></span>                                                                       | <span data-ttu-id="7ff2d-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="7ff2d-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="7ff2d-133">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="7ff2d-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="7ff2d-134">да</span><span class="sxs-lookup"><span data-stu-id="7ff2d-134">yes</span></span>                 |
| [<span data-ttu-id="7ff2d-135">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ff2d-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="7ff2d-136">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="7ff2d-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7ff2d-137">Требования</span><span class="sxs-lookup"><span data-stu-id="7ff2d-137">Requirements</span></span>



| <span data-ttu-id="7ff2d-138">Требование</span><span class="sxs-lookup"><span data-stu-id="7ff2d-138">Requirement</span></span> | <span data-ttu-id="7ff2d-139">Значение</span><span class="sxs-lookup"><span data-stu-id="7ff2d-139">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff2d-140">Header</span><span class="sxs-lookup"><span data-stu-id="7ff2d-140">Header</span></span><br/> | <dl> <span data-ttu-id="7ff2d-141"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ff2d-141"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ff2d-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ff2d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff2d-143">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7ff2d-143">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

