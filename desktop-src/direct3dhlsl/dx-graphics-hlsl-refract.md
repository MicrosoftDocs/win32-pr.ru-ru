---
title: рефракт
description: Возвращает вектор дробной части с использованием входного луча, нормали области и индекса передробки.
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- рефракт HLSL
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e499d078a020ade1ff9ff2566c3fd15b2a820d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997151"
---
# <a name="refract"></a><span data-ttu-id="12634-104">рефракт</span><span class="sxs-lookup"><span data-stu-id="12634-104">refract</span></span>

<span data-ttu-id="12634-105">Возвращает вектор дробной части с использованием входного луча, нормали области и индекса передробки.</span><span class="sxs-lookup"><span data-stu-id="12634-105">Returns a refraction vector using an entering ray, a surface normal, and a refraction index.</span></span>



| <span data-ttu-id="12634-106">*RET* рефракт (*i*, *n*,?)</span><span class="sxs-lookup"><span data-stu-id="12634-106">*ret* refract(*i*, *n*, ?)</span></span> |
|----------------------------|



 

## <a name="parameters"></a><span data-ttu-id="12634-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="12634-107">Parameters</span></span>



| <span data-ttu-id="12634-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="12634-108">Item</span></span>                                                   | <span data-ttu-id="12634-109">Описание</span><span class="sxs-lookup"><span data-stu-id="12634-109">Description</span></span>                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="12634-110"><span id="i"></span><span id="I"></span>*сохранении*</span><span class="sxs-lookup"><span data-stu-id="12634-110"><span id="i"></span><span id="I"></span>*i*</span></span><br/> | <span data-ttu-id="12634-111">\[в \] векторе направления лучей с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="12634-111">\[in\] A floating-point, ray direction vector.</span></span><br/>    |
| <span data-ttu-id="12634-112"><span id="n"></span><span id="N"></span>*\n*</span><span class="sxs-lookup"><span data-stu-id="12634-112"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="12634-113">\[в \] векторе нормали с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="12634-113">\[in\] A floating-point, surface normal vector.</span></span><br/>   |
| <span data-ttu-id="12634-114">*?*</span><span class="sxs-lookup"><span data-stu-id="12634-114">*?*</span></span><br/>                                         | <span data-ttu-id="12634-115">\[в \] скалярном индексе с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="12634-115">\[in\] A floating-point, refraction index scalar.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="12634-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12634-116">Return Value</span></span>

<span data-ttu-id="12634-117">Вектор дробной части с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="12634-117">A floating-point, refraction vector.</span></span> <span data-ttu-id="12634-118">Если угол между входом в луч i и областью нормали n слишком велик для данного индекса передробки?, то возвращаемое значение равно (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="12634-118">If the angle between the entering ray i and the surface normal n is too great for a given refraction index ?, the return value is (0,0,0).</span></span>

## <a name="type-description"></a><span data-ttu-id="12634-119">Описание типа</span><span class="sxs-lookup"><span data-stu-id="12634-119">Type Description</span></span>



| <span data-ttu-id="12634-120">Имя</span><span class="sxs-lookup"><span data-stu-id="12634-120">Name</span></span>              | [<span data-ttu-id="12634-121">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="12634-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="12634-122">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="12634-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="12634-123">Размер</span><span class="sxs-lookup"><span data-stu-id="12634-123">Size</span></span>                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="12634-124">*i*</span><span class="sxs-lookup"><span data-stu-id="12634-124">*i*</span></span>               | [<span data-ttu-id="12634-125">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="12634-125">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="12634-126">**float**</span><span class="sxs-lookup"><span data-stu-id="12634-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="12634-127">any</span><span class="sxs-lookup"><span data-stu-id="12634-127">any</span></span>                            |
| <span data-ttu-id="12634-128">*n*</span><span class="sxs-lookup"><span data-stu-id="12634-128">*n*</span></span>               | [<span data-ttu-id="12634-129">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="12634-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="12634-130">**float**</span><span class="sxs-lookup"><span data-stu-id="12634-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="12634-131">те же измерения, что и входные данные *i*</span><span class="sxs-lookup"><span data-stu-id="12634-131">same dimension(s) as input *i*</span></span> |
| <span data-ttu-id="12634-132">?</span><span class="sxs-lookup"><span data-stu-id="12634-132">?</span></span>                 | [<span data-ttu-id="12634-133">**скаляр**</span><span class="sxs-lookup"><span data-stu-id="12634-133">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="12634-134">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="12634-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="12634-135">1</span><span class="sxs-lookup"><span data-stu-id="12634-135">1</span></span>                              |
| <span data-ttu-id="12634-136">передробить вектор</span><span class="sxs-lookup"><span data-stu-id="12634-136">refraction vector</span></span> | [<span data-ttu-id="12634-137">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="12634-137">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="12634-138">**float**</span><span class="sxs-lookup"><span data-stu-id="12634-138">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="12634-139">те же измерения, что и входные данные *i*</span><span class="sxs-lookup"><span data-stu-id="12634-139">same dimension(s) as input *i*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="12634-140">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="12634-140">Minimum Shader Model</span></span>

<span data-ttu-id="12634-141">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="12634-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="12634-142">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="12634-142">Shader Model</span></span>                                                                       | <span data-ttu-id="12634-143">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="12634-143">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="12634-144">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="12634-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="12634-145">да</span><span class="sxs-lookup"><span data-stu-id="12634-145">yes</span></span>                 |
| [<span data-ttu-id="12634-146">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12634-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="12634-147">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="12634-147">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="12634-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12634-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12634-149">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="12634-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

