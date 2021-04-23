---
title: Функция ddy_fine
description: Выполняет частичное производные от высокой точности относительно координаты x пространства экрана. | Функция ddy_fine
ms.assetid: 29fcdbc9-470b-4b5b-b18c-f75dd2c87920
keywords:
- Функция ddy_fine HLSL
topic_type:
- apiref
api_name:
- ddy_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a4cb297180a4988cb049ccebfa4f82571c4655c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998288"
---
# <a name="ddy_fine-function"></a><span data-ttu-id="be9f6-105">ДДИ, \_ функция</span><span class="sxs-lookup"><span data-stu-id="be9f6-105">ddy\_fine function</span></span>

<span data-ttu-id="be9f6-106">Выполняет частичное производные от высокой точности относительно координаты x пространства экрана.</span><span class="sxs-lookup"><span data-stu-id="be9f6-106">Computes a high precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="be9f6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be9f6-107">Syntax</span></span>

``` syntax
float ddy_fine(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="be9f6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="be9f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be9f6-109">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be9f6-109">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be9f6-110">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="be9f6-110">Type: **float**</span></span>

<span data-ttu-id="be9f6-111">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="be9f6-111">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be9f6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be9f6-112">Return value</span></span>

<span data-ttu-id="be9f6-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="be9f6-113">Type: **float**</span></span>

<span data-ttu-id="be9f6-114">Частичная точность, производная от *value*.</span><span class="sxs-lookup"><span data-stu-id="be9f6-114">The high precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="be9f6-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="be9f6-115">Remarks</span></span>

<span data-ttu-id="be9f6-116">Также доступны следующие перегруженные версии:</span><span class="sxs-lookup"><span data-stu-id="be9f6-116">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddy_fine(float2 value);
float3 ddy_fine(float3 value);
float4 ddy_fine(float4 value);  
```

### <a name="minimum-shader-model"></a><span data-ttu-id="be9f6-117">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="be9f6-117">Minimum Shader Model</span></span>

<span data-ttu-id="be9f6-118">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="be9f6-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="be9f6-119">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="be9f6-119">Shader Model</span></span>                                                                | <span data-ttu-id="be9f6-120">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="be9f6-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="be9f6-121">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="be9f6-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="be9f6-122">да</span><span class="sxs-lookup"><span data-stu-id="be9f6-122">yes</span></span>       |



 

<span data-ttu-id="be9f6-123">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="be9f6-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="be9f6-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="be9f6-124">Vertex</span></span> | <span data-ttu-id="be9f6-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="be9f6-125">Hull</span></span> | <span data-ttu-id="be9f6-126">Домен</span><span class="sxs-lookup"><span data-stu-id="be9f6-126">Domain</span></span> | <span data-ttu-id="be9f6-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="be9f6-127">Geometry</span></span> | <span data-ttu-id="be9f6-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="be9f6-128">Pixel</span></span> | <span data-ttu-id="be9f6-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="be9f6-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="be9f6-130">x</span><span class="sxs-lookup"><span data-stu-id="be9f6-130">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="be9f6-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be9f6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9f6-132">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="be9f6-132">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="be9f6-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="be9f6-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




