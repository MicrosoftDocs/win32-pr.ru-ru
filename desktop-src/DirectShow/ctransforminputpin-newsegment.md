---
description: 'Метод Невсегмент уведомляет ПИН-код о том, что примеры носителей, полученные после этого вызова, группируются как сегмент. Этот метод реализует метод Ипин:: Невсегмент.'
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: Ктрансформинпутпин. Невсегмент, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25c455fe5ec6ddf9157e991b70b468ace653daa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675845"
---
# <a name="ctransforminputpinnewsegment-method"></a><span data-ttu-id="95d25-104">Ктрансформинпутпин. Невсегмент, метод</span><span class="sxs-lookup"><span data-stu-id="95d25-104">CTransformInputPin.NewSegment method</span></span>

<span data-ttu-id="95d25-105">`NewSegment`Метод уведомляет ПИН-код о том, что примеры носителей, полученные после этого вызова, группируются как сегмент.</span><span class="sxs-lookup"><span data-stu-id="95d25-105">The `NewSegment` method notifies the pin that media samples received after this call are grouped as a segment.</span></span> <span data-ttu-id="95d25-106">Этот метод реализует метод [**Ипин:: невсегмент**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .</span><span class="sxs-lookup"><span data-stu-id="95d25-106">This method implements the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d25-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95d25-107">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="95d25-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="95d25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d25-109">*тстарт*</span><span class="sxs-lookup"><span data-stu-id="95d25-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="95d25-110">Время начала сегмента.</span><span class="sxs-lookup"><span data-stu-id="95d25-110">Start time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="95d25-111">*тстоп*</span><span class="sxs-lookup"><span data-stu-id="95d25-111">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="95d25-112">Время окончания сегмента.</span><span class="sxs-lookup"><span data-stu-id="95d25-112">Stop time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="95d25-113">*драте*</span><span class="sxs-lookup"><span data-stu-id="95d25-113">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="95d25-114">Интенсивность сегмента.</span><span class="sxs-lookup"><span data-stu-id="95d25-114">Rate of the segment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95d25-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95d25-115">Return value</span></span>

<span data-ttu-id="95d25-116">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="95d25-116">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95d25-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95d25-117">Remarks</span></span>

<span data-ttu-id="95d25-118">Этот метод переопределяет метод [**кбасепин:: невсегмент**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="95d25-118">This method overrides the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span> <span data-ttu-id="95d25-119">Он вызывает метод [**ктрансформфилтер:: невсегмент**](ctransformfilter-newsegment.md) фильтра для предоставления вызова в нисходящем направлении.</span><span class="sxs-lookup"><span data-stu-id="95d25-119">It calls the filter's [**CTransformFilter::NewSegment**](ctransformfilter-newsegment.md) method to deliver the call downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="95d25-120">Требования</span><span class="sxs-lookup"><span data-stu-id="95d25-120">Requirements</span></span>



| <span data-ttu-id="95d25-121">Требование</span><span class="sxs-lookup"><span data-stu-id="95d25-121">Requirement</span></span> | <span data-ttu-id="95d25-122">Значение</span><span class="sxs-lookup"><span data-stu-id="95d25-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95d25-123">Header</span><span class="sxs-lookup"><span data-stu-id="95d25-123">Header</span></span><br/>  | <dl> <span data-ttu-id="95d25-124"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95d25-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="95d25-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="95d25-125">Library</span></span><br/> | <dl> <span data-ttu-id="95d25-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="95d25-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




