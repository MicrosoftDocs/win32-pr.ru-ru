---
description: Метод Деливерневсегмент доставляет уведомление о новом сегменте в подключенный входной ПИН-код.
ms.assetid: 304f0267-88e0-4642-98a2-68ce973bdeab
title: Кбасеаутпутпин. Деливерневсегмент, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverNewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3eb6d31a50095affdf38d44b69040304674ec6fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669175"
---
# <a name="cbaseoutputpindelivernewsegment-method"></a><span data-ttu-id="456d0-103">Кбасеаутпутпин. Деливерневсегмент, метод</span><span class="sxs-lookup"><span data-stu-id="456d0-103">CBaseOutputPin.DeliverNewSegment method</span></span>

<span data-ttu-id="456d0-104">`DeliverNewSegment`Метод доставляет уведомление о новом сегменте в подключенный входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="456d0-104">The `DeliverNewSegment` method delivers a new-segment notification to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="456d0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="456d0-105">Syntax</span></span>


```C++
virtual HRESULT DeliverNewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="456d0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="456d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="456d0-107">*тстарт*</span><span class="sxs-lookup"><span data-stu-id="456d0-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="456d0-108">Начальная координата носителя сегмента, в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="456d0-108">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="456d0-109">*тстоп*</span><span class="sxs-lookup"><span data-stu-id="456d0-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="456d0-110">Конечное расположение носителя сегмента в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="456d0-110">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="456d0-111">*драте*</span><span class="sxs-lookup"><span data-stu-id="456d0-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="456d0-112">Скорость обработки этого сегмента в процентах от исходной ставки.</span><span class="sxs-lookup"><span data-stu-id="456d0-112">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="456d0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="456d0-113">Return value</span></span>

<span data-ttu-id="456d0-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="456d0-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="456d0-115">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="456d0-115">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="456d0-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="456d0-116">Return code</span></span>                                                                                           | <span data-ttu-id="456d0-117">Описание</span><span class="sxs-lookup"><span data-stu-id="456d0-117">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="456d0-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="456d0-118"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="456d0-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="456d0-119">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="456d0-120"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="456d0-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="456d0-121">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="456d0-121">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="456d0-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="456d0-122">Remarks</span></span>

<span data-ttu-id="456d0-123">Этот метод вызывает метод [**Ипин:: невсегмент**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="456d0-123">This method calls the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="456d0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="456d0-124">Requirements</span></span>



| <span data-ttu-id="456d0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="456d0-125">Requirement</span></span> | <span data-ttu-id="456d0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="456d0-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="456d0-127">Header</span><span class="sxs-lookup"><span data-stu-id="456d0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="456d0-128"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="456d0-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="456d0-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="456d0-129">Library</span></span><br/> | <dl> <span data-ttu-id="456d0-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="456d0-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="456d0-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="456d0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="456d0-132">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="456d0-132">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




