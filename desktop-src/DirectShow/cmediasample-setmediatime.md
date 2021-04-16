---
description: 'Метод Сетмедиатиме задает время носителя для этого образца. Этот метод реализует метод Имедиасампле:: Сетмедиатиме.'
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: Кмедиасампле. Сетмедиатиме, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0240ef40f4c37f6c5528c979b2e89b43b03b3451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665269"
---
# <a name="cmediasamplesetmediatime-method"></a><span data-ttu-id="256f0-104">Кмедиасампле. Сетмедиатиме, метод</span><span class="sxs-lookup"><span data-stu-id="256f0-104">CMediaSample.SetMediaTime method</span></span>

<span data-ttu-id="256f0-105">`SetMediaTime`Метод задает время носителя для этого образца.</span><span class="sxs-lookup"><span data-stu-id="256f0-105">The `SetMediaTime` method sets the media times for this sample.</span></span> <span data-ttu-id="256f0-106">Этот метод реализует метод [**имедиасампле:: сетмедиатиме**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .</span><span class="sxs-lookup"><span data-stu-id="256f0-106">This method implements the [**IMediaSample::SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="256f0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="256f0-107">Syntax</span></span>


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a><span data-ttu-id="256f0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="256f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="256f0-109">*пстарт*</span><span class="sxs-lookup"><span data-stu-id="256f0-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="256f0-110">Указатель на время запуска носителя или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="256f0-110">Pointer to the media start time, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="256f0-111">*Ожидаем*</span><span class="sxs-lookup"><span data-stu-id="256f0-111">*pEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="256f0-112">Указатель на время окончания воспроизведения или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="256f0-112">Pointer to the media stop time, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="256f0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="256f0-113">Return value</span></span>

<span data-ttu-id="256f0-114">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="256f0-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="256f0-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="256f0-115">Remarks</span></span>

<span data-ttu-id="256f0-116">Время окончания работы с носителем должно быть больше времени начала носителя.</span><span class="sxs-lookup"><span data-stu-id="256f0-116">The media stop time must be greater than the media start time.</span></span> <span data-ttu-id="256f0-117">Чтобы сделать носитель недействительным, используйте **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="256f0-117">Use **NULL** to invalidate the media times.</span></span>

<span data-ttu-id="256f0-118">Параметр *ожидания* задает абсолютное время носителя, но переменная-член [**кмедиасампле:: m \_ медиаенд**](cmediasample-m-mediaend.md) вычисляется как смещение от *пстарт*.</span><span class="sxs-lookup"><span data-stu-id="256f0-118">The *pEnd* parameter specifies an absolute media time, but the [**CMediaSample::m\_MediaEnd**](cmediasample-m-mediaend.md) member variable is calculated as an offset from *pStart*.</span></span> <span data-ttu-id="256f0-119">Иными словами, **m \_ медиаенд**  =  \* *птиминд* \* *птиместарт*.  </span><span class="sxs-lookup"><span data-stu-id="256f0-119">In other words, **m\_MediaEnd** = \**pTimeEnd*  \**pTimeStart*.</span></span>

<span data-ttu-id="256f0-120">Дополнительные сведения о времени мультимедиа см. [в разделе время и часы в DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="256f0-120">For information about media times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="256f0-121">Требования</span><span class="sxs-lookup"><span data-stu-id="256f0-121">Requirements</span></span>



| <span data-ttu-id="256f0-122">Требование</span><span class="sxs-lookup"><span data-stu-id="256f0-122">Requirement</span></span> | <span data-ttu-id="256f0-123">Значение</span><span class="sxs-lookup"><span data-stu-id="256f0-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="256f0-124">Header</span><span class="sxs-lookup"><span data-stu-id="256f0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="256f0-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="256f0-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="256f0-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="256f0-126">Library</span></span><br/> | <dl> <span data-ttu-id="256f0-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="256f0-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="256f0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="256f0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="256f0-129">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="256f0-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




