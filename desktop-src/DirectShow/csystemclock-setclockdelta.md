---
description: 'Метод Сетклоккделта корректирует время в часах. Этот метод реализует метод Иамклоккаджуст:: Сетклоккделта.'
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: Ксистемклокк. Сетклоккделта, метод (Сисклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.SetClockDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc1027081cc8713cffd2979e20627c037d0799f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656889"
---
# <a name="csystemclocksetclockdelta-method"></a><span data-ttu-id="c3363-104">Ксистемклокк. Сетклоккделта, метод</span><span class="sxs-lookup"><span data-stu-id="c3363-104">CSystemClock.SetClockDelta method</span></span>

<span data-ttu-id="c3363-105">`SetClockDelta`Метод корректирует время.</span><span class="sxs-lookup"><span data-stu-id="c3363-105">The `SetClockDelta` method adjusts the clock time.</span></span> <span data-ttu-id="c3363-106">Этот метод реализует метод [**иамклоккаджуст:: сетклоккделта**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) .</span><span class="sxs-lookup"><span data-stu-id="c3363-106">This method implements the [**IAMClockAdjust::SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3363-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3363-107">Syntax</span></span>


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a><span data-ttu-id="c3363-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3363-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3363-109">*ртделта*</span><span class="sxs-lookup"><span data-stu-id="c3363-109">*rtDelta*</span></span> 
</dt> <dd>

<span data-ttu-id="c3363-110">Указывает величину, на которую следует отрегулировать часы, как [**значение \_ времени ссылки**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="c3363-110">Specifies the amount by which to adjust the clock, as a [**REFERENCE\_TIME**](reference-time.md) value.</span></span> <span data-ttu-id="c3363-111">Положительное значение перемещает часы вперед, а отрицательное значение перемещает часы назад.</span><span class="sxs-lookup"><span data-stu-id="c3363-111">A positive value moves the clock forward, and a negative value moves the clock backward.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3363-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3363-112">Return value</span></span>

<span data-ttu-id="c3363-113">Возвращает значение S \_ ОК или код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c3363-113">Returns S\_OK or an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3363-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3363-114">Remarks</span></span>

<span data-ttu-id="c3363-115">Этот метод просто вызывает [**кбасереференцеклокк:: сеттимеделта**](cbasereferenceclock-settimedelta.md).</span><span class="sxs-lookup"><span data-stu-id="c3363-115">This method simply calls [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).</span></span>

<span data-ttu-id="c3363-116">Значения времени, возвращаемые функцией [**иреференцеклокк:: OnTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) , монотонно увеличиваются.</span><span class="sxs-lookup"><span data-stu-id="c3363-116">The time values returned by [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) are monotonically increasing.</span></span> <span data-ttu-id="c3363-117">Если вы установили часы обратно, **время** будет продолжать сообщать о старом времени до тех пор, пока внутренняя синхронизация не завершится.</span><span class="sxs-lookup"><span data-stu-id="c3363-117">If you set the clock back, **GetTime** continues to report the old time until the internal clock catches up.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3363-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c3363-118">Requirements</span></span>



| <span data-ttu-id="c3363-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c3363-119">Requirement</span></span> | <span data-ttu-id="c3363-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c3363-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3363-121">Версия</span><span class="sxs-lookup"><span data-stu-id="c3363-121">Version</span></span><br/> | <span data-ttu-id="c3363-122">Класс Ксистемклокк</span><span class="sxs-lookup"><span data-stu-id="c3363-122">CSystemClock Class</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="c3363-123">Header</span><span class="sxs-lookup"><span data-stu-id="c3363-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c3363-124"><dt>Сисклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3363-124"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c3363-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c3363-125">Library</span></span><br/> | <dl> <span data-ttu-id="c3363-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c3363-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




