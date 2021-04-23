---
title: Функция ddx_coarse
description: Выполняет частичное производные от низкой точности относительно координаты x на экране.
ms.assetid: 5719f45d-b2ae-4916-8f31-c2797b661814
keywords:
- Функция ddx_coarse HLSL
topic_type:
- apiref
api_name:
- ddx_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f9d4805a1d516a5d8980fcd8209fd6733fe86c4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069135"
---
# <a name="ddx_coarse-function"></a><span data-ttu-id="35ffe-104">\_функция DDX грубая</span><span class="sxs-lookup"><span data-stu-id="35ffe-104">ddx\_coarse function</span></span>

<span data-ttu-id="35ffe-105">Выполняет частичное производные от низкой точности относительно координаты x на экране.</span><span class="sxs-lookup"><span data-stu-id="35ffe-105">Computes a low precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ffe-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35ffe-106">Syntax</span></span>

``` syntax
float ddx_coarse(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="35ffe-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="35ffe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ffe-108">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35ffe-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ffe-109">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="35ffe-109">Type: **float**</span></span>

<span data-ttu-id="35ffe-110">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="35ffe-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35ffe-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35ffe-111">Return value</span></span>

<span data-ttu-id="35ffe-112">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="35ffe-112">Type: **float**</span></span>

<span data-ttu-id="35ffe-113">Частичная точность, производная от *value*.</span><span class="sxs-lookup"><span data-stu-id="35ffe-113">The low precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="35ffe-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="35ffe-114">Remarks</span></span>

<span data-ttu-id="35ffe-115">Также доступны следующие перегруженные версии:</span><span class="sxs-lookup"><span data-stu-id="35ffe-115">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddx_coarse(float2 value);
float3 ddx_coarse(float3 value);
float4 ddx_coarse(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="35ffe-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="35ffe-116">Minimum Shader Model</span></span>

<span data-ttu-id="35ffe-117">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="35ffe-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="35ffe-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="35ffe-118">Shader Model</span></span>                                                                | <span data-ttu-id="35ffe-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="35ffe-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="35ffe-120">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="35ffe-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="35ffe-121">да</span><span class="sxs-lookup"><span data-stu-id="35ffe-121">yes</span></span>       |



 

<span data-ttu-id="35ffe-122">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="35ffe-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="35ffe-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="35ffe-123">Vertex</span></span> | <span data-ttu-id="35ffe-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="35ffe-124">Hull</span></span> | <span data-ttu-id="35ffe-125">Домен</span><span class="sxs-lookup"><span data-stu-id="35ffe-125">Domain</span></span> | <span data-ttu-id="35ffe-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="35ffe-126">Geometry</span></span> | <span data-ttu-id="35ffe-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="35ffe-127">Pixel</span></span> | <span data-ttu-id="35ffe-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="35ffe-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="35ffe-129">x</span><span class="sxs-lookup"><span data-stu-id="35ffe-129">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="35ffe-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35ffe-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ffe-131">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="35ffe-131">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="35ffe-132">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="35ffe-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




