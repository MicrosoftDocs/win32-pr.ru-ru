---
description: Метод Невсегмент уведомляет фильтр о том, что примеры носителей, полученные после этого вызова, группируются в виде сегмента.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: Ктрансформфилтер. Невсегмент, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd046288886d3e7619419dd591dd94310f56020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657747"
---
# <a name="ctransformfilternewsegment-method"></a><span data-ttu-id="5ea2c-103">Ктрансформфилтер. Невсегмент, метод</span><span class="sxs-lookup"><span data-stu-id="5ea2c-103">CTransformFilter.NewSegment method</span></span>

<span data-ttu-id="5ea2c-104">`NewSegment`Метод уведомляет фильтр о том, что примеры носителей, полученные после этого вызова, группируются в виде сегмента.</span><span class="sxs-lookup"><span data-stu-id="5ea2c-104">The `NewSegment` method notifies the filter that media samples received after this call are grouped as a segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea2c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ea2c-105">Syntax</span></span>


```C++
virtual HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="5ea2c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ea2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ea2c-107">*тстарт*</span><span class="sxs-lookup"><span data-stu-id="5ea2c-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea2c-108">Время начала сегмента относительно исходного источника.</span><span class="sxs-lookup"><span data-stu-id="5ea2c-108">Start time of the segment, relative to the original source.</span></span>

</dd> <dt>

<span data-ttu-id="5ea2c-109">*тстоп*</span><span class="sxs-lookup"><span data-stu-id="5ea2c-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea2c-110">Время окончания сегмента относительно исходного источника.</span><span class="sxs-lookup"><span data-stu-id="5ea2c-110">Stop time of the segment, relative to the original source.</span></span>

</dd> <dt>

<span data-ttu-id="5ea2c-111">*драте*</span><span class="sxs-lookup"><span data-stu-id="5ea2c-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea2c-112">Скорость обработки сегмента.</span><span class="sxs-lookup"><span data-stu-id="5ea2c-112">Rate at which the segment should be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ea2c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ea2c-113">Return value</span></span>

<span data-ttu-id="5ea2c-114">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5ea2c-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ea2c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ea2c-115">Remarks</span></span>

<span data-ttu-id="5ea2c-116">Метод [**ктрансформинпутпин:: невсегмент**](ctransforminputpin-newsegment.md) входного контакта вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="5ea2c-116">The input pin's [**CTransformInputPin::NewSegment**](ctransforminputpin-newsegment.md) method calls this method.</span></span> <span data-ttu-id="5ea2c-117">Этот метод доставляет `NewSegment` вызов нисходящего входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="5ea2c-117">This method delivers the `NewSegment` call to the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ea2c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5ea2c-118">Requirements</span></span>



| <span data-ttu-id="5ea2c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5ea2c-119">Requirement</span></span> | <span data-ttu-id="5ea2c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5ea2c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea2c-121">Header</span><span class="sxs-lookup"><span data-stu-id="5ea2c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5ea2c-122"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ea2c-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5ea2c-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5ea2c-123">Library</span></span><br/> | <dl> <span data-ttu-id="5ea2c-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5ea2c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ea2c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ea2c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea2c-126">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="5ea2c-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




