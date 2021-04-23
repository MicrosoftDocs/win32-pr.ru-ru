---
description: Управление графиком записи
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Управление графиком записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0089fa11adbc0ac861fb9e8e30e2cd0f56b23680
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909052"
---
# <a name="controlling-a-capture-graph"></a><span data-ttu-id="704c6-103">Управление графиком записи</span><span class="sxs-lookup"><span data-stu-id="704c6-103">Controlling a Capture Graph</span></span>

<span data-ttu-id="704c6-104">Интерфейс [**Имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) диспетчера графа фильтров имеет методы для запуска, остановки и приостановки всей диаграммы.</span><span class="sxs-lookup"><span data-stu-id="704c6-104">The Filter Graph Manager's [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface has methods for running, stopping, and pausing the entire graph.</span></span> <span data-ttu-id="704c6-105">Однако если граф фильтра имеет захват и предварительный просмотр потоков, то, скорее всего, потребуется управлять двумя потоками независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="704c6-105">If the filter graph has capture and preview streams, however, you probably want to control the two streams independently.</span></span> <span data-ttu-id="704c6-106">Например, может потребоваться предварительный просмотр видео без записи.</span><span class="sxs-lookup"><span data-stu-id="704c6-106">For example, you might want to preview the video without capturing it.</span></span> <span data-ttu-id="704c6-107">Это можно сделать с помощью метода [**ICaptureGraphBuilder2:: контролстреам**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) .</span><span class="sxs-lookup"><span data-stu-id="704c6-107">You can do this through the [**ICaptureGraphBuilder2::ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) method.</span></span>

> [!Note]  
> <span data-ttu-id="704c6-108">Этот метод не работает при записи в файл формата ASF.</span><span class="sxs-lookup"><span data-stu-id="704c6-108">This method does not work when capturing to an Advanced Systems Format (ASF) file.</span></span>

 

<span data-ttu-id="704c6-109">Управление потоком записи</span><span class="sxs-lookup"><span data-stu-id="704c6-109">Controlling the Capture Stream</span></span>

<span data-ttu-id="704c6-110">Следующий код задает выполнение потока видеозаписи в течение четырех секунд, начиная с одной секунды после выполнения графа:</span><span class="sxs-lookup"><span data-stu-id="704c6-110">The following code sets the video capture stream to run for four seconds, starting one second after the graph runs:</span></span>


```C++
// Control the video capture stream. 
REFERENCE_TIME rtStart = 10000000, rtStop = 50000000;
const WORD wStartCookie = 1, wStopCookie = 2;  // Arbitrary values.
hr = pBuild->ControlStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                 // Capture filter.
    &rtStart, &rtStop,     // Start and stop times.
    wStartCookie, wStopCookie  // Values for the start and stop events.
);
pControl->Run();
```



<span data-ttu-id="704c6-111">Первый параметр указывает, какой поток следует контролировать, как GUID категории ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="704c6-111">The first parameter specifies which stream to control, as a pin category GUID.</span></span> <span data-ttu-id="704c6-112">Второй параметр задает тип носителя.</span><span class="sxs-lookup"><span data-stu-id="704c6-112">The second parameter gives the media type.</span></span> <span data-ttu-id="704c6-113">Третий параметр — это указатель на фильтр записи.</span><span class="sxs-lookup"><span data-stu-id="704c6-113">The third parameter is a pointer to the capture filter.</span></span> <span data-ttu-id="704c6-114">Чтобы управлять всеми потоками записи в графе, установите для второго и третьего параметров **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="704c6-114">To control all the capture streams in the graph, set the second and third parameters to **NULL**.</span></span>

