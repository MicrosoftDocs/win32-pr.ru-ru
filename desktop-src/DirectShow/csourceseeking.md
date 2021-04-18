---
description: Класс Ксаурцесикинг является абстрактным классом для реализации поиска в фильтрах источников с одним выходным закреплением.
ms.assetid: 46e711e1-78d4-4e83-9df1-06032edeba6a
title: Класс Ксаурцесикинг (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf9bf0ca0fabd00c27f4ef4b795af5271605fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688933"
---
# <a name="csourceseeking-class"></a><span data-ttu-id="ed612-103">Класс Ксаурцесикинг</span><span class="sxs-lookup"><span data-stu-id="ed612-103">CSourceSeeking class</span></span>

![Иерархия классов ксаурцесикинг](images/cutil15.png)

<span data-ttu-id="ed612-105">Класс **ксаурцесикинг** является абстрактным классом для реализации поиска в фильтрах источников с одним выходным закреплением.</span><span class="sxs-lookup"><span data-stu-id="ed612-105">The **CSourceSeeking** class is an abstract class for implementing seeking in source filters with one output pin.</span></span>

<span data-ttu-id="ed612-106">Этот класс поддерживает интерфейс [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="ed612-106">This class supports the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="ed612-107">Он предоставляет реализации по умолчанию для всех методов **имедиасикинг** .</span><span class="sxs-lookup"><span data-stu-id="ed612-107">It provides default implementations for all of the **IMediaSeeking** methods.</span></span> <span data-ttu-id="ed612-108">Защищенные переменные членов хранят время начала, время окончания и текущую скорость.</span><span class="sxs-lookup"><span data-stu-id="ed612-108">Protected member variables store the start time, stop time, and current rate.</span></span> <span data-ttu-id="ed612-109">По умолчанию в качестве формата времени, поддерживаемого классом, используется **\_ Формат времени \_ носителя \_** (100-наносекундных единиц).</span><span class="sxs-lookup"><span data-stu-id="ed612-109">By default, the only time format supported by the class is **TIME\_FORMAT\_MEDIA\_TIME** (100-nanosecond units).</span></span> <span data-ttu-id="ed612-110">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="ed612-110">See Remarks for more information.</span></span>



| <span data-ttu-id="ed612-111">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="ed612-111">Protected Member Variables</span></span>                                          | <span data-ttu-id="ed612-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ed612-112">Description</span></span>                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed612-113">**m \_ ртдуратион**</span><span class="sxs-lookup"><span data-stu-id="ed612-113">**m\_rtDuration**</span></span>](csourceseeking-m-rtduration.md)                | <span data-ttu-id="ed612-114">Длительность потока.</span><span class="sxs-lookup"><span data-stu-id="ed612-114">Duration of the stream.</span></span>                                                                     |
| [<span data-ttu-id="ed612-115">**m \_ ртстарт**</span><span class="sxs-lookup"><span data-stu-id="ed612-115">**m\_rtStart**</span></span>](csourceseeking-m-rtstart.md)                      | <span data-ttu-id="ed612-116">Время начала.</span><span class="sxs-lookup"><span data-stu-id="ed612-116">Start time.</span></span>                                                                                 |
| [<span data-ttu-id="ed612-117">**m \_ ртстоп**</span><span class="sxs-lookup"><span data-stu-id="ed612-117">**m\_rtStop**</span></span>](csourceseeking-m-rtstop.md)                        | <span data-ttu-id="ed612-118">Время окончания.</span><span class="sxs-lookup"><span data-stu-id="ed612-118">Stop time.</span></span>                                                                                  |
| [<span data-ttu-id="ed612-119">**m \_ дратесикинг**</span><span class="sxs-lookup"><span data-stu-id="ed612-119">**m\_dRateSeeking**</span></span>](csourceseeking-m-drateseeking.md)            | <span data-ttu-id="ed612-120">Скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ed612-120">Playback rate.</span></span>                                                                              |
| [<span data-ttu-id="ed612-121">**m \_ двсикингкапс**</span><span class="sxs-lookup"><span data-stu-id="ed612-121">**m\_dwSeekingCaps**</span></span>](csourceseeking-m-dwseekingcaps.md)          | <span data-ttu-id="ed612-122">Поиск возможностей.</span><span class="sxs-lookup"><span data-stu-id="ed612-122">Seeking capabilities.</span></span>                                                                       |
| [<span data-ttu-id="ed612-123">**m \_ плокк**</span><span class="sxs-lookup"><span data-stu-id="ed612-123">**m\_pLock**</span></span>](csourceseeking-m-plock.md)                          | <span data-ttu-id="ed612-124">Указатель на объект критической секции для блокировки.</span><span class="sxs-lookup"><span data-stu-id="ed612-124">Pointer to a critical section object for locking.</span></span>                                           |
| <span data-ttu-id="ed612-125">Защищенные методы</span><span class="sxs-lookup"><span data-stu-id="ed612-125">Protected Methods</span></span>                                                   | <span data-ttu-id="ed612-126">Описание</span><span class="sxs-lookup"><span data-stu-id="ed612-126">Description</span></span>                                                                                 |
| [<span data-ttu-id="ed612-127">**ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="ed612-127">**CSourceSeeking**</span></span>](csourceseeking-csourceseeking.md)             | <span data-ttu-id="ed612-128">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="ed612-128">Constructor method.</span></span>                                                                         |
| <span data-ttu-id="ed612-129">Чистые виртуальные методы</span><span class="sxs-lookup"><span data-stu-id="ed612-129">Pure Virtual Methods</span></span>                                                | <span data-ttu-id="ed612-130">Описание</span><span class="sxs-lookup"><span data-stu-id="ed612-130">Description</span></span>                                                                                 |
| [<span data-ttu-id="ed612-131">**чанжерате**</span><span class="sxs-lookup"><span data-stu-id="ed612-131">**ChangeRate**</span></span>](csourceseeking-changerate.md)                     | <span data-ttu-id="ed612-132">Вызывается при изменении частоты воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ed612-132">Called when the playback rate changes.</span></span>                                                      |
| [<span data-ttu-id="ed612-133">**чанжестарт**</span><span class="sxs-lookup"><span data-stu-id="ed612-133">**ChangeStart**</span></span>](csourceseeking-changestart.md)                   | <span data-ttu-id="ed612-134">Вызывается при изменении начальной должности.</span><span class="sxs-lookup"><span data-stu-id="ed612-134">Called when the start position changes.</span></span>                                                     |
| [<span data-ttu-id="ed612-135">**чанжестоп**</span><span class="sxs-lookup"><span data-stu-id="ed612-135">**ChangeStop**</span></span>](csourceseeking-changestop.md)                     | <span data-ttu-id="ed612-136">Вызывается при изменении позиции окончания.</span><span class="sxs-lookup"><span data-stu-id="ed612-136">Called when the stop position changes.</span></span>                                                      |
| <span data-ttu-id="ed612-137">Методы Имедиасикинг</span><span class="sxs-lookup"><span data-stu-id="ed612-137">IMediaSeeking Methods</span></span>                                               | <span data-ttu-id="ed612-138">Описание</span><span class="sxs-lookup"><span data-stu-id="ed612-138">Description</span></span>                                                                                 |
| [<span data-ttu-id="ed612-139">**исформатсуппортед**</span><span class="sxs-lookup"><span data-stu-id="ed612-139">**IsFormatSupported**</span></span>](csourceseeking-isformatsupported.md)       | <span data-ttu-id="ed612-140">Определяет, поддерживается ли указанный формат времени.</span><span class="sxs-lookup"><span data-stu-id="ed612-140">Determines whether a specified time format is supported.</span></span>                                    |
| [<span data-ttu-id="ed612-141">**куерипреферредформат**</span><span class="sxs-lookup"><span data-stu-id="ed612-141">**QueryPreferredFormat**</span></span>](csourceseeking-querypreferredformat.md) | <span data-ttu-id="ed612-142">Возвращает предпочтительный формат времени объекта.</span><span class="sxs-lookup"><span data-stu-id="ed612-142">Retrieves the object's preferred time format.</span></span>                                               |
| [<span data-ttu-id="ed612-143">**сеттимеформат**</span><span class="sxs-lookup"><span data-stu-id="ed612-143">**SetTimeFormat**</span></span>](csourceseeking-settimeformat.md)               | <span data-ttu-id="ed612-144">Задает формат времени.</span><span class="sxs-lookup"><span data-stu-id="ed612-144">Sets the time format.</span></span>                                                                       |
| [<span data-ttu-id="ed612-145">**исусингтимеформат**</span><span class="sxs-lookup"><span data-stu-id="ed612-145">**IsUsingTimeFormat**</span></span>](csourceseeking-isusingtimeformat.md)       | <span data-ttu-id="ed612-146">Определяет, является ли указанный формат времени используемым в данный момент форматом.</span><span class="sxs-lookup"><span data-stu-id="ed612-146">Determines whether a specified time format is the format currently in use.</span></span>                  |
| [<span data-ttu-id="ed612-147">**жеттимеформат**</span><span class="sxs-lookup"><span data-stu-id="ed612-147">**GetTimeFormat**</span></span>](csourceseeking-gettimeformat.md)               | <span data-ttu-id="ed612-148">Извлекает текущий формат времени.</span><span class="sxs-lookup"><span data-stu-id="ed612-148">Retrieves the current time format.</span></span>                                                          |
| [<span data-ttu-id="ed612-149">**Длительное время**</span><span class="sxs-lookup"><span data-stu-id="ed612-149">**GetDuration**</span></span>](csourceseeking-getduration.md)                   | <span data-ttu-id="ed612-150">Возвращает длительность потока.</span><span class="sxs-lookup"><span data-stu-id="ed612-150">Retrieves the duration of the stream.</span></span>                                                       |
| [<span data-ttu-id="ed612-151">**жетстоппоситион**</span><span class="sxs-lookup"><span data-stu-id="ed612-151">**GetStopPosition**</span></span>](csourceseeking-getstopposition.md)           | <span data-ttu-id="ed612-152">Возвращает время, когда воспроизведение будет прервано относительно длительности потока.</span><span class="sxs-lookup"><span data-stu-id="ed612-152">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> |
| [<span data-ttu-id="ed612-153">**жеткуррентпоситион**</span><span class="sxs-lookup"><span data-stu-id="ed612-153">**GetCurrentPosition**</span></span>](csourceseeking-getcurrentposition.md)     | <span data-ttu-id="ed612-154">Извлекает текущую координату относительно общей продолжительности потока.</span><span class="sxs-lookup"><span data-stu-id="ed612-154">Retrieves the current position, relative to the total duration of the stream.</span></span>               |
| [<span data-ttu-id="ed612-155">**Возможности**</span><span class="sxs-lookup"><span data-stu-id="ed612-155">**GetCapabilities**</span></span>](csourceseeking-getcapabilities.md)           | <span data-ttu-id="ed612-156">Извлекает все возможности поиска в потоке.</span><span class="sxs-lookup"><span data-stu-id="ed612-156">Retrieves all the seeking capabilities of the stream.</span></span>                                       |
| [<span data-ttu-id="ed612-157">**чекккапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="ed612-157">**CheckCapabilities**</span></span>](csourceseeking-checkcapabilities.md)       | <span data-ttu-id="ed612-158">Запрашивает, имеет ли поток указанные возможности поиска.</span><span class="sxs-lookup"><span data-stu-id="ed612-158">Queries whether the stream has specified seeking capabilities.</span></span>                              |
| [<span data-ttu-id="ed612-159">**конверттимеформат**</span><span class="sxs-lookup"><span data-stu-id="ed612-159">**ConvertTimeFormat**</span></span>](csourceseeking-converttimeformat.md)       | <span data-ttu-id="ed612-160">Преобразует из одного формата времени в другой.</span><span class="sxs-lookup"><span data-stu-id="ed612-160">Converts from one time format to another.</span></span>                                                   |
| [<span data-ttu-id="ed612-161">**сетпоситионс**</span><span class="sxs-lookup"><span data-stu-id="ed612-161">**SetPositions**</span></span>](csourceseeking-setpositions.md)                 | <span data-ttu-id="ed612-162">Установка текущей позиции и позиции окончания.</span><span class="sxs-lookup"><span data-stu-id="ed612-162">Sets the current position and the stop position.</span></span>                                            |
| [<span data-ttu-id="ed612-163">**Выстановки**</span><span class="sxs-lookup"><span data-stu-id="ed612-163">**GetPositions**</span></span>](csourceseeking-getpositions.md)                 | <span data-ttu-id="ed612-164">Извлекает текущую и заданную позиции.</span><span class="sxs-lookup"><span data-stu-id="ed612-164">Retrieves the current position and the stop position.</span></span>                                       |
| [<span data-ttu-id="ed612-165">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="ed612-165">**GetAvailable**</span></span>](csourceseeking-getavailable.md)                 | <span data-ttu-id="ed612-166">Извлекает диапазон времени, в течение которого поиск является эффективным.</span><span class="sxs-lookup"><span data-stu-id="ed612-166">Retrieves the range of times in which seeking is efficient.</span></span>                                 |
| [<span data-ttu-id="ed612-167">**сетрате**</span><span class="sxs-lookup"><span data-stu-id="ed612-167">**SetRate**</span></span>](csourceseeking-setrate.md)                           | <span data-ttu-id="ed612-168">Задает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ed612-168">Sets the playback rate.</span></span>                                                                     |
| [<span data-ttu-id="ed612-169">**Коэффициент**</span><span class="sxs-lookup"><span data-stu-id="ed612-169">**GetRate**</span></span>](csourceseeking-getrate.md)                           | <span data-ttu-id="ed612-170">Возвращает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ed612-170">Retrieves the playback rate.</span></span>                                                                |
| [<span data-ttu-id="ed612-171">**жетпреролл**</span><span class="sxs-lookup"><span data-stu-id="ed612-171">**GetPreroll**</span></span>](csourceseeking-getpreroll.md)                     | <span data-ttu-id="ed612-172">Извлекает время предвремени.</span><span class="sxs-lookup"><span data-stu-id="ed612-172">Retrieves the preroll time.</span></span>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="ed612-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed612-173">Remarks</span></span>

<span data-ttu-id="ed612-174">При изменении начальной позиции, позиции окончания или скорости воспроизведения объект **ксаурцесикинг** вызывает соответствующий чистый виртуальный метод:</span><span class="sxs-lookup"><span data-stu-id="ed612-174">Whenever the start position, stop position, or playback rate changes, the **CSourceSeeking** object calls a corresponding pure virtual method:</span></span>

-   <span data-ttu-id="ed612-175">Начальное расположение: [ **ксаурцесикинг:: чанжестарт**](csourceseeking-changestart.md)</span><span class="sxs-lookup"><span data-stu-id="ed612-175">Start position: [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md)</span></span>
-   <span data-ttu-id="ed612-176">Позиция окончания: [ **ксаурцесикинг:: чанжестоп**](csourceseeking-changestop.md)</span><span class="sxs-lookup"><span data-stu-id="ed612-176">Stop position: [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md)</span></span>
-   <span data-ttu-id="ed612-177">Скорость воспроизведения: [ **ксаурцесикинг:: чанжерате**](csourceseeking-changerate.md)</span><span class="sxs-lookup"><span data-stu-id="ed612-177">Playback rate: [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md)</span></span>

<span data-ttu-id="ed612-178">Производный класс должен реализовывать эти методы.</span><span class="sxs-lookup"><span data-stu-id="ed612-178">The derived class must implement these methods.</span></span> <span data-ttu-id="ed612-179">После любой операции поиска фильтр должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ed612-179">After any seek operation, a filter must do the following:</span></span>

1.  <span data-ttu-id="ed612-180">Вызовите метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) для входного контакта нисходящего входа.</span><span class="sxs-lookup"><span data-stu-id="ed612-180">Call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the downstream input pin.</span></span>
2.  <span data-ttu-id="ed612-181">Остановите рабочий поток, который доставляет данные.</span><span class="sxs-lookup"><span data-stu-id="ed612-181">Halt the worker thread that is delivering data.</span></span>
3.  <span data-ttu-id="ed612-182">Вызовите метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="ed612-182">Call the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>
4.  <span data-ttu-id="ed612-183">Перезапустите рабочий поток.</span><span class="sxs-lookup"><span data-stu-id="ed612-183">Restart the worker thread.</span></span>
5.  <span data-ttu-id="ed612-184">Вызовите метод [**Ипин:: невсегмент**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="ed612-184">Call the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin.</span></span>
6.  <span data-ttu-id="ed612-185">Задайте свойство ненепрерывности в первом примере.</span><span class="sxs-lookup"><span data-stu-id="ed612-185">Set the discontinuity property on the first sample.</span></span> <span data-ttu-id="ed612-186">Вызовите метод [**имедиасампле:: сетдисконтинуити**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="ed612-186">Call the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

<span data-ttu-id="ed612-187">Вызов [**бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) освобождает рабочий поток, если поток блокируется, ожидая доставки примера.</span><span class="sxs-lookup"><span data-stu-id="ed612-187">The call to [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) frees the worker thread, if the thread is blocked waiting to deliver a sample.</span></span>

<span data-ttu-id="ed612-188">На шаге 2 Убедитесь, что поток остановил отправку данных.</span><span class="sxs-lookup"><span data-stu-id="ed612-188">In step 2, make sure that the thread has stopped sending data.</span></span> <span data-ttu-id="ed612-189">В зависимости от реализации может потребоваться подождать, пока поток завершит работу, или поток, чтобы передать ответ какого-либо типа.</span><span class="sxs-lookup"><span data-stu-id="ed612-189">Depending on the implementation, you might need to wait for the thread to exit, or for the thread to signal a response of some kind.</span></span> <span data-ttu-id="ed612-190">Если фильтр использует класс [**ксаурцестреам**](csourcestream.md) , метод [**ксаурцестреам::**](csourcestream-stop.md) End блокируется до тех пор, пока рабочий поток не ответит.</span><span class="sxs-lookup"><span data-stu-id="ed612-190">If your filter uses the [**CSourceStream**](csourcestream.md) class, the [**CSourceStream::Stop**](csourcestream-stop.md) method blocks until the worker thread replies.</span></span>

<span data-ttu-id="ed612-191">В идеале новый сегмент (шаг 5) должен быть доставлен из рабочего потока.</span><span class="sxs-lookup"><span data-stu-id="ed612-191">Ideally, the new segment (step 5) should be delivered from the worker thread.</span></span> <span data-ttu-id="ed612-192">Это также можно сделать с помощью объекта **ксаурцесикинг** , если фильтр сериализует его с помощью примеров.</span><span class="sxs-lookup"><span data-stu-id="ed612-192">It can also be done by the **CSourceSeeking** object, as long as the filter serializes it with the samples.</span></span>

<span data-ttu-id="ed612-193">В следующем примере показана возможная реализация.</span><span class="sxs-lookup"><span data-stu-id="ed612-193">The following example shows a possible implementation.</span></span> <span data-ttu-id="ed612-194">Предполагается, что выходной ПИН-код фильтра источника является производным от **ксаурцесикинг** и [**ксаурцестреам**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="ed612-194">It assumes that the source filter's output pin is derived from **CSourceSeeking** and [**CSourceStream**](csourcestream.md).</span></span> <span data-ttu-id="ed612-195">В этом примере определяется вспомогательный метод Упдатефромсик, который выполняет шаги 1 4.</span><span class="sxs-lookup"><span data-stu-id="ed612-195">This example defines a helper method, UpdateFromSeek, that performs steps 1 4.</span></span> <span data-ttu-id="ed612-196">Метод [**ксаурцестреам:: онсреадстартплай**](csourcestream-onthreadstartplay.md) переопределен для отправки нового сегмента и для установки флага, указывающего на ненепрерывность.</span><span class="sxs-lookup"><span data-stu-id="ed612-196">The [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md) method is overridden to send the new segment, and to set a flag indicating the discontinuity.</span></span> <span data-ttu-id="ed612-197">Рабочий поток выбирает этот флаг и вызывает метод [**имедиасампле:: сетдисконтинуити**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) :</span><span class="sxs-lookup"><span data-stu-id="ed612-197">The worker thread picks up this flag and calls the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method:</span></span>


```C++
void CMyStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        Stop();
        DeliverEndFlush();
        Run();
    }
}

HRESULT CMyStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



### <a name="supporting-additional-time-formats"></a><span data-ttu-id="ed612-198">Поддержка дополнительных форматов времени</span><span class="sxs-lookup"><span data-stu-id="ed612-198">Supporting Additional Time Formats</span></span>

<span data-ttu-id="ed612-199">По умолчанию этот класс поддерживает поиск только в единицах времени ссылки ( \_ Формат времени \_ носителя \_ ).</span><span class="sxs-lookup"><span data-stu-id="ed612-199">By default, this class supports seeking only in units of reference time (TIME\_FORMAT\_MEDIA\_TIME).</span></span> <span data-ttu-id="ed612-200">Для поддержки дополнительных форматов времени Переопределите методы [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , которые работают с форматами времени:</span><span class="sxs-lookup"><span data-stu-id="ed612-200">To support additional time formats, override the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods that deal with time formats:</span></span>

-   [<span data-ttu-id="ed612-201">**Имедиасикинг:: Жеттимеформат**</span><span class="sxs-lookup"><span data-stu-id="ed612-201">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="ed612-202">**Имедиасикинг:: Жеттимеформат**</span><span class="sxs-lookup"><span data-stu-id="ed612-202">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="ed612-203">**Имедиасикинг:: Исусингтимеформат**</span><span class="sxs-lookup"><span data-stu-id="ed612-203">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="ed612-204">**Имедиасикинг:: Исусингтимеформат**</span><span class="sxs-lookup"><span data-stu-id="ed612-204">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="ed612-205">**Имедиасикинг:: Сеттимеформат**</span><span class="sxs-lookup"><span data-stu-id="ed612-205">**IMediaSeeking::SetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

<span data-ttu-id="ed612-206">Кроме того, переопределите оставшиеся методы [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , чтобы выполнить необходимые преобразования между форматами времени.</span><span class="sxs-lookup"><span data-stu-id="ed612-206">In addition, override the remaining [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods to perform the necessary conversions between time formats.</span></span> <span data-ttu-id="ed612-207">После вызова метода [**сеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) все методы **имедиасикинг** должны обрабатывать входящие и исходящие параметры времени в новом формате времени.</span><span class="sxs-lookup"><span data-stu-id="ed612-207">After the [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method is called, all **IMediaSeeking** methods must treat incoming and outgoing time parameters as being in the new time format.</span></span> <span data-ttu-id="ed612-208">Например, если переменная *m \_ ртдуратион* представляет продолжительность в единицах времени ссылки, но текущий формат времени — frames [**, метод IsReference**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) должен возвращать значение *m \_ ртдуратион* , преобразованное в кадры.</span><span class="sxs-lookup"><span data-stu-id="ed612-208">For example, if the *m\_rtDuration* variable represents the duration in units of reference time, but the current time format is frames, then the [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method must return the value *m\_rtDuration* converted to frames.</span></span> <span data-ttu-id="ed612-209">Пример:</span><span class="sxs-lookup"><span data-stu-id="ed612-209">For example:</span></span>


```
STDMETHODIMP GetDuration(LONGLONG *pDuration)
{
    HRESULT hr = CSourceSeeking::GetDuration(pDuration);
    if (SUCCEEDED(hr))
    {
        if (m_TimeFormat == TIME_FORMAT_FRAME)
        {
            // Convert from reference time to frames.
            *pDuration = TimeToFrame(*pDuration);  // Private method.
        }
    }
    return hr
} 
```



<span data-ttu-id="ed612-210">Кроме того, убедитесь в том, что в \_ \_ методе [**Имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) установлен флаг "я искал ретурнтиме".</span><span class="sxs-lookup"><span data-stu-id="ed612-210">Also, make sure to check for the AM\_SEEKING\_ReturnTime flag in the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span> <span data-ttu-id="ed612-211">Если этот флаг существует, при возврате значений позиций в вызывающий объект преобразуйте их в время ссылки.</span><span class="sxs-lookup"><span data-stu-id="ed612-211">If this flag is present, convert the position values into reference times when you return them to the caller.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed612-212">Требования</span><span class="sxs-lookup"><span data-stu-id="ed612-212">Requirements</span></span>



| <span data-ttu-id="ed612-213">Требование</span><span class="sxs-lookup"><span data-stu-id="ed612-213">Requirement</span></span> | <span data-ttu-id="ed612-214">Значение</span><span class="sxs-lookup"><span data-stu-id="ed612-214">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed612-215">Header</span><span class="sxs-lookup"><span data-stu-id="ed612-215">Header</span></span><br/>  | <dl> <span data-ttu-id="ed612-216"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed612-216"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ed612-217">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ed612-217">Library</span></span><br/> | <dl> <span data-ttu-id="ed612-218"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ed612-218"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed612-219">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed612-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed612-220">Поддержка поиска в фильтре источника</span><span class="sxs-lookup"><span data-stu-id="ed612-220">Supporting Seeking in a Source Filter</span></span>](supporting-seeking-in-a-source-filter.md)
</dt> </dl>

 

 




