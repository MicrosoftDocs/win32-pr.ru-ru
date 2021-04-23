---
description: Метод Сетдефаулттимерресолутион задает разрешение таймера ссылочного времени.
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: Кбасереференцеклокк. Сетдефаулттимерресолутион, метод (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 146162784ad52a7f7930613ec5c648e40d22900f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669199"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a><span data-ttu-id="a4e19-103">Кбасереференцеклокк. Сетдефаулттимерресолутион, метод</span><span class="sxs-lookup"><span data-stu-id="a4e19-103">CBaseReferenceClock.SetDefaultTimerResolution method</span></span>

<span data-ttu-id="a4e19-104">`SetDefaultTimerResolution`Метод задает разрешение таймера ссылочного времени.</span><span class="sxs-lookup"><span data-stu-id="a4e19-104">The `SetDefaultTimerResolution` method sets the resolution of the reference clock's timer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4e19-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4e19-105">Syntax</span></span>


```C++
STDMETHODIMP SetDefaultTimerResolution(
   REFERENCE_TIME timerResolution
);
```



## <a name="parameters"></a><span data-ttu-id="a4e19-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4e19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4e19-107">*тимерресолутион*</span><span class="sxs-lookup"><span data-stu-id="a4e19-107">*timerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="a4e19-108">Минимальное разрешение таймера (в 100-наносекундных единицах).</span><span class="sxs-lookup"><span data-stu-id="a4e19-108">Minimum timer resolution, in 100-nanosecond units.</span></span> <span data-ttu-id="a4e19-109">Если значение равно нулю, то контрольный таймер отменяет предыдущий запрос.</span><span class="sxs-lookup"><span data-stu-id="a4e19-109">If the value is zero, the reference clock cancels its previous request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4e19-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4e19-110">Return value</span></span>

<span data-ttu-id="a4e19-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a4e19-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4e19-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4e19-112">Remarks</span></span>

<span data-ttu-id="a4e19-113">Этот метод реализует метод [**иреференцеклокктимерконтрол:: сетдефаулттимерресолутион**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) .</span><span class="sxs-lookup"><span data-stu-id="a4e19-113">This method implements the [**IReferenceClockTimerControl::SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4e19-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a4e19-114">Requirements</span></span>



| <span data-ttu-id="a4e19-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a4e19-115">Requirement</span></span> | <span data-ttu-id="a4e19-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a4e19-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4e19-117">Header</span><span class="sxs-lookup"><span data-stu-id="a4e19-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a4e19-118"><dt>Рефклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4e19-118"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a4e19-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a4e19-119">Library</span></span><br/> | <dl> <span data-ttu-id="a4e19-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a4e19-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4e19-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4e19-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4e19-122">**Класс Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="a4e19-122">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




