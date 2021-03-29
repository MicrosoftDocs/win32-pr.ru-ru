---
description: Класс Ксаурцестреам предоставляет выходной ПИН-код для класса фильтра Ксаурце.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: Класс Ксаурцестреам (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36b9085df8c15e765c751be8b5fcdfd4f4a02140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675911"
---
# <a name="csourcestream-class"></a><span data-ttu-id="143a2-103">Класс Ксаурцестреам</span><span class="sxs-lookup"><span data-stu-id="143a2-103">CSourceStream class</span></span>

![Иерархия классов ксаурцестреам](images/source02.png)

<span data-ttu-id="143a2-105">Класс **ксаурцестреам** предоставляет выходной ПИН-код для класса фильтра [**ксаурце**](csource.md) .</span><span class="sxs-lookup"><span data-stu-id="143a2-105">The **CSourceStream** class provides an output pin for the [**CSource**](csource.md) filter class.</span></span>

<span data-ttu-id="143a2-106">Сведения об использовании этого класса см. в разделе [**ксаурце**](csource.md).</span><span class="sxs-lookup"><span data-stu-id="143a2-106">For information on using this class, see [**CSource**](csource.md).</span></span> <span data-ttu-id="143a2-107">Этот класс наследует класс [**камсреад**](camthread.md) , который предоставляет рабочий поток для потоковой передачи данных из ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="143a2-107">This class inherits the [**CAMThread**](camthread.md) class, which provides a worker thread for streaming data from the pin.</span></span> <span data-ttu-id="143a2-108">Класс **ксаурцестреам** реализует следующие вспомогательные методы для отправки запросов в поток:</span><span class="sxs-lookup"><span data-stu-id="143a2-108">The **CSourceStream** class implements the following helper methods to send requests to the thread:</span></span>

-   [<span data-ttu-id="143a2-109">**Ксаурцестреам:: Exit**</span><span class="sxs-lookup"><span data-stu-id="143a2-109">**CSourceStream::Exit**</span></span>](csourcestream-exit.md)
-   [<span data-ttu-id="143a2-110">**Ксаурцестреам:: init**</span><span class="sxs-lookup"><span data-stu-id="143a2-110">**CSourceStream::Init**</span></span>](csourcestream-init.md)
-   [<span data-ttu-id="143a2-111">**Ксаурцестреам::P Аусе**</span><span class="sxs-lookup"><span data-stu-id="143a2-111">**CSourceStream::Pause**</span></span>](csourcestream-pause.md)
-   [<span data-ttu-id="143a2-112">**Ксаурцестреам:: Run**</span><span class="sxs-lookup"><span data-stu-id="143a2-112">**CSourceStream::Run**</span></span>](csourcestream-run.md)
-   [<span data-ttu-id="143a2-113">**Ксаурцестреам:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="143a2-113">**CSourceStream::Stop**</span></span>](csourcestream-stop.md)

<span data-ttu-id="143a2-114">Первый запрос к потоку должен иметь значение [**init**](csourcestream-init.md).</span><span class="sxs-lookup"><span data-stu-id="143a2-114">The first request to the thread must be [**Init**](csourcestream-init.md).</span></span> <span data-ttu-id="143a2-115">Запрос на [**выход**](csourcestream-exit.md) завершает поток.</span><span class="sxs-lookup"><span data-stu-id="143a2-115">The [**Exit**](csourcestream-exit.md) request terminates the thread.</span></span> <span data-ttu-id="143a2-116">На практике необязательно вызывать ни один из этих методов напрямую, так как методы закрепления [**ксаурцестреам:: Active**](csourcestream-active.md) и [**Ксаурцестреам:: Inactive**](csourcestream-inactive.md) вызывают их по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="143a2-116">In practice, it is not necessary to call any of these methods directly, because the pin's [**CSourceStream::Active**](csourcestream-active.md) and [**CSourceStream::Inactive**](csourcestream-inactive.md) methods call them as needed.</span></span>

<span data-ttu-id="143a2-117">Класс также предоставляет несколько методов "handler":</span><span class="sxs-lookup"><span data-stu-id="143a2-117">The class also provides several "handler" methods:</span></span>

-   [<span data-ttu-id="143a2-118">**Ксаурцестреам:: Онсреадкреате**</span><span class="sxs-lookup"><span data-stu-id="143a2-118">**CSourceStream::OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)
-   [<span data-ttu-id="143a2-119">**Ксаурцестреам:: Онсреаддестрой**</span><span class="sxs-lookup"><span data-stu-id="143a2-119">**CSourceStream::OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)
-   [<span data-ttu-id="143a2-120">**Ксаурцестреам:: Онсреадстартплай**</span><span class="sxs-lookup"><span data-stu-id="143a2-120">**CSourceStream::OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)

<span data-ttu-id="143a2-121">Они не выполняют никаких действий в базовом классе, но производный класс может переопределять их.</span><span class="sxs-lookup"><span data-stu-id="143a2-121">These do nothing in the base class, but the derived class can override them.</span></span>



| <span data-ttu-id="143a2-122">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="143a2-122">Protected Member Variables</span></span>                                             | <span data-ttu-id="143a2-123">Описание</span><span class="sxs-lookup"><span data-stu-id="143a2-123">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="143a2-124">**m \_ пфилтер**</span><span class="sxs-lookup"><span data-stu-id="143a2-124">**m\_pFilter**</span></span>](csourcestream-m-pfilter.md)                          | <span data-ttu-id="143a2-125">Указатель на фильтр, содержащий этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="143a2-125">Pointer to the filter that contains this pin.</span></span>                                                                                     |
| <span data-ttu-id="143a2-126">Защищенные методы</span><span class="sxs-lookup"><span data-stu-id="143a2-126">Protected Methods</span></span>                                                      | <span data-ttu-id="143a2-127">Описание</span><span class="sxs-lookup"><span data-stu-id="143a2-127">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="143a2-128">**онсреадкреате**</span><span class="sxs-lookup"><span data-stu-id="143a2-128">**OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)                 | <span data-ttu-id="143a2-129">Вызывается при инициализации потока потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="143a2-129">Called when the streaming thread is initialized.</span></span> <span data-ttu-id="143a2-130">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="143a2-130">Virtual.</span></span>                                                                         |
| [<span data-ttu-id="143a2-131">**онсреаддестрой**</span><span class="sxs-lookup"><span data-stu-id="143a2-131">**OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)               | <span data-ttu-id="143a2-132">Вызывается, когда поток потоковой передачи собирается завершить работу.</span><span class="sxs-lookup"><span data-stu-id="143a2-132">Called when the streaming thread is about to exit.</span></span> <span data-ttu-id="143a2-133">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="143a2-133">Virtual.</span></span>                                                                       |
| [<span data-ttu-id="143a2-134">**онсреадстартплай**</span><span class="sxs-lookup"><span data-stu-id="143a2-134">**OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)           | <span data-ttu-id="143a2-135">Вызывается в начале метода [**ксаурцестреам::D обуфферпроцессинглуп**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="143a2-135">Called at the start of the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="143a2-136">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="143a2-136">Virtual.</span></span> |
| [<span data-ttu-id="143a2-137">**Активна**</span><span class="sxs-lookup"><span data-stu-id="143a2-137">**Active**</span></span>](csourcestream-active.md)                                 | <span data-ttu-id="143a2-138">Уведомляет ПИН-код о том, что фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="143a2-138">Notifies the pin that the filter is now active.</span></span>                                                                                   |
| [<span data-ttu-id="143a2-139">**Неактивно**</span><span class="sxs-lookup"><span data-stu-id="143a2-139">**Inactive**</span></span>](csourcestream-inactive.md)                             | <span data-ttu-id="143a2-140">Уведомляет ПИН-код о том, что фильтр больше не активен.</span><span class="sxs-lookup"><span data-stu-id="143a2-140">Notifies the pin that the filter is no longer active.</span></span>                                                                             |
| [<span data-ttu-id="143a2-141">**Запрос на**</span><span class="sxs-lookup"><span data-stu-id="143a2-141">**GetRequest**</span></span>](csourcestream-getrequest.md)                         | <span data-ttu-id="143a2-142">Ожидает следующий запрос потока.</span><span class="sxs-lookup"><span data-stu-id="143a2-142">Waits for the next thread request.</span></span>                                                                                                |
| [<span data-ttu-id="143a2-143">**чеккрекуест**</span><span class="sxs-lookup"><span data-stu-id="143a2-143">**CheckRequest**</span></span>](csourcestream-checkrequest.md)                     | <span data-ttu-id="143a2-144">Проверяет наличие запроса потока без блокировки.</span><span class="sxs-lookup"><span data-stu-id="143a2-144">Checks if there is a thread request, without blocking.</span></span>                                                                            |
| [<span data-ttu-id="143a2-145">**среадпрок**</span><span class="sxs-lookup"><span data-stu-id="143a2-145">**ThreadProc**</span></span>](csourcestream-threadproc.md)                         | <span data-ttu-id="143a2-146">Потоковая процедура.</span><span class="sxs-lookup"><span data-stu-id="143a2-146">Thread procedure.</span></span> <span data-ttu-id="143a2-147">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="143a2-147">Virtual.</span></span>                                                                                                        |
| [<span data-ttu-id="143a2-148">**добуфферпроцессинглуп**</span><span class="sxs-lookup"><span data-stu-id="143a2-148">**DoBufferProcessingLoop**</span></span>](csourcestream-dobufferprocessingloop.md) | <span data-ttu-id="143a2-149">Создает данные мультимедиа и доставляет их в нисходящий входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="143a2-149">Generates media data and delivers it to the downstream input pin.</span></span> <span data-ttu-id="143a2-150">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="143a2-150">Virtual.</span></span>                                                        |
| [<span data-ttu-id="143a2-151">**чеккмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="143a2-151">**CheckMediaType**</span></span>](csourcestream-checkmediatype.md)                 | <span data-ttu-id="143a2-152">Определяет, принимает ли ПИН-код конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="143a2-152">Determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="143a2-153">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="143a2-153">Virtual.</span></span>                                                                     |
| [<span data-ttu-id="143a2-154">**жетмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="143a2-154">**GetMediaType**</span></span>](csourcestream-getmediatype.md)                     | <span data-ttu-id="143a2-155">Извлекает предпочтительный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="143a2-155">Retrieves a preferred media type.</span></span> <span data-ttu-id="143a2-156">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="143a2-156">Virtual.</span></span>                                                                                        |
| <span data-ttu-id="143a2-157">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="143a2-157">Public Methods</span></span>                                                         | <span data-ttu-id="143a2-158">Описание</span><span class="sxs-lookup"><span data-stu-id="143a2-158">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="143a2-159">**ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="143a2-159">**CSourceStream**</span></span>](csourcestream-csourcestream.md)                   | <span data-ttu-id="143a2-160">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="143a2-160">Constructor method.</span></span>                                                                                                               |
| [<span data-ttu-id="143a2-161">**~ Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="143a2-161">**~ CSourceStream**</span></span>](csourcestream--csourcestream.md)                | <span data-ttu-id="143a2-162">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="143a2-162">Destructor method.</span></span> <span data-ttu-id="143a2-163">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="143a2-163">Virtual.</span></span>                                                                                                       |
| [<span data-ttu-id="143a2-164">**Ini**</span><span class="sxs-lookup"><span data-stu-id="143a2-164">**Init**</span></span>](csourcestream-init.md)                                     | <span data-ttu-id="143a2-165">Инициализирует поток потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="143a2-165">Initializes the streaming thread.</span></span>                                                                                                 |
| [<span data-ttu-id="143a2-166">**Выход**</span><span class="sxs-lookup"><span data-stu-id="143a2-166">**Exit**</span></span>](csourcestream-exit.md)                                     | <span data-ttu-id="143a2-167">Сообщает потоку потоковой передачи о выходе.</span><span class="sxs-lookup"><span data-stu-id="143a2-167">Signals the streaming thread to exit.</span></span>                                                                                             |
| [<span data-ttu-id="143a2-168">**Выполнить**</span><span class="sxs-lookup"><span data-stu-id="143a2-168">**Run**</span></span>](csourcestream-run.md)                                       | <span data-ttu-id="143a2-169">Сообщает потоку потоковой передачи о выполнении.</span><span class="sxs-lookup"><span data-stu-id="143a2-169">Signals the streaming thread to run.</span></span>                                                                                              |
| [<span data-ttu-id="143a2-170">**Пауза**</span><span class="sxs-lookup"><span data-stu-id="143a2-170">**Pause**</span></span>](csourcestream-pause.md)                                   | <span data-ttu-id="143a2-171">Сигнализирует потоку потоковой передачи на активность.</span><span class="sxs-lookup"><span data-stu-id="143a2-171">Signals the streaming thread to become active.</span></span>                                                                                    |
| [<span data-ttu-id="143a2-172">**Stop**</span><span class="sxs-lookup"><span data-stu-id="143a2-172">**Stop**</span></span>](csourcestream-stop.md)                                     | <span data-ttu-id="143a2-173">Сигнализирует потоку потоковой передачи на завершение.</span><span class="sxs-lookup"><span data-stu-id="143a2-173">Signals the streaming thread to stop.</span></span>                                                                                             |
| <span data-ttu-id="143a2-174">Чистые виртуальные методы</span><span class="sxs-lookup"><span data-stu-id="143a2-174">Pure Virtual Methods</span></span>                                                   | <span data-ttu-id="143a2-175">Описание</span><span class="sxs-lookup"><span data-stu-id="143a2-175">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="143a2-176">**филлбуффер**</span><span class="sxs-lookup"><span data-stu-id="143a2-176">**FillBuffer**</span></span>](csourcestream-fillbuffer.md)                         | <span data-ttu-id="143a2-177">Заполняет образец носителя данными.</span><span class="sxs-lookup"><span data-stu-id="143a2-177">Fills a media sample with data.</span></span>                                                                                                   |
| <span data-ttu-id="143a2-178">Методы Ипин</span><span class="sxs-lookup"><span data-stu-id="143a2-178">IPin Methods</span></span>                                                           | <span data-ttu-id="143a2-179">Описание</span><span class="sxs-lookup"><span data-stu-id="143a2-179">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="143a2-180">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="143a2-180">**QueryId**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | <span data-ttu-id="143a2-181">Возвращает идентификатор для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="143a2-181">Retrieves an identifier for the pin.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="143a2-182">Требования</span><span class="sxs-lookup"><span data-stu-id="143a2-182">Requirements</span></span>



| <span data-ttu-id="143a2-183">Требование</span><span class="sxs-lookup"><span data-stu-id="143a2-183">Requirement</span></span> | <span data-ttu-id="143a2-184">Значение</span><span class="sxs-lookup"><span data-stu-id="143a2-184">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="143a2-185">Header</span><span class="sxs-lookup"><span data-stu-id="143a2-185">Header</span></span><br/>  | <dl> <span data-ttu-id="143a2-186"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="143a2-186"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="143a2-187">Библиотека</span><span class="sxs-lookup"><span data-stu-id="143a2-187">Library</span></span><br/> | <dl> <span data-ttu-id="143a2-188"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="143a2-188"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="143a2-189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="143a2-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="143a2-190">Запись фильтров источника</span><span class="sxs-lookup"><span data-stu-id="143a2-190">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




