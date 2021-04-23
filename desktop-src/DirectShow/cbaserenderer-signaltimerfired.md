---
description: Метод Сигналтимерфиред очищает идентификатор таймера, используемый для планирования подготовки к просмотру.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Кбасерендерер. Сигналтимерфиред, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SignalTimerFired
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dd29b37869fc6f07c2d876dfa0d1d306b04b111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669341"
---
# <a name="cbaserenderersignaltimerfired-method"></a><span data-ttu-id="9b68c-103">Кбасерендерер. Сигналтимерфиред, метод</span><span class="sxs-lookup"><span data-stu-id="9b68c-103">CBaseRenderer.SignalTimerFired method</span></span>

<span data-ttu-id="9b68c-104">`SignalTimerFired`Метод очищает идентификатор таймера, используемый для планирования подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="9b68c-104">The `SignalTimerFired` method clears the timer identifier used to schedule rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b68c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b68c-105">Syntax</span></span>


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a><span data-ttu-id="9b68c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b68c-106">Parameters</span></span>

<span data-ttu-id="9b68c-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9b68c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9b68c-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b68c-108">Return value</span></span>

<span data-ttu-id="9b68c-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9b68c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b68c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b68c-110">Remarks</span></span>

<span data-ttu-id="9b68c-111">Фильтр вызывает этот метод, когда таймер отрисовки активирует (см [**. кбасерендерер:: ваитфоррендертиме**](cbaserenderer-waitforrendertime.md)) или при отмене таймера (см. [**Кбасерендерер:: канцелнотификатион**](cbaserenderer-cancelnotification.md)).</span><span class="sxs-lookup"><span data-stu-id="9b68c-111">The filter calls this method when the rendering timer activates (see [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) or when the timer is canceled (see [**CBaseRenderer::CancelNotification**](cbaserenderer-cancelnotification.md)).</span></span> <span data-ttu-id="9b68c-112">Метод сбрасывает переменную члена [**кбасерендерер:: m \_ двадвисе**](cbaserenderer-m-dwadvise.md) в нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="9b68c-112">The method resets the [**CBaseRenderer::m\_dwAdvise**](cbaserenderer-m-dwadvise.md) member variable to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b68c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9b68c-113">Requirements</span></span>



| <span data-ttu-id="9b68c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9b68c-114">Requirement</span></span> | <span data-ttu-id="9b68c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9b68c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b68c-116">Header</span><span class="sxs-lookup"><span data-stu-id="9b68c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9b68c-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b68c-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9b68c-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9b68c-118">Library</span></span><br/> | <dl> <span data-ttu-id="9b68c-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9b68c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b68c-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b68c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b68c-121">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="9b68c-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




