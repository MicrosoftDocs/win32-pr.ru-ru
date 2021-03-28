---
title: countbits - функция
description: Подсчитывает количество битов (на компонент) во входном числе.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- Функция каунтбитс HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60d3cd63502c6217e6fb0b0ff17685b2d2b5bf25
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069136"
---
# <a name="countbits-function"></a><span data-ttu-id="e5e7d-104">countbits - функция</span><span class="sxs-lookup"><span data-stu-id="e5e7d-104">countbits function</span></span>

<span data-ttu-id="e5e7d-105">Подсчитывает количество битов (на компонент) во входном числе.</span><span class="sxs-lookup"><span data-stu-id="e5e7d-105">Counts the number of bits (per component) in the input integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5e7d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5e7d-106">Syntax</span></span>

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="e5e7d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5e7d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5e7d-108">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5e7d-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5e7d-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="e5e7d-109">Type: **uint**</span></span>

<span data-ttu-id="e5e7d-110">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="e5e7d-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5e7d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5e7d-111">Return value</span></span>

<span data-ttu-id="e5e7d-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="e5e7d-112">Type: **uint**</span></span>

<span data-ttu-id="e5e7d-113">Число битов.</span><span class="sxs-lookup"><span data-stu-id="e5e7d-113">The number of bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5e7d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5e7d-114">Remarks</span></span>

<span data-ttu-id="e5e7d-115">Также доступны следующие перегруженные версии:</span><span class="sxs-lookup"><span data-stu-id="e5e7d-115">The following overloaded versions are also available:</span></span>

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="e5e7d-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e5e7d-116">Minimum Shader Model</span></span>

<span data-ttu-id="e5e7d-117">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="e5e7d-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e5e7d-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e5e7d-118">Shader Model</span></span>                                                                | <span data-ttu-id="e5e7d-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e5e7d-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e5e7d-120">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="e5e7d-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="e5e7d-121">да</span><span class="sxs-lookup"><span data-stu-id="e5e7d-121">yes</span></span>       |



 

<span data-ttu-id="e5e7d-122">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="e5e7d-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="e5e7d-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="e5e7d-123">Vertex</span></span> | <span data-ttu-id="e5e7d-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="e5e7d-124">Hull</span></span> | <span data-ttu-id="e5e7d-125">Домен</span><span class="sxs-lookup"><span data-stu-id="e5e7d-125">Domain</span></span> | <span data-ttu-id="e5e7d-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="e5e7d-126">Geometry</span></span> | <span data-ttu-id="e5e7d-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="e5e7d-127">Pixel</span></span> | <span data-ttu-id="e5e7d-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="e5e7d-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e5e7d-129">x</span><span class="sxs-lookup"><span data-stu-id="e5e7d-129">x</span></span>      | <span data-ttu-id="e5e7d-130">x</span><span class="sxs-lookup"><span data-stu-id="e5e7d-130">x</span></span>    | <span data-ttu-id="e5e7d-131">x</span><span class="sxs-lookup"><span data-stu-id="e5e7d-131">x</span></span>      | <span data-ttu-id="e5e7d-132">x</span><span class="sxs-lookup"><span data-stu-id="e5e7d-132">x</span></span>        | <span data-ttu-id="e5e7d-133">x</span><span class="sxs-lookup"><span data-stu-id="e5e7d-133">x</span></span>     | <span data-ttu-id="e5e7d-134">x</span><span class="sxs-lookup"><span data-stu-id="e5e7d-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e5e7d-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5e7d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5e7d-136">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="e5e7d-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="e5e7d-137">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="e5e7d-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




