---
description: Класс Кбасереференцеклокк реализует ссылочное время.
ms.assetid: 898e1968-a9ab-4bb9-abf0-943bfae502e2
title: Класс Кбасереференцеклокк (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1da55a57faac201a2dbf0ef4d8a9774157d9215d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668755"
---
# <a name="cbasereferenceclock-class"></a><span data-ttu-id="95e6d-103">Класс Кбасереференцеклокк</span><span class="sxs-lookup"><span data-stu-id="95e6d-103">CBaseReferenceClock class</span></span>

![Иерархия классов кбасереференцеклокк](images/rclock01.png)

<span data-ttu-id="95e6d-105">`CBaseReferenceClock`Класс реализует ссылочное время.</span><span class="sxs-lookup"><span data-stu-id="95e6d-105">The `CBaseReferenceClock` class implements a reference clock.</span></span>



| <span data-ttu-id="95e6d-106">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="95e6d-106">Protected Member Variables</span></span>                                                         | <span data-ttu-id="95e6d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="95e6d-107">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="95e6d-108">**m \_ псчедуле**</span><span class="sxs-lookup"><span data-stu-id="95e6d-108">**m\_pSchedule**</span></span>](cbasereferenceclock-m-pschedule.md)                            | <span data-ttu-id="95e6d-109">Объект [**камсчедуле**](camschedule.md) , который обрабатывает задачи планирования для часов.</span><span class="sxs-lookup"><span data-stu-id="95e6d-109">[**CAMSchedule**](camschedule.md) object that handles scheduling tasks for the clock.</span></span> |
| <span data-ttu-id="95e6d-110">Защищенные методы</span><span class="sxs-lookup"><span data-stu-id="95e6d-110">Protected Methods</span></span>                                                                  | <span data-ttu-id="95e6d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="95e6d-111">Description</span></span>                                                                            |
| [<span data-ttu-id="95e6d-112">**~ Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="95e6d-112">**~CBaseReferenceClock**</span></span>](cbasereferenceclock--cbasereferenceclock.md)           | <span data-ttu-id="95e6d-113">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="95e6d-113">Destructor method.</span></span>                                                                     |
| <span data-ttu-id="95e6d-114">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="95e6d-114">Public Methods</span></span>                                                                     | <span data-ttu-id="95e6d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="95e6d-115">Description</span></span>                                                                            |
| [<span data-ttu-id="95e6d-116">**кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="95e6d-116">**CBaseReferenceClock**</span></span>](cbasereferenceclock-cbasereferenceclock.md)             | <span data-ttu-id="95e6d-117">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="95e6d-117">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="95e6d-118">**жетприватетиме**</span><span class="sxs-lookup"><span data-stu-id="95e6d-118">**GetPrivateTime**</span></span>](cbasereferenceclock-getprivatetime.md)                       | <span data-ttu-id="95e6d-119">Извлекает реальное время из часов.</span><span class="sxs-lookup"><span data-stu-id="95e6d-119">Retrieves the real time from the clock.</span></span>                                                |
| [<span data-ttu-id="95e6d-120">**сеттимеделта**</span><span class="sxs-lookup"><span data-stu-id="95e6d-120">**SetTimeDelta**</span></span>](cbasereferenceclock-settimedelta.md)                           | <span data-ttu-id="95e6d-121">Регулирует время внутренних часов.</span><span class="sxs-lookup"><span data-stu-id="95e6d-121">Adjusts the internal clock time.</span></span>                                                       |
| [<span data-ttu-id="95e6d-122">**Задание по расписанию**</span><span class="sxs-lookup"><span data-stu-id="95e6d-122">**GetSchedule**</span></span>](cbasereferenceclock-getschedule.md)                             | <span data-ttu-id="95e6d-123">Извлекает указатель на объект расписания часов.</span><span class="sxs-lookup"><span data-stu-id="95e6d-123">Retrieves a pointer to the clock's scheduling object.</span></span>                                  |
| [<span data-ttu-id="95e6d-124">**тригжерсреад**</span><span class="sxs-lookup"><span data-stu-id="95e6d-124">**TriggerThread**</span></span>](cbasereferenceclock-triggerthread.md)                         | <span data-ttu-id="95e6d-125">Пробуждает рабочий поток, который обрабатывает планирование.</span><span class="sxs-lookup"><span data-stu-id="95e6d-125">Wakes up the worker thread that handles scheduling.</span></span>                                    |
| <span data-ttu-id="95e6d-126">Методы Иреференцеклокк</span><span class="sxs-lookup"><span data-stu-id="95e6d-126">IReferenceClock Methods</span></span>                                                            | <span data-ttu-id="95e6d-127">Описание</span><span class="sxs-lookup"><span data-stu-id="95e6d-127">Description</span></span>                                                                            |
| [<span data-ttu-id="95e6d-128">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="95e6d-128">**GetTime**</span></span>](cbasereferenceclock-gettime.md)                                     | <span data-ttu-id="95e6d-129">Извлекает текущее время ссылки.</span><span class="sxs-lookup"><span data-stu-id="95e6d-129">Retrieves the current reference time.</span></span>                                                  |
| [<span data-ttu-id="95e6d-130">**адвисетиме**</span><span class="sxs-lookup"><span data-stu-id="95e6d-130">**AdviseTime**</span></span>](cbasereferenceclock-advisetime.md)                               | <span data-ttu-id="95e6d-131">Создает одноразовый запрос Advise.</span><span class="sxs-lookup"><span data-stu-id="95e6d-131">Creates a one-shot advise request.</span></span>                                                     |
| [<span data-ttu-id="95e6d-132">**адвисепериодик**</span><span class="sxs-lookup"><span data-stu-id="95e6d-132">**AdvisePeriodic**</span></span>](cbasereferenceclock-adviseperiodic.md)                       | <span data-ttu-id="95e6d-133">Создает периодические запросы рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="95e6d-133">Creates a periodic advise request.</span></span>                                                     |
| [<span data-ttu-id="95e6d-134">**Unadvise**</span><span class="sxs-lookup"><span data-stu-id="95e6d-134">**Unadvise**</span></span>](cbasereferenceclock-unadvise.md)                                   | <span data-ttu-id="95e6d-135">Удаляет ожидающий запрос рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="95e6d-135">Removes a pending advise request.</span></span>                                                      |
| <span data-ttu-id="95e6d-136">Методы Иреференцеклокктимерконтрол</span><span class="sxs-lookup"><span data-stu-id="95e6d-136">IReferenceClockTimerControl Methods</span></span>                                                | <span data-ttu-id="95e6d-137">Описание</span><span class="sxs-lookup"><span data-stu-id="95e6d-137">Description</span></span>                                                                            |
| [<span data-ttu-id="95e6d-138">**жетдефаулттимерресолутион**</span><span class="sxs-lookup"><span data-stu-id="95e6d-138">**GetDefaultTimerResolution**</span></span>](cbasereferenceclock-getdefaulttimerresolution.md) | <span data-ttu-id="95e6d-139">Возвращает текущее разрешение таймера ссылочного времени.</span><span class="sxs-lookup"><span data-stu-id="95e6d-139">Returns the current resolution of the reference clock's timer.</span></span>                         |
| [<span data-ttu-id="95e6d-140">**сетдефаулттимерресолутион**</span><span class="sxs-lookup"><span data-stu-id="95e6d-140">**SetDefaultTimerResolution**</span></span>](cbasereferenceclock-setdefaulttimerresolution.md) | <span data-ttu-id="95e6d-141">Задает разрешение таймера ссылочного времени.</span><span class="sxs-lookup"><span data-stu-id="95e6d-141">Sets the resolution of the reference clock's timer.</span></span>                                    |
| <span data-ttu-id="95e6d-142">Вспомогательные функции</span><span class="sxs-lookup"><span data-stu-id="95e6d-142">Helper Functions</span></span>                                                                   | <span data-ttu-id="95e6d-143">Описание</span><span class="sxs-lookup"><span data-stu-id="95e6d-143">Description</span></span>                                                                            |
| [<span data-ttu-id="95e6d-144">**конверттомиллисекондс**</span><span class="sxs-lookup"><span data-stu-id="95e6d-144">**ConvertToMilliseconds**</span></span>](converttomilliseconds.md)                             | <span data-ttu-id="95e6d-145">Преобразует время ссылки в миллисекунды.</span><span class="sxs-lookup"><span data-stu-id="95e6d-145">Converts a reference time to milliseconds.</span></span>                                             |



 

