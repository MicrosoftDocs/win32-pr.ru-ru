---
title: reversebits - функция
description: Изменяет порядок битов на каждый компонент на обратный.
ms.assetid: dad46e25-9980-4645-98eb-d834db704fc8
keywords:
- Функция реверсебитс HLSL
topic_type:
- apiref
api_name:
- reversebits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d98b824883ddc4f06e6c11d30c2759bb0fc2be26
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487141"
---
# <a name="reversebits-function"></a><span data-ttu-id="14ce1-104">reversebits - функция</span><span class="sxs-lookup"><span data-stu-id="14ce1-104">reversebits function</span></span>

<span data-ttu-id="14ce1-105">Изменяет порядок битов на каждый компонент на обратный.</span><span class="sxs-lookup"><span data-stu-id="14ce1-105">Reverses the order of the bits, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ce1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14ce1-106">Syntax</span></span>

``` syntax
uint reversebits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="14ce1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="14ce1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14ce1-108">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14ce1-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14ce1-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="14ce1-109">Type: **uint**</span></span>

<span data-ttu-id="14ce1-110">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="14ce1-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14ce1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14ce1-111">Return value</span></span>

<span data-ttu-id="14ce1-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="14ce1-112">Type: **uint**</span></span>

<span data-ttu-id="14ce1-113">Входное значение с обратным порядком битов.</span><span class="sxs-lookup"><span data-stu-id="14ce1-113">The input value, with the bit order reversed.</span></span>

## <a name="remarks"></a><span data-ttu-id="14ce1-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="14ce1-114">Remarks</span></span>

<span data-ttu-id="14ce1-115">Также доступны следующие перегруженные версии:</span><span class="sxs-lookup"><span data-stu-id="14ce1-115">The following overloaded versions are also available:</span></span>

``` syntax
uint2 reversebits(uint2 value);
uint3 reversebits(uint3 value);
uint4 reversebits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="14ce1-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="14ce1-116">Minimum Shader Model</span></span>

<span data-ttu-id="14ce1-117">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="14ce1-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="14ce1-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="14ce1-118">Shader Model</span></span>                                                                | <span data-ttu-id="14ce1-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="14ce1-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="14ce1-120">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="14ce1-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="14ce1-121">да</span><span class="sxs-lookup"><span data-stu-id="14ce1-121">yes</span></span>       |



 

<span data-ttu-id="14ce1-122">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="14ce1-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="14ce1-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="14ce1-123">Vertex</span></span> | <span data-ttu-id="14ce1-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="14ce1-124">Hull</span></span> | <span data-ttu-id="14ce1-125">Домен</span><span class="sxs-lookup"><span data-stu-id="14ce1-125">Domain</span></span> | <span data-ttu-id="14ce1-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="14ce1-126">Geometry</span></span> | <span data-ttu-id="14ce1-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="14ce1-127">Pixel</span></span> | <span data-ttu-id="14ce1-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="14ce1-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="14ce1-129">x</span><span class="sxs-lookup"><span data-stu-id="14ce1-129">x</span></span>      | <span data-ttu-id="14ce1-130">x</span><span class="sxs-lookup"><span data-stu-id="14ce1-130">x</span></span>    | <span data-ttu-id="14ce1-131">x</span><span class="sxs-lookup"><span data-stu-id="14ce1-131">x</span></span>      | <span data-ttu-id="14ce1-132">x</span><span class="sxs-lookup"><span data-stu-id="14ce1-132">x</span></span>        | <span data-ttu-id="14ce1-133">x</span><span class="sxs-lookup"><span data-stu-id="14ce1-133">x</span></span>     | <span data-ttu-id="14ce1-134">x</span><span class="sxs-lookup"><span data-stu-id="14ce1-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="14ce1-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14ce1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14ce1-136">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="14ce1-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="14ce1-137">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="14ce1-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




