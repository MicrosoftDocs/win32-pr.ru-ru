---
title: Функция Евалуатеаттрибутеатцентроид
description: Вычисляется на центроид пикселей.
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- Функция Евалуатеаттрибутеатцентроид HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee95c7f2f202dfd0065e5e9c30003cc46fd29281
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411822"
---
# <a name="evaluateattributeatcentroid-function"></a><span data-ttu-id="98707-104">Функция Евалуатеаттрибутеатцентроид</span><span class="sxs-lookup"><span data-stu-id="98707-104">EvaluateAttributeAtCentroid function</span></span>

<span data-ttu-id="98707-105">Вычисляется на центроид пикселей.</span><span class="sxs-lookup"><span data-stu-id="98707-105">Evaluates at the pixel centroid.</span></span>

## <a name="syntax"></a><span data-ttu-id="98707-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98707-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a><span data-ttu-id="98707-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="98707-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98707-108">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="98707-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98707-109">Тип: **attrib numeric**</span><span class="sxs-lookup"><span data-stu-id="98707-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="98707-110">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="98707-110">The input value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98707-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="98707-111">Remarks</span></span>

<span data-ttu-id="98707-112">Режим интерполяции может быть **линейным** или **линейным \_ без \_ перспективы** для переменной.</span><span class="sxs-lookup"><span data-stu-id="98707-112">Interpolation mode can be **linear** or **linear\_no\_perspective** on the variable.</span></span> <span data-ttu-id="98707-113">Использование **центроид** или **Sample** не учитывается.</span><span class="sxs-lookup"><span data-stu-id="98707-113">Use of **centroid** or **sample** is ignored.</span></span> <span data-ttu-id="98707-114">Также разрешены атрибуты с интерполяцией константы. в этом случае пример индекса игнорируется.</span><span class="sxs-lookup"><span data-stu-id="98707-114">Attributes with constant interpolation are also allowed, in which case the sample index is ignored.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="98707-115">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="98707-115">Minimum Shader Model</span></span>

<span data-ttu-id="98707-116">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="98707-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="98707-117">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="98707-117">Shader Model</span></span>                                                                | <span data-ttu-id="98707-118">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="98707-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="98707-119">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="98707-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="98707-120">да</span><span class="sxs-lookup"><span data-stu-id="98707-120">yes</span></span>       |



 

<span data-ttu-id="98707-121">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="98707-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="98707-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="98707-122">Vertex</span></span> | <span data-ttu-id="98707-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="98707-123">Hull</span></span> | <span data-ttu-id="98707-124">Домен</span><span class="sxs-lookup"><span data-stu-id="98707-124">Domain</span></span> | <span data-ttu-id="98707-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="98707-125">Geometry</span></span> | <span data-ttu-id="98707-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="98707-126">Pixel</span></span> | <span data-ttu-id="98707-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="98707-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="98707-128">x</span><span class="sxs-lookup"><span data-stu-id="98707-128">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="98707-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98707-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98707-130">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="98707-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="98707-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="98707-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