## <a name="remarks"></a><span data-ttu-id="95e6d-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95e6d-146">Remarks</span></span>

<span data-ttu-id="95e6d-147">Этот класс реализует ссылочный таймер, который поддерживает интерфейсы [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) и [**иреференцеклокктимерконтрол**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) .</span><span class="sxs-lookup"><span data-stu-id="95e6d-147">This class implements a reference clock that supports the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) and [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) interfaces.</span></span> <span data-ttu-id="95e6d-148">Если фильтр может предоставить эталонный период для графа фильтра, например путем доступа к устройству, он может использовать этот класс для реализации часов.</span><span class="sxs-lookup"><span data-stu-id="95e6d-148">If a filter can provide a reference clock for the filter graph for example, by accessing a hardware device it can use this class to implement the clock.</span></span>

<span data-ttu-id="95e6d-149">`CBaseReferenceClock`Объект поддерживает два различных значения времени:</span><span class="sxs-lookup"><span data-stu-id="95e6d-149">The `CBaseReferenceClock` object maintains two distinct time values:</span></span>

-   <span data-ttu-id="95e6d-150">На внутреннем уровне метод [**кбасереференцеклокк:: жетприватетиме**](cbasereferenceclock-getprivatetime.md) возвращает фактическое время, сохраненное в часах.</span><span class="sxs-lookup"><span data-stu-id="95e6d-150">Internally, the [**CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) method returns the actual time kept by the clock.</span></span>
-   <span data-ttu-id="95e6d-151">Во внешнем метод [**кбасереференцеклокк::**](cbasereferenceclock-gettime.md) IsReference возвращает время ссылки для графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="95e6d-151">Externally, the [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method returns the reference time for the filter graph.</span></span>

<span data-ttu-id="95e6d-152">Это допустимо, чтобы внутренние часы выполнялись в обратном направлении в короткие периоды.</span><span class="sxs-lookup"><span data-stu-id="95e6d-152">It is valid for the internal clock to run backward over brief periods.</span></span> <span data-ttu-id="95e6d-153">Например, если часы переносятся вперед, фильтр может изменить его обратно.</span><span class="sxs-lookup"><span data-stu-id="95e6d-153">For example, if the clock drifts forward, the filter can adjust it backward.</span></span> <span data-ttu-id="95e6d-154">(См. [**кбасереференцеклокк:: сеттимеделта**](cbasereferenceclock-settimedelta.md).) Метод  **жетприватетиме** использует значения времени, сообщаемые параметром</span><span class="sxs-lookup"><span data-stu-id="95e6d-154">(See [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).) The **GetTime** method uses the time values reported by **GetPrivateTime**.</span></span> <span data-ttu-id="95e6d-155">Однако время ссылки монотонно возрастает; Иными словами, он никогда не выполняется назад.</span><span class="sxs-lookup"><span data-stu-id="95e6d-155">However, the reference time is monotonically increasing; in other words, it never runs backward.</span></span> <span data-ttu-id="95e6d-156">Таким образом, если внутренняя тактовая частота выполняется назад, во **время ожидания** происходит создание отчета о старом времени до тех пор, пока внутреннее время не будет перехватываться.</span><span class="sxs-lookup"><span data-stu-id="95e6d-156">Therefore, if the internal clock runs backward, **GetTime** continues to report the old time until the internal clock catches up.</span></span>

<span data-ttu-id="95e6d-157">Например, два метода могут возвращать следующие последовательности:</span><span class="sxs-lookup"><span data-stu-id="95e6d-157">For example, the two methods might return the following sequences:</span></span>

``` syntax
GetPrivateTime: 105, 106, 103, 104, 105, 106, 107, 108
GetTime:        105, 106, 106, 106, 106, 106, 107, 108
```

<span data-ttu-id="95e6d-158">В третьем такте времени внутренняя шкала времени переходит в обратное значение в 103.</span><span class="sxs-lookup"><span data-stu-id="95e6d-158">On the third clock tick, the internal clock jumps backward to 103.</span></span> <span data-ttu-id="95e6d-159">Метод метода **time** до тех пор сообщает 106, пока не будут перехватываться внутренние часы.</span><span class="sxs-lookup"><span data-stu-id="95e6d-159">The **GetTime** method continues to report 106 until the internal clock catches up.</span></span>

<span data-ttu-id="95e6d-160">По умолчанию **жетприватетиме** возвращает системное время с помощью вызова функции **тимежеттиме** .</span><span class="sxs-lookup"><span data-stu-id="95e6d-160">By default, **GetPrivateTime** returns the system time, through a call to the **timeGetTime** function.</span></span> <span data-ttu-id="95e6d-161">Фильтр, предоставляющий ссылочное время с внешнего устройства, может выполнять одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="95e6d-161">A filter that is providing a reference clock from an external device can do one of the following:</span></span>

-   <span data-ttu-id="95e6d-162">Переопределите **жетприватетиме** , чтобы вернуть время с устройства.</span><span class="sxs-lookup"><span data-stu-id="95e6d-162">Override **GetPrivateTime** to return the time from the device.</span></span>
-   <span data-ttu-id="95e6d-163">Отслеживайте расхождения между временем устройства и системным временем и вызовите **сеттимеделта** для внесения исправлений.</span><span class="sxs-lookup"><span data-stu-id="95e6d-163">Monitor the discrepancy between the device time and the system time, and call **SetTimeDelta** to make corrections.</span></span>

<span data-ttu-id="95e6d-164">Этот класс использует объект [**камсчедуле**](camschedule.md) для обработки планирования запросов рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="95e6d-164">This class uses a [**CAMSchedule**](camschedule.md) object to handle scheduling of advise requests.</span></span> <span data-ttu-id="95e6d-165">Дополнительные сведения см. в документации по классу **камсчедуле** .</span><span class="sxs-lookup"><span data-stu-id="95e6d-165">For details, see the documentation for the **CAMSchedule** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="95e6d-166">Требования</span><span class="sxs-lookup"><span data-stu-id="95e6d-166">Requirements</span></span>



| <span data-ttu-id="95e6d-167">Требование</span><span class="sxs-lookup"><span data-stu-id="95e6d-167">Requirement</span></span> | <span data-ttu-id="95e6d-168">Значение</span><span class="sxs-lookup"><span data-stu-id="95e6d-168">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95e6d-169">Header</span><span class="sxs-lookup"><span data-stu-id="95e6d-169">Header</span></span><br/>  | <dl> <span data-ttu-id="95e6d-170"><dt>Рефклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95e6d-170"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="95e6d-171">Библиотека</span><span class="sxs-lookup"><span data-stu-id="95e6d-171">Library</span></span><br/> | <dl> <span data-ttu-id="95e6d-172"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="95e6d-172"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




