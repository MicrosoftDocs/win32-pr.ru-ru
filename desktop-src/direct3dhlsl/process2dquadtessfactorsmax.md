---
title: Функция Process2DQuadTessFactorsMax
description: Создает исправленные факторы тесселяции для четырех исправлений. | Функция Process2DQuadTessFactorsMax
ms.assetid: 1de95946-d82d-42ba-93d7-ab8383fd5018
keywords:
- Функция Process2DQuadTessFactorsMax HLSL
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d090c102671ec89fa347db95da2b21b5f11adcfe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998051"
---
# <a name="process2dquadtessfactorsmax-function"></a><span data-ttu-id="15c1d-105">Функция Process2DQuadTessFactorsMax</span><span class="sxs-lookup"><span data-stu-id="15c1d-105">Process2DQuadTessFactorsMax function</span></span>

<span data-ttu-id="15c1d-106">Создает исправленные факторы тесселяции для четырех исправлений.</span><span class="sxs-lookup"><span data-stu-id="15c1d-106">Generates the corrected tessellation factors for a quad patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="15c1d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15c1d-107">Syntax</span></span>

``` syntax
void Process2DQuadTessFactorsMax(
  in  float4 RawEdgeFactors,
  in  float2 InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="15c1d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="15c1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15c1d-109">*Раведжефакторс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15c1d-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15c1d-110">Тип: **float4**</span><span class="sxs-lookup"><span data-stu-id="15c1d-110">Type: **float4**</span></span>

<span data-ttu-id="15c1d-111">Факторы тесселяции краев, передаваемые в стадию тесселяции.</span><span class="sxs-lookup"><span data-stu-id="15c1d-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="15c1d-112">*Инсидескале* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15c1d-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15c1d-113">Тип: **float2**</span><span class="sxs-lookup"><span data-stu-id="15c1d-113">Type: **float2**</span></span>

<span data-ttu-id="15c1d-114">Коэффициент масштабирования, применяемый к коэффициентам тесселяции UV, вычисленным на этапе тесселяции.</span><span class="sxs-lookup"><span data-stu-id="15c1d-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="15c1d-115">Допустимый диапазон для Инсидескале — от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="15c1d-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="15c1d-116">*Раундедеджетессфакторс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="15c1d-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15c1d-117">Тип: **float4**</span><span class="sxs-lookup"><span data-stu-id="15c1d-117">Type: **float4**</span></span>

<span data-ttu-id="15c1d-118">Скругленные границы — коэффициенты тесселяции, вычисленные на этапе тесселяции.</span><span class="sxs-lookup"><span data-stu-id="15c1d-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="15c1d-119">*Раундединсидетессфакторс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="15c1d-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15c1d-120">Тип: **float2**</span><span class="sxs-lookup"><span data-stu-id="15c1d-120">Type: **float2**</span></span>

<span data-ttu-id="15c1d-121">Коэффициенты закругленной тесселяции, вычисленные на этапе тесселяции для внутренних границ.</span><span class="sxs-lookup"><span data-stu-id="15c1d-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="15c1d-122">*Унраундединсидетессфакторс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="15c1d-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15c1d-123">Тип: **float2**</span><span class="sxs-lookup"><span data-stu-id="15c1d-123">Type: **float2**</span></span>

<span data-ttu-id="15c1d-124">Коэффициенты тесселяции, вычисленные на этапе тесселяции для внутренних границ.</span><span class="sxs-lookup"><span data-stu-id="15c1d-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15c1d-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15c1d-125">Return value</span></span>

<span data-ttu-id="15c1d-126">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="15c1d-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15c1d-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="15c1d-127">Remarks</span></span>

<span data-ttu-id="15c1d-128">Формирует исправленные факторы тесселяции для четырех исправлений, вычисляя внутренние факторы тесселяции в качестве максимального значения факторов тесселяции краев.</span><span class="sxs-lookup"><span data-stu-id="15c1d-128">Generates the corrected tessellation factors for a quad patch, computing the inside tessellation factors as the maximum of the edge tessellation factors.</span></span> <span data-ttu-id="15c1d-129">Значения параметров "вы" и "V" в списке факторов тесселяции вычисляются независимо друг от друга с максимальным числом сторон в домене, а затем масштабируются по Инсидескале.</span><span class="sxs-lookup"><span data-stu-id="15c1d-129">The U and V inside tessellation factors are computed independently using the maximums of opposing sides of the domain, then are scaled by InsideScale.</span></span> <span data-ttu-id="15c1d-130">Затем результат округляется в зависимости от режима секционирования, но неокругленные результаты доступны с помощью параметра Унраундединсидетессфакторс.</span><span class="sxs-lookup"><span data-stu-id="15c1d-130">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactors parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="15c1d-131">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="15c1d-131">Minimum Shader Model</span></span>

<span data-ttu-id="15c1d-132">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="15c1d-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="15c1d-133">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="15c1d-133">Shader Model</span></span>                                                                | <span data-ttu-id="15c1d-134">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="15c1d-134">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="15c1d-135">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="15c1d-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="15c1d-136">да</span><span class="sxs-lookup"><span data-stu-id="15c1d-136">yes</span></span>       |



 

<span data-ttu-id="15c1d-137">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="15c1d-137">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="15c1d-138">Вершина</span><span class="sxs-lookup"><span data-stu-id="15c1d-138">Vertex</span></span> | <span data-ttu-id="15c1d-139">Поверхности</span><span class="sxs-lookup"><span data-stu-id="15c1d-139">Hull</span></span> | <span data-ttu-id="15c1d-140">Домен</span><span class="sxs-lookup"><span data-stu-id="15c1d-140">Domain</span></span> | <span data-ttu-id="15c1d-141">Геометрия</span><span class="sxs-lookup"><span data-stu-id="15c1d-141">Geometry</span></span> | <span data-ttu-id="15c1d-142">Пиксель</span><span class="sxs-lookup"><span data-stu-id="15c1d-142">Pixel</span></span> | <span data-ttu-id="15c1d-143">Вычисления</span><span class="sxs-lookup"><span data-stu-id="15c1d-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="15c1d-144">x</span><span class="sxs-lookup"><span data-stu-id="15c1d-144">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="15c1d-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15c1d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15c1d-146">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="15c1d-146">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="15c1d-147">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="15c1d-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




