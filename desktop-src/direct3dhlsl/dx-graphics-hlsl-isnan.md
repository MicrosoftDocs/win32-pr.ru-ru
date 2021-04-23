---
title: isNaN (Корекрт \_ Math. h)
description: Определяет, является ли указанное значение NAN или КНАН.
ms.assetid: 09085634-e610-4793-848e-abda8241f1cc
keywords:
- IsNaN HLSL
topic_type:
- apiref
api_name:
- isnan
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9f4549b6a142f5bf6011cdfb144de92efde64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081936"
---
# <a name="isnan"></a><span data-ttu-id="a52b4-104">IsNaN</span><span class="sxs-lookup"><span data-stu-id="a52b4-104">isnan</span></span>

<span data-ttu-id="a52b4-105">Определяет, является ли указанное значение NAN или КНАН.</span><span class="sxs-lookup"><span data-stu-id="a52b4-105">Determines if the specified value is NAN or QNAN.</span></span>



| <span data-ttu-id="a52b4-106">*RET* isNaN (*x*)</span><span class="sxs-lookup"><span data-stu-id="a52b4-106">*ret* isnan(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="a52b4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a52b4-107">Parameters</span></span>



| <span data-ttu-id="a52b4-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="a52b4-108">Item</span></span>                                                   | <span data-ttu-id="a52b4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a52b4-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="a52b4-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="a52b4-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="a52b4-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="a52b4-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a52b4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a52b4-112">Return Value</span></span>

<span data-ttu-id="a52b4-113">Возвращает значение, равное тому же размеру, что и входные данные, со значением **true** , если параметр *x* равен NaN или КНАН.</span><span class="sxs-lookup"><span data-stu-id="a52b4-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is NAN or QNAN.</span></span> <span data-ttu-id="a52b4-114">В противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a52b4-114">Otherwise, **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="a52b4-115">Описание типа</span><span class="sxs-lookup"><span data-stu-id="a52b4-115">Type Description</span></span>



| <span data-ttu-id="a52b4-116">Имя</span><span class="sxs-lookup"><span data-stu-id="a52b4-116">Name</span></span>  | [<span data-ttu-id="a52b4-117">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="a52b4-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a52b4-118">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="a52b4-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="a52b4-119">Размер</span><span class="sxs-lookup"><span data-stu-id="a52b4-119">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="a52b4-120">*x*</span><span class="sxs-lookup"><span data-stu-id="a52b4-120">*x*</span></span>   | <span data-ttu-id="a52b4-121">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="a52b4-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="a52b4-122">**float**</span><span class="sxs-lookup"><span data-stu-id="a52b4-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a52b4-123">any</span><span class="sxs-lookup"><span data-stu-id="a52b4-123">any</span></span>      |
| <span data-ttu-id="a52b4-124">*обратно*</span><span class="sxs-lookup"><span data-stu-id="a52b4-124">*ret*</span></span> | <span data-ttu-id="a52b4-125">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="a52b4-125">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="a52b4-126">**bool**</span><span class="sxs-lookup"><span data-stu-id="a52b4-126">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="a52b4-127">в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="a52b4-127">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a52b4-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a52b4-128">Minimum Shader Model</span></span>

<span data-ttu-id="a52b4-129">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a52b4-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a52b4-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a52b4-130">Shader Model</span></span>                                                                       | <span data-ttu-id="a52b4-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="a52b4-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="a52b4-132">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="a52b4-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="a52b4-133">да</span><span class="sxs-lookup"><span data-stu-id="a52b4-133">yes</span></span>                 |
| [<span data-ttu-id="a52b4-134">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a52b4-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="a52b4-135">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="a52b4-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a52b4-136">Требования</span><span class="sxs-lookup"><span data-stu-id="a52b4-136">Requirements</span></span>



| <span data-ttu-id="a52b4-137">Требование</span><span class="sxs-lookup"><span data-stu-id="a52b4-137">Requirement</span></span> | <span data-ttu-id="a52b4-138">Значение</span><span class="sxs-lookup"><span data-stu-id="a52b4-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a52b4-139">Header</span><span class="sxs-lookup"><span data-stu-id="a52b4-139">Header</span></span><br/> | <dl> <span data-ttu-id="a52b4-140"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a52b4-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a52b4-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a52b4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a52b4-142">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a52b4-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

