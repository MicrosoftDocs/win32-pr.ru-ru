---
description: Кбасефилтер. Стреамтиме, метод Стреамтиме извлекает текущее время потока.
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: Кбасефилтер. Стреамтиме, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3334ac273a733c3f0591b76af7e76460997a199
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120072"
---
# <a name="cbasefilterstreamtime-method"></a><span data-ttu-id="e58f0-103">Кбасефилтер. Стреамтиме, метод</span><span class="sxs-lookup"><span data-stu-id="e58f0-103">CBaseFilter.StreamTime method</span></span>

<span data-ttu-id="e58f0-104">Метод **стреамтиме** извлекает текущее время потока.</span><span class="sxs-lookup"><span data-stu-id="e58f0-104">The **StreamTime** method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="e58f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e58f0-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="e58f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e58f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e58f0-107">*ртстреам* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="e58f0-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e58f0-108">Ссылка на объект [**крефтиме**](creftime.md) , который получает текущее время потока.</span><span class="sxs-lookup"><span data-stu-id="e58f0-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e58f0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e58f0-109">Return value</span></span>

<span data-ttu-id="e58f0-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e58f0-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e58f0-111">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e58f0-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="e58f0-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e58f0-112">Return code</span></span>                                                                                      | <span data-ttu-id="e58f0-113">Описание</span><span class="sxs-lookup"><span data-stu-id="e58f0-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="e58f0-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e58f0-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="e58f0-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="e58f0-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="e58f0-116"><dt>**VFW \_ E \_ без \_ часов**</dt></span><span class="sxs-lookup"><span data-stu-id="e58f0-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="e58f0-117">Нет доступных эталонных таймеров.</span><span class="sxs-lookup"><span data-stu-id="e58f0-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e58f0-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="e58f0-118">Remarks</span></span>

<span data-ttu-id="e58f0-119">Время потока определяется как текущее время ссылки (в соответствии с заданным временем) минус время начала (заданное параметром [**кбасефилтер:: m \_ тстарт**](cbasefilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="e58f0-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseFilter::m\_tStart**](cbasefilter-m-tstart.md)).</span></span> <span data-ttu-id="e58f0-120">*Метка времени* в образце носителя указывает время потока, когда он должен быть визуализирован.</span><span class="sxs-lookup"><span data-stu-id="e58f0-120">A media sample's *time stamp* specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="e58f0-121">Если образец с отметкой времени, меньшим, чем текущее время потока, еще не был визуализирован, то это поздно.</span><span class="sxs-lookup"><span data-stu-id="e58f0-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

<span data-ttu-id="e58f0-122">Этот метод получает время потока, вызывая [**иреференцеклокк::**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) IsReference для получения текущего времени ссылки, а затем вычитая начальное время начала.</span><span class="sxs-lookup"><span data-stu-id="e58f0-122">This method gets the stream time by calling [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) to get the current reference time, and then subtracting the initial start time.</span></span>

## <a name="requirements"></a><span data-ttu-id="e58f0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e58f0-123">Requirements</span></span>



| <span data-ttu-id="e58f0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e58f0-124">Requirement</span></span> | <span data-ttu-id="e58f0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e58f0-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e58f0-126">Header</span><span class="sxs-lookup"><span data-stu-id="e58f0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e58f0-127"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e58f0-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e58f0-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e58f0-128">Library</span></span><br/> | <dl> <span data-ttu-id="e58f0-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e58f0-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e58f0-130">См. также</span><span class="sxs-lookup"><span data-stu-id="e58f0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e58f0-131">Время и часы в DirectShow</span><span class="sxs-lookup"><span data-stu-id="e58f0-131">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="e58f0-132">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="e58f0-132">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




