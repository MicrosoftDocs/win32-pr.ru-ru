---
title: Функция Евалуатеаттрибутеатсампле
description: Вычисляется в расположении с индексированным образцом.
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- Функция Евалуатеаттрибутеатсампле HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b183f86599d08a6892e33c169b938dc09a2b55de
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783678"
---
# <a name="evaluateattributeatsample-function"></a><span data-ttu-id="aadd0-104">Функция Евалуатеаттрибутеатсампле</span><span class="sxs-lookup"><span data-stu-id="aadd0-104">EvaluateAttributeAtSample function</span></span>

<span data-ttu-id="aadd0-105">Вычисляется в расположении с индексированным образцом.</span><span class="sxs-lookup"><span data-stu-id="aadd0-105">Evaluates at the indexed sample location.</span></span>

## <a name="syntax"></a><span data-ttu-id="aadd0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aadd0-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="aadd0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="aadd0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aadd0-108">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aadd0-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aadd0-109">Тип: **attrib numeric**</span><span class="sxs-lookup"><span data-stu-id="aadd0-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="aadd0-110">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="aadd0-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="aadd0-111">*sampleindex* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aadd0-111">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aadd0-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="aadd0-112">Type: **uint**</span></span>

<span data-ttu-id="aadd0-113">Расположение образца.</span><span class="sxs-lookup"><span data-stu-id="aadd0-113">The sample location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aadd0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="aadd0-114">Remarks</span></span>

<span data-ttu-id="aadd0-115">Режим интерполяции может быть **линейным** или **линейным \_ без \_ перспективы** для переменной.</span><span class="sxs-lookup"><span data-stu-id="aadd0-115">Interpolation mode can be **linear** or **linear\_no\_perspective** on the variable.</span></span> <span data-ttu-id="aadd0-116">Использование **центроид** или **Sample** не учитывается.</span><span class="sxs-lookup"><span data-stu-id="aadd0-116">Use of **centroid** or **sample** is ignored.</span></span> <span data-ttu-id="aadd0-117">Также разрешены атрибуты с интерполяцией константы. в этом случае пример индекса игнорируется.</span><span class="sxs-lookup"><span data-stu-id="aadd0-117">Attributes with constant interpolation are also allowed, in which case the sample index is ignored.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="aadd0-118">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="aadd0-118">Minimum Shader Model</span></span>

<span data-ttu-id="aadd0-119">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="aadd0-119">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aadd0-120">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="aadd0-120">Shader Model</span></span>                                                                | <span data-ttu-id="aadd0-121">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="aadd0-121">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="aadd0-122">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="aadd0-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="aadd0-123">да</span><span class="sxs-lookup"><span data-stu-id="aadd0-123">yes</span></span>       |



 

<span data-ttu-id="aadd0-124">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="aadd0-124">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="aadd0-125">Вершина</span><span class="sxs-lookup"><span data-stu-id="aadd0-125">Vertex</span></span> | <span data-ttu-id="aadd0-126">Поверхности</span><span class="sxs-lookup"><span data-stu-id="aadd0-126">Hull</span></span> | <span data-ttu-id="aadd0-127">Домен</span><span class="sxs-lookup"><span data-stu-id="aadd0-127">Domain</span></span> | <span data-ttu-id="aadd0-128">Геометрия</span><span class="sxs-lookup"><span data-stu-id="aadd0-128">Geometry</span></span> | <span data-ttu-id="aadd0-129">Пиксель</span><span class="sxs-lookup"><span data-stu-id="aadd0-129">Pixel</span></span> | <span data-ttu-id="aadd0-130">Вычисления</span><span class="sxs-lookup"><span data-stu-id="aadd0-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="aadd0-131">x</span><span class="sxs-lookup"><span data-stu-id="aadd0-131">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="aadd0-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aadd0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aadd0-133">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="aadd0-133">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="aadd0-134">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="aadd0-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




