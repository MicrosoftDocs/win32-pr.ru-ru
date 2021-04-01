---
description: В этом разделе описывается, как пользовательский фильтр захвата DirectShow должен формировать выходные данные.
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: Создание данных в фильтре записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c9e5bed6fc7e01aa89bf6f495c1bbdf6e42a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990156"
---
# <a name="producing-data-in-a-capture-filter"></a><span data-ttu-id="a303f-103">Создание данных в фильтре записи</span><span class="sxs-lookup"><span data-stu-id="a303f-103">Producing Data in a Capture Filter</span></span>

<span data-ttu-id="a303f-104">В этом разделе описывается, как пользовательский фильтр захвата DirectShow должен формировать выходные данные.</span><span class="sxs-lookup"><span data-stu-id="a303f-104">This topic describes how a custom DirectShow capture filter should generate output data.</span></span>

## <a name="filter-state-changes"></a><span data-ttu-id="a303f-105">Фильтрация изменений состояния</span><span class="sxs-lookup"><span data-stu-id="a303f-105">Filter State Changes</span></span>

<span data-ttu-id="a303f-106">Фильтр записи должен создавать данные только при выполнении фильтра.</span><span class="sxs-lookup"><span data-stu-id="a303f-106">A capture filter should produce data only when the filter is running.</span></span> <span data-ttu-id="a303f-107">Не отправляйте данные с ваших ПИН-кодов при приостановке фильтра.</span><span class="sxs-lookup"><span data-stu-id="a303f-107">Do not send data from your pins when the filter is paused.</span></span> <span data-ttu-id="a303f-108">Кроме того, при приостановке фильтра следует возвращать **VFW \_ S не \_ удается \_ подсказку** из метода [**кбасефилтер::**](cbasefilter-getstate.md) noreturn.</span><span class="sxs-lookup"><span data-stu-id="a303f-108">Also, return **VFW\_S\_CANT\_CUE** from the [**CBaseFilter::GetState**](cbasefilter-getstate.md) method when the filter is paused.</span></span> <span data-ttu-id="a303f-109">Это возвращаемое значение информирует диспетчер графа фильтра о том, что не следует ждать каких-либо данных из фильтра, пока фильтр приостановлен.</span><span class="sxs-lookup"><span data-stu-id="a303f-109">This return value informs the Filter Graph Manager that it should not wait for any data from your filter while the filter is paused.</span></span> <span data-ttu-id="a303f-110">Дополнительные сведения см. в разделе [Фильтрация состояний](filter-states.md).</span><span class="sxs-lookup"><span data-stu-id="a303f-110">For more information, see [Filter States](filter-states.md).</span></span>

<span data-ttu-id="a303f-111">В следующем коде показано, как реализовать метод [**имедиафилтер::**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) WebMethod:</span><span class="sxs-lookup"><span data-stu-id="a303f-111">The following code shows how to implement the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method:</span></span>


```C++
CMyVidcapFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
    {
        return VFW_S_CANT_CUE;
    }
    else
    {
        return S_OK;
    }
}
```



## <a name="controlling-individual-streams"></a><span data-ttu-id="a303f-112">Управление отдельными потоками</span><span class="sxs-lookup"><span data-stu-id="a303f-112">Controlling Individual Streams</span></span>

