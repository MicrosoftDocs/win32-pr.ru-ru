---
title: Функция ddy_coarse
description: Выполняет частичное производные от низкой точности относительно координаты y экранного пространства.
ms.assetid: f6103cd3-f7ee-41c2-b3cf-9e72ca84b25e
keywords:
- Функция ddy_coarse HLSL
topic_type:
- apiref
api_name:
- ddy_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6fef330e919a31e39306742bb03280454d47626
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069134"
---
# <a name="ddy_coarse-function"></a><span data-ttu-id="daafb-104">ДДИ \_ грубая функция</span><span class="sxs-lookup"><span data-stu-id="daafb-104">ddy\_coarse function</span></span>

<span data-ttu-id="daafb-105">Выполняет частичное производные от низкой точности относительно координаты y экранного пространства.</span><span class="sxs-lookup"><span data-stu-id="daafb-105">Computes a low precision partial derivative with respect to the screen-space y-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="daafb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="daafb-106">Syntax</span></span>

``` syntax
float ddy_coarse(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="daafb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="daafb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daafb-108">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="daafb-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daafb-109">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="daafb-109">Type: **float**</span></span>

<span data-ttu-id="daafb-110">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="daafb-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daafb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="daafb-111">Return value</span></span>

<span data-ttu-id="daafb-112">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="daafb-112">Type: **float**</span></span>

<span data-ttu-id="daafb-113">Частичная точность, производная от *value*.</span><span class="sxs-lookup"><span data-stu-id="daafb-113">The low precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="daafb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="daafb-114">Remarks</span></span>

<span data-ttu-id="daafb-115">Также доступны следующие перегруженные версии:</span><span class="sxs-lookup"><span data-stu-id="daafb-115">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddy_coarse(float2 value);
float3 ddy_coarse(float3 value);
float4 ddy_coarse(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="daafb-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="daafb-116">Minimum Shader Model</span></span>

<span data-ttu-id="daafb-117">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="daafb-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="daafb-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="daafb-118">Shader Model</span></span>                                                                | <span data-ttu-id="daafb-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="daafb-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="daafb-120">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="daafb-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="daafb-121">да</span><span class="sxs-lookup"><span data-stu-id="daafb-121">yes</span></span>       |



 

<span data-ttu-id="daafb-122">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="daafb-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="daafb-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="daafb-123">Vertex</span></span> | <span data-ttu-id="daafb-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="daafb-124">Hull</span></span> | <span data-ttu-id="daafb-125">Домен</span><span class="sxs-lookup"><span data-stu-id="daafb-125">Domain</span></span> | <span data-ttu-id="daafb-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="daafb-126">Geometry</span></span> | <span data-ttu-id="daafb-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="daafb-127">Pixel</span></span> | <span data-ttu-id="daafb-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="daafb-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="daafb-129">x</span><span class="sxs-lookup"><span data-stu-id="daafb-129">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="daafb-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="daafb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daafb-131">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="daafb-131">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="daafb-132">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="daafb-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