<span data-ttu-id="704c6-115">Следующие два параметра определяют время начала и окончания работы потока относительно времени начала выполнения графа.</span><span class="sxs-lookup"><span data-stu-id="704c6-115">The next two parameters define the times when the stream will start and stop, relative to the time when the graph starts running.</span></span> <span data-ttu-id="704c6-116">Вызовите [**имедиаконтрол:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) , чтобы запустить граф.</span><span class="sxs-lookup"><span data-stu-id="704c6-116">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the graph.</span></span> <span data-ttu-id="704c6-117">До запуска графа метод **контролстреам** не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="704c6-117">Until you run the graph, the **ControlStream** method has no effect.</span></span> <span data-ttu-id="704c6-118">Если граф уже запущен, параметры вступают в силу немедленно.</span><span class="sxs-lookup"><span data-stu-id="704c6-118">If the graph is already running, the settings take effect immediately.</span></span>

<span data-ttu-id="704c6-119">Последние два параметра используются для получения уведомлений о событиях при запуске и остановке потока.</span><span class="sxs-lookup"><span data-stu-id="704c6-119">The last two parameters are used for getting event notifications when the stream starts and stops.</span></span> <span data-ttu-id="704c6-120">Для каждого потока, управляемого с помощью этого метода, граф фильтра отправляет пару событий: [**\_ элемент управления потоком EC \_ \_ запущен**](ec-stream-control-started.md) при запуске потока, а [**\_ Управление потоком EC \_ \_ остановлено**](ec-stream-control-stopped.md) при остановке потока.</span><span class="sxs-lookup"><span data-stu-id="704c6-120">For each stream that you control using this method, the filter graph sends a pair of events: [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) when the stream starts, and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) when the stream stops.</span></span> <span data-ttu-id="704c6-121">Значения **встарткукие** и **встопкукие** используются в качестве второго параметра события.</span><span class="sxs-lookup"><span data-stu-id="704c6-121">The values of **wStartCookie** and **wStopCookie** are used as the second event parameter.</span></span> <span data-ttu-id="704c6-122">Таким же *lParam2* в событии Start равно **Встарткукие**, а *lParam2* в событии «завершение» равно **встопкукие**.</span><span class="sxs-lookup"><span data-stu-id="704c6-122">Thus, *lParam2* in the start event equals **wStartCookie**, and *lParam2* in the stop event equals **wStopCookie**.</span></span> <span data-ttu-id="704c6-123">В следующем коде показано, как получить эти события:</span><span class="sxs-lookup"><span data-stu-id="704c6-123">The following code shows how to get these events:</span></span>


```C++
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch (evCode)
    {
    case EC_STREAM_CONTROL_STARTED: 
    // param2 == wStartCookie
    break;

    case EC_STREAM_CONTROL_STOPPED: 
    // param2 == wStopCookie
    break;
    
    } 
    pEvent->FreeEventParams(evCode, param1, param2);
}
```



<span data-ttu-id="704c6-124">Метод **контролстреам** определяет некоторые специальные значения времени начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="704c6-124">The **ControlStream** method defines some special values for the start and stop times.</span></span>



| <span data-ttu-id="704c6-125">Метка</span><span class="sxs-lookup"><span data-stu-id="704c6-125">Label</span></span> | <span data-ttu-id="704c6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="704c6-126">Value</span></span> |
|-------------|----------------------------------------|------------------------------------|
|             | <span data-ttu-id="704c6-127">Начало</span><span class="sxs-lookup"><span data-stu-id="704c6-127">Start</span></span>                                  | <span data-ttu-id="704c6-128">Stop</span><span class="sxs-lookup"><span data-stu-id="704c6-128">Stop</span></span>                               |
| <span data-ttu-id="704c6-129">макслонглонг</span><span class="sxs-lookup"><span data-stu-id="704c6-129">MAXLONGLONG</span></span> | <span data-ttu-id="704c6-130">Никогда не запускать этот поток.</span><span class="sxs-lookup"><span data-stu-id="704c6-130">Never start this stream.</span></span>               | <span data-ttu-id="704c6-131">Не останавливайтесь до тех пор, пока граф не прекратит работу.</span><span class="sxs-lookup"><span data-stu-id="704c6-131">Do not stop until the graph stops.</span></span> |
| <span data-ttu-id="704c6-132">**NULL**</span><span class="sxs-lookup"><span data-stu-id="704c6-132">**NULL**</span></span>    | <span data-ttu-id="704c6-133">Запустить сразу после выполнения графа.</span><span class="sxs-lookup"><span data-stu-id="704c6-133">Start immediately when the graph runs.</span></span> | <span data-ttu-id="704c6-134">Немедленное завершение.</span><span class="sxs-lookup"><span data-stu-id="704c6-134">Stop immediately.</span></span>                  |



 

