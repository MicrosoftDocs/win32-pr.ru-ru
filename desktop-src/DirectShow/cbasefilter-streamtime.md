---
description: Метод Стреамтиме извлекает текущее время потока.
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
ms.openlocfilehash: f4370758eb4ab15a9e53a5157550ee2129783c7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657821"
---
# <a name="cbasefilterstreamtime-method"></a><span data-ttu-id="23418-103">Кбасефилтер. Стреамтиме, метод</span><span class="sxs-lookup"><span data-stu-id="23418-103">CBaseFilter.StreamTime method</span></span>

<span data-ttu-id="23418-104">Метод **стреамтиме** извлекает текущее время потока.</span><span class="sxs-lookup"><span data-stu-id="23418-104">The **StreamTime** method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="23418-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23418-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="23418-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="23418-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23418-107">*ртстреам* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="23418-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="23418-108">Ссылка на объект [**крефтиме**](creftime.md) , который получает текущее время потока.</span><span class="sxs-lookup"><span data-stu-id="23418-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23418-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23418-109">Return value</span></span>

<span data-ttu-id="23418-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23418-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="23418-111">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="23418-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="23418-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="23418-112">Return code</span></span>                                                                                      | <span data-ttu-id="23418-113">Описание</span><span class="sxs-lookup"><span data-stu-id="23418-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="23418-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="23418-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="23418-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="23418-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="23418-116"><dt>**VFW \_ E \_ без \_ часов**</dt></span><span class="sxs-lookup"><span data-stu-id="23418-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="23418-117">Нет доступных эталонных таймеров.</span><span class="sxs-lookup"><span data-stu-id="23418-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="23418-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23418-118">Remarks</span></span>

<span data-ttu-id="23418-119">Время потока определяется как текущее время ссылки (в соответствии с заданным временем) минус время начала (заданное параметром [**кбасефилтер:: m \_ тстарт**](cbasefilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="23418-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseFilter::m\_tStart**](cbasefilter-m-tstart.md)).</span></span> <span data-ttu-id="23418-120">*Метка времени* в образце носителя указывает время потока, когда он должен быть визуализирован.</span><span class="sxs-lookup"><span data-stu-id="23418-120">A media sample's *time stamp* specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="23418-121">Если образец с отметкой времени, меньшим, чем текущее время потока, еще не был визуализирован, то это поздно.</span><span class="sxs-lookup"><span data-stu-id="23418-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

<span data-ttu-id="23418-122">Этот метод получает время потока, вызывая [**иреференцеклокк::**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) IsReference для получения текущего времени ссылки, а затем вычитая начальное время начала.</span><span class="sxs-lookup"><span data-stu-id="23418-122">This method gets the stream time by calling [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) to get the current reference time, and then subtracting the initial start time.</span></span>

## <a name="requirements"></a><span data-ttu-id="23418-123">Требования</span><span class="sxs-lookup"><span data-stu-id="23418-123">Requirements</span></span>



| <span data-ttu-id="23418-124">Требование</span><span class="sxs-lookup"><span data-stu-id="23418-124">Requirement</span></span> | <span data-ttu-id="23418-125">Значение</span><span class="sxs-lookup"><span data-stu-id="23418-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23418-126">Header</span><span class="sxs-lookup"><span data-stu-id="23418-126">Header</span></span><br/>  | <dl> <span data-ttu-id="23418-127"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23418-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="23418-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="23418-128">Library</span></span><br/> | <dl> <span data-ttu-id="23418-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="23418-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23418-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23418-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23418-131">Время и часы в DirectShow</span><span class="sxs-lookup"><span data-stu-id="23418-131">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="23418-132">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="23418-132">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




