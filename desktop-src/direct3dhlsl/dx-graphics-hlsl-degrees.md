---
title: градусы
description: Преобразует указанное значение из радианов в градусы.
ms.assetid: e60a3ec4-9177-457a-8314-a5788f353633
keywords:
- градусы HLSL
topic_type:
- apiref
api_name:
- degrees
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47d8bba0ee43da81a18baaeaffca0e3c917e460d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413152"
---
# <a name="degrees"></a><span data-ttu-id="78d4f-104">градусы</span><span class="sxs-lookup"><span data-stu-id="78d4f-104">degrees</span></span>

<span data-ttu-id="78d4f-105">Преобразует указанное значение из радианов в градусы.</span><span class="sxs-lookup"><span data-stu-id="78d4f-105">Converts the specified value from radians to degrees.</span></span>



| <span data-ttu-id="78d4f-106">*RET* градусы (*x*)</span><span class="sxs-lookup"><span data-stu-id="78d4f-106">*ret* degrees(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="78d4f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="78d4f-107">Parameters</span></span>



| <span data-ttu-id="78d4f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="78d4f-108">Item</span></span>                                                   | <span data-ttu-id="78d4f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="78d4f-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="78d4f-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="78d4f-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="78d4f-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="78d4f-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="78d4f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78d4f-112">Return Value</span></span>

<span data-ttu-id="78d4f-113">Результат преобразования параметра *x* из радианов в градусы.</span><span class="sxs-lookup"><span data-stu-id="78d4f-113">The result of converting the *x* parameter from radians to degrees.</span></span>

## <a name="type-description"></a><span data-ttu-id="78d4f-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="78d4f-114">Type Description</span></span>



| <span data-ttu-id="78d4f-115">Имя</span><span class="sxs-lookup"><span data-stu-id="78d4f-115">Name</span></span>  | [<span data-ttu-id="78d4f-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="78d4f-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="78d4f-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="78d4f-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="78d4f-118">Размер</span><span class="sxs-lookup"><span data-stu-id="78d4f-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="78d4f-119">*x*</span><span class="sxs-lookup"><span data-stu-id="78d4f-119">*x*</span></span>   | <span data-ttu-id="78d4f-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="78d4f-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="78d4f-121">**float**</span><span class="sxs-lookup"><span data-stu-id="78d4f-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="78d4f-122">any</span><span class="sxs-lookup"><span data-stu-id="78d4f-122">any</span></span>                            |
| <span data-ttu-id="78d4f-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="78d4f-123">*ret*</span></span> | <span data-ttu-id="78d4f-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="78d4f-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="78d4f-125">**float**</span><span class="sxs-lookup"><span data-stu-id="78d4f-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="78d4f-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="78d4f-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="78d4f-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="78d4f-127">Minimum Shader Model</span></span>

<span data-ttu-id="78d4f-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="78d4f-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="78d4f-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="78d4f-129">Shader Model</span></span>                                                                       | <span data-ttu-id="78d4f-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="78d4f-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="78d4f-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="78d4f-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="78d4f-132">да</span><span class="sxs-lookup"><span data-stu-id="78d4f-132">yes</span></span>       |
| [<span data-ttu-id="78d4f-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="78d4f-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="78d4f-134">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="78d4f-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="78d4f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78d4f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d4f-136">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="78d4f-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

