---
title: Round (Корекрт \_ Math. h)
description: Округляет указанное значение до ближайшего целого числа.
ms.assetid: 258ce717-dca1-4ed2-ad98-1ecfdb58f939
keywords:
- Round HLSL
topic_type:
- apiref
api_name:
- round
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00bf845dfe16a92729b523fba62f6fd6dcde2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000404"
---
# <a name="round"></a><span data-ttu-id="b7530-104">round</span><span class="sxs-lookup"><span data-stu-id="b7530-104">round</span></span>

<span data-ttu-id="b7530-105">Округляет указанное значение до ближайшего целого числа.</span><span class="sxs-lookup"><span data-stu-id="b7530-105">Rounds the specified value to the nearest integer.</span></span> <span data-ttu-id="b7530-106">Половинные случаи округляются до ближайшего четного значения.</span><span class="sxs-lookup"><span data-stu-id="b7530-106">Halfway cases are rounded to the nearest even.</span></span>



| <span data-ttu-id="b7530-107">*RET* -круглый (*x*)</span><span class="sxs-lookup"><span data-stu-id="b7530-107">*ret* round(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="b7530-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7530-108">Parameters</span></span>



| <span data-ttu-id="b7530-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="b7530-109">Item</span></span>                                                   | <span data-ttu-id="b7530-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b7530-110">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="b7530-111"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b7530-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b7530-112">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="b7530-112">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b7530-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7530-113">Return Value</span></span>

<span data-ttu-id="b7530-114">Параметр *x* , округленный до ближайшего целого числа в пределах типа с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="b7530-114">The *x* parameter, rounded to the nearest integer within a floating-point type.</span></span>

## <a name="type-description"></a><span data-ttu-id="b7530-115">Описание типа</span><span class="sxs-lookup"><span data-stu-id="b7530-115">Type Description</span></span>



| <span data-ttu-id="b7530-116">Имя</span><span class="sxs-lookup"><span data-stu-id="b7530-116">Name</span></span>  | [<span data-ttu-id="b7530-117">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="b7530-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b7530-118">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="b7530-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b7530-119">Размер</span><span class="sxs-lookup"><span data-stu-id="b7530-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b7530-120">*x*</span><span class="sxs-lookup"><span data-stu-id="b7530-120">*x*</span></span>   | <span data-ttu-id="b7530-121">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="b7530-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="b7530-122">**float**</span><span class="sxs-lookup"><span data-stu-id="b7530-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7530-123">any</span><span class="sxs-lookup"><span data-stu-id="b7530-123">any</span></span>                            |
| <span data-ttu-id="b7530-124">*обратно*</span><span class="sxs-lookup"><span data-stu-id="b7530-124">*ret*</span></span> | <span data-ttu-id="b7530-125">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="b7530-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b7530-126">**float**</span><span class="sxs-lookup"><span data-stu-id="b7530-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7530-127">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="b7530-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b7530-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b7530-128">Minimum Shader Model</span></span>

<span data-ttu-id="b7530-129">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="b7530-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b7530-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b7530-130">Shader Model</span></span>                                                                       | <span data-ttu-id="b7530-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="b7530-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="b7530-132">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="b7530-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b7530-133">да</span><span class="sxs-lookup"><span data-stu-id="b7530-133">yes</span></span>                 |
| [<span data-ttu-id="b7530-134">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7530-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b7530-135">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="b7530-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b7530-136">Требования</span><span class="sxs-lookup"><span data-stu-id="b7530-136">Requirements</span></span>



| <span data-ttu-id="b7530-137">Требование</span><span class="sxs-lookup"><span data-stu-id="b7530-137">Requirement</span></span> | <span data-ttu-id="b7530-138">Значение</span><span class="sxs-lookup"><span data-stu-id="b7530-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7530-139">Header</span><span class="sxs-lookup"><span data-stu-id="b7530-139">Header</span></span><br/> | <dl> <span data-ttu-id="b7530-140"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7530-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7530-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7530-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7530-142">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b7530-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

