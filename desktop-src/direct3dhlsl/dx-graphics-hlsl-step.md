---
title: Шаг
description: Сравнивает два значения, возвращая 0 или 1 в зависимости от того, какое значение больше.
ms.assetid: 1c1c4ec4-ae97-42ce-99af-71903e0b5edf
keywords:
- шаг HLSL
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9c800e8d8c6f78386139f822f118163f3b431f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793296"
---
# <a name="step"></a><span data-ttu-id="4e530-104">Шаг</span><span class="sxs-lookup"><span data-stu-id="4e530-104">step</span></span>

<span data-ttu-id="4e530-105">Сравнивает два значения, возвращая 0 или 1 в зависимости от того, какое значение больше.</span><span class="sxs-lookup"><span data-stu-id="4e530-105">Compares two values, returning 0 or 1 based on which value is greater.</span></span>



| <span data-ttu-id="4e530-106">шаг *RET* (*y*, *x*)</span><span class="sxs-lookup"><span data-stu-id="4e530-106">*ret* step(*y*, *x*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="4e530-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e530-107">Parameters</span></span>



| <span data-ttu-id="4e530-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="4e530-108">Item</span></span>                                                   | <span data-ttu-id="4e530-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4e530-109">Description</span></span>                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4e530-110"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="4e530-110"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="4e530-111">\[в \] первом сравниваемом значении с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4e530-111">\[in\] The first floating-point value to compare.</span></span><br/>  |
| <span data-ttu-id="4e530-112"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="4e530-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="4e530-113">\[во \] втором сравниваемом значении с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4e530-113">\[in\] The second floating-point value to compare.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4e530-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e530-114">Return Value</span></span>

<span data-ttu-id="4e530-115">1, если параметр *x* больше или равен значению параметра *y* ; в противном случае — значение 0.</span><span class="sxs-lookup"><span data-stu-id="4e530-115">1 if the *x* parameter is greater than or equal to the *y* parameter; otherwise, 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e530-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="4e530-116">Remarks</span></span>

<span data-ttu-id="4e530-117">Эта функция использует следующую формулу: (*x*  >=  *y*)?</span><span class="sxs-lookup"><span data-stu-id="4e530-117">This function uses the following formula: (*x* >= *y*) ?</span></span> <span data-ttu-id="4e530-118">1:0.</span><span class="sxs-lookup"><span data-stu-id="4e530-118">1 : 0.</span></span> <span data-ttu-id="4e530-119">Функция возвращает значение 0 или 1 в зависимости от того, превышает ли параметр *x* значение параметра *y* .</span><span class="sxs-lookup"><span data-stu-id="4e530-119">The function returns either 0 or 1 depending on whether the *x* parameter is greater than the *y* parameter.</span></span> <span data-ttu-id="4e530-120">Чтобы вычислить гладкую интерполяцию между 0 и 1, используйте встроенную функцию [**смусстеп**](dx-graphics-hlsl-smoothstep.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="4e530-120">To compute a smooth interpolation between 0 and 1, use the [**smoothstep**](dx-graphics-hlsl-smoothstep.md) HLSL intrinsic function.</span></span>

## <a name="type-description"></a><span data-ttu-id="4e530-121">Описание типа</span><span class="sxs-lookup"><span data-stu-id="4e530-121">Type Description</span></span>



| <span data-ttu-id="4e530-122">Имя</span><span class="sxs-lookup"><span data-stu-id="4e530-122">Name</span></span>  | [<span data-ttu-id="4e530-123">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="4e530-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="4e530-124">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="4e530-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="4e530-125">Размер</span><span class="sxs-lookup"><span data-stu-id="4e530-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="4e530-126">*y*</span><span class="sxs-lookup"><span data-stu-id="4e530-126">*y*</span></span>   | <span data-ttu-id="4e530-127">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="4e530-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="4e530-128">**float**</span><span class="sxs-lookup"><span data-stu-id="4e530-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4e530-129">any</span><span class="sxs-lookup"><span data-stu-id="4e530-129">any</span></span>                            |
| <span data-ttu-id="4e530-130">*x*</span><span class="sxs-lookup"><span data-stu-id="4e530-130">*x*</span></span>   | <span data-ttu-id="4e530-131">то же, что входные данные *y*</span><span class="sxs-lookup"><span data-stu-id="4e530-131">same as input *y*</span></span>                                                                                              | [<span data-ttu-id="4e530-132">**float**</span><span class="sxs-lookup"><span data-stu-id="4e530-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4e530-133">те же измерения, что и входные данные *y*</span><span class="sxs-lookup"><span data-stu-id="4e530-133">same dimension(s) as input *y*</span></span> |
| <span data-ttu-id="4e530-134">*обратно*</span><span class="sxs-lookup"><span data-stu-id="4e530-134">*ret*</span></span> | <span data-ttu-id="4e530-135">то же, что входные данные *y*</span><span class="sxs-lookup"><span data-stu-id="4e530-135">same as input *y*</span></span>                                                                                              | [<span data-ttu-id="4e530-136">**float**</span><span class="sxs-lookup"><span data-stu-id="4e530-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4e530-137">те же измерения, что и входные данные *y*</span><span class="sxs-lookup"><span data-stu-id="4e530-137">same dimension(s) as input *y*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4e530-138">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4e530-138">Minimum Shader Model</span></span>

<span data-ttu-id="4e530-139">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="4e530-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4e530-140">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4e530-140">Shader Model</span></span>                                                                       | <span data-ttu-id="4e530-141">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="4e530-141">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="4e530-142">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="4e530-142">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="4e530-143">да</span><span class="sxs-lookup"><span data-stu-id="4e530-143">yes</span></span>                         |
| [<span data-ttu-id="4e530-144">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e530-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="4e530-145">Да (VS \_ 1 \_ 1 и PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="4e530-145">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="4e530-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e530-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e530-147">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4e530-147">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

