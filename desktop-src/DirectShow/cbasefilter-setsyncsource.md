---
description: 'Метод Сетсинксаурце задает время ссылки для фильтра. Этот метод реализует метод Имедиафилтер:: Сетсинксаурце.'
ms.assetid: 298039fc-dd38-4063-8752-2669b134b8ef
title: Кбасефилтер. Сетсинксаурце, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8eaab23f1afd7e7b502d6828bc3f10cbfec49410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657823"
---
# <a name="cbasefiltersetsyncsource-method"></a><span data-ttu-id="33f7d-104">Кбасефилтер. Сетсинксаурце, метод</span><span class="sxs-lookup"><span data-stu-id="33f7d-104">CBaseFilter.SetSyncSource method</span></span>

<span data-ttu-id="33f7d-105">Метод **сетсинксаурце** задает время ссылки для фильтра.</span><span class="sxs-lookup"><span data-stu-id="33f7d-105">The **SetSyncSource** method sets a reference clock for the filter.</span></span> <span data-ttu-id="33f7d-106">Этот метод реализует метод [**имедиафилтер:: сетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="33f7d-106">This method implements the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="33f7d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33f7d-107">Syntax</span></span>


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a><span data-ttu-id="33f7d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="33f7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33f7d-109">*пклокк*</span><span class="sxs-lookup"><span data-stu-id="33f7d-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="33f7d-110">Указатель на интерфейс [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) часов или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="33f7d-110">Pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33f7d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33f7d-111">Return value</span></span>

<span data-ttu-id="33f7d-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="33f7d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33f7d-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33f7d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="33f7d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="33f7d-114">Requirements</span></span>



| <span data-ttu-id="33f7d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="33f7d-115">Requirement</span></span> | <span data-ttu-id="33f7d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="33f7d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33f7d-117">Header</span><span class="sxs-lookup"><span data-stu-id="33f7d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="33f7d-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33f7d-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="33f7d-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="33f7d-119">Library</span></span><br/> | <dl> <span data-ttu-id="33f7d-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="33f7d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33f7d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33f7d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33f7d-122">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="33f7d-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




