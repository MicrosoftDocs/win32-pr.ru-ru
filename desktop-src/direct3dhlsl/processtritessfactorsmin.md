---
title: Функция Процесстритессфакторсмин
description: Создает исправленные коэффициенты тесселяции для более трехуровневого обновления. | Функция Процесстритессфакторсмин
ms.assetid: fa1e19c2-fadf-42d4-9574-834eaf871393
keywords:
- Функция Процесстритессфакторсмин HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f82c7935d47813d833ccc21a7ec0134adee1cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547559"
---
# <a name="processtritessfactorsmin-function"></a><span data-ttu-id="7cf76-105">Функция Процесстритессфакторсмин</span><span class="sxs-lookup"><span data-stu-id="7cf76-105">ProcessTriTessFactorsMin function</span></span>

<span data-ttu-id="7cf76-106">Создает исправленные коэффициенты тесселяции для более трехуровневого обновления.</span><span class="sxs-lookup"><span data-stu-id="7cf76-106">Generates the corrected tessellation factors for a tri patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf76-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cf76-107">Syntax</span></span>

``` syntax
void ProcessTriTessFactorsMin(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactors,
  out float UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="7cf76-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cf76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cf76-109">*Раведжефакторс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cf76-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf76-110">Тип: **float3**</span><span class="sxs-lookup"><span data-stu-id="7cf76-110">Type: **float3**</span></span>

<span data-ttu-id="7cf76-111">Факторы тесселяции краев, передаваемые в стадию тесселяции.</span><span class="sxs-lookup"><span data-stu-id="7cf76-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="7cf76-112">*Инсидескале* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cf76-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf76-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="7cf76-113">Type: **float**</span></span>

<span data-ttu-id="7cf76-114">Коэффициент масштабирования, применяемый к коэффициентам тесселяции UV, вычисленным на этапе тесселяции.</span><span class="sxs-lookup"><span data-stu-id="7cf76-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="7cf76-115">Допустимый диапазон для Инсидескале — от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="7cf76-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="7cf76-116">*Раундедеджетессфакторс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7cf76-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf76-117">Тип: **float3**</span><span class="sxs-lookup"><span data-stu-id="7cf76-117">Type: **float3**</span></span>

<span data-ttu-id="7cf76-118">Скругленные границы — коэффициенты тесселяции, вычисленные на этапе тесселяции.</span><span class="sxs-lookup"><span data-stu-id="7cf76-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="7cf76-119">*Раундединсидетессфакторс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7cf76-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf76-120">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="7cf76-120">Type: **float**</span></span>

<span data-ttu-id="7cf76-121">Коэффициенты закругленной тесселяции, вычисленные на этапе тесселяции для внутренних границ.</span><span class="sxs-lookup"><span data-stu-id="7cf76-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="7cf76-122">*Унраундединсидетессфакторс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7cf76-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf76-123">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="7cf76-123">Type: **float**</span></span>

<span data-ttu-id="7cf76-124">Коэффициенты тесселяции, вычисленные на этапе тесселяции для внутренних границ.</span><span class="sxs-lookup"><span data-stu-id="7cf76-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cf76-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cf76-125">Return value</span></span>

<span data-ttu-id="7cf76-126">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7cf76-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cf76-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="7cf76-127">Remarks</span></span>

<span data-ttu-id="7cf76-128">Формирует исправленные коэффициенты тесселяции для трехуровневого обновления, вычисляя внутренний фактор тесселяции как минимум для факторов тесселяции краев, которые затем масштабируются по Инсидескале.</span><span class="sxs-lookup"><span data-stu-id="7cf76-128">Generates the corrected tessellation factors for a tri patch, computing the inside tessellation factor as the minimum of the edge tessellation factors, which is then scaled by InsideScale.</span></span> <span data-ttu-id="7cf76-129">Затем результат округляется в зависимости от режима секционирования, но неокругленные результаты доступны с помощью параметра Унраундединсидетессфактор.</span><span class="sxs-lookup"><span data-stu-id="7cf76-129">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactor parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="7cf76-130">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7cf76-130">Minimum Shader Model</span></span>

<span data-ttu-id="7cf76-131">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="7cf76-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7cf76-132">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7cf76-132">Shader Model</span></span>                                                                | <span data-ttu-id="7cf76-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="7cf76-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="7cf76-134">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="7cf76-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="7cf76-135">да</span><span class="sxs-lookup"><span data-stu-id="7cf76-135">yes</span></span>       |



 

<span data-ttu-id="7cf76-136">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="7cf76-136">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="7cf76-137">Вершина</span><span class="sxs-lookup"><span data-stu-id="7cf76-137">Vertex</span></span> | <span data-ttu-id="7cf76-138">Поверхности</span><span class="sxs-lookup"><span data-stu-id="7cf76-138">Hull</span></span> | <span data-ttu-id="7cf76-139">Домен</span><span class="sxs-lookup"><span data-stu-id="7cf76-139">Domain</span></span> | <span data-ttu-id="7cf76-140">Геометрия</span><span class="sxs-lookup"><span data-stu-id="7cf76-140">Geometry</span></span> | <span data-ttu-id="7cf76-141">Пиксель</span><span class="sxs-lookup"><span data-stu-id="7cf76-141">Pixel</span></span> | <span data-ttu-id="7cf76-142">Вычисления</span><span class="sxs-lookup"><span data-stu-id="7cf76-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="7cf76-143">x</span><span class="sxs-lookup"><span data-stu-id="7cf76-143">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="7cf76-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cf76-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf76-145">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="7cf76-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="7cf76-146">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="7cf76-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