<span data-ttu-id="704c6-135">Например, следующий код немедленно останавливает поток записи:</span><span class="sxs-lookup"><span data-stu-id="704c6-135">For example, the following code stops the capture stream immediately:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="704c6-136">Несмотря на то, что вы можете прерывать поток записи и перезапускать его позже, это приведет к созданию разрыва в метках времени.</span><span class="sxs-lookup"><span data-stu-id="704c6-136">Although you can stop the capture stream and restart it later, this will create a gap in the time stamps.</span></span> <span data-ttu-id="704c6-137">При воспроизведении видео во время пропуска появится сообщение о зависании (в зависимости от формата файла).</span><span class="sxs-lookup"><span data-stu-id="704c6-137">On playback, the video will appear to stall during the gap (depending on the file format).</span></span>

<span data-ttu-id="704c6-138">Управление потоком предварительной версии</span><span class="sxs-lookup"><span data-stu-id="704c6-138">Controlling the Preview Stream</span></span>

<span data-ttu-id="704c6-139">Чтобы управлять предварительной версией ПИН-кода, вызовите **контролстреам** , но Задайте первый параметр для закрепления \_ категории \_ Предварительная версия.</span><span class="sxs-lookup"><span data-stu-id="704c6-139">To control the preview pin, call **ControlStream** but set the first parameter to PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="704c6-140">Это работает так же, как и для \_ захвата категорий ПИН-кодов \_ , за исключением того, что нельзя использовать время ссылки для указания запуска и завершения, так как в кадрах предварительной версии отсутствуют отметки времени.</span><span class="sxs-lookup"><span data-stu-id="704c6-140">This works just like it does for PIN\_CATEGORY\_CAPTURE, except that you cannot use reference times to specify the start and stop, because the preview frames do not have time stamps.</span></span> <span data-ttu-id="704c6-141">Поэтому необходимо использовать **значение NULL** или макслонглонг.</span><span class="sxs-lookup"><span data-stu-id="704c6-141">Therefore, you must use **NULL** or MAXLONGLONG.</span></span> <span data-ttu-id="704c6-142">Чтобы запустить предварительный просмотр потока, используйте **значение NULL** :</span><span class="sxs-lookup"><span data-stu-id="704c6-142">Use **NULL** to start the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="704c6-143">Чтобы прерывать предварительный просмотр потока, используйте МАКСЛОНГЛОНГ.</span><span class="sxs-lookup"><span data-stu-id="704c6-143">Use MAXLONGLONG to stop the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="704c6-144">Не имеет значения, поступает ли поток просмотра из предварительной версии в фильтре записи или из фильтра Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="704c6-144">It does not matter whether the preview stream comes from a preview pin on the capture filter, or from the Smart Tee filter.</span></span> <span data-ttu-id="704c6-145">Метод **контролстреам** работает в любом направлении.</span><span class="sxs-lookup"><span data-stu-id="704c6-145">The **ControlStream** method works either way.</span></span>

<span data-ttu-id="704c6-146">Однако для ПИН-портов видео метод завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="704c6-146">For video port pins, however, the method will fail.</span></span> <span data-ttu-id="704c6-147">В этом случае другой подход заключается в скрытии окна видео.</span><span class="sxs-lookup"><span data-stu-id="704c6-147">In that case, another approach is to hide the video window.</span></span> <span data-ttu-id="704c6-148">Запросите граф для **ивидеовиндов** и используйте метод [**ивидеовиндов::p UT \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) , чтобы показать или скрыть окно.</span><span class="sxs-lookup"><span data-stu-id="704c6-148">Query the graph for **IVideoWindow**, and use the [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) method to show or hide the window.</span></span>


