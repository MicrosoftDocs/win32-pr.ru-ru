---
description: Класс Кпоспасссру обрабатывает команды Seek для фильтров преобразования, передавая их в следующий фильтр.
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: Класс Кпоспасссру (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77bd8adfac5d609af356f7cef0a5da086c052b8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668575"
---
# <a name="cpospassthru-class"></a><span data-ttu-id="e5290-103">Класс Кпоспасссру</span><span class="sxs-lookup"><span data-stu-id="e5290-103">CPosPassThru class</span></span>

![Иерархия базового класса кпоспасссру](images/cutil14.png)

<span data-ttu-id="e5290-105">`CPosPassThru`Класс обрабатывает команды Seek для фильтров преобразования, передавая их в следующий фильтр.</span><span class="sxs-lookup"><span data-stu-id="e5290-105">The `CPosPassThru` class handles seek commands for transform filters, by passing them upstream to the next filter.</span></span>

<span data-ttu-id="e5290-106">Когда приложение выполняет поиск графа фильтра, диспетчер графа фильтров передает команду Seek фильтрам модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="e5290-106">When an application seeks the filter graph, the Filter Graph Manager gives the seek command to the renderer filters.</span></span> <span data-ttu-id="e5290-107">Команда передается в качестве выходного ПИН-кода каждого фильтра, пока не достигнет фильтра, который может выполнить команду (если она есть).</span><span class="sxs-lookup"><span data-stu-id="e5290-107">The command is passed upstream, through each filter's output pin, until it reaches a filter that can execute the command (if any).</span></span> <span data-ttu-id="e5290-108">Дополнительные сведения см. в разделе [Поиск](seeking.md).</span><span class="sxs-lookup"><span data-stu-id="e5290-108">For details, see [Seeking](seeking.md).</span></span> <span data-ttu-id="e5290-109">`CPosPassThru`Класс передает все команды поиска в выходной закрепление вышестоящего фильтра, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="e5290-109">The `CPosPassThru` class passes all seek commands to the output pin on the upstream filter, as shown in the following diagram.</span></span>

![класс кпоспасссру отправляет команды поиска в виде вышестоящего потока.](images/cpospassthru.png)

<span data-ttu-id="e5290-111">Хотя этот класс предоставляется в библиотеке базовых классов, DirectShow также предоставляет тот же класс в Quartz.dll.</span><span class="sxs-lookup"><span data-stu-id="e5290-111">Although this class is provided in the base class library, DirectShow also provides the same class in Quartz.dll.</span></span> <span data-ttu-id="e5290-112">Использование Quartz.dll версии может немного уменьшить размер кода в фильтре, так как класс загружается во время выполнения из библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="e5290-112">Using the Quartz.dll version can reduce the code size in your filter somewhat, because the class is loaded at run-time from the DLL.</span></span> <span data-ttu-id="e5290-113">Чтобы использовать эту версию, вызовите функцию [**креатепоспасссру**](createpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="e5290-113">To use that version, call the [**CreatePosPassThru**](createpospassthru.md) function.</span></span>

<span data-ttu-id="e5290-114">В методе **нонделегатингкуеринтерфаце** выходного контакта делегируйте объекту **кпоспасссру** каждый раз, когда запрошенный интерфейс является [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) или [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="e5290-114">In your output pin's **NonDelegatingQueryInterface** method, delegate to the **CPosPassThru** object whenever the requested interface is [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) or [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), as shown in the following code:</span></span>


```
// The following member variables are assumed:
IPin *m_pInput;    // Pointer to the input pin on your filter.
IUnknown *m_pPos;  // Pointer to the CPosPassThru object.

STDMETHODIMP CMyPin::NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    HRESULT hr
    if (riid == IID_IMediaPosition || riid == IID_IMediaSeeking) 
    {
        if (m_pPos == NULL) 
        {
            // We have not created the CPosPassThru object yet. Do so now.
            hr = CreatePosPassThru(GetOwner(), FALSE, m_pInput, &m_pPos);
            if (FAILED(hr)) return hr;
        }
        return m_pPos->QueryInterface(riid, ppv);
    } 
    else
    {
         // Other interfaces (not shown).
    }
}

~CMyPin::CMyPin() 
{
    // Release the CPosPassThruObject.
    if (m_pPos != NULL) m_pPos->Release();
}
```



<span data-ttu-id="e5290-115">За исключением указанных случаев, все методы [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) и [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) в этом классе вызывают соответствующий метод для подключенного ПИН-кода и возвращают результат.</span><span class="sxs-lookup"><span data-stu-id="e5290-115">Except where noted, all [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods in this class call the corresponding method on the connected pin and return the result.</span></span>



| <span data-ttu-id="e5290-116">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="e5290-116">Public Methods</span></span>                                                    | <span data-ttu-id="e5290-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e5290-117">Description</span></span>                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5290-118">**кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="e5290-118">**CPosPassThru**</span></span>](cpospassthru-cpospassthru.md)                 | <span data-ttu-id="e5290-119">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="e5290-119">Constructor method.</span></span>                                                                                 |
| [<span data-ttu-id="e5290-120">**форцерефреш**</span><span class="sxs-lookup"><span data-stu-id="e5290-120">**ForceRefresh**</span></span>](cpospassthru-forcerefresh.md)                 | <span data-ttu-id="e5290-121">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="e5290-121">Obsolete.</span></span>                                                                                           |
| [<span data-ttu-id="e5290-122">**жетмедиатиме**</span><span class="sxs-lookup"><span data-stu-id="e5290-122">**GetMediaTime**</span></span>](cpospassthru-getmediatime.md)                 | <span data-ttu-id="e5290-123">Извлекает метки времени для текущего образца.</span><span class="sxs-lookup"><span data-stu-id="e5290-123">Retrieves the time stamps on the current sample.</span></span> <span data-ttu-id="e5290-124">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="e5290-124">Virtual.</span></span>                                           |
| <span data-ttu-id="e5290-125">Методы Имедиапоситион</span><span class="sxs-lookup"><span data-stu-id="e5290-125">IMediaPosition Methods</span></span>                                            | <span data-ttu-id="e5290-126">Описание</span><span class="sxs-lookup"><span data-stu-id="e5290-126">Description</span></span>                                                                                         |
| [<span data-ttu-id="e5290-127">**получить \_ Длительность**</span><span class="sxs-lookup"><span data-stu-id="e5290-127">**get\_Duration**</span></span>](cpospassthru-get-duration.md)                | <span data-ttu-id="e5290-128">Возвращает длительность потока.</span><span class="sxs-lookup"><span data-stu-id="e5290-128">Retrieves the duration of the stream.</span></span>                                                               |
| [<span data-ttu-id="e5290-129">**разместить \_ CurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="e5290-129">**put\_CurrentPosition**</span></span>](cpospassthru-put-currentposition.md)  | <span data-ttu-id="e5290-130">Задает текущую точку относительно общей продолжительности потока.</span><span class="sxs-lookup"><span data-stu-id="e5290-130">Sets the current position, relative to the total duration of the stream.</span></span>                            |
| [<span data-ttu-id="e5290-131">**получить \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="e5290-131">**get\_StopTime**</span></span>](cpospassthru-get-stoptime.md)                | <span data-ttu-id="e5290-132">Возвращает время, когда воспроизведение будет прервано относительно длительности потока.</span><span class="sxs-lookup"><span data-stu-id="e5290-132">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span>         |
| [<span data-ttu-id="e5290-133">**разместить \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="e5290-133">**put\_StopTime**</span></span>](cpospassthru-put-stoptime.md)                | <span data-ttu-id="e5290-134">Задает время, когда воспроизведение будет прервано относительно длительности потока.</span><span class="sxs-lookup"><span data-stu-id="e5290-134">Sets the time at which the playback will stop, relative to the duration of the stream.</span></span>              |
| [<span data-ttu-id="e5290-135">**получить \_ прероллтиме**</span><span class="sxs-lookup"><span data-stu-id="e5290-135">**get\_PrerollTime**</span></span>](cpospassthru-get-prerolltime.md)          | <span data-ttu-id="e5290-136">Извлекает объем данных, которые будут помещены в очередь перед начальной позицией.</span><span class="sxs-lookup"><span data-stu-id="e5290-136">Retrieves the amount of data that will be queued before the start position.</span></span>                         |
| [<span data-ttu-id="e5290-137">**разместить \_ прероллтиме**</span><span class="sxs-lookup"><span data-stu-id="e5290-137">**put\_PrerollTime**</span></span>](cpospassthru-put-prerolltime.md)          | <span data-ttu-id="e5290-138">Задает объем данных, которые будут помещены в очередь перед начальной позицией.</span><span class="sxs-lookup"><span data-stu-id="e5290-138">Sets the amount of data that will be queued before the start position.</span></span>                              |
| [<span data-ttu-id="e5290-139">**получить \_ скорость**</span><span class="sxs-lookup"><span data-stu-id="e5290-139">**get\_Rate**</span></span>](cpospassthru-get-rate.md)                        | <span data-ttu-id="e5290-140">Возвращает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e5290-140">Retrieves the playback rate.</span></span>                                                                        |
| [<span data-ttu-id="e5290-141">**\_скорость размещения**</span><span class="sxs-lookup"><span data-stu-id="e5290-141">**put\_Rate**</span></span>](cpospassthru-put-rate.md)                        | <span data-ttu-id="e5290-142">Задает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e5290-142">Sets the playback rate.</span></span>                                                                             |
| [<span data-ttu-id="e5290-143">**получить \_ CurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="e5290-143">**get\_CurrentPosition**</span></span>](cpospassthru-get-currentposition.md)  | <span data-ttu-id="e5290-144">Извлекает текущую координату относительно общей продолжительности потока.</span><span class="sxs-lookup"><span data-stu-id="e5290-144">Retrieves the current position, relative to the total duration of the stream.</span></span>                       |
| [<span data-ttu-id="e5290-145">**кансикфорвард**</span><span class="sxs-lookup"><span data-stu-id="e5290-145">**CanSeekForward**</span></span>](cpospassthru-canseekforward.md)             | <span data-ttu-id="e5290-146">Определяет, можно ли выполнить поиск в потоке назад.</span><span class="sxs-lookup"><span data-stu-id="e5290-146">Determines whether the stream can be seeked backward.</span></span>                                               |
| [<span data-ttu-id="e5290-147">**кансикбакквард**</span><span class="sxs-lookup"><span data-stu-id="e5290-147">**CanSeekBackward**</span></span>](cpospassthru-canseekbackward.md)           | <span data-ttu-id="e5290-148">Определяет, можно ли выполнить поиск в потоке вперед.</span><span class="sxs-lookup"><span data-stu-id="e5290-148">Determines whether the stream can be seeked forward.</span></span>                                                |
| <span data-ttu-id="e5290-149">Методы Имедиасикинг</span><span class="sxs-lookup"><span data-stu-id="e5290-149">IMediaSeeking Methods</span></span>                                             | <span data-ttu-id="e5290-150">Описание</span><span class="sxs-lookup"><span data-stu-id="e5290-150">Description</span></span>                                                                                         |
| [<span data-ttu-id="e5290-151">**чекккапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="e5290-151">**CheckCapabilities**</span></span>](cpospassthru-checkcapabilities.md)       | <span data-ttu-id="e5290-152">Запрашивает, имеет ли поток указанные возможности поиска.</span><span class="sxs-lookup"><span data-stu-id="e5290-152">Queries whether a stream has specified seeking capabilities.</span></span>                                        |
| [<span data-ttu-id="e5290-153">**конверттимеформат**</span><span class="sxs-lookup"><span data-stu-id="e5290-153">**ConvertTimeFormat**</span></span>](cpospassthru-converttimeformat.md)       | <span data-ttu-id="e5290-154">Преобразует из одного формата времени в другой.</span><span class="sxs-lookup"><span data-stu-id="e5290-154">Converts from one time format to another.</span></span>                                                           |
| [<span data-ttu-id="e5290-155">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="e5290-155">**GetAvailable**</span></span>](cpospassthru-getavailable.md)                 | <span data-ttu-id="e5290-156">Извлекает диапазон времени, в течение которого поиск является эффективным.</span><span class="sxs-lookup"><span data-stu-id="e5290-156">Retrieves the range of times in which seeking is efficient.</span></span>                                         |
| [<span data-ttu-id="e5290-157">**Возможности**</span><span class="sxs-lookup"><span data-stu-id="e5290-157">**GetCapabilities**</span></span>](cpospassthru-getcapabilities.md)           | <span data-ttu-id="e5290-158">Извлекает все возможности поиска в потоке.</span><span class="sxs-lookup"><span data-stu-id="e5290-158">Retrieves all the seeking capabilities of the stream.</span></span>                                               |
| [<span data-ttu-id="e5290-159">**жеткуррентпоситион**</span><span class="sxs-lookup"><span data-stu-id="e5290-159">**GetCurrentPosition**</span></span>](cpospassthru-getcurrentposition.md)     | <span data-ttu-id="e5290-160">Извлекает текущую координату относительно общей продолжительности потока.</span><span class="sxs-lookup"><span data-stu-id="e5290-160">Retrieves the current position, relative to the total duration of the stream.</span></span>                       |
| [<span data-ttu-id="e5290-161">**Длительное время**</span><span class="sxs-lookup"><span data-stu-id="e5290-161">**GetDuration**</span></span>](cpospassthru-getduration.md)                   | <span data-ttu-id="e5290-162">Возвращает длительность потока.</span><span class="sxs-lookup"><span data-stu-id="e5290-162">Retrieves the duration of the stream.</span></span>                                                               |
| [<span data-ttu-id="e5290-163">**Выстановки**</span><span class="sxs-lookup"><span data-stu-id="e5290-163">**GetPositions**</span></span>](cpospassthru-getpositions.md)                 | <span data-ttu-id="e5290-164">Извлекает текущую и заданную позиции относительно общей продолжительности потока.</span><span class="sxs-lookup"><span data-stu-id="e5290-164">Retrieves the current position and the stop position, relative to the total duration of the stream.</span></span> |
| [<span data-ttu-id="e5290-165">**жетпреролл**</span><span class="sxs-lookup"><span data-stu-id="e5290-165">**GetPreroll**</span></span>](cpospassthru-getpreroll.md)                     | <span data-ttu-id="e5290-166">Извлекает объем данных, которые будут помещены в очередь перед начальной позицией.</span><span class="sxs-lookup"><span data-stu-id="e5290-166">Retrieves the amount of data that will be queued before the start position.</span></span>                         |
| [<span data-ttu-id="e5290-167">**Коэффициент**</span><span class="sxs-lookup"><span data-stu-id="e5290-167">**GetRate**</span></span>](cpospassthru-getrate.md)                           | <span data-ttu-id="e5290-168">Возвращает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e5290-168">Retrieves the playback rate.</span></span>                                                                        |
| [<span data-ttu-id="e5290-169">**жетстоппоситион**</span><span class="sxs-lookup"><span data-stu-id="e5290-169">**GetStopPosition**</span></span>](cpospassthru-getstopposition.md)           | <span data-ttu-id="e5290-170">Возвращает время, когда воспроизведение будет прервано относительно длительности потока.</span><span class="sxs-lookup"><span data-stu-id="e5290-170">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span>         |
| [<span data-ttu-id="e5290-171">**жеттимеформат**</span><span class="sxs-lookup"><span data-stu-id="e5290-171">**GetTimeFormat**</span></span>](cpospassthru-gettimeformat.md)               | <span data-ttu-id="e5290-172">Извлекает текущий формат времени.</span><span class="sxs-lookup"><span data-stu-id="e5290-172">Retrieves the current time format.</span></span>                                                                  |
| [<span data-ttu-id="e5290-173">**исформатсуппортед**</span><span class="sxs-lookup"><span data-stu-id="e5290-173">**IsFormatSupported**</span></span>](cpospassthru-isformatsupported.md)       | <span data-ttu-id="e5290-174">Определяет, поддерживается ли указанный формат времени.</span><span class="sxs-lookup"><span data-stu-id="e5290-174">Determines whether a specified time format is supported.</span></span>                                            |
| [<span data-ttu-id="e5290-175">**исусингтимеформат**</span><span class="sxs-lookup"><span data-stu-id="e5290-175">**IsUsingTimeFormat**</span></span>](cpospassthru-isusingtimeformat.md)       | <span data-ttu-id="e5290-176">Определяет, является ли указанный формат времени используемым в данный момент форматом.</span><span class="sxs-lookup"><span data-stu-id="e5290-176">Determines whether a specified time format is the format currently in use.</span></span>                          |
| [<span data-ttu-id="e5290-177">**куерипреферредформат**</span><span class="sxs-lookup"><span data-stu-id="e5290-177">**QueryPreferredFormat**</span></span>](cpospassthru-querypreferredformat.md) | <span data-ttu-id="e5290-178">Возвращает предпочтительный формат времени для потока.</span><span class="sxs-lookup"><span data-stu-id="e5290-178">Retrieves the preferred time format for the stream.</span></span>                                                 |
| [<span data-ttu-id="e5290-179">**сетпоситионс**</span><span class="sxs-lookup"><span data-stu-id="e5290-179">**SetPositions**</span></span>](cpospassthru-setpositions.md)                 | <span data-ttu-id="e5290-180">Установка текущей позиции и позиции окончания.</span><span class="sxs-lookup"><span data-stu-id="e5290-180">Sets the current position and the stop position.</span></span>                                                    |
| [<span data-ttu-id="e5290-181">**сетрате**</span><span class="sxs-lookup"><span data-stu-id="e5290-181">**SetRate**</span></span>](cpospassthru-setrate.md)                           | <span data-ttu-id="e5290-182">Задает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e5290-182">Sets the playback rate.</span></span>                                                                             |
| [<span data-ttu-id="e5290-183">**сеттимеформат**</span><span class="sxs-lookup"><span data-stu-id="e5290-183">**SetTimeFormat**</span></span>](cpospassthru-settimeformat.md)               | <span data-ttu-id="e5290-184">Задает формат времени.</span><span class="sxs-lookup"><span data-stu-id="e5290-184">Sets the time format.</span></span>                                                                               |
| <span data-ttu-id="e5290-185">Вспомогательные функции</span><span class="sxs-lookup"><span data-stu-id="e5290-185">Helper Functions</span></span>                                                  | <span data-ttu-id="e5290-186">Описание</span><span class="sxs-lookup"><span data-stu-id="e5290-186">Description</span></span>                                                                                         |
| [<span data-ttu-id="e5290-187">**креатепоспасссру**</span><span class="sxs-lookup"><span data-stu-id="e5290-187">**CreatePosPassThru**</span></span>](createpospassthru.md)                    | <span data-ttu-id="e5290-188">Создает `CPosPassThru` объект или [**крендерерпоспасссру**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="e5290-188">Creates a `CPosPassThru` or [**CRendererPosPassThru**](crendererpospassthru.md) object.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="e5290-189">Требования</span><span class="sxs-lookup"><span data-stu-id="e5290-189">Requirements</span></span>



| <span data-ttu-id="e5290-190">Требование</span><span class="sxs-lookup"><span data-stu-id="e5290-190">Requirement</span></span> | <span data-ttu-id="e5290-191">Значение</span><span class="sxs-lookup"><span data-stu-id="e5290-191">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5290-192">Header</span><span class="sxs-lookup"><span data-stu-id="e5290-192">Header</span></span><br/>  | <dl> <span data-ttu-id="e5290-193"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5290-193"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e5290-194">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5290-194">Library</span></span><br/> | <dl> <span data-ttu-id="e5290-195"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e5290-195"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




