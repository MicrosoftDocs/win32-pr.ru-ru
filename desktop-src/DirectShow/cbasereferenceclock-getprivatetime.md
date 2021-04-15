---
description: Метод Жетприватетиме извлекает значение реального времени из часов.
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: Кбасереференцеклокк. Жетприватетиме, метод (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetPrivateTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 387df10472e4913d33722492bf07601faf08e3ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669202"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a><span data-ttu-id="1e172-103">Кбасереференцеклокк. Жетприватетиме, метод</span><span class="sxs-lookup"><span data-stu-id="1e172-103">CBaseReferenceClock.GetPrivateTime method</span></span>

<span data-ttu-id="1e172-104">`GetPrivateTime`Метод получает значение реального времени из часов.</span><span class="sxs-lookup"><span data-stu-id="1e172-104">The `GetPrivateTime` method retrieves the real time from the clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e172-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e172-105">Syntax</span></span>


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a><span data-ttu-id="1e172-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e172-106">Parameters</span></span>

<span data-ttu-id="1e172-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1e172-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e172-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e172-108">Return value</span></span>

<span data-ttu-id="1e172-109">Возвращает текущее время (в 100-наносекундных единицах).</span><span class="sxs-lookup"><span data-stu-id="1e172-109">Returns the current clock time, in 100-nanosecond units.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e172-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e172-110">Remarks</span></span>

<span data-ttu-id="1e172-111">Этот метод возвращает реальное время, сообщаемое часами.</span><span class="sxs-lookup"><span data-stu-id="1e172-111">This method returns the real time reported by the clock.</span></span> <span data-ttu-id="1e172-112">Внешние вызывающие объекты используют метод [**кбасереференцеклокк:: OnTime**](cbasereferenceclock-gettime.md) , который вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="1e172-112">External callers use the [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method, which calls this method.</span></span> <span data-ttu-id="1e172-113">В отличие от метода со **временем** , внутренние часы могут проходить назад.</span><span class="sxs-lookup"><span data-stu-id="1e172-113">Unlike the **GetTime** method, the internal clock is allowed to go backward.</span></span> <span data-ttu-id="1e172-114">Если это происходит, метод **метода noreturn по** ошибке возвращает время последнего отчета, пока метод не закончится `GetPrivateTime` .</span><span class="sxs-lookup"><span data-stu-id="1e172-114">If that happens, the **GetTime** method continues to return the last time that it reported, until the `GetPrivateTime` method catches up.</span></span>

<span data-ttu-id="1e172-115">Этот метод возвращает системное время.</span><span class="sxs-lookup"><span data-stu-id="1e172-115">This method returns the system time.</span></span> <span data-ttu-id="1e172-116">Переопределите этот метод, если часы получают время из другого источника.</span><span class="sxs-lookup"><span data-stu-id="1e172-116">Override this method if your clock gets the time from another source.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e172-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1e172-117">Requirements</span></span>



| <span data-ttu-id="1e172-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1e172-118">Requirement</span></span> | <span data-ttu-id="1e172-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1e172-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e172-120">Header</span><span class="sxs-lookup"><span data-stu-id="1e172-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1e172-121"><dt>Рефклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e172-121"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1e172-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1e172-122">Library</span></span><br/> | <dl> <span data-ttu-id="1e172-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1e172-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e172-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e172-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e172-125">**Класс Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="1e172-125">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




