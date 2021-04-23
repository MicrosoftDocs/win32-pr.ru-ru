---
description: 'Метод Невсегмент уведомляет ПИН-код о том, что примеры носителей, полученные после этого вызова, группируются как сегмент. Реализует метод Ипин:: Невсегмент.'
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Кбасепин. Невсегмент, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f128ce8cb2fee5479efeddd5932d0392b92a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657367"
---
# <a name="cbasepinnewsegment-method"></a><span data-ttu-id="ae8f2-104">Кбасепин. Невсегмент, метод</span><span class="sxs-lookup"><span data-stu-id="ae8f2-104">CBasePin.NewSegment method</span></span>

<span data-ttu-id="ae8f2-105">`NewSegment`Метод уведомляет ПИН-код о том, что примеры носителей, полученные после этого вызова, группируются как сегмент.</span><span class="sxs-lookup"><span data-stu-id="ae8f2-105">The `NewSegment` method notifies the pin that media samples received after this call are grouped as a segment.</span></span> <span data-ttu-id="ae8f2-106">Реализует метод [**Ипин:: невсегмент**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .</span><span class="sxs-lookup"><span data-stu-id="ae8f2-106">Implements the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae8f2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae8f2-107">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="ae8f2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae8f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae8f2-109">*тстарт*</span><span class="sxs-lookup"><span data-stu-id="ae8f2-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="ae8f2-110">Начальная координата носителя сегмента, в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="ae8f2-110">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="ae8f2-111">*тстоп*</span><span class="sxs-lookup"><span data-stu-id="ae8f2-111">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="ae8f2-112">Конечное расположение носителя сегмента в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="ae8f2-112">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="ae8f2-113">*драте*</span><span class="sxs-lookup"><span data-stu-id="ae8f2-113">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="ae8f2-114">Скорость обработки этого сегмента в процентах от исходной ставки.</span><span class="sxs-lookup"><span data-stu-id="ae8f2-114">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae8f2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae8f2-115">Return value</span></span>

<span data-ttu-id="ae8f2-116">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ae8f2-116">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae8f2-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae8f2-117">Remarks</span></span>

<span data-ttu-id="ae8f2-118">Этот метод задает переменные члена [**кбасепин:: m \_ тстарт**](cbasepin-m-tstart.md), [**кбасепин:: m \_ тстоп**](cbasepin-m-tstop.md)и [**кбасепин:: m \_ драте**](cbasepin-m-drate.md) .</span><span class="sxs-lookup"><span data-stu-id="ae8f2-118">This method sets the [**CBasePin::m\_tStart**](cbasepin-m-tstart.md), [**CBasePin::m\_tStop**](cbasepin-m-tstop.md), and [**CBasePin::m\_dRate**](cbasepin-m-drate.md) member variables.</span></span> <span data-ttu-id="ae8f2-119">В производном классе Переопределите этот метод, чтобы передать уведомление в нисходящее.</span><span class="sxs-lookup"><span data-stu-id="ae8f2-119">In your derived class, override this method to pass the notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae8f2-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ae8f2-120">Requirements</span></span>



| <span data-ttu-id="ae8f2-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ae8f2-121">Requirement</span></span> | <span data-ttu-id="ae8f2-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ae8f2-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8f2-123">Header</span><span class="sxs-lookup"><span data-stu-id="ae8f2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ae8f2-124"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae8f2-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ae8f2-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ae8f2-125">Library</span></span><br/> | <dl> <span data-ttu-id="ae8f2-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ae8f2-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae8f2-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae8f2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae8f2-128">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="ae8f2-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




