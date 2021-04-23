---
description: Метод Жетдефаулттимерресолутион возвращает текущее разрешение таймера ссылочного времени.
ms.assetid: 14176f9c-7fa1-47f6-a261-9c66e271a3f2
title: Кбасереференцеклокк. Жетдефаулттимерресолутион, метод (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40a1c430f95b13086d50811e63cc2e411b3bf377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657311"
---
# <a name="cbasereferenceclockgetdefaulttimerresolution-method"></a><span data-ttu-id="ad3dd-103">Кбасереференцеклокк. Жетдефаулттимерресолутион, метод</span><span class="sxs-lookup"><span data-stu-id="ad3dd-103">CBaseReferenceClock.GetDefaultTimerResolution method</span></span>

<span data-ttu-id="ad3dd-104">`GetDefaultTimerResolution`Метод возвращает текущее разрешение таймера ссылочного времени.</span><span class="sxs-lookup"><span data-stu-id="ad3dd-104">The `GetDefaultTimerResolution` method returns the current resolution of the reference clock's timer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad3dd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad3dd-105">Syntax</span></span>


```C++
STDMETHODIMP GetDefaultTimerResolution(
   REFERENCE_TIME *pTimerResolution
);
```



## <a name="parameters"></a><span data-ttu-id="ad3dd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad3dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad3dd-107">*птимерресолутион*</span><span class="sxs-lookup"><span data-stu-id="ad3dd-107">*pTimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="ad3dd-108">Получает запрошенное разрешение таймера в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="ad3dd-108">Receives the requested timer resolution, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad3dd-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad3dd-109">Return value</span></span>

<span data-ttu-id="ad3dd-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ad3dd-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad3dd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad3dd-111">Remarks</span></span>

<span data-ttu-id="ad3dd-112">Этот метод реализует метод [**иреференцеклокктимерконтрол:: жетдефаулттимерресолутион**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) .</span><span class="sxs-lookup"><span data-stu-id="ad3dd-112">This method implements the [**IReferenceClockTimerControl::GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad3dd-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ad3dd-113">Requirements</span></span>



| <span data-ttu-id="ad3dd-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ad3dd-114">Requirement</span></span> | <span data-ttu-id="ad3dd-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ad3dd-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad3dd-116">Header</span><span class="sxs-lookup"><span data-stu-id="ad3dd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ad3dd-117"><dt>Рефклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad3dd-117"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ad3dd-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ad3dd-118">Library</span></span><br/> | <dl> <span data-ttu-id="ad3dd-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ad3dd-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad3dd-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad3dd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad3dd-121">**Класс Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="ad3dd-121">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




