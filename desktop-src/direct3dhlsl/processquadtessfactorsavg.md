---
title: Функция Процесскуадтессфакторсавг
description: Создает исправленные факторы тесселяции для четырех исправлений. | Функция Процесскуадтессфакторсавг
ms.assetid: 3af1dad3-1923-45f3-9908-ca403e7f0cfe
keywords:
- Функция Процесскуадтессфакторсавг HLSL
topic_type:
- apiref
api_name:
- ProcessQuadTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36a50dd971161f3e03514947db447774da5b6a62
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998194"
---
# <a name="processquadtessfactorsavg-function"></a><span data-ttu-id="7299f-105">Функция Процесскуадтессфакторсавг</span><span class="sxs-lookup"><span data-stu-id="7299f-105">ProcessQuadTessFactorsAvg function</span></span>

<span data-ttu-id="7299f-106">Создает исправленные факторы тесселяции для четырех исправлений.</span><span class="sxs-lookup"><span data-stu-id="7299f-106">Generates the corrected tessellation factors for a quad patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="7299f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7299f-107">Syntax</span></span>

``` syntax
void ProcessQuadTessFactorsAvg(
  in  float4 RawEdgeFactors,
  in  float InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="7299f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7299f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7299f-109">*Раведжефакторс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7299f-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7299f-110">Тип: **float4**</span><span class="sxs-lookup"><span data-stu-id="7299f-110">Type: **float4**</span></span>

<span data-ttu-id="7299f-111">Факторы тесселяции краев, передаваемые в стадию тесселяции.</span><span class="sxs-lookup"><span data-stu-id="7299f-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="7299f-112">*Инсидескале* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7299f-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7299f-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="7299f-113">Type: **float**</span></span>

<span data-ttu-id="7299f-114">Коэффициент масштабирования, применяемый к коэффициентам тесселяции UV, вычисленным на этапе тесселяции.</span><span class="sxs-lookup"><span data-stu-id="7299f-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="7299f-115">Допустимый диапазон для Инсидескале — от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="7299f-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="7299f-116">*Раундедеджетессфакторс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7299f-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7299f-117">Тип: **float4**</span><span class="sxs-lookup"><span data-stu-id="7299f-117">Type: **float4**</span></span>

<span data-ttu-id="7299f-118">Скругленные границы — коэффициенты тесселяции, вычисленные на этапе тесселяции.</span><span class="sxs-lookup"><span data-stu-id="7299f-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="7299f-119">*Раундединсидетессфакторс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7299f-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7299f-120">Тип: **float2**</span><span class="sxs-lookup"><span data-stu-id="7299f-120">Type: **float2**</span></span>

<span data-ttu-id="7299f-121">Коэффициенты закругленной тесселяции, вычисленные на этапе тесселяции для внутренних границ.</span><span class="sxs-lookup"><span data-stu-id="7299f-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="7299f-122">*Унраундединсидетессфакторс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7299f-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7299f-123">Тип: **float2**</span><span class="sxs-lookup"><span data-stu-id="7299f-123">Type: **float2**</span></span>

<span data-ttu-id="7299f-124">Коэффициенты тесселяции, вычисленные на этапе тесселяции для внутренних границ.</span><span class="sxs-lookup"><span data-stu-id="7299f-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7299f-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7299f-125">Return value</span></span>

<span data-ttu-id="7299f-126">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7299f-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7299f-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="7299f-127">Remarks</span></span>

<span data-ttu-id="7299f-128">Формирует исправленные факторы тесселяции для четырех исправлений, вычисляя внутренние факторы тесселяции в качестве среднего значения факторов тесселяции краев.</span><span class="sxs-lookup"><span data-stu-id="7299f-128">Generates the corrected tessellation factors for a quad patch, computing the inside tessellation factors as the average of the edge tessellation factors.</span></span> <span data-ttu-id="7299f-129">Внутренние факторы Тесс будут идентичными значениями, определяемыми средним значением всех четырех ребер, масштабируемых по Инсидескале.</span><span class="sxs-lookup"><span data-stu-id="7299f-129">The inside tess factors will be identical values determined by the average of all four edges scaled by InsideScale.</span></span> <span data-ttu-id="7299f-130">Затем результат округляется в зависимости от режима секционирования, но неокругленные результаты доступны с помощью параметра Унраундединсидетессфакторс.</span><span class="sxs-lookup"><span data-stu-id="7299f-130">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactors parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="7299f-131">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7299f-131">Minimum Shader Model</span></span>

<span data-ttu-id="7299f-132">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="7299f-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7299f-133">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7299f-133">Shader Model</span></span>                                                                | <span data-ttu-id="7299f-134">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="7299f-134">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="7299f-135">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="7299f-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="7299f-136">да</span><span class="sxs-lookup"><span data-stu-id="7299f-136">yes</span></span>       |



 

<span data-ttu-id="7299f-137">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="7299f-137">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="7299f-138">Вершина</span><span class="sxs-lookup"><span data-stu-id="7299f-138">Vertex</span></span> | <span data-ttu-id="7299f-139">Поверхности</span><span class="sxs-lookup"><span data-stu-id="7299f-139">Hull</span></span> | <span data-ttu-id="7299f-140">Домен</span><span class="sxs-lookup"><span data-stu-id="7299f-140">Domain</span></span> | <span data-ttu-id="7299f-141">Геометрия</span><span class="sxs-lookup"><span data-stu-id="7299f-141">Geometry</span></span> | <span data-ttu-id="7299f-142">Пиксель</span><span class="sxs-lookup"><span data-stu-id="7299f-142">Pixel</span></span> | <span data-ttu-id="7299f-143">Вычисления</span><span class="sxs-lookup"><span data-stu-id="7299f-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="7299f-144">x</span><span class="sxs-lookup"><span data-stu-id="7299f-144">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="7299f-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7299f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7299f-146">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="7299f-146">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="7299f-147">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="7299f-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




