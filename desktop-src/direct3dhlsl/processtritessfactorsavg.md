---
title: Функция Процесстритессфакторсавг
description: Создает исправленные коэффициенты тесселяции для более трехуровневого обновления. | Функция Процесстритессфакторсавг
ms.assetid: 005a63b6-f35d-42d6-bb29-f4ebb374080e
keywords:
- Функция Процесстритессфакторсавг HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90cfa86a09e0e76c90f0013cfa6121917ca25378
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998082"
---
# <a name="processtritessfactorsavg-function"></a><span data-ttu-id="d34f5-105">Функция Процесстритессфакторсавг</span><span class="sxs-lookup"><span data-stu-id="d34f5-105">ProcessTriTessFactorsAvg function</span></span>

<span data-ttu-id="d34f5-106">Создает исправленные коэффициенты тесселяции для более трехуровневого обновления.</span><span class="sxs-lookup"><span data-stu-id="d34f5-106">Generates the corrected tessellation factors for a tri patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="d34f5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d34f5-107">Syntax</span></span>

``` syntax
void ProcessTriTessFactorsAvg(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a><span data-ttu-id="d34f5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d34f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d34f5-109">*Раведжефакторс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d34f5-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34f5-110">Тип: **float3**</span><span class="sxs-lookup"><span data-stu-id="d34f5-110">Type: **float3**</span></span>

<span data-ttu-id="d34f5-111">Факторы тесселяции краев, передаваемые в стадию тесселяции.</span><span class="sxs-lookup"><span data-stu-id="d34f5-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="d34f5-112">*Инсидескале* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d34f5-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34f5-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d34f5-113">Type: **float**</span></span>

<span data-ttu-id="d34f5-114">Коэффициент масштабирования, применяемый к коэффициентам тесселяции UV, вычисленным на этапе тесселяции.</span><span class="sxs-lookup"><span data-stu-id="d34f5-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="d34f5-115">Допустимый диапазон для Инсидескале — от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="d34f5-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="d34f5-116">*Раундедеджетессфакторс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d34f5-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d34f5-117">Тип: **float3**</span><span class="sxs-lookup"><span data-stu-id="d34f5-117">Type: **float3**</span></span>

<span data-ttu-id="d34f5-118">Скругленные границы — коэффициенты тесселяции, вычисленные на этапе тесселяции.</span><span class="sxs-lookup"><span data-stu-id="d34f5-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="d34f5-119">*Раундединсидетессфактор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d34f5-119">*RoundedInsideTessFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d34f5-120">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d34f5-120">Type: **float**</span></span>

<span data-ttu-id="d34f5-121">Коэффициенты тесселяции, вычисляемые на этапе тесселяции, и округляются.</span><span class="sxs-lookup"><span data-stu-id="d34f5-121">The tessellation factors calculated by the tessellator stage, and rounded.</span></span>

</dd> <dt>

<span data-ttu-id="d34f5-122">*Унраундединсидетессфактор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d34f5-122">*UnroundedInsideTessFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d34f5-123">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d34f5-123">Type: **float**</span></span>

<span data-ttu-id="d34f5-124">Первоначальные, нескругленные, UV, вычисляются на этапе тесселяции.</span><span class="sxs-lookup"><span data-stu-id="d34f5-124">The original, unrounded, UV tessellation factors computed by the tessellation stage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d34f5-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d34f5-125">Return value</span></span>

<span data-ttu-id="d34f5-126">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d34f5-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d34f5-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="d34f5-127">Remarks</span></span>

<span data-ttu-id="d34f5-128">Формирует исправленные коэффициенты тесселяции для трехуровневого обновления, вычисляя внутренний коэффициент тесселяции в виде среднего коэффициента тесселяции краев, который затем масштабируется по Инсидескале.</span><span class="sxs-lookup"><span data-stu-id="d34f5-128">Generates the corrected tessellation factors for a tri patch, computing the inside tessellation factor as the average of the edge tessellation factors, which is then scaled by InsideScale.</span></span> <span data-ttu-id="d34f5-129">Затем результат округляется в зависимости от режима секционирования, но неокругленные результаты доступны с помощью параметра Унраундединсидетессфактор.</span><span class="sxs-lookup"><span data-stu-id="d34f5-129">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactor parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="d34f5-130">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d34f5-130">Minimum Shader Model</span></span>

<span data-ttu-id="d34f5-131">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="d34f5-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d34f5-132">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d34f5-132">Shader Model</span></span>                                                                | <span data-ttu-id="d34f5-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d34f5-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d34f5-134">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="d34f5-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="d34f5-135">да</span><span class="sxs-lookup"><span data-stu-id="d34f5-135">yes</span></span>       |



 

<span data-ttu-id="d34f5-136">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="d34f5-136">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="d34f5-137">Вершина</span><span class="sxs-lookup"><span data-stu-id="d34f5-137">Vertex</span></span> | <span data-ttu-id="d34f5-138">Поверхности</span><span class="sxs-lookup"><span data-stu-id="d34f5-138">Hull</span></span> | <span data-ttu-id="d34f5-139">Домен</span><span class="sxs-lookup"><span data-stu-id="d34f5-139">Domain</span></span> | <span data-ttu-id="d34f5-140">Геометрия</span><span class="sxs-lookup"><span data-stu-id="d34f5-140">Geometry</span></span> | <span data-ttu-id="d34f5-141">Пиксель</span><span class="sxs-lookup"><span data-stu-id="d34f5-141">Pixel</span></span> | <span data-ttu-id="d34f5-142">Вычисления</span><span class="sxs-lookup"><span data-stu-id="d34f5-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="d34f5-143">x</span><span class="sxs-lookup"><span data-stu-id="d34f5-143">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="d34f5-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d34f5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34f5-145">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="d34f5-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="d34f5-146">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d34f5-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




