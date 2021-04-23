---
title: countbits - функция
description: Подсчитывает количество битов (на компонент), заданных во входном целочисленном параметре.
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
ms.openlocfilehash: 357aceca6e2aea261a9e94212b58ff6308c99560
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925627"
---
# <a name="countbits-function"></a><span data-ttu-id="a5f03-104">countbits - функция</span><span class="sxs-lookup"><span data-stu-id="a5f03-104">countbits function</span></span>

<span data-ttu-id="a5f03-105">Подсчитывает количество битов (на компонент), заданных во входном целочисленном параметре.</span><span class="sxs-lookup"><span data-stu-id="a5f03-105">Counts the number of bits (per component) set in the input integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f03-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5f03-106">Syntax</span></span>

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="a5f03-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5f03-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5f03-108">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5f03-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f03-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="a5f03-109">Type: **uint**</span></span>

<span data-ttu-id="a5f03-110">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="a5f03-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5f03-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5f03-111">Return value</span></span>

<span data-ttu-id="a5f03-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="a5f03-112">Type: **uint**</span></span>

<span data-ttu-id="a5f03-113">Число битов.</span><span class="sxs-lookup"><span data-stu-id="a5f03-113">The number of bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5f03-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5f03-114">Remarks</span></span>

<span data-ttu-id="a5f03-115">Также доступны следующие перегруженные версии:</span><span class="sxs-lookup"><span data-stu-id="a5f03-115">The following overloaded versions are also available:</span></span>

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="a5f03-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a5f03-116">Minimum Shader Model</span></span>

<span data-ttu-id="a5f03-117">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a5f03-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a5f03-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a5f03-118">Shader Model</span></span>                                                                | <span data-ttu-id="a5f03-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="a5f03-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a5f03-120">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="a5f03-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="a5f03-121">да</span><span class="sxs-lookup"><span data-stu-id="a5f03-121">yes</span></span>       |



 

<span data-ttu-id="a5f03-122">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="a5f03-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="a5f03-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="a5f03-123">Vertex</span></span> | <span data-ttu-id="a5f03-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="a5f03-124">Hull</span></span> | <span data-ttu-id="a5f03-125">Домен</span><span class="sxs-lookup"><span data-stu-id="a5f03-125">Domain</span></span> | <span data-ttu-id="a5f03-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="a5f03-126">Geometry</span></span> | <span data-ttu-id="a5f03-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="a5f03-127">Pixel</span></span> | <span data-ttu-id="a5f03-128">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="a5f03-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a5f03-129">x</span><span class="sxs-lookup"><span data-stu-id="a5f03-129">x</span></span>      | <span data-ttu-id="a5f03-130">x</span><span class="sxs-lookup"><span data-stu-id="a5f03-130">x</span></span>    | <span data-ttu-id="a5f03-131">x</span><span class="sxs-lookup"><span data-stu-id="a5f03-131">x</span></span>      | <span data-ttu-id="a5f03-132">x</span><span class="sxs-lookup"><span data-stu-id="a5f03-132">x</span></span>        | <span data-ttu-id="a5f03-133">x</span><span class="sxs-lookup"><span data-stu-id="a5f03-133">x</span></span>     | <span data-ttu-id="a5f03-134">x</span><span class="sxs-lookup"><span data-stu-id="a5f03-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a5f03-135">См. также</span><span class="sxs-lookup"><span data-stu-id="a5f03-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5f03-136">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="a5f03-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="a5f03-137">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="a5f03-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




