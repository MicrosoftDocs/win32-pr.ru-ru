---
title: Функция Процессисолинетессфакторс
description: Создает округленные факторы тесселяции для исолине.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- Функция Процессисолинетессфакторс HLSL
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10da0e5bf0f2138c57da3fcfe962bc6a88800068
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784356"
---
# <a name="processisolinetessfactors-function"></a><span data-ttu-id="5dd17-104">Функция Процессисолинетессфакторс</span><span class="sxs-lookup"><span data-stu-id="5dd17-104">ProcessIsolineTessFactors function</span></span>

<span data-ttu-id="5dd17-105">Создает округленные факторы тесселяции для исолине.</span><span class="sxs-lookup"><span data-stu-id="5dd17-105">Generates the rounded tessellation factors for an isoline.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dd17-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dd17-106">Syntax</span></span>

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a><span data-ttu-id="5dd17-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5dd17-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dd17-108">*Равдетаилфактор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5dd17-108">*RawDetailFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd17-109">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="5dd17-109">Type: **float**</span></span>

<span data-ttu-id="5dd17-110">Требуемый подробный фактор.</span><span class="sxs-lookup"><span data-stu-id="5dd17-110">The desired detail factor.</span></span>

</dd> <dt>

<span data-ttu-id="5dd17-111">*Равденситифактор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5dd17-111">*RawDensityFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd17-112">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="5dd17-112">Type: **float**</span></span>

<span data-ttu-id="5dd17-113">Требуемый коэффициент плотности.</span><span class="sxs-lookup"><span data-stu-id="5dd17-113">The desired density factor.</span></span>

</dd> <dt>

<span data-ttu-id="5dd17-114">*Раундеддетаилфактор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5dd17-114">*RoundedDetailFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd17-115">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="5dd17-115">Type: **float**</span></span>

<span data-ttu-id="5dd17-116">Скругленный коэффициент детализации для диапазона, который может использоваться в тесселяции.</span><span class="sxs-lookup"><span data-stu-id="5dd17-116">The rounded detail factor clamped to a range that can be used by the tessellator.</span></span>

</dd> <dt>

<span data-ttu-id="5dd17-117">*Раундедденситифактор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5dd17-117">*RoundedDensityFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd17-118">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="5dd17-118">Type: **float**</span></span>

<span data-ttu-id="5dd17-119">В качестве коэффициента округления к ранжесат может использоваться тесселяция.</span><span class="sxs-lookup"><span data-stu-id="5dd17-119">The rounded density factor clamped to a rangethat can be used by the tessellator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dd17-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5dd17-120">Return value</span></span>

<span data-ttu-id="5dd17-121">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5dd17-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dd17-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="5dd17-122">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="5dd17-123">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5dd17-123">Minimum Shader Model</span></span>

<span data-ttu-id="5dd17-124">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="5dd17-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5dd17-125">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5dd17-125">Shader Model</span></span>                                                                | <span data-ttu-id="5dd17-126">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="5dd17-126">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5dd17-127">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="5dd17-127">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="5dd17-128">да</span><span class="sxs-lookup"><span data-stu-id="5dd17-128">yes</span></span>       |



 

<span data-ttu-id="5dd17-129">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="5dd17-129">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="5dd17-130">Вершина</span><span class="sxs-lookup"><span data-stu-id="5dd17-130">Vertex</span></span> | <span data-ttu-id="5dd17-131">Поверхности</span><span class="sxs-lookup"><span data-stu-id="5dd17-131">Hull</span></span> | <span data-ttu-id="5dd17-132">Домен</span><span class="sxs-lookup"><span data-stu-id="5dd17-132">Domain</span></span> | <span data-ttu-id="5dd17-133">Геометрия</span><span class="sxs-lookup"><span data-stu-id="5dd17-133">Geometry</span></span> | <span data-ttu-id="5dd17-134">Пиксель</span><span class="sxs-lookup"><span data-stu-id="5dd17-134">Pixel</span></span> | <span data-ttu-id="5dd17-135">Вычисления</span><span class="sxs-lookup"><span data-stu-id="5dd17-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="5dd17-136">x</span><span class="sxs-lookup"><span data-stu-id="5dd17-136">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="5dd17-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dd17-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dd17-138">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="5dd17-138">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="5dd17-139">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="5dd17-139">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