```C++
// Hide the video window.
IVideoWindow *pVidWin = 0;
hr = pGraph->QueryInterface(IID_IVideoWindow, (void**)&pVidWin);
if (SUCCEEDED(hr))
{
    pVidWin->put_Visible(OAFALSE);
    pVidWin->Release();
}
```



<span data-ttu-id="704c6-149">Кроме того, при вызове [**ивидеовиндов::p UT \_ автоотображения**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) со значением оафалсе перед запуском графа фильтр модуля подготовки видео скрывает окно до тех пор, пока не будет указано иное.</span><span class="sxs-lookup"><span data-stu-id="704c6-149">Also, if you call [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value OAFALSE before you run the graph, the Video Renderer filter hides the window until you specify otherwise.</span></span> <span data-ttu-id="704c6-150">По умолчанию модуль подготовки видео отображает окно при запуске графа.</span><span class="sxs-lookup"><span data-stu-id="704c6-150">By default, the Video Renderer shows the window when you run the graph.</span></span>

<span data-ttu-id="704c6-151">Примечания об управлении потоком</span><span class="sxs-lookup"><span data-stu-id="704c6-151">Remarks about Stream Control</span></span>

<span data-ttu-id="704c6-152">Поведением по умолчанию для ПИН-кода является доставка образцов при выполнении графа.</span><span class="sxs-lookup"><span data-stu-id="704c6-152">The default behavior for a pin is to deliver samples when the graph runs.</span></span> <span data-ttu-id="704c6-153">Например, предположим, что вы вызываете **контролстреам** с \_ захватом категории ПИН-кода, \_ но не с \_ предварительной версией категории ПИН-кода \_ .</span><span class="sxs-lookup"><span data-stu-id="704c6-153">For example, suppose that you call **ControlStream** with PIN\_CATEGORY\_CAPTURE but not with PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="704c6-154">При запуске графа предварительный просмотр потока выполняется немедленно, а поток отслеживания выполняется в любое время, указанное в **контролстреам**.</span><span class="sxs-lookup"><span data-stu-id="704c6-154">When you run the graph, the preview stream will run immediately, while the capture stream will run at whatever time you specified in **ControlStream**.</span></span>

<span data-ttu-id="704c6-155">Если вы захватываете несколько потоков и отправляете их в фильтр мультиплексора — например, если вы записываете аудио и видео в AVI-файл, следует одновременно управлять обоими потоками.</span><span class="sxs-lookup"><span data-stu-id="704c6-155">If you are capturing more than one stream and sending them to a mux filter — for example, if you are capturing audio and video to an AVI file — you should control both streams in tandem.</span></span> <span data-ttu-id="704c6-156">В противном случае фильтр мультиплексора может блокировать ожидание одного потока, так как он пытается чередования двух потоков.</span><span class="sxs-lookup"><span data-stu-id="704c6-156">Otherwise, the mux filter might block waiting for one stream, as it tries to interleave the two streams.</span></span> <span data-ttu-id="704c6-157">Задайте то же время начала и окончания для всех потоков записи перед запуском графа:</span><span class="sxs-lookup"><span data-stu-id="704c6-157">Set the same start and stop times on all capture streams before running the graph:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="704c6-158">На внутреннем уровне метод **контролстреам** использует интерфейс [**иамстреамконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , который предоставляется на контактах фильтра записи, интеллектуального tee Filter (при наличии) и, возможно, фильтра мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="704c6-158">Internally, the **ControlStream** method uses the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, which is exposed on the pins of the capture filter, the Smart Tee filter (if present), and possibly the mux filter.</span></span> <span data-ttu-id="704c6-159">Этот интерфейс можно использовать напрямую, вместо того чтобы вызывать **контролстреам**, хотя это и не имеет особого преимущества.</span><span class="sxs-lookup"><span data-stu-id="704c6-159">You can use this interface directly, instead of calling **ControlStream**, although there is no particular advantage to doing so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="704c6-160">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="704c6-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="704c6-161">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="704c6-161">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



