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
ms.openlocfilehash: 573730053a93a110381637ef8e62dc08a4aa1535
ms.sourcegitcommit: 1897c2a39b4ac4ca4b1e4aec394cef2ce2619c03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/06/2021
ms.locfileid: "113316486"
---
# <a name="wavereadlaneat-function"></a><span data-ttu-id="4b283-104">Функция Вавереадланеат</span><span class="sxs-lookup"><span data-stu-id="4b283-104">WaveReadLaneAt function</span></span>

<span data-ttu-id="4b283-105">Возвращает значение выражения для заданного индекса полосы в заданной волны.</span><span class="sxs-lookup"><span data-stu-id="4b283-105">Returns the value of the expression for the given lane index within the specified wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b283-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b283-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a><span data-ttu-id="4b283-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b283-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b283-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="4b283-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="4b283-109">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="4b283-109">The expression to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="4b283-110">*ланеиндекс*</span><span class="sxs-lookup"><span data-stu-id="4b283-110">*laneIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="4b283-111">Индекс полосы, для которой будет возвращен результат *expr* .</span><span class="sxs-lookup"><span data-stu-id="4b283-111">The index of the lane for which the *expr* result will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b283-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b283-112">Return value</span></span>

<span data-ttu-id="4b283-113">Полученное значение является результатом *выражения expr*.</span><span class="sxs-lookup"><span data-stu-id="4b283-113">The resulting value is the result of *expr*.</span></span> <span data-ttu-id="4b283-114">Он будет единообразным, если *ланеиндекс* является однородным.</span><span class="sxs-lookup"><span data-stu-id="4b283-114">It will be uniform if *laneIndex* is uniform.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b283-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b283-115">Remarks</span></span>

<span data-ttu-id="4b283-116">Эта функция фактически является широковещательной рассылкой значения на *ланеиндекс*"th".</span><span class="sxs-lookup"><span data-stu-id="4b283-116">This function is effectively a broadcast of the value in the *laneIndex*'th lane.</span></span>

<span data-ttu-id="4b283-117">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="4b283-117">This function is supported from shader model 6.0 in all shader stages.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b283-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b283-118">See also</span></span>

* [<span data-ttu-id="4b283-119">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="4b283-119">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [<span data-ttu-id="4b283-120">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="4b283-120">Shader Model 6</span></span>](shader-model-6-0.md)
