---
title: Функция Вавереадланеат
description: Возвращает значение выражения для заданного индекса полосы в заданной волны.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- Функция Вавереадланеат HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e40940f2df6685a3096da6886ad3bcb6d9ca99af
ms.sourcegitcommit: 4423a9d48f1c90d2ec2eca68e9cae30df1787f25
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2020
ms.locfileid: "104412748"
---
# <a name="wavereadlaneat-function"></a><span data-ttu-id="ccd76-104">Функция Вавереадланеат</span><span class="sxs-lookup"><span data-stu-id="ccd76-104">WaveReadLaneAt function</span></span>

<span data-ttu-id="ccd76-105">Возвращает значение выражения для заданного индекса полосы в заданной волны.</span><span class="sxs-lookup"><span data-stu-id="ccd76-105">Returns the value of the expression for the given lane index within the specified wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd76-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ccd76-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a><span data-ttu-id="ccd76-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccd76-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd76-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="ccd76-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="ccd76-109">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="ccd76-109">The expression to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="ccd76-110">*ланеиндекс*</span><span class="sxs-lookup"><span data-stu-id="ccd76-110">*laneIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="ccd76-111">Индекс полосы, для которой будет возвращен результат *expr* .</span><span class="sxs-lookup"><span data-stu-id="ccd76-111">The index of the lane for which the *expr* result will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccd76-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ccd76-112">Return value</span></span>

<span data-ttu-id="ccd76-113">Полученное значение является результатом *выражения expr*.</span><span class="sxs-lookup"><span data-stu-id="ccd76-113">The resulting value is the result of *expr*.</span></span> <span data-ttu-id="ccd76-114">Он будет единообразным, если *ланеиндекс* является однородным.</span><span class="sxs-lookup"><span data-stu-id="ccd76-114">It will be uniform if *laneIndex* is uniform.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccd76-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="ccd76-115">Remarks</span></span>

<span data-ttu-id="ccd76-116">Эта функция фактически является широковещательной рассылкой значения в Ланеиндекс'с Lane.</span><span class="sxs-lookup"><span data-stu-id="ccd76-116">This function is effectively a broadcast of the value in the laneIndex’th lane.</span></span>

<span data-ttu-id="ccd76-117">Эта функция поддерживается из модели шейдеров 6,0 в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ccd76-117">This function is supported from shader model 6.0, in the following types of shaders:</span></span>



| <span data-ttu-id="ccd76-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="ccd76-118">Vertex</span></span> | <span data-ttu-id="ccd76-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ccd76-119">Hull</span></span> | <span data-ttu-id="ccd76-120">Домен</span><span class="sxs-lookup"><span data-stu-id="ccd76-120">Domain</span></span> | <span data-ttu-id="ccd76-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ccd76-121">Geometry</span></span> | <span data-ttu-id="ccd76-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ccd76-122">Pixel</span></span> | <span data-ttu-id="ccd76-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ccd76-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ccd76-124">x</span><span class="sxs-lookup"><span data-stu-id="ccd76-124">x</span></span>     | <span data-ttu-id="ccd76-125">x</span><span class="sxs-lookup"><span data-stu-id="ccd76-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ccd76-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccd76-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd76-127">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="ccd76-127">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="ccd76-128">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="ccd76-128">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




