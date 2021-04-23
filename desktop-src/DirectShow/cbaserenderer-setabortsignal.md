---
description: Метод Сетабортсигнал задает флаг, который указывает, следует ли прерывать отрисовку и отклонять дальнейшие выборки.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: Кбасерендерер. Сетабортсигнал, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70527d5e43ccab4df7b2110a33df8d813bd16d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668769"
---
# <a name="cbaserenderersetabortsignal-method"></a><span data-ttu-id="a7836-103">Кбасерендерер. Сетабортсигнал, метод</span><span class="sxs-lookup"><span data-stu-id="a7836-103">CBaseRenderer.SetAbortSignal method</span></span>

<span data-ttu-id="a7836-104">`SetAbortSignal`Метод задает флаг, указывающий, следует ли прерывать отрисовку и отклонять дальнейшие выборки.</span><span class="sxs-lookup"><span data-stu-id="a7836-104">The `SetAbortSignal` method sets a flag which indicates whether to stop rendering and reject further samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7836-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7836-105">Syntax</span></span>


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a><span data-ttu-id="a7836-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7836-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7836-107">*баборт*</span><span class="sxs-lookup"><span data-stu-id="a7836-107">*bAbort*</span></span> 
</dt> <dd>

<span data-ttu-id="a7836-108">Логическое значение, указывающее, следует ли прерывать подготовку к просмотру.</span><span class="sxs-lookup"><span data-stu-id="a7836-108">Boolean value indicating whether to stop rendering.</span></span> <span data-ttu-id="a7836-109">Если **значение равно true**, то фильтр не будет отображать больше выборок.</span><span class="sxs-lookup"><span data-stu-id="a7836-109">If **TRUE**, the filter will not render any more samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7836-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7836-110">Return value</span></span>

<span data-ttu-id="a7836-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a7836-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7836-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7836-112">Remarks</span></span>

<span data-ttu-id="a7836-113">Этот метод задает флаг [**кбасерендерер:: m \_ баборт**](cbaserenderer-m-babort.md) .</span><span class="sxs-lookup"><span data-stu-id="a7836-113">This method sets the [**CBaseRenderer::m\_bAbort**](cbaserenderer-m-babort.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7836-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a7836-114">Requirements</span></span>



| <span data-ttu-id="a7836-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a7836-115">Requirement</span></span> | <span data-ttu-id="a7836-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a7836-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7836-117">Header</span><span class="sxs-lookup"><span data-stu-id="a7836-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a7836-118"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7836-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a7836-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a7836-119">Library</span></span><br/> | <dl> <span data-ttu-id="a7836-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a7836-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7836-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7836-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7836-122">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="a7836-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




