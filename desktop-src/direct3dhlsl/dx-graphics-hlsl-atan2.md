---
title: atan2 (Корекрт \_ Math. h)
description: Возвращает арктангенс двух значений (x, y).
ms.assetid: e7b53751-f321-4390-8f8f-ec1fa3aaa798
keywords:
- atan2 HLSL
topic_type:
- apiref
api_name:
- atan2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fbc6574d0fc0d53a165ae7da87c2627a295be4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273768"
---
# <a name="atan2"></a><span data-ttu-id="fea8f-104">atan2</span><span class="sxs-lookup"><span data-stu-id="fea8f-104">atan2</span></span>

<span data-ttu-id="fea8f-105">Возвращает арктангенс двух значений (x, y).</span><span class="sxs-lookup"><span data-stu-id="fea8f-105">Returns the arctangent of two values (x,y).</span></span>



| <span data-ttu-id="fea8f-106">*RET* atan2 (*y*, *x*)</span><span class="sxs-lookup"><span data-stu-id="fea8f-106">*ret* atan2(*y*, *x*)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="fea8f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fea8f-107">Parameters</span></span>



| <span data-ttu-id="fea8f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="fea8f-108">Item</span></span>                                                   | <span data-ttu-id="fea8f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fea8f-109">Description</span></span>                    |
|--------------------------------------------------------|--------------------------------|
| <span data-ttu-id="fea8f-110"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="fea8f-110"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="fea8f-111">\[в \] значении y.</span><span class="sxs-lookup"><span data-stu-id="fea8f-111">\[in\] The y value.</span></span><br/> |
| <span data-ttu-id="fea8f-112"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="fea8f-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="fea8f-113">\[в \] значении x.</span><span class="sxs-lookup"><span data-stu-id="fea8f-113">\[in\] The x value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="fea8f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fea8f-114">Return Value</span></span>

<span data-ttu-id="fea8f-115">Арктангенс (y, x).</span><span class="sxs-lookup"><span data-stu-id="fea8f-115">The arctangent of (y,x).</span></span>

## <a name="remarks"></a><span data-ttu-id="fea8f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="fea8f-116">Remarks</span></span>

<span data-ttu-id="fea8f-117">Знаки параметров *x* и *y* используются для определения квадранта возвращаемых значений в диапазоне от-π до π.</span><span class="sxs-lookup"><span data-stu-id="fea8f-117">The signs of the *x* and *y* parameters are used to determine the quadrant of the return values within the range of -π to π.</span></span> <span data-ttu-id="fea8f-118">Встроенная функция **atan2** HLSL четко определена для всех точек, кроме начала координат, даже если *y* равно 0 и *x* не равно 0.</span><span class="sxs-lookup"><span data-stu-id="fea8f-118">The **atan2** HLSL intrinsic function is well-defined for every point other than the origin, even if *y* equals 0 and *x* does not equal 0.</span></span>

## <a name="type-description"></a><span data-ttu-id="fea8f-119">Описание типа</span><span class="sxs-lookup"><span data-stu-id="fea8f-119">Type Description</span></span>



| <span data-ttu-id="fea8f-120">Имя</span><span class="sxs-lookup"><span data-stu-id="fea8f-120">Name</span></span>  | [<span data-ttu-id="fea8f-121">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="fea8f-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="fea8f-122">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="fea8f-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="fea8f-123">Размер</span><span class="sxs-lookup"><span data-stu-id="fea8f-123">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="fea8f-124">*y*</span><span class="sxs-lookup"><span data-stu-id="fea8f-124">*y*</span></span>   | <span data-ttu-id="fea8f-125">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="fea8f-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="fea8f-126">**float**</span><span class="sxs-lookup"><span data-stu-id="fea8f-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fea8f-127">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="fea8f-127">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="fea8f-128">*x*</span><span class="sxs-lookup"><span data-stu-id="fea8f-128">*x*</span></span>   | <span data-ttu-id="fea8f-129">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="fea8f-129">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="fea8f-130">**float**</span><span class="sxs-lookup"><span data-stu-id="fea8f-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fea8f-131">any</span><span class="sxs-lookup"><span data-stu-id="fea8f-131">any</span></span>                            |
| <span data-ttu-id="fea8f-132">*обратно*</span><span class="sxs-lookup"><span data-stu-id="fea8f-132">*ret*</span></span> | <span data-ttu-id="fea8f-133">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="fea8f-133">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="fea8f-134">**float**</span><span class="sxs-lookup"><span data-stu-id="fea8f-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fea8f-135">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="fea8f-135">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fea8f-136">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fea8f-136">Minimum Shader Model</span></span>

<span data-ttu-id="fea8f-137">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="fea8f-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fea8f-138">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fea8f-138">Shader Model</span></span>                                                                       | <span data-ttu-id="fea8f-139">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="fea8f-139">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="fea8f-140">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="fea8f-140">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="fea8f-141">да</span><span class="sxs-lookup"><span data-stu-id="fea8f-141">yes</span></span>       |
| [<span data-ttu-id="fea8f-142">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fea8f-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="fea8f-143">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="fea8f-143">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="fea8f-144">Требования</span><span class="sxs-lookup"><span data-stu-id="fea8f-144">Requirements</span></span>



| <span data-ttu-id="fea8f-145">Требование</span><span class="sxs-lookup"><span data-stu-id="fea8f-145">Requirement</span></span> | <span data-ttu-id="fea8f-146">Значение</span><span class="sxs-lookup"><span data-stu-id="fea8f-146">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="fea8f-147">Header</span><span class="sxs-lookup"><span data-stu-id="fea8f-147">Header</span></span><br/> | <dl> <span data-ttu-id="fea8f-148"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fea8f-148"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fea8f-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fea8f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fea8f-150">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="fea8f-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

