---
title: exp
description: Возвращает значение экспоненты Base-e или ex указанного значения.
ms.assetid: 7a713251-af47-4f8d-b708-40309b80ba18
keywords:
- EXP HLSL
topic_type:
- apiref
api_name:
- exp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 699eb97ae0fd6bbdeba0da47693178d1e4c48e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792043"
---
# <a name="exp"></a><span data-ttu-id="90675-104">exp</span><span class="sxs-lookup"><span data-stu-id="90675-104">exp</span></span>

<span data-ttu-id="90675-105">Возвращает значение экспоненты Base-e, или e<sup>x</sup>, для указанного значения.</span><span class="sxs-lookup"><span data-stu-id="90675-105">Returns the base-e exponential, or e<sup>x</sup>, of the specified value.</span></span>



| <span data-ttu-id="90675-106">*RET* -exp (*x*)</span><span class="sxs-lookup"><span data-stu-id="90675-106">*ret* exp(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="90675-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="90675-107">Parameters</span></span>



| <span data-ttu-id="90675-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="90675-108">Item</span></span>                                                   | <span data-ttu-id="90675-109">Описание</span><span class="sxs-lookup"><span data-stu-id="90675-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="90675-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="90675-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="90675-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="90675-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="90675-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90675-112">Return Value</span></span>

<span data-ttu-id="90675-113">Экспоненциальный показатель параметра *x* в Base-e.</span><span class="sxs-lookup"><span data-stu-id="90675-113">The base-e exponential of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="90675-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="90675-114">Type Description</span></span>



| <span data-ttu-id="90675-115">Имя</span><span class="sxs-lookup"><span data-stu-id="90675-115">Name</span></span>  | [<span data-ttu-id="90675-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="90675-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="90675-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="90675-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="90675-118">Размер</span><span class="sxs-lookup"><span data-stu-id="90675-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="90675-119">*x*</span><span class="sxs-lookup"><span data-stu-id="90675-119">*x*</span></span>   | <span data-ttu-id="90675-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="90675-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="90675-121">**float**</span><span class="sxs-lookup"><span data-stu-id="90675-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="90675-122">any</span><span class="sxs-lookup"><span data-stu-id="90675-122">any</span></span>                            |
| <span data-ttu-id="90675-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="90675-123">*ret*</span></span> | <span data-ttu-id="90675-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="90675-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="90675-125">**float**</span><span class="sxs-lookup"><span data-stu-id="90675-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="90675-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="90675-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="90675-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="90675-127">Minimum Shader Model</span></span>

<span data-ttu-id="90675-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="90675-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="90675-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="90675-129">Shader Model</span></span>                                                                       | <span data-ttu-id="90675-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="90675-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="90675-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="90675-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="90675-132">да</span><span class="sxs-lookup"><span data-stu-id="90675-132">yes</span></span>       |
| [<span data-ttu-id="90675-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="90675-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="90675-134">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="90675-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="90675-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90675-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90675-136">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="90675-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

