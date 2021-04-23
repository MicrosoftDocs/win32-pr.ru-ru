---
description: Класс Камсчедуле реализует планировщик для ссылочных синхронизирующих импульсов.
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: Класс Камсчедуле (Дссчедуле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bef8ad07347284c53a3490c21032070788fa3ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668962"
---
# <a name="camschedule-class"></a><span data-ttu-id="16f27-103">Класс Камсчедуле</span><span class="sxs-lookup"><span data-stu-id="16f27-103">CAMSchedule class</span></span>

<span data-ttu-id="16f27-104">`CAMSchedule`Класс реализует планировщик для ссылочных синхронизирующих импульсов.</span><span class="sxs-lookup"><span data-stu-id="16f27-104">The `CAMSchedule` class implements a scheduler for reference clocks.</span></span>



| <span data-ttu-id="16f27-105">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="16f27-105">Public Methods</span></span>                                             | <span data-ttu-id="16f27-106">Описание</span><span class="sxs-lookup"><span data-stu-id="16f27-106">Description</span></span>                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="16f27-107">**камсчедуле**</span><span class="sxs-lookup"><span data-stu-id="16f27-107">**CAMSchedule**</span></span>](camschedule-camschedule.md)             | <span data-ttu-id="16f27-108">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="16f27-108">Constructor method.</span></span>                                                                  |
| [<span data-ttu-id="16f27-109">**~ Камсчедуле**</span><span class="sxs-lookup"><span data-stu-id="16f27-109">**~CAMSchedule**</span></span>](camschedule--camschedule.md)           | <span data-ttu-id="16f27-110">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="16f27-110">Destructor method.</span></span> <span data-ttu-id="16f27-111">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="16f27-111">Virtual.</span></span>                                                          |
| [<span data-ttu-id="16f27-112">**жетадвисекаунт**</span><span class="sxs-lookup"><span data-stu-id="16f27-112">**GetAdviseCount**</span></span>](camschedule-getadvisecount.md)       | <span data-ttu-id="16f27-113">Возвращает число ожидающих запросов рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="16f27-113">Retrieves the number of pending advise requests.</span></span>                                     |
| [<span data-ttu-id="16f27-114">**жетнекстадвисетиме**</span><span class="sxs-lookup"><span data-stu-id="16f27-114">**GetNextAdviseTime**</span></span>](camschedule-getnextadvisetime.md) | <span data-ttu-id="16f27-115">Извлекает время следующего запроса на выadvise.</span><span class="sxs-lookup"><span data-stu-id="16f27-115">Retrieves the time of the next advise request.</span></span>                                       |
| [<span data-ttu-id="16f27-116">**аддадвисепаккет**</span><span class="sxs-lookup"><span data-stu-id="16f27-116">**AddAdvisePacket**</span></span>](camschedule-addadvisepacket.md)     | <span data-ttu-id="16f27-117">Добавляет запрос advise в список ожидающих запросов.</span><span class="sxs-lookup"><span data-stu-id="16f27-117">Adds an advise request to the list of pending requests.</span></span>                              |
| [<span data-ttu-id="16f27-118">**Unadvise**</span><span class="sxs-lookup"><span data-stu-id="16f27-118">**Unadvise**</span></span>](camschedule-unadvise.md)                   | <span data-ttu-id="16f27-119">Удаляет запрос Advise.</span><span class="sxs-lookup"><span data-stu-id="16f27-119">Removes an advise request.</span></span>                                                           |
| [<span data-ttu-id="16f27-120">**Извещен**</span><span class="sxs-lookup"><span data-stu-id="16f27-120">**Advise**</span></span>](camschedule-advise.md)                       | <span data-ttu-id="16f27-121">Отправляет все запросы, запланированные на указанное время или ранее.</span><span class="sxs-lookup"><span data-stu-id="16f27-121">Dispatches all requests that are scheduled for a specified time or earlier.</span></span>          |
| [<span data-ttu-id="16f27-122">**Четный**</span><span class="sxs-lookup"><span data-stu-id="16f27-122">**GetEvent**</span></span>](camschedule-getevent.md)                   | <span data-ttu-id="16f27-123">Извлекает дескриптор события, который используется для сигнализации об изменении в следующем времени.</span><span class="sxs-lookup"><span data-stu-id="16f27-123">Retrieves an event handle, which is used to signal a change in the next advise time.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="16f27-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16f27-124">Remarks</span></span>

<span data-ttu-id="16f27-125">Этот вспомогательный объект содержит список запросов рекомендаций для времени ссылки.</span><span class="sxs-lookup"><span data-stu-id="16f27-125">This helper object maintains a list of advise requests for a reference clock.</span></span> <span data-ttu-id="16f27-126">Класс [**кбасереференцеклокк**](cbasereferenceclock.md) использует его для планирования запросов рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="16f27-126">The [**CBaseReferenceClock**](cbasereferenceclock.md) class uses it to help schedule advise requests.</span></span> <span data-ttu-id="16f27-127">Часы используют этот объект следующим образом:</span><span class="sxs-lookup"><span data-stu-id="16f27-127">Clocks use this object in the following manner:</span></span>

