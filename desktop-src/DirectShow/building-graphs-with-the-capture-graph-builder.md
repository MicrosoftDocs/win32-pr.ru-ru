---
description: Построение диаграмм с помощью построителя графа записи
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: Построение диаграмм с помощью построителя графа записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e48347a73cdac545723ac226cc58a0175dec5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895081"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a><span data-ttu-id="03ffd-103">Построение диаграмм с помощью построителя графа записи</span><span class="sxs-lookup"><span data-stu-id="03ffd-103">Building Graphs with the Capture Graph Builder</span></span>

<span data-ttu-id="03ffd-104">Несмотря на свое имя, построитель диаграмм для записи полезен для создания различных типов графов настраиваемых фильтров, а не только для записи графов.</span><span class="sxs-lookup"><span data-stu-id="03ffd-104">Despite its name, the Capture Graph Builder is useful for building many kinds of custom filter graphs, not only capture graphs.</span></span> <span data-ttu-id="03ffd-105">В этой статье содержится краткий обзор использования этого объекта.</span><span class="sxs-lookup"><span data-stu-id="03ffd-105">This article provides a brief overview of how to use this object.</span></span>

<span data-ttu-id="03ffd-106">Построитель графов записи предоставляет интерфейс [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="03ffd-106">The Capture Graph Builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="03ffd-107">Начните с вызова [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать построитель графов записи и диспетчер графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="03ffd-107">Start by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Capture Graph Builder and the Filter Graph Manager.</span></span> <span data-ttu-id="03ffd-108">Затем инициализируйте построитель диаграмм записи путем вызова [**ICaptureGraphBuilder2:: сетфилтерграф**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) с указателем на диспетчер графа фильтров, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="03ffd-108">Then initialize the Capture Graph Builder by calling [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) with a pointer to the Filter Graph Manager, as follows:</span></span>


```C++
IGraphBuilder *pGraph = NULL;
ICaptureGraphBuilder2 *pBuilder = NULL;

// Create the Filter Graph Manager.
HRESULT hr =  CoCreateInstance(CLSID_FilterGraph, NULL,
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);

if (SUCCEEDED(hr))
{
    // Create the Capture Graph Builder.
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL,
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, 
        (void **)&pBuilder);
    if (SUCCEEDED(hr))
    {
        pBuilder->SetFiltergraph(pGraph);
    }
};
```



## <a name="connecting-filters"></a><span data-ttu-id="03ffd-109">Фильтры подключения</span><span class="sxs-lookup"><span data-stu-id="03ffd-109">Connecting Filters</span></span>

<span data-ttu-id="03ffd-110">Метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) соединяет два или три фильтра вместе в цепочке.</span><span class="sxs-lookup"><span data-stu-id="03ffd-110">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method connects two or three filters together in a chain.</span></span> <span data-ttu-id="03ffd-111">Как правило, метод работает наилучшим образом, если у каждого фильтра есть не более одного входного ПИН-кода или выходного контакта одного типа.</span><span class="sxs-lookup"><span data-stu-id="03ffd-111">Generally, the method works best when each filter has no more than one input pin or output pin of the same type.</span></span> <span data-ttu-id="03ffd-112">Это обсуждение начинается с того, что первые два параметра **RenderStream** и основное внимание уделяется последним трем параметрам.</span><span class="sxs-lookup"><span data-stu-id="03ffd-112">This discussion begins by ignoring the first two parameters of **RenderStream** and focusing on the last three parameters.</span></span> <span data-ttu-id="03ffd-113">Третий параметр — это указатель [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , который может указывать либо фильтр (как указатель интерфейса [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) ), либо выходной ПИН-код (как указатель интерфейса [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ).</span><span class="sxs-lookup"><span data-stu-id="03ffd-113">The third parameter is an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer, which can specify either a filter (as an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface pointer) or an output pin (as an [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface pointer).</span></span> <span data-ttu-id="03ffd-114">Четвертый и пятый параметры указывают указатели **ибасефилтер** .</span><span class="sxs-lookup"><span data-stu-id="03ffd-114">The fourth and fifth parameters specify **IBaseFilter** pointers.</span></span> <span data-ttu-id="03ffd-115">Метод **RenderStream** соединяет все три фильтра в цепочке.</span><span class="sxs-lookup"><span data-stu-id="03ffd-115">The **RenderStream** method connects all three filters in a chain.</span></span> <span data-ttu-id="03ffd-116">Например, предположим, что *A*, *B* и *C* являются фильтрами.</span><span class="sxs-lookup"><span data-stu-id="03ffd-116">For example, suppose that *A*, *B*, and *C* are filters.</span></span> <span data-ttu-id="03ffd-117">Предположим, что у каждого фильтра есть только один входной ПИН-код и один выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="03ffd-117">Assume for now that each filter has exactly one input pin and one output pin.</span></span> <span data-ttu-id="03ffd-118">Следующий вызов подключается к B, а затем б к C:</span><span class="sxs-lookup"><span data-stu-id="03ffd-118">The following call connects A to B, and then B to C:</span></span>

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

<span data-ttu-id="03ffd-119">Все соединения имеют "Интеллектуальные", то есть при необходимости к диаграмме добавляются дополнительные фильтры.</span><span class="sxs-lookup"><span data-stu-id="03ffd-119">All connections are "intelligent," meaning that additional filters are added to the graph as needed.</span></span> <span data-ttu-id="03ffd-120">Дополнительные сведения см. в разделе [Intelligent Connect](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="03ffd-120">For details, see [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="03ffd-121">Чтобы подключить только два фильтра, присвойте среднему значению значение **null**.</span><span class="sxs-lookup"><span data-stu-id="03ffd-121">To connect just two filters, set the middle value to **NULL**.</span></span> <span data-ttu-id="03ffd-122">Например, этот вызов подключается к C:</span><span class="sxs-lookup"><span data-stu-id="03ffd-122">For example, this call connects A to C:</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

<span data-ttu-id="03ffd-123">Вы можете создать более длинные цепочки, вызвав метод дважды:</span><span class="sxs-lookup"><span data-stu-id="03ffd-123">You can create longer chains by calling the method twice:</span></span>

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

<span data-ttu-id="03ffd-124">Если последний параметр имеет **значение NULL**, метод автоматически находит модуль визуализации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="03ffd-124">If the last parameter is **NULL**, the method automatically locates a default renderer.</span></span> <span data-ttu-id="03ffd-125">В нем используется модуль [подготовки видео](video-renderer-filter.md) для видео и модуль [воспроизведения DirectSound](directsound-renderer-filter.md) для аудио.</span><span class="sxs-lookup"><span data-stu-id="03ffd-125">It uses the [Video Renderer](video-renderer-filter.md) for video and the [DirectSound Renderer](directsound-renderer-filter.md) for audio.</span></span> <span data-ttu-id="03ffd-126">Следовательно</span><span class="sxs-lookup"><span data-stu-id="03ffd-126">Thus:</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

<span data-ttu-id="03ffd-127">эквивалентно</span><span class="sxs-lookup"><span data-stu-id="03ffd-127">is equivalent to</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

<span data-ttu-id="03ffd-128">где *R* — соответствующий модуль подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="03ffd-128">where *R* is the appropriate renderer.</span></span> <span data-ttu-id="03ffd-129">Однако, чтобы подключить фильтр модуля подготовки к просмотру видео вместо модуля подготовки видео, необходимо явно указать его.</span><span class="sxs-lookup"><span data-stu-id="03ffd-129">To connect the Video Mixing Renderer filter instead of the Video Renderer, however, you must specify it explicitly.</span></span>

<span data-ttu-id="03ffd-130">Если в третьем параметре указать фильтр, а не ПИН-код, может потребоваться указать, какой из выходных контактов следует использовать для соединения.</span><span class="sxs-lookup"><span data-stu-id="03ffd-130">If you specify a filter in the third parameter, rather than a pin, you may need to indicate which output pin should be used for the connection.</span></span> <span data-ttu-id="03ffd-131">Это назначение первых двух параметров метода.</span><span class="sxs-lookup"><span data-stu-id="03ffd-131">That is the purpose of the method's first two parameters.</span></span> <span data-ttu-id="03ffd-132">Первый параметр применяется только к фильтрам записи.</span><span class="sxs-lookup"><span data-stu-id="03ffd-132">The first parameter applies only to capture filters.</span></span> <span data-ttu-id="03ffd-133">Он указывает идентификатор GUID, указывающий категорию ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="03ffd-133">It specifies a GUID that indicates a pin category.</span></span> <span data-ttu-id="03ffd-134">Полный список категорий см. в разделе [закрепить набор свойств](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="03ffd-134">For a complete list of categories, see [Pin Property Set](pin-property-set.md).</span></span> <span data-ttu-id="03ffd-135">Две категории допустимы для всех фильтров захвата:</span><span class="sxs-lookup"><span data-stu-id="03ffd-135">Two of the categories are valid for all capture filters:</span></span>

-   <span data-ttu-id="03ffd-136">**закрепить \_ \_ запись категорий**</span><span class="sxs-lookup"><span data-stu-id="03ffd-136">**PIN\_CATEGORY\_CAPTURE**</span></span>
-   <span data-ttu-id="03ffd-137">**\_ \_ Предварительный просмотр категории закрепления**</span><span class="sxs-lookup"><span data-stu-id="03ffd-137">**PIN\_CATEGORY\_PREVIEW**</span></span>

<span data-ttu-id="03ffd-138">Если фильтр записи не предоставляет отдельные ПИН-коды для записи и предварительного просмотра, метод [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) вставляет [Интеллектуальный фильтр tee](smart-tee-filter.md) , который разделяет поток на поток записи и предварительный просмотр потока.</span><span class="sxs-lookup"><span data-stu-id="03ffd-138">If a capture filter does not supply separate pins for capture and preview, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="03ffd-139">С точки зрения приложения можно просто обрабатывать все фильтры захвата как имеющие отдельные ПИН-коды и игнорировать базовую топологию графа.</span><span class="sxs-lookup"><span data-stu-id="03ffd-139">From the application's standpoint, you can simply treat all capture filters as having separate pins and ignore the underlying topology of the graph.</span></span>

<span data-ttu-id="03ffd-140">Для записи файла Подключите ПИН-код записи к фильтру мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="03ffd-140">For file capture, connect the capture pin to a mux filter.</span></span> <span data-ttu-id="03ffd-141">Для интерактивной предварительной версии Подключите предварительный ПИН-код к модулю подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="03ffd-141">For live preview, connect the preview pin to a renderer.</span></span> <span data-ttu-id="03ffd-142">При переключении двух категорий диаграмма может удалить слишком много кадров во время записи файла; но если граф подключен правильно, он удаляет предварительные кадры по мере необходимости для поддержания пропускной способности потока записи.</span><span class="sxs-lookup"><span data-stu-id="03ffd-142">If you switch the two categories, the graph might drop an excessive number of frames during the file capture; but if the graph is connected properly, it drops preview frames as needed in order to maintain throughput on the capture stream.</span></span>

<span data-ttu-id="03ffd-143">В следующем примере показано, как подключить оба потока:</span><span class="sxs-lookup"><span data-stu-id="03ffd-143">The following example shows how to connect both streams:</span></span>


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



<span data-ttu-id="03ffd-144">Некоторые фильтры записи также поддерживают закрытые субтитры, обозначенные **закреплением \_ Category \_ ВБИ**.</span><span class="sxs-lookup"><span data-stu-id="03ffd-144">Some capture filters also support closed captions, indicated by **PIN\_CATEGORY\_VBI**.</span></span> <span data-ttu-id="03ffd-145">Чтобы записать скрытые субтитры в файл, выводите эту категорию в фильтр мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="03ffd-145">To capture the closed captions to a file, render this category to the mux filter.</span></span> <span data-ttu-id="03ffd-146">Чтобы просмотреть скрытые субтитры в окне предварительного просмотра, подключитесь к модулю подготовки отчетов:</span><span class="sxs-lookup"><span data-stu-id="03ffd-146">To view the closed captions in your preview window, connect to the renderer:</span></span>


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



<span data-ttu-id="03ffd-147">Второй параметр, [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , определяет тип носителя и обычно является одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="03ffd-147">The second parameter to [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifies the media type, and is typically one of the following:</span></span>

-   <span data-ttu-id="03ffd-148">MEDIATYPE \_ Audio</span><span class="sxs-lookup"><span data-stu-id="03ffd-148">MEDIATYPE\_Audio</span></span>
-   <span data-ttu-id="03ffd-149">\_Видео MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="03ffd-149">MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="03ffd-150">МУЛЬТИМЕДИА с \_ чередованием (DV)</span><span class="sxs-lookup"><span data-stu-id="03ffd-150">MEDIATYPE\_Interleaved (DV)</span></span>

<span data-ttu-id="03ffd-151">Этот параметр можно использовать каждый раз, когда выходные сигналы фильтра поддерживают перечисление предпочтительных типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="03ffd-151">You can use this parameter whenever the filter's output pins support the enumeration of preferred media types.</span></span> <span data-ttu-id="03ffd-152">Для файловых источников построитель диаграмм автоматически добавляет фильтр синтаксического анализатора при необходимости, а затем запрашивает типы мультимедиа в средстве синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="03ffd-152">For file sources, the Capture Graph Builder automatically adds a parser filter if needed, and then queries the media types on the parser.</span></span> <span data-ttu-id="03ffd-153">(Пример см. в разделе о повторном [сжатии AVI-файла](recompressing-an-avi-file.md).) Кроме того, если последний фильтр в цепочке имеет несколько входных ПИН-кодов, метод пытается перечислить типы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="03ffd-153">(For an example, see [Recompressing an AVI File](recompressing-an-avi-file.md).) Also, if the last filter in the chain has several input pins, the method attempts to enumerate their media types.</span></span> <span data-ttu-id="03ffd-154">Однако не все фильтры поддерживают эту функцию.</span><span class="sxs-lookup"><span data-stu-id="03ffd-154">However, not all filters support this functionality.</span></span>

## <a name="finding-interfaces-on-filters-and-pins"></a><span data-ttu-id="03ffd-155">Поиск интерфейсов в фильтрах и ПИН-кодах</span><span class="sxs-lookup"><span data-stu-id="03ffd-155">Finding Interfaces on Filters and Pins</span></span>

<span data-ttu-id="03ffd-156">После создания графа, как правило, необходимо разместить различные интерфейсы, предоставляемые фильтрами и ПИН-коды в графе.</span><span class="sxs-lookup"><span data-stu-id="03ffd-156">After you build a graph, you will typically need to locate various interfaces exposed by filters and pins in the graph.</span></span> <span data-ttu-id="03ffd-157">Например, фильтр захвата может предоставлять интерфейс [**иамдроппедфрамес**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) , тогда как в закреплении вывода фильтра может предоставляться интерфейс [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="03ffd-157">For example, a capture filter might expose the [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface, while the filter's output pins might expose the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface.</span></span>

<span data-ttu-id="03ffd-158">Самый простой способ найти интерфейс — использовать метод [**ICaptureGraphBuilder2:: финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) .</span><span class="sxs-lookup"><span data-stu-id="03ffd-158">The simplest way to find an interface is to use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method.</span></span> <span data-ttu-id="03ffd-159">Этот метод просматривает граф (фильтры и ПИН-коды) до тех пор, пока не найдет нужный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="03ffd-159">This method walks the graph (filters and pins) until it locates the desired interface.</span></span> <span data-ttu-id="03ffd-160">Вы можете указать начальную точку для поиска, а также ограничить поиск фильтрами, которые восходящий или нисходящий от начальной точки.</span><span class="sxs-lookup"><span data-stu-id="03ffd-160">You can specify the starting point for the search, and you can limit the search to filters upstream or downstream from the starting point.</span></span>

<span data-ttu-id="03ffd-161">В следующем примере выполняется поиск интерфейса [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) на ПИН-коде предварительной версии видео:</span><span class="sxs-lookup"><span data-stu-id="03ffd-161">The following example searches for the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface on a video preview pin:</span></span>


```C++
IAMStreamConfig *pConfig = NULL;
HRESULT hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, 
    &MEDIATYPE_Video,
    pVCap, 
    IID_IAMStreamConfig, 
    (void**)&pConfig
);
if (SUCCESSFUL(hr))
{
    /* ... */
    pConfig->Release();
}
```



> [!Note]  
> <span data-ttu-id="03ffd-162">В разделе [Поиск интерфейса на фильтре или ПИН-коде](find-an-interface-on-a-filter-or-pin.md) показан альтернативный подход, использующий интерфейс [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) вместо [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2).</span><span class="sxs-lookup"><span data-stu-id="03ffd-162">The topic [Find an Interface on a Filter or Pin](find-an-interface-on-a-filter-or-pin.md) shows an alternative approach that uses the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface instead of [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2).</span></span> <span data-ttu-id="03ffd-163">Используемый подход зависит от вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="03ffd-163">Which approach to use depends on your application.</span></span> <span data-ttu-id="03ffd-164">Если приложение уже использует **ICaptureGraphBuilder2** для построения графа, то [**ICaptureGraphBuilder2:: финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) является хорошим подходом.</span><span class="sxs-lookup"><span data-stu-id="03ffd-164">If your application already uses **ICaptureGraphBuilder2** to build the graph, then [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) is a good approach.</span></span> <span data-ttu-id="03ffd-165">В противном случае рассмотрите возможность использования методов **играфбуилдер** .</span><span class="sxs-lookup"><span data-stu-id="03ffd-165">Otherwise, consider using the **IGraphBuilder** methods.</span></span>

 

## <a name="finding-pins"></a><span data-ttu-id="03ffd-166">Поиск ПИН-кодов</span><span class="sxs-lookup"><span data-stu-id="03ffd-166">Finding Pins</span></span>

<span data-ttu-id="03ffd-167">Реже всего может потребоваться указать отдельный ПИН-код для фильтра, хотя в большинстве случаев методы [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) и [**финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) помогут вам устранить неполадки.</span><span class="sxs-lookup"><span data-stu-id="03ffd-167">Less commonly, you may need to locate an individual pin on a filter, although in most cases the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) and [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) methods will save you the trouble.</span></span> <span data-ttu-id="03ffd-168">Если вам нужно найти определенный ПИН-код для фильтра, рекомендуется использовать вспомогательный метод [**ICaptureGraphBuilder2:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) .</span><span class="sxs-lookup"><span data-stu-id="03ffd-168">If you do need to find a particular pin on a filter, the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) helper method is useful.</span></span> <span data-ttu-id="03ffd-169">Укажите категорию, тип мультимедиа (видео или аудио), направление, а также укажите, должен ли ПИН-код быть неподключенным.</span><span class="sxs-lookup"><span data-stu-id="03ffd-169">Specify the category, the media type (video or audio), the direction, and whether the pin must be unconnected.</span></span>

<span data-ttu-id="03ffd-170">Например, следующий код выполняет поиск неподключенного ПИН-кода предварительной версии видео на фильтре записи:</span><span class="sxs-lookup"><span data-stu-id="03ffd-170">For example, the following code searches for an unconnected video preview pin on a capture filter:</span></span>


```C++
IPin *pPin = NULL;
hr = pBuild->FindPin(
    pCap,                   // Pointer to the filter to search.
    PINDIR_OUTPUT,          // Search for an output pin.
    &PIN_CATEGORY_PREVIEW,  // Search for a preview pin.
    &MEDIATYPE_Video,       // Search for a video pin.
    TRUE,                   // The pin must be unconnected. 
    0,                      // Return the first matching pin (index 0).
    &pPin);                 // This variable receives the IPin pointer.
if (SUCCESSFUL(hr))
{
    /* ... */
    pPin->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="03ffd-171">См. также</span><span class="sxs-lookup"><span data-stu-id="03ffd-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03ffd-172">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="03ffd-172">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