<span data-ttu-id="a303f-113">Выходные сигналы фильтра записи должны поддерживать интерфейс [**иамстреамконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , чтобы приложение может включать или отключать каждый ПИН-код отдельно.</span><span class="sxs-lookup"><span data-stu-id="a303f-113">A capture filter's output pins should support the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, so that an application can turn each pin on or off individually.</span></span> <span data-ttu-id="a303f-114">Например, приложение может выполнить предварительный просмотр без записи, а затем переключиться в режим записи без перестроения графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="a303f-114">For example, an application can preview without capturing, and then switch to capture mode without rebuilding the filter graph.</span></span> <span data-ttu-id="a303f-115">Для реализации этого интерфейса можно использовать класс [**кбасестреамконтрол**](cbasestreamcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="a303f-115">You can use the [**CBaseStreamControl**](cbasestreamcontrol.md) class to implement this interface.</span></span>

## <a name="time-stamps"></a><span data-ttu-id="a303f-116">Метки времени</span><span class="sxs-lookup"><span data-stu-id="a303f-116">Time Stamps</span></span>

<span data-ttu-id="a303f-117">Когда фильтр захватывает пример, отметка времени для образца с текущим временем потока.</span><span class="sxs-lookup"><span data-stu-id="a303f-117">When the filter captures a sample, time stamp the sample with the current stream time.</span></span> <span data-ttu-id="a303f-118">Время окончания — это время начала и длительность.</span><span class="sxs-lookup"><span data-stu-id="a303f-118">The end time is the start time plus the duration.</span></span> <span data-ttu-id="a303f-119">Например, если фильтр записывается в десять выборок в секунду, а время потока составляет 200 000 000 единиц, когда фильтр захватывает образец, отметки времени должны быть 200000000 и 201000000.</span><span class="sxs-lookup"><span data-stu-id="a303f-119">For example, if the filter is capturing at ten samples per second, and the stream time is 200,000,000 units when the filter captures the sample, the time stamps should be 200000000 and 201000000.</span></span> <span data-ttu-id="a303f-120">(10 000 000 единиц в секунду.)</span><span class="sxs-lookup"><span data-stu-id="a303f-120">(There are 10,000,000 units per second.)</span></span>

<span data-ttu-id="a303f-121">Чтобы вычислить время потока, вызовите метод [**иреференцеклокк:: Time**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) , чтобы получить текущее время ссылки, а затем вычитание исходное время начала.</span><span class="sxs-lookup"><span data-stu-id="a303f-121">To calculate the stream time, call the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method to get the current reference time, and then substract the original start time.</span></span> <span data-ttu-id="a303f-122">Кроме того, можно вызвать метод [**кбасефилтер:: стреамтиме**](cbasefilter-streamtime.md) , который выполняет то же вычисление.</span><span class="sxs-lookup"><span data-stu-id="a303f-122">Alternatively, call the [**CBaseFilter::StreamTime**](cbasefilter-streamtime.md) method, which performs the same calculation.</span></span> <span data-ttu-id="a303f-123">Чтобы задать метку времени для образца, вызовите метод [**имедиасампле:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .</span><span class="sxs-lookup"><span data-stu-id="a303f-123">To set the time stamp on a sample, call the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method.</span></span>

<span data-ttu-id="a303f-124">Однако если фильтр имеет предварительный ПИН-код, образцы из ПИН-кода предварительной версии не должны иметь отметки времени.</span><span class="sxs-lookup"><span data-stu-id="a303f-124">If the filter has a preview pin, however, samples from the preview pin should not have time stamps.</span></span> <span data-ttu-id="a303f-125">Причина в том, что образцы всегда будут обращаться к модулю прорисовки немного позже, чем время записи.</span><span class="sxs-lookup"><span data-stu-id="a303f-125">The reason is that samples will always reach the renderer slightly after the time of capture.</span></span> <span data-ttu-id="a303f-126">Если образцы имеют отметку времени, то модуль подготовки отчетов будет обрабатывать их как последние и может попытаться отследить, удалив образцы.</span><span class="sxs-lookup"><span data-stu-id="a303f-126">If the samples are time stamped, the renderer will treat them as late, and it may try to catch up by dropping samples.</span></span> <span data-ttu-id="a303f-127">(Дополнительные сведения см. в статье [Фильтры захвата видео DirectShow](directshow-video-capture-filters.md).) Обратите внимание, что интерфейс [**иамстреамконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) требует, чтобы ПИН-код следит за временем выборки.</span><span class="sxs-lookup"><span data-stu-id="a303f-127">(For more information, see [DirectShow Video Capture Filters](directshow-video-capture-filters.md).) Note that the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface requires the pin to keep track of sample times.</span></span> <span data-ttu-id="a303f-128">Для предварительного просмотра ПИН-кода может потребоваться изменить реализацию, чтобы не полагаться на отметки времени.</span><span class="sxs-lookup"><span data-stu-id="a303f-128">For a preview pin, you might need to modify the implementation so that it does not rely on time stamps.</span></span>

<span data-ttu-id="a303f-129">Метки времени должны всегда увеличиваться от одного до следующего.</span><span class="sxs-lookup"><span data-stu-id="a303f-129">Time stamps must always increase from one sample to the next.</span></span> <span data-ttu-id="a303f-130">Это справедливо даже в случае приостановки фильтра.</span><span class="sxs-lookup"><span data-stu-id="a303f-130">This is true even when the filter pauses.</span></span> <span data-ttu-id="a303f-131">Если фильтр выполняется, приостанавливает работу, а затем снова запускается, первый пример после приостановки должен иметь более крупную метку времени, чем последняя выборка до приостановки.</span><span class="sxs-lookup"><span data-stu-id="a303f-131">If the filter runs, pauses, and then runs again, the first sample after the pause must have a larger time stamp than the last sample before the pause.</span></span>

<span data-ttu-id="a303f-132">В зависимости от собираемых данных может быть целесообразно установить время мультимедиа для образцов.</span><span class="sxs-lookup"><span data-stu-id="a303f-132">Depending on the data you are capturing, it might be appropriate to set the media time on the samples.</span></span>

<span data-ttu-id="a303f-133">Дополнительные сведения см. [в разделе время и часы в DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="a303f-133">For more information, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a303f-134">См. также</span><span class="sxs-lookup"><span data-stu-id="a303f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a303f-135">Фильтры захвата видео DirectShow</span><span class="sxs-lookup"><span data-stu-id="a303f-135">DirectShow Video Capture Filters</span></span>](directshow-video-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="a303f-136">Время и часы в DirectShow</span><span class="sxs-lookup"><span data-stu-id="a303f-136">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="a303f-137">Запись фильтров записи</span><span class="sxs-lookup"><span data-stu-id="a303f-137">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



