---
description: Построение графа повторного сжатия
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: Построение графа повторного сжатия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8ea604bead34c22c123bbabe5d88e985006a9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894206"
---
# <a name="building-the-recompression-graph"></a><span data-ttu-id="420a4-103">Построение графа повторного сжатия</span><span class="sxs-lookup"><span data-stu-id="420a4-103">Building the Recompression Graph</span></span>

<span data-ttu-id="420a4-104">Типичный граф фильтра для повторного сжатия файла AVI выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="420a4-104">A typical filter graph for AVI file recompression looks like the following:</span></span>

![Граф повторного сжатия AVI](images/avi2avi4.png)

<span data-ttu-id="420a4-106">[Фильтр-разделитель AVI](avi-splitter-filter.md) извлекает данные из [фильтра источника файлов (Async)](file-source--async--filter.md) и анализирует их в видеопотоки и звуковые потоки.</span><span class="sxs-lookup"><span data-stu-id="420a4-106">The [AVI Splitter Filter](avi-splitter-filter.md) pulls data from the [File Source (Async) Filter](file-source--async--filter.md) and parses it into video and audio streams.</span></span> <span data-ttu-id="420a4-107">Программа декодирования видео декодирует сжатое видео, когда оно повторно сжимается программой сжатия видео.</span><span class="sxs-lookup"><span data-stu-id="420a4-107">The video decompressor decodes the compressed video, where it is recompressed by the video compressor.</span></span> <span data-ttu-id="420a4-108">Выбор декомпрессоров зависит от исходного файла. оно будет автоматически обработано [интеллектуальным подключением](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="420a4-108">The choice of decompressors depends on the source file; it will be handled automatically by [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="420a4-109">Приложение должно выбрать программу сжатия, как правило, путем показа пользователю списка.</span><span class="sxs-lookup"><span data-stu-id="420a4-109">The application must choose the compressor, typically by presenting a list to the user.</span></span> <span data-ttu-id="420a4-110">(См. раздел [Выбор фильтра сжатия](choosing-a-compression-filter.md).)</span><span class="sxs-lookup"><span data-stu-id="420a4-110">(See [Choosing a Compression Filter](choosing-a-compression-filter.md).)</span></span>

<span data-ttu-id="420a4-111">После этого сжатое видео переходит в [Фильтр мультиплексора AVI](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="420a4-111">The compressed video then goes to the [AVI Mux Filter](avi-mux-filter.md).</span></span> <span data-ttu-id="420a4-112">Аудиопоток в этом примере не сжимается, поэтому он перемещается непосредственно из AVI-разделителя в мультиплексор AVI.</span><span class="sxs-lookup"><span data-stu-id="420a4-112">The audio stream in this example is not compressed, so it goes directly from the AVI Splitter to the AVI Mux.</span></span> <span data-ttu-id="420a4-113">Мультиплексор AVI покидает два потока, а [фильтр записи файлов](file-writer-filter.md) записывает выходные данные на диск.</span><span class="sxs-lookup"><span data-stu-id="420a4-113">The AVI Mux interleaves the two streams, and the [File Writer Filter](file-writer-filter.md) writes the output to disk.</span></span> <span data-ttu-id="420a4-114">Обратите внимание, что требуется наличие AVI-мультиплексора, даже если у исходного файла нет звукового потока.</span><span class="sxs-lookup"><span data-stu-id="420a4-114">Note that the AVI Mux is required even if the original file does not have an audio stream.</span></span>

<span data-ttu-id="420a4-115">Самый простой способ создать диаграмму фильтра — использовать [Построитель диаграмм записи](capture-graph-builder.md), который является компонентом DirectShow для создания графов записи и других настраиваемых графов фильтра.</span><span class="sxs-lookup"><span data-stu-id="420a4-115">The easiest way to build this filter graph is to use the [Capture Graph Builder](capture-graph-builder.md), which is a DirectShow component for building capture graphs and other custom filter graphs.</span></span>

<span data-ttu-id="420a4-116">Начните с вызова CoCreateInstance для создания построителя графа записи:</span><span class="sxs-lookup"><span data-stu-id="420a4-116">Start by calling CoCreateInstance to create the Capture Graph Builder:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



<span data-ttu-id="420a4-117">Затем с помощью построителя графа записи создайте граф фильтра:</span><span class="sxs-lookup"><span data-stu-id="420a4-117">Then use the Capture Graph Builder to build the filter graph:</span></span>

1.  <span data-ttu-id="420a4-118">Создайте раздел отрисовки диаграммы, включающий фильтр мультиплексора и [модуль записи файлов](file-writer-filter.md)AVI.</span><span class="sxs-lookup"><span data-stu-id="420a4-118">Build the rendering section of the graph, which includes the AVI Mux filter and the [File Writer](file-writer-filter.md).</span></span>
2.  <span data-ttu-id="420a4-119">Добавьте фильтр источника и фильтр сжатия в граф.</span><span class="sxs-lookup"><span data-stu-id="420a4-119">Add the source filter and the compression filter to the graph.</span></span>
3.  <span data-ttu-id="420a4-120">Подключите фильтр источника к фильтру МУЛЬТИПЛЕКСОРа.</span><span class="sxs-lookup"><span data-stu-id="420a4-120">Connect the source filter to the MUX filter.</span></span> <span data-ttu-id="420a4-121">Построитель диаграмм записи вставляет любые фильтры разделителя и декодера, необходимые для анализа исходного файла.</span><span class="sxs-lookup"><span data-stu-id="420a4-121">The capture graph builder inserts whatever splitter and decoder filters are needed to parse the source file.</span></span> <span data-ttu-id="420a4-122">Он также может маршрутизировать видео-и звуковые потоки с помощью фильтров сжатия.</span><span class="sxs-lookup"><span data-stu-id="420a4-122">It can also route the video and audio streams through compression filters.</span></span>

<span data-ttu-id="420a4-123">В следующих разделах описывается каждый из этих шагов.</span><span class="sxs-lookup"><span data-stu-id="420a4-123">The following sections explain each of these steps.</span></span>

<span data-ttu-id="420a4-124">Создание раздела подготовки к просмотру</span><span class="sxs-lookup"><span data-stu-id="420a4-124">Build the Rendering Section</span></span>

<span data-ttu-id="420a4-125">Чтобы создать раздел отрисовки графа, вызовите метод [**ICaptureGraphBuilder2:: сетаутпутфиленаме**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) .</span><span class="sxs-lookup"><span data-stu-id="420a4-125">To build the rendering section of the graph, call the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method.</span></span> <span data-ttu-id="420a4-126">Этот метод принимает входные параметры, которые указывают подтип носителя для выходных данных и имя выходного файла.</span><span class="sxs-lookup"><span data-stu-id="420a4-126">This method takes input parameters that specify the media subtype for the output and the name of the output file.</span></span> <span data-ttu-id="420a4-127">Он возвращает указатели на фильтр МУЛЬТИПЛЕКСОРа и модуль записи файлов.</span><span class="sxs-lookup"><span data-stu-id="420a4-127">It returns pointers to the MUX filter and the file writer.</span></span> <span data-ttu-id="420a4-128">Фильтр МУЛЬТИПЛЕКСОРа необходим для следующего этапа построения Graph.</span><span class="sxs-lookup"><span data-stu-id="420a4-128">The MUX filter is needed for the next stage of graph building.</span></span> <span data-ttu-id="420a4-129">Для этого примера указатель на модуль записи файлов не требуется, поэтому параметр может иметь **значение NULL**:</span><span class="sxs-lookup"><span data-stu-id="420a4-129">The pointer to the file writer is not needed for this example, so that parameter can be **NULL**:</span></span>


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



<span data-ttu-id="420a4-130">Когда метод возвращает значение, фильтр МУЛЬТИПЛЕКСОРа имеет необработанный счетчик ссылок, поэтому не забудьте освободить указатель позже.</span><span class="sxs-lookup"><span data-stu-id="420a4-130">When the method returns, the MUX filter has an outstanding reference count, so be sure to release the pointer later.</span></span>

<span data-ttu-id="420a4-131">На следующей диаграмме показана диаграмма фильтра на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="420a4-131">The following diagram shows the filter graph at this point.</span></span>

![раздел подготовки к просмотру на графе фильтра](images/avi2avi1.png)

<span data-ttu-id="420a4-133">Фильтр МУЛЬТИПЛЕКСОРа предоставляет два интерфейса для управления форматом AVI:</span><span class="sxs-lookup"><span data-stu-id="420a4-133">The MUX filter exposes two interfaces for controlling the AVI format:</span></span>

-   <span data-ttu-id="420a4-134">[**Интерфейс иконфигинтерлеавинг**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): задает режим взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="420a4-134">[**IConfigInterleaving Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): Sets the interleaving mode.</span></span>
-   <span data-ttu-id="420a4-135">[**Интерфейс иконфигавимукс**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): задает главный поток и Индекс совместимости AVI.</span><span class="sxs-lookup"><span data-stu-id="420a4-135">[**IConfigAviMux Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): Sets the master stream and the AVI compatibility index.</span></span>

<span data-ttu-id="420a4-136">Добавление фильтров источника и сжатия</span><span class="sxs-lookup"><span data-stu-id="420a4-136">Add the Source and Compression Filters</span></span>

<span data-ttu-id="420a4-137">Следующим шагом является добавление фильтров источника и сжатия к графу фильтра.</span><span class="sxs-lookup"><span data-stu-id="420a4-137">The next step is to add the source and compression filters to the filter graph.</span></span> <span data-ttu-id="420a4-138">Построитель диаграмм для записи автоматически создает экземпляр диспетчера графа фильтров при вызове Сетаутпутфиленаме.</span><span class="sxs-lookup"><span data-stu-id="420a4-138">The Capture Graph Builder automatically creates an instance of the Filter Graph Manager when you call SetOutputFileName.</span></span> <span data-ttu-id="420a4-139">Получите указатель на него, вызвав метод [**ICaptureGraphBuilder2:: жетфилтерграф**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) :</span><span class="sxs-lookup"><span data-stu-id="420a4-139">Get a pointer to it by calling the [**ICaptureGraphBuilder2::GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) method:</span></span>


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



<span data-ttu-id="420a4-140">Теперь вызовите метод [**играфбуилдер:: аддсаурцефилтер**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) , чтобы добавить фильтр источника асинхронного файла, и метод [**Ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , чтобы добавить видео компрессор:</span><span class="sxs-lookup"><span data-stu-id="420a4-140">Now call the [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) method to add the Async File Source filter, and the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method to add the video compressor:</span></span>


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



<span data-ttu-id="420a4-141">На этом этапе фильтр источника и фильтр сжатия не подключены ни к чему другому в графе, как показано на следующем рисунке:</span><span class="sxs-lookup"><span data-stu-id="420a4-141">At this point, the source filter and the compression filter are not connected to anything else in the graph, as shown in the following illustration:</span></span>

![Фильтрация графа с помощью фильтров источника и сжатия](images/avi2avi2.png)

<span data-ttu-id="420a4-143">Подключение источника к мультиплексору</span><span class="sxs-lookup"><span data-stu-id="420a4-143">Connect the Source to the Mux</span></span>

<span data-ttu-id="420a4-144">Последним шагом является подключение фильтра по источнику к фильтру мультиплексора AVI через видео-компрессор.</span><span class="sxs-lookup"><span data-stu-id="420a4-144">The final step is to connect the source filter to the AVI Mux filter, through the video compressor.</span></span> <span data-ttu-id="420a4-145">Используйте метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , который подключает выходной ПИН-код к фильтру источника к указанному фильтру приемника (при необходимости с помощью фильтра сжатия).</span><span class="sxs-lookup"><span data-stu-id="420a4-145">Use the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method, which connects an output pin on the source filter to a specified sink filter, optionally through a compression filter.</span></span>

<span data-ttu-id="420a4-146">Первые два параметра указывают, какой из ПИН-кодов фильтра источника подключается, путем назначения категории закрепления и типа носителя.</span><span class="sxs-lookup"><span data-stu-id="420a4-146">The first two parameters specify which of the source filter's pins to connect, by designating a pin category and a media type.</span></span> <span data-ttu-id="420a4-147">Фильтр источника "асинхронный файл" имеет только один выходной ПИН-код, поэтому эти параметры должны иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="420a4-147">The Async File Source filter has only one output pin, so these parameters should be **NULL**.</span></span> <span data-ttu-id="420a4-148">Следующие три параметра указывают фильтр источника, фильтр сжатия (если он есть) и фильтр мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="420a4-148">The next three parameters specify the source filter, the compression filter (if any), and the Mux filter.</span></span>

<span data-ttu-id="420a4-149">В следующем примере кода демонстрируется визуализация видеопотока через видео-компрессор.</span><span class="sxs-lookup"><span data-stu-id="420a4-149">The following code example renders the video stream through the video compressor:</span></span>


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



<span data-ttu-id="420a4-150">На схеме ниже показан граф фильтра на данный момент.</span><span class="sxs-lookup"><span data-stu-id="420a4-150">The following diagram shows the filter graph so far.</span></span>

![Визуализированный поток видео](images/avi2avi3.png)

<span data-ttu-id="420a4-152">При условии, что исходный файл имеет звуковой поток, фильтр [разделителя AVI](avi-splitter-filter.md) создал выходной ПИН-код для аудио.</span><span class="sxs-lookup"><span data-stu-id="420a4-152">Assuming that the source file has an audio stream, the [AVI Splitter](avi-splitter-filter.md) filter has created an output pin for the audio.</span></span> <span data-ttu-id="420a4-153">Чтобы подключить этот ПИН-код, вызовите RenderStream еще раз:</span><span class="sxs-lookup"><span data-stu-id="420a4-153">To connect this pin, call RenderStream again:</span></span>


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



<span data-ttu-id="420a4-154">Здесь не указан фильтр сжатия.</span><span class="sxs-lookup"><span data-stu-id="420a4-154">Here, no compression filter is specified.</span></span> <span data-ttu-id="420a4-155">Выходной ПИН-код фильтра источника уже подключен, поэтому метод RenderStream выполняет поиск неподключенного выходного контакта в фильтре разделителя.</span><span class="sxs-lookup"><span data-stu-id="420a4-155">The source filter's output pin is already connected, so the RenderStream method searches for an unconnected output pin on the splitter filter.</span></span> <span data-ttu-id="420a4-156">Он находит звуковой ПИН-код и подключает его непосредственно к фильтру МУЛЬТИПЛЕКСОРа.</span><span class="sxs-lookup"><span data-stu-id="420a4-156">It finds the audio pin and connects it directly to the MUX filter.</span></span> <span data-ttu-id="420a4-157">Если исходный файл не имеет аудиопотока, второй вызов RenderStream завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="420a4-157">If the source file does not have an audio stream, the second call to RenderStream will fail.</span></span> <span data-ttu-id="420a4-158">Это нормальная ситуация.</span><span class="sxs-lookup"><span data-stu-id="420a4-158">This is expected behavior.</span></span> <span data-ttu-id="420a4-159">Граф завершается после первого вызова RenderStream, поэтому сбой второго вызова является безвредным.</span><span class="sxs-lookup"><span data-stu-id="420a4-159">The graph is complete after the first call to RenderStream, so the failure in the second call is harmless.</span></span>

<span data-ttu-id="420a4-160">В этом примере важен порядок двух вызовов RenderStream.</span><span class="sxs-lookup"><span data-stu-id="420a4-160">In this example, the order of the two RenderStream calls is important.</span></span> <span data-ttu-id="420a4-161">Поскольку второй вызов не задает компрессор, он подключается к любому неподключенному ПИН-коду из разделителя AVI.</span><span class="sxs-lookup"><span data-stu-id="420a4-161">Because the second call does not specify a compressor, it will connect any unconnected pin from the AVI Splitter.</span></span> <span data-ttu-id="420a4-162">Если вы сделаете этот вызов еще до другого, он может подключить видеопоток к мультиплексору в виде AVI, без сжатия видео.</span><span class="sxs-lookup"><span data-stu-id="420a4-162">If you make this call before the other one, it might connect the video stream to the AVI Mux, without your video compressor.</span></span> <span data-ttu-id="420a4-163">Поэтому сначала должен быть вызван более конкретный вызов (с фильтром сжатия).</span><span class="sxs-lookup"><span data-stu-id="420a4-163">Therefore, the more specific call (with the compression filter) must happen first.</span></span>

<span data-ttu-id="420a4-164">В предыдущем обсуждении предполагается, что исходный файл является файлом AVI.</span><span class="sxs-lookup"><span data-stu-id="420a4-164">The previous discussion has assumed that the source file is an AVI file.</span></span> <span data-ttu-id="420a4-165">Однако эта методика также работает с другими типами файлов, например с файлами MPEG.</span><span class="sxs-lookup"><span data-stu-id="420a4-165">However, this technique also works with other file types, such as MPEG files.</span></span> <span data-ttu-id="420a4-166">Итоговый граф фильтра будет немного отличаться.</span><span class="sxs-lookup"><span data-stu-id="420a4-166">The resulting filter graph will be somewhat different.</span></span>

## <a name="related-topics"></a><span data-ttu-id="420a4-167">См. также</span><span class="sxs-lookup"><span data-stu-id="420a4-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="420a4-168">Повторное сжатие файла AVI</span><span class="sxs-lookup"><span data-stu-id="420a4-168">Recompressing an AVI File</span></span>](recompressing-an-avi-file.md)
</dt> </dl>

 

 



