---
title: исинф (Корекрт \_ Math. h)
description: Определяет, является ли указанное значение бесконечным.
ms.assetid: 2028dc5a-e48b-4081-a0ec-35901113aab6
keywords:
- исинф HLSL
topic_type:
- apiref
api_name:
- isinf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4df738438d62d5a66dd3b08ad769d475df562d5f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273846"
---
# <a name="isinf"></a><span data-ttu-id="2ee7b-104">isinf</span><span class="sxs-lookup"><span data-stu-id="2ee7b-104">isinf</span></span>

<span data-ttu-id="2ee7b-105">Определяет, является ли указанное значение бесконечным.</span><span class="sxs-lookup"><span data-stu-id="2ee7b-105">Determines if the specified value is infinite.</span></span>



| <span data-ttu-id="2ee7b-106">*RET* исинф (*x*)</span><span class="sxs-lookup"><span data-stu-id="2ee7b-106">*ret* isinf(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="2ee7b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ee7b-107">Parameters</span></span>



| <span data-ttu-id="2ee7b-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="2ee7b-108">Item</span></span>                                                   | <span data-ttu-id="2ee7b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2ee7b-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="2ee7b-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="2ee7b-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="2ee7b-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="2ee7b-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="2ee7b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ee7b-112">Return Value</span></span>

<span data-ttu-id="2ee7b-113">Возвращает значение, равное тому же размеру, что и входные данные, со значением **true** , если параметр *x* имеет значение + INF или-INF.</span><span class="sxs-lookup"><span data-stu-id="2ee7b-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is +INF or -INF.</span></span> <span data-ttu-id="2ee7b-114">В противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="2ee7b-114">Otherwise, **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="2ee7b-115">Описание типа</span><span class="sxs-lookup"><span data-stu-id="2ee7b-115">Type Description</span></span>



| <span data-ttu-id="2ee7b-116">Имя</span><span class="sxs-lookup"><span data-stu-id="2ee7b-116">Name</span></span>  | [<span data-ttu-id="2ee7b-117">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="2ee7b-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="2ee7b-118">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="2ee7b-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="2ee7b-119">Размер</span><span class="sxs-lookup"><span data-stu-id="2ee7b-119">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="2ee7b-120">*x*</span><span class="sxs-lookup"><span data-stu-id="2ee7b-120">*x*</span></span>   | <span data-ttu-id="2ee7b-121">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="2ee7b-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="2ee7b-122">**float**</span><span class="sxs-lookup"><span data-stu-id="2ee7b-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2ee7b-123">any</span><span class="sxs-lookup"><span data-stu-id="2ee7b-123">any</span></span>      |
| <span data-ttu-id="2ee7b-124">*обратно*</span><span class="sxs-lookup"><span data-stu-id="2ee7b-124">*ret*</span></span> | <span data-ttu-id="2ee7b-125">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="2ee7b-125">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="2ee7b-126">**bool**</span><span class="sxs-lookup"><span data-stu-id="2ee7b-126">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="2ee7b-127">в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="2ee7b-127">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2ee7b-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2ee7b-128">Minimum Shader Model</span></span>

<span data-ttu-id="2ee7b-129">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="2ee7b-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2ee7b-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2ee7b-130">Shader Model</span></span>                                                                       | <span data-ttu-id="2ee7b-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="2ee7b-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="2ee7b-132">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="2ee7b-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="2ee7b-133">да</span><span class="sxs-lookup"><span data-stu-id="2ee7b-133">yes</span></span>                 |
| [<span data-ttu-id="2ee7b-134">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2ee7b-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="2ee7b-135">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="2ee7b-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="2ee7b-136">Требования</span><span class="sxs-lookup"><span data-stu-id="2ee7b-136">Requirements</span></span>



| <span data-ttu-id="2ee7b-137">Требование</span><span class="sxs-lookup"><span data-stu-id="2ee7b-137">Requirement</span></span> | <span data-ttu-id="2ee7b-138">Значение</span><span class="sxs-lookup"><span data-stu-id="2ee7b-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee7b-139">Header</span><span class="sxs-lookup"><span data-stu-id="2ee7b-139">Header</span></span><br/> | <dl> <span data-ttu-id="2ee7b-140"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ee7b-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ee7b-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ee7b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ee7b-142">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="2ee7b-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

