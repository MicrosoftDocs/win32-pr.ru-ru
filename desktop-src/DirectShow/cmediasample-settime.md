---
description: 'Метод SetTime задает время потока, когда должен начинаться и заканчиваться этот образец. Этот метод реализует метод Имедиасампле:: SetTime.'
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: Кмедиасампле. SetTime, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935c4f3aa565b291e459d36e067805944b4fd6b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674794"
---
# <a name="cmediasamplesettime-method"></a><span data-ttu-id="0a8c5-104">Кмедиасампле. SetTime, метод</span><span class="sxs-lookup"><span data-stu-id="0a8c5-104">CMediaSample.SetTime method</span></span>

<span data-ttu-id="0a8c5-105">`SetTime`Метод задает время потока, когда должен начинаться и заканчиваться этот образец.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-105">The `SetTime` method sets the stream times when this sample should begin and finish.</span></span> <span data-ttu-id="0a8c5-106">Этот метод реализует метод [**имедиасампле:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .</span><span class="sxs-lookup"><span data-stu-id="0a8c5-106">This method implements the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a8c5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a8c5-107">Syntax</span></span>


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a><span data-ttu-id="0a8c5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a8c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a8c5-109">*птиместарт*</span><span class="sxs-lookup"><span data-stu-id="0a8c5-109">*pTimeStart*</span></span> 
</dt> <dd>

<span data-ttu-id="0a8c5-110">Указатель на время потока, с которого начинается выборка, в единицах 100-наносекундных или **null**.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-110">Pointer to the stream time at which the sample begins, in 100-nanosecond units, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0a8c5-111">*птиминд*</span><span class="sxs-lookup"><span data-stu-id="0a8c5-111">*pTimeEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0a8c5-112">Указатель на время потока, в котором заканчивается образец, в единицах 100-наносекундных или **null**.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-112">Pointer to the stream time at which the sample ends, in 100-nanosecond units, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a8c5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a8c5-113">Return value</span></span>

<span data-ttu-id="0a8c5-114">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a8c5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a8c5-115">Remarks</span></span>

<span data-ttu-id="0a8c5-116">Этот метод задает переменные конечного элемента [**кмедиасампле:: m \_ Start**](cmediasample-m-start.md) и [**кмедиасампле: \_ : m**](cmediasample-m-end.md) , которые определяют метки времени.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-116">This method sets the [**CMediaSample::m\_Start**](cmediasample-m-start.md) and [**CMediaSample::m\_End**](cmediasample-m-end.md) member variables, which specify the time stamps.</span></span> <span data-ttu-id="0a8c5-117">Он также обновляет переменную члена [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) , которая указывает, являются ли отметки времени допустимыми.</span><span class="sxs-lookup"><span data-stu-id="0a8c5-117">It also updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies whether the time stamps are valid.</span></span>

<span data-ttu-id="0a8c5-118">Дополнительные сведения о метках времени см. [в разделе время и часы в DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="0a8c5-118">For information about time stamps, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a8c5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0a8c5-119">Requirements</span></span>



| <span data-ttu-id="0a8c5-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0a8c5-120">Requirement</span></span> | <span data-ttu-id="0a8c5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0a8c5-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a8c5-122">Header</span><span class="sxs-lookup"><span data-stu-id="0a8c5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0a8c5-123"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a8c5-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0a8c5-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0a8c5-124">Library</span></span><br/> | <dl> <span data-ttu-id="0a8c5-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0a8c5-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a8c5-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a8c5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a8c5-127">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="0a8c5-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




