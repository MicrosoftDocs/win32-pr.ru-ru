---
title: ограничение (Корекрт \_ Math. h)
description: Определяет, является ли указанное значение с плавающей точкой конечным.
ms.assetid: 8be10499-2d06-4520-9697-dab2f461bd0d
keywords:
- HLSL
topic_type:
- apiref
api_name:
- isfinite
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c943dadccad9f485668948f366698f3bce5e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998390"
---
# <a name="isfinite"></a><span data-ttu-id="f44f7-104">isFinite</span><span class="sxs-lookup"><span data-stu-id="f44f7-104">isfinite</span></span>

<span data-ttu-id="f44f7-105">Определяет, является ли указанное значение с плавающей точкой конечным.</span><span class="sxs-lookup"><span data-stu-id="f44f7-105">Determines if the specified floating-point value is finite.</span></span>



| <span data-ttu-id="f44f7-106">*RET* -ограничение (*x*)</span><span class="sxs-lookup"><span data-stu-id="f44f7-106">*ret* isfinite(*x*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="f44f7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f44f7-107">Parameters</span></span>



| <span data-ttu-id="f44f7-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="f44f7-108">Item</span></span>                                                   | <span data-ttu-id="f44f7-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f44f7-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="f44f7-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="f44f7-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="f44f7-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="f44f7-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="f44f7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f44f7-112">Return Value</span></span>

<span data-ttu-id="f44f7-113">Возвращает значение, равное тому же размеру, что и входные данные, со значением **true** , если параметр *x* является конечным; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="f44f7-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is finite; otherwise **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="f44f7-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="f44f7-114">Type Description</span></span>



| <span data-ttu-id="f44f7-115">Имя</span><span class="sxs-lookup"><span data-stu-id="f44f7-115">Name</span></span>  | [<span data-ttu-id="f44f7-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="f44f7-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="f44f7-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="f44f7-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f44f7-118">Размер</span><span class="sxs-lookup"><span data-stu-id="f44f7-118">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="f44f7-119">*x*</span><span class="sxs-lookup"><span data-stu-id="f44f7-119">*x*</span></span>   | <span data-ttu-id="f44f7-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="f44f7-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="f44f7-121">**float**</span><span class="sxs-lookup"><span data-stu-id="f44f7-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f44f7-122">any</span><span class="sxs-lookup"><span data-stu-id="f44f7-122">any</span></span>      |
| <span data-ttu-id="f44f7-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="f44f7-123">*ret*</span></span> | <span data-ttu-id="f44f7-124">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="f44f7-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="f44f7-125">**bool**</span><span class="sxs-lookup"><span data-stu-id="f44f7-125">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="f44f7-126">в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="f44f7-126">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f44f7-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f44f7-127">Minimum Shader Model</span></span>

<span data-ttu-id="f44f7-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="f44f7-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f44f7-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f44f7-129">Shader Model</span></span>                                                                       | <span data-ttu-id="f44f7-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="f44f7-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="f44f7-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="f44f7-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="f44f7-132">да</span><span class="sxs-lookup"><span data-stu-id="f44f7-132">yes</span></span>                 |
| [<span data-ttu-id="f44f7-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f44f7-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="f44f7-134">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="f44f7-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f44f7-135">Требования</span><span class="sxs-lookup"><span data-stu-id="f44f7-135">Requirements</span></span>



| <span data-ttu-id="f44f7-136">Требование</span><span class="sxs-lookup"><span data-stu-id="f44f7-136">Requirement</span></span> | <span data-ttu-id="f44f7-137">Значение</span><span class="sxs-lookup"><span data-stu-id="f44f7-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f44f7-138">Header</span><span class="sxs-lookup"><span data-stu-id="f44f7-138">Header</span></span><br/> | <dl> <span data-ttu-id="f44f7-139"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f44f7-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f44f7-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f44f7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f44f7-141">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="f44f7-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

