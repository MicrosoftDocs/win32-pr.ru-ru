---
title: TRUNC (Корекрт \_ Math. h)
description: Усекает значение с плавающей запятой до целочисленного компонента.
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- TRUNC HLSL
topic_type:
- apiref
api_name:
- trunc
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34493f60e60bc0dce35f5f9db50360265191c742
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998459"
---
# <a name="trunc"></a><span data-ttu-id="87114-104">trunc</span><span class="sxs-lookup"><span data-stu-id="87114-104">trunc</span></span>

<span data-ttu-id="87114-105">Усекает значение с плавающей запятой до целочисленного компонента.</span><span class="sxs-lookup"><span data-stu-id="87114-105">Truncates a floating-point value to the integer component.</span></span>



| <span data-ttu-id="87114-106">RET TRUNC (*x*)</span><span class="sxs-lookup"><span data-stu-id="87114-106">ret trunc(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="87114-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="87114-107">Parameters</span></span>



| <span data-ttu-id="87114-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="87114-108">Item</span></span>                                                   | <span data-ttu-id="87114-109">Описание</span><span class="sxs-lookup"><span data-stu-id="87114-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="87114-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="87114-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="87114-111">\[в \] указанных входных данных.</span><span class="sxs-lookup"><span data-stu-id="87114-111">\[in\] The specified input.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="87114-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87114-112">Return Value</span></span>

<span data-ttu-id="87114-113">Входное значение, усеченное до целочисленного компонента.</span><span class="sxs-lookup"><span data-stu-id="87114-113">The input value truncated to an integer component.</span></span>

## <a name="remarks"></a><span data-ttu-id="87114-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="87114-114">Remarks</span></span>

<span data-ttu-id="87114-115">Эта функция усекает значение с плавающей запятой до целочисленного компонента.</span><span class="sxs-lookup"><span data-stu-id="87114-115">This function truncates a floating-point value to the integer component.</span></span> <span data-ttu-id="87114-116">При значении с плавающей запятой, равном 1,6, функция TRUNC возвращает 1,0, где, как функция [**Round (DirectX HLSL)**](dx-graphics-hlsl-round.md) возвращает значение 2,0.</span><span class="sxs-lookup"><span data-stu-id="87114-116">Given a floating-point value of 1.6, the trunc function would return 1.0, where as the [**round (DirectX HLSL)**](dx-graphics-hlsl-round.md) function would return 2.0.</span></span>

## <a name="type-description"></a><span data-ttu-id="87114-117">Описание типа</span><span class="sxs-lookup"><span data-stu-id="87114-117">Type Description</span></span>



| <span data-ttu-id="87114-118">Имя</span><span class="sxs-lookup"><span data-stu-id="87114-118">Name</span></span> | [<span data-ttu-id="87114-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="87114-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="87114-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="87114-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="87114-121">Размер</span><span class="sxs-lookup"><span data-stu-id="87114-121">Size</span></span>                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| <span data-ttu-id="87114-122">*x*</span><span class="sxs-lookup"><span data-stu-id="87114-122">*x*</span></span>  | <span data-ttu-id="87114-123">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="87114-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="87114-124">**float**</span><span class="sxs-lookup"><span data-stu-id="87114-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="87114-125">any</span><span class="sxs-lookup"><span data-stu-id="87114-125">any</span></span>                          |
| <span data-ttu-id="87114-126">обратно</span><span class="sxs-lookup"><span data-stu-id="87114-126">ret</span></span>  | <span data-ttu-id="87114-127">Тот же тип, что и входные данные x</span><span class="sxs-lookup"><span data-stu-id="87114-127">Same type as input x</span></span>                                                                                           | [<span data-ttu-id="87114-128">**float**</span><span class="sxs-lookup"><span data-stu-id="87114-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="87114-129">Те же измерения, что и входные x</span><span class="sxs-lookup"><span data-stu-id="87114-129">Same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="87114-130">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="87114-130">Minimum Shader Model</span></span>

<span data-ttu-id="87114-131">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="87114-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="87114-132">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="87114-132">Shader Model</span></span>                                                                       | <span data-ttu-id="87114-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="87114-133">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="87114-134">[Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) и более высокие модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="87114-134">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="87114-135">да</span><span class="sxs-lookup"><span data-stu-id="87114-135">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="87114-136">Требования</span><span class="sxs-lookup"><span data-stu-id="87114-136">Requirements</span></span>



| <span data-ttu-id="87114-137">Требование</span><span class="sxs-lookup"><span data-stu-id="87114-137">Requirement</span></span> | <span data-ttu-id="87114-138">Значение</span><span class="sxs-lookup"><span data-stu-id="87114-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="87114-139">Header</span><span class="sxs-lookup"><span data-stu-id="87114-139">Header</span></span><br/> | <dl> <span data-ttu-id="87114-140"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="87114-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87114-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87114-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87114-142">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="87114-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

