---
title: фацефорвард
description: Зеркально отражает нормальную поверхность (при необходимости) на противоположную сторону. Возвращает результат в виде n.
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- фацефорвард HLSL
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6a3f035ed4f0d16b500864f941bc4fe5413ff54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134058"
---
# <a name="faceforward"></a><span data-ttu-id="e3db1-104">фацефорвард</span><span class="sxs-lookup"><span data-stu-id="e3db1-104">faceforward</span></span>

<span data-ttu-id="e3db1-105">Зеркально отражает нормальную поверхность (при необходимости) на противоположную сторону. Возвращает результат в виде n.</span><span class="sxs-lookup"><span data-stu-id="e3db1-105">Flips the surface-normal (if needed) to face in a direction opposite to i; returns the result in n.</span></span>



| <span data-ttu-id="e3db1-106">*RET* фацефорвард (*n*, *i*, *NG*)</span><span class="sxs-lookup"><span data-stu-id="e3db1-106">*ret* faceforward(*n*, *i*, *ng*)</span></span> |
|-----------------------------------|



 

<span data-ttu-id="e3db1-107">Эта функция использует следующую формулу:-*n*  знак (точка (*i*, *NG*)).</span><span class="sxs-lookup"><span data-stu-id="e3db1-107">This function uses the following formula: -*n*  sign(dot(*i*, *ng*)).</span></span>

## <a name="parameters"></a><span data-ttu-id="e3db1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3db1-108">Parameters</span></span>



| <span data-ttu-id="e3db1-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="e3db1-109">Item</span></span>                                                      | <span data-ttu-id="e3db1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e3db1-110">Description</span></span>                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3db1-111"><span id="n"></span><span id="N"></span>*\n*</span><span class="sxs-lookup"><span data-stu-id="e3db1-111"><span id="n"></span><span id="N"></span>*n*</span></span><br/>    | <span data-ttu-id="e3db1-112">\[в \] полученном векторе обычной поверхности с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="e3db1-112">\[in\] The resulting floating-point surface-normal vector.</span></span><br/>                                           |
| <span data-ttu-id="e3db1-113"><span id="i"></span><span id="I"></span>*сохранении*</span><span class="sxs-lookup"><span data-stu-id="e3db1-113"><span id="i"></span><span id="I"></span>*i*</span></span><br/>    | <span data-ttu-id="e3db1-114">\[в \] векторе инцидента с плавающей запятой, который указывает позицию представления на позицию заливки.</span><span class="sxs-lookup"><span data-stu-id="e3db1-114">\[in\] A floating-point, incident vector that points from the view position to the shading position.</span></span><br/> |
| <span data-ttu-id="e3db1-115"><span id="ng"></span><span id="NG"></span>*NG*</span><span class="sxs-lookup"><span data-stu-id="e3db1-115"><span id="ng"></span><span id="NG"></span>*ng*</span></span><br/> | <span data-ttu-id="e3db1-116">\[в \] векторной плоскости с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="e3db1-116">\[in\] A floating-point surface-normal vector.</span></span><br/>                                                       |



 

## <a name="return-value"></a><span data-ttu-id="e3db1-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3db1-117">Return Value</span></span>

<span data-ttu-id="e3db1-118">Вектор нормали с плавающей запятой, который является направленным направлением представления.</span><span class="sxs-lookup"><span data-stu-id="e3db1-118">A floating-point, surface normal vector that is facing the view direction.</span></span>

## <a name="type-description"></a><span data-ttu-id="e3db1-119">Описание типа</span><span class="sxs-lookup"><span data-stu-id="e3db1-119">Type Description</span></span>



| <span data-ttu-id="e3db1-120">Имя</span><span class="sxs-lookup"><span data-stu-id="e3db1-120">Name</span></span>  | [<span data-ttu-id="e3db1-121">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="e3db1-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="e3db1-122">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="e3db1-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e3db1-123">Размер</span><span class="sxs-lookup"><span data-stu-id="e3db1-123">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="e3db1-124">*n*</span><span class="sxs-lookup"><span data-stu-id="e3db1-124">*n*</span></span>   | [<span data-ttu-id="e3db1-125">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="e3db1-125">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e3db1-126">**float**</span><span class="sxs-lookup"><span data-stu-id="e3db1-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e3db1-127">any</span><span class="sxs-lookup"><span data-stu-id="e3db1-127">any</span></span>                            |
| <span data-ttu-id="e3db1-128">*i*</span><span class="sxs-lookup"><span data-stu-id="e3db1-128">*i*</span></span>   | [<span data-ttu-id="e3db1-129">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="e3db1-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e3db1-130">**float**</span><span class="sxs-lookup"><span data-stu-id="e3db1-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e3db1-131">те же измерения, что и входные данные *n*</span><span class="sxs-lookup"><span data-stu-id="e3db1-131">same dimension(s) as input *n*</span></span> |
| <span data-ttu-id="e3db1-132">*NG*</span><span class="sxs-lookup"><span data-stu-id="e3db1-132">*ng*</span></span>  | [<span data-ttu-id="e3db1-133">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="e3db1-133">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e3db1-134">**float**</span><span class="sxs-lookup"><span data-stu-id="e3db1-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e3db1-135">те же измерения, что и у входных данных *n*</span><span class="sxs-lookup"><span data-stu-id="e3db1-135">same dimensions as input *n*</span></span>   |
| <span data-ttu-id="e3db1-136">*обратно*</span><span class="sxs-lookup"><span data-stu-id="e3db1-136">*ret*</span></span> | [<span data-ttu-id="e3db1-137">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="e3db1-137">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e3db1-138">**float**</span><span class="sxs-lookup"><span data-stu-id="e3db1-138">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e3db1-139">те же измерения, что и у входных данных *n*</span><span class="sxs-lookup"><span data-stu-id="e3db1-139">same dimensions as input *n*</span></span>   |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e3db1-140">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e3db1-140">Minimum Shader Model</span></span>

<span data-ttu-id="e3db1-141">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="e3db1-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e3db1-142">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e3db1-142">Shader Model</span></span>                                                                       | <span data-ttu-id="e3db1-143">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e3db1-143">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="e3db1-144">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="e3db1-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="e3db1-145">да</span><span class="sxs-lookup"><span data-stu-id="e3db1-145">yes</span></span>                   |
| [<span data-ttu-id="e3db1-146">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3db1-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="e3db1-147">VS \_ 1 \_ 1 и PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="e3db1-147">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="e3db1-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3db1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3db1-149">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e3db1-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

