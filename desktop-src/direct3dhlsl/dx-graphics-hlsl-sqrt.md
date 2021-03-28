---
title: sqrt
description: Возвращает квадратный корень заданного значения с плавающей запятой на компонент.
ms.assetid: e8debc60-1441-4974-9ab3-6d1c2217caaf
keywords:
- HLSL Sqrt
topic_type:
- apiref
api_name:
- sqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff3c872dac6da28a1ec92993e387bd23daec7f86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104412993"
---
# <a name="sqrt"></a><span data-ttu-id="ce3ae-104">sqrt</span><span class="sxs-lookup"><span data-stu-id="ce3ae-104">sqrt</span></span>

<span data-ttu-id="ce3ae-105">Возвращает квадратный корень заданного значения с плавающей запятой на компонент.</span><span class="sxs-lookup"><span data-stu-id="ce3ae-105">Returns the square root of the specified floating-point value, per component.</span></span>



| <span data-ttu-id="ce3ae-106">*RET* Sqrt (*x*)</span><span class="sxs-lookup"><span data-stu-id="ce3ae-106">*ret* sqrt(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="ce3ae-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce3ae-107">Parameters</span></span>



| <span data-ttu-id="ce3ae-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="ce3ae-108">Item</span></span>                                                   | <span data-ttu-id="ce3ae-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ce3ae-109">Description</span></span>                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="ce3ae-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="ce3ae-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ce3ae-111">\[в \] указанном значении с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="ce3ae-111">\[in\] The specified floating-point value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ce3ae-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce3ae-112">Return Value</span></span>

<span data-ttu-id="ce3ae-113">Квадратный корень параметра *x* на компонент.</span><span class="sxs-lookup"><span data-stu-id="ce3ae-113">The square root of the *x* parameter, per component.</span></span>

## <a name="type-description"></a><span data-ttu-id="ce3ae-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="ce3ae-114">Type Description</span></span>



| <span data-ttu-id="ce3ae-115">Имя</span><span class="sxs-lookup"><span data-stu-id="ce3ae-115">Name</span></span>  | [<span data-ttu-id="ce3ae-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="ce3ae-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ce3ae-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="ce3ae-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ce3ae-118">Размер</span><span class="sxs-lookup"><span data-stu-id="ce3ae-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ce3ae-119">*x*</span><span class="sxs-lookup"><span data-stu-id="ce3ae-119">*x*</span></span>   | <span data-ttu-id="ce3ae-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="ce3ae-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ce3ae-121">**float**</span><span class="sxs-lookup"><span data-stu-id="ce3ae-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ce3ae-122">any</span><span class="sxs-lookup"><span data-stu-id="ce3ae-122">any</span></span>                            |
| <span data-ttu-id="ce3ae-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="ce3ae-123">*ret*</span></span> | <span data-ttu-id="ce3ae-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="ce3ae-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ce3ae-125">**float**</span><span class="sxs-lookup"><span data-stu-id="ce3ae-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ce3ae-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="ce3ae-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ce3ae-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ce3ae-127">Minimum Shader Model</span></span>

<span data-ttu-id="ce3ae-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ce3ae-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ce3ae-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ce3ae-129">Shader Model</span></span>                                                                       | <span data-ttu-id="ce3ae-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ce3ae-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="ce3ae-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="ce3ae-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="ce3ae-132">да</span><span class="sxs-lookup"><span data-stu-id="ce3ae-132">yes</span></span>                 |
| [<span data-ttu-id="ce3ae-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce3ae-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ce3ae-134">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="ce3ae-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="ce3ae-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce3ae-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce3ae-136">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ce3ae-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

