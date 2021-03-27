---
title: Функция ddx_fine
description: Выполняет частичное производные от высокой точности относительно координаты x пространства экрана. | Функция ddx_fine
ms.assetid: 41062d6f-2b7f-4594-a6de-da37ded5d444
keywords:
- Функция ddx_fine HLSL
topic_type:
- apiref
api_name:
- ddx_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c1a579ba5899cf4d3ac3f25ef5a40337f6291977
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986756"
---
# <a name="ddx_fine-function"></a><span data-ttu-id="5a6ec-105">\_функция DDX прекрасно</span><span class="sxs-lookup"><span data-stu-id="5a6ec-105">ddx\_fine function</span></span>

<span data-ttu-id="5a6ec-106">Выполняет частичное производные от высокой точности относительно координаты x пространства экрана.</span><span class="sxs-lookup"><span data-stu-id="5a6ec-106">Computes a high precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a6ec-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a6ec-107">Syntax</span></span>

``` syntax
float ddx_fine(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="5a6ec-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a6ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a6ec-109">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a6ec-109">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6ec-110">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="5a6ec-110">Type: **float**</span></span>

<span data-ttu-id="5a6ec-111">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="5a6ec-111">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a6ec-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a6ec-112">Return value</span></span>

<span data-ttu-id="5a6ec-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="5a6ec-113">Type: **float**</span></span>

<span data-ttu-id="5a6ec-114">Частичная точность, производная от *value*.</span><span class="sxs-lookup"><span data-stu-id="5a6ec-114">The high precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a6ec-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="5a6ec-115">Remarks</span></span>

<span data-ttu-id="5a6ec-116">Также доступны следующие перегруженные версии:</span><span class="sxs-lookup"><span data-stu-id="5a6ec-116">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddx_fine(float2 value);
float3 ddx_fine(float3 value);
float4 ddx_fine(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="5a6ec-117">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5a6ec-117">Minimum Shader Model</span></span>

<span data-ttu-id="5a6ec-118">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="5a6ec-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5a6ec-119">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5a6ec-119">Shader Model</span></span>                                                                | <span data-ttu-id="5a6ec-120">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="5a6ec-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5a6ec-121">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="5a6ec-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="5a6ec-122">да</span><span class="sxs-lookup"><span data-stu-id="5a6ec-122">yes</span></span>       |



 

<span data-ttu-id="5a6ec-123">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="5a6ec-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="5a6ec-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="5a6ec-124">Vertex</span></span> | <span data-ttu-id="5a6ec-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="5a6ec-125">Hull</span></span> | <span data-ttu-id="5a6ec-126">Домен</span><span class="sxs-lookup"><span data-stu-id="5a6ec-126">Domain</span></span> | <span data-ttu-id="5a6ec-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="5a6ec-127">Geometry</span></span> | <span data-ttu-id="5a6ec-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="5a6ec-128">Pixel</span></span> | <span data-ttu-id="5a6ec-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="5a6ec-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5a6ec-130">x</span><span class="sxs-lookup"><span data-stu-id="5a6ec-130">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="5a6ec-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a6ec-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a6ec-132">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="5a6ec-132">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="5a6ec-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="5a6ec-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