1.  <span data-ttu-id="16f27-128">Часы создают рабочий поток для обработки планирования.</span><span class="sxs-lookup"><span data-stu-id="16f27-128">The clock creates a worker thread to handle scheduling.</span></span>
2.  <span data-ttu-id="16f27-129">Рабочий поток вызывает метод [**камсчедуле:: четный**](camschedule-getevent.md) для получения обработчика событий от планировщика.</span><span class="sxs-lookup"><span data-stu-id="16f27-129">The worker thread calls the [**CAMSchedule::GetEvent**](camschedule-getevent.md) method to retrieve an event handle from the scheduler.</span></span> <span data-ttu-id="16f27-130">Он ждет от этого события, исходя из неограниченного времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="16f27-130">It waits on this event, initially with an infinite time-out.</span></span>
3.  <span data-ttu-id="16f27-131">Чтобы запланировать новый запрос advise, часы вызывают метод [**камсчедуле:: аддадвисепаккет**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="16f27-131">To schedule a new advise request, the clock calls the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span> <span data-ttu-id="16f27-132">Запрос на выadvise может быть одним или несколькими снимками.</span><span class="sxs-lookup"><span data-stu-id="16f27-132">An advise request can be one-shot or periodic.</span></span> <span data-ttu-id="16f27-133">Планировщик сохраняет список запросов в нужном порядке времени.</span><span class="sxs-lookup"><span data-stu-id="16f27-133">The scheduler keeps the list of requests in time order.</span></span>
4.  <span data-ttu-id="16f27-134">Если запрос добавляется в начало списка, планировщик сигнализирует о событии.</span><span class="sxs-lookup"><span data-stu-id="16f27-134">If a request is added to the front of the list, the scheduler signals the event.</span></span> <span data-ttu-id="16f27-135">(Сначала список пуст, поэтому первый запрос гарантированно сигнализирует о событии.)</span><span class="sxs-lookup"><span data-stu-id="16f27-135">(The list is empty at first, so the first request is guaranteed to signal the event.)</span></span>
5.  <span data-ttu-id="16f27-136">Когда событие получает сигнал, Рабочий поток вызывает метод [**камсчедуле:: Advise**](camschedule-advise.md) , указывая текущее время ссылки.</span><span class="sxs-lookup"><span data-stu-id="16f27-136">When the event is signaled, the worker thread calls the [**CAMSchedule::Advise**](camschedule-advise.md) method, specifying the current reference time.</span></span> <span data-ttu-id="16f27-137">Если срок действия ожидающих запросов истек, планировщик отправляет их.</span><span class="sxs-lookup"><span data-stu-id="16f27-137">If any pending requests have expired, the scheduler dispatches them.</span></span>
6.  <span data-ttu-id="16f27-138">Метод advise Возвращает время следующего запроса.</span><span class="sxs-lookup"><span data-stu-id="16f27-138">The Advise method returns the time of the next request.</span></span> <span data-ttu-id="16f27-139">Рабочий поток использует это значение для вычисления нового значения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="16f27-139">The worker thread uses this value to calculate a new time-out value.</span></span>
7.  <span data-ttu-id="16f27-140">Шаги 2 6 повторяются бессрочно.</span><span class="sxs-lookup"><span data-stu-id="16f27-140">Steps 2 6 repeat indefinitely.</span></span>
8.  <span data-ttu-id="16f27-141">Для завершения рабочего потока часы задают внутренний флаг и сигнализирует о событии.</span><span class="sxs-lookup"><span data-stu-id="16f27-141">To terminate the worker thread, the clock sets an internal flag and signals the event.</span></span>

<span data-ttu-id="16f27-142">На шаге 2 событие получает сигнал или время ожидания истекает. Если событие имеет сигнальное значение, это означает, что новый запрос был добавлен в начало списка.</span><span class="sxs-lookup"><span data-stu-id="16f27-142">In step 2, either the event is signaled, or the wait times out. If the event is signaled, it means that a new request was added to the front of the list.</span></span> <span data-ttu-id="16f27-143">Рабочий поток должен вычислить новое значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="16f27-143">The worker thread must calculate a new time-out value.</span></span> <span data-ttu-id="16f27-144">С другой стороны, если время ожидания истекло, это означает, что запрос на рекомендацию пришел к оплате и должен быть отправлен.</span><span class="sxs-lookup"><span data-stu-id="16f27-144">On the other hand, if the wait times out, it means that an advise request has come due and must be dispatched.</span></span> <span data-ttu-id="16f27-145">Вызов инструкции advise на шаге 5 обрабатывает оба варианта.</span><span class="sxs-lookup"><span data-stu-id="16f27-145">The call to Advise in step 5 handles both cases.</span></span>

## <a name="requirements"></a><span data-ttu-id="16f27-146">Требования</span><span class="sxs-lookup"><span data-stu-id="16f27-146">Requirements</span></span>



| <span data-ttu-id="16f27-147">Требование</span><span class="sxs-lookup"><span data-stu-id="16f27-147">Requirement</span></span> | <span data-ttu-id="16f27-148">Значение</span><span class="sxs-lookup"><span data-stu-id="16f27-148">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16f27-149">Header</span><span class="sxs-lookup"><span data-stu-id="16f27-149">Header</span></span><br/>  | <dl> <span data-ttu-id="16f27-150"><dt>Дссчедуле. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16f27-150"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="16f27-151">Библиотека</span><span class="sxs-lookup"><span data-stu-id="16f27-151">Library</span></span><br/> | <dl> <span data-ttu-id="16f27-152"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="16f27-152"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




