---
description: Запись проекта в файл
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: Запись проекта в файл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f63ddbc6a021362134d420220f7e25c662553f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683625"
---
# <a name="writing-a-project-to-a-file"></a><span data-ttu-id="36a6e-103">Запись проекта в файл</span><span class="sxs-lookup"><span data-stu-id="36a6e-103">Writing a Project to a File</span></span>

<span data-ttu-id="36a6e-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="36a6e-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="36a6e-105">В этой статье описывается, как записать проект [служб редактирования DirectShow](directshow-editing-services.md) в файл.</span><span class="sxs-lookup"><span data-stu-id="36a6e-105">This article describes how to write a [DirectShow Editing Services](directshow-editing-services.md) project to a file.</span></span> <span data-ttu-id="36a6e-106">Сначала он описывает, как записать файл с помощью базовой подсистемы визуализации.</span><span class="sxs-lookup"><span data-stu-id="36a6e-106">First it describes how to write a file with the basic render engine.</span></span> <span data-ttu-id="36a6e-107">Затем он описывает интеллектуальное повторное сжатие с помощью интеллектуального механизма визуализации.</span><span class="sxs-lookup"><span data-stu-id="36a6e-107">Then it describes smart recompression with the smart render engine.</span></span>

<span data-ttu-id="36a6e-108">Общие сведения о визуализации проектов в службах редактирования DirectShow см. [в разделе о механизмах подготовки](about-the-render-engines.md)отчетов.</span><span class="sxs-lookup"><span data-stu-id="36a6e-108">For an overview of how DirectShow Editing Services renders projects, see [About the Render Engines](about-the-render-engines.md).</span></span>

<span data-ttu-id="36a6e-109">**Использование базового механизма визуализации**</span><span class="sxs-lookup"><span data-stu-id="36a6e-109">**Using the Basic Render Engine**</span></span>

<span data-ttu-id="36a6e-110">Начните с создания внешнего интерфейса графа следующим образом:</span><span class="sxs-lookup"><span data-stu-id="36a6e-110">Start by building the front end of the graph, as follows:</span></span>

1.  <span data-ttu-id="36a6e-111">Создайте подсистему визуализации.</span><span class="sxs-lookup"><span data-stu-id="36a6e-111">Create the render engine.</span></span>
2.  <span data-ttu-id="36a6e-112">Укажите временную шкалу.</span><span class="sxs-lookup"><span data-stu-id="36a6e-112">Specify the timeline.</span></span>
3.  <span data-ttu-id="36a6e-113">Задайте диапазон отрисовки.</span><span class="sxs-lookup"><span data-stu-id="36a6e-113">Set the render range.</span></span> <span data-ttu-id="36a6e-114">(необязательно)</span><span class="sxs-lookup"><span data-stu-id="36a6e-114">(Optional)</span></span>
4.  <span data-ttu-id="36a6e-115">Создание внешнего интерфейса графа.</span><span class="sxs-lookup"><span data-stu-id="36a6e-115">Build the front end of the graph.</span></span>

<span data-ttu-id="36a6e-116">Эти шаги показаны в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="36a6e-116">The following code example shows these steps.</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



<span data-ttu-id="36a6e-117">Далее добавьте к графу фильтров фильтры для мультиплексирования и записи файлов.</span><span class="sxs-lookup"><span data-stu-id="36a6e-117">Next, add multiplexer and file-writing filters to the filter graph.</span></span> <span data-ttu-id="36a6e-118">Проще всего это сделать с помощью [построителя графа записи](capture-graph-builder.md), компонента DirectShow для создания графов записи.</span><span class="sxs-lookup"><span data-stu-id="36a6e-118">The easiest way to do this is with the [Capture Graph Builder](capture-graph-builder.md), a DirectShow component for building capture graphs.</span></span> <span data-ttu-id="36a6e-119">Построитель графов записи предоставляет интерфейс [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="36a6e-119">The capture graph builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="36a6e-120">Выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="36a6e-120">Perform the following steps:</span></span>

1.  <span data-ttu-id="36a6e-121">Создайте экземпляр построителя графа записи.</span><span class="sxs-lookup"><span data-stu-id="36a6e-121">Create an instance of the capture graph builder.</span></span>
2.  <span data-ttu-id="36a6e-122">Получите указатель на граф и передайте его в построитель Graph.</span><span class="sxs-lookup"><span data-stu-id="36a6e-122">Obtain a pointer to the graph and pass it to the graph builder.</span></span>
3.  <span data-ttu-id="36a6e-123">Укажите имя и тип носителя для выходного файла.</span><span class="sxs-lookup"><span data-stu-id="36a6e-123">Specify the name and media type of the output file.</span></span> <span data-ttu-id="36a6e-124">Этот шаг также получает указатель на фильтр мультиплексора, который требуется позже.</span><span class="sxs-lookup"><span data-stu-id="36a6e-124">This step also obtains a pointer to the mux filter, which is required later.</span></span>

<span data-ttu-id="36a6e-125">Эти шаги показаны в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="36a6e-125">The following code example shows these steps.</span></span>


```C++
CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, CLSCTX_INPROC, 
    IID_ICaptureGraphBuilder2, (void **)&pBuilder);

// Get a pointer to the graph front end.
IGraphBuilder *pGraph;
pRender->GetFilterGraph(&pGraph);
pBuilder->SetFiltergraph(pGraph);

// Create the file-writing section.
IBaseFilter *pMux;
pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("Output.avi"), &pMux, NULL);
```



<span data-ttu-id="36a6e-126">Наконец, подключите выходные контакты на внешнем интерфейсе к фильтру мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="36a6e-126">Finally, connect the output pins on the front end to the mux filter.</span></span>

1.  <span data-ttu-id="36a6e-127">Получение числа групп.</span><span class="sxs-lookup"><span data-stu-id="36a6e-127">Retrieve the number of groups.</span></span>
2.  <span data-ttu-id="36a6e-128">Для каждого ПИН-кода получите указатель на ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="36a6e-128">For each pin, obtain a pointer to the pin.</span></span>
3.  <span data-ttu-id="36a6e-129">При необходимости создайте экземпляр фильтра сжатия для сжатия потока.</span><span class="sxs-lookup"><span data-stu-id="36a6e-129">Optionally, create an instance of a compression filter to compress the stream.</span></span> <span data-ttu-id="36a6e-130">Тип сжатия будет зависеть от типа носителя группы.</span><span class="sxs-lookup"><span data-stu-id="36a6e-130">The type of compressor will depend on the media type of the group.</span></span> <span data-ttu-id="36a6e-131">[Перечислитель системных устройств](system-device-enumerator.md) можно использовать для перечисления доступных фильтров сжатия.</span><span class="sxs-lookup"><span data-stu-id="36a6e-131">You can use the [System Device Enumerator](system-device-enumerator.md) to enumerate the available compression filters.</span></span> <span data-ttu-id="36a6e-132">Дополнительные сведения см. в разделе [Перечисление устройств и фильтров](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="36a6e-132">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>
4.  <span data-ttu-id="36a6e-133">При необходимости задайте параметры сжатия, такие как частота ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="36a6e-133">Optionally, set compression parameters such as the key-frame rate.</span></span> <span data-ttu-id="36a6e-134">Этот шаг подробно описан далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="36a6e-134">This step is discussed in detail later in the article.</span></span>
5.  <span data-ttu-id="36a6e-135">Вызовите [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span><span class="sxs-lookup"><span data-stu-id="36a6e-135">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span> <span data-ttu-id="36a6e-136">Этот метод принимает указатели на ПИН-код, фильтр сжатия (если он есть) и мультиплексор.</span><span class="sxs-lookup"><span data-stu-id="36a6e-136">This method takes pointers to the pin, the compression filter (if any), and the multiplexer.</span></span>

<span data-ttu-id="36a6e-137">В следующем примере кода показано, как подключить выходные контакты.</span><span class="sxs-lookup"><span data-stu-id="36a6e-137">The following code example shows how to connect the output pins.</span></span>


```C++
long NumGroups;
pTimeline->GetGroupCount(&NumGroups);

// Loop through the groups and get the output pins.
for (i = 0; i < NumGroups; i++)
{
    IPin *pPin;
    if (pRender->GetGroupOutputPin(i, &pPin) == S_OK) 
    {
        IBaseFilter *pCompressor;
        // Create a compressor filter. (Not shown.)
        // Set compression parameters. (Not shown.)

        // Connect the pin.
        pBuilder->RenderStream(NULL, NULL, pPin, pCompressor, pMux);
        pCompressor->Release();
        pPin->Release();
    }
}
```



<span data-ttu-id="36a6e-138">Чтобы задать параметры сжатия (шаг 4, ранее), используйте интерфейс [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) .</span><span class="sxs-lookup"><span data-stu-id="36a6e-138">To set compression parameters (step 4, previously), use the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface.</span></span> <span data-ttu-id="36a6e-139">Этот интерфейс предоставляется на выходных контактах фильтров сжатия.</span><span class="sxs-lookup"><span data-stu-id="36a6e-139">This interface is exposed on the output pins of compression filters.</span></span> <span data-ttu-id="36a6e-140">Перечислите ПИН-коды фильтра сжатия и запросите все выходные данные для **иамвидеокомпрессион**.</span><span class="sxs-lookup"><span data-stu-id="36a6e-140">Enumerate the compression filter's pins, and query each output pin for **IAMVideoCompression**.</span></span> <span data-ttu-id="36a6e-141">(Дополнительные сведения о перечислении ПИН-кодов см. в разделе [перечисление ПИН](enumerating-pins.md)-кодов.) Не забудьте освободить все указатели интерфейса, полученные на этом шаге.</span><span class="sxs-lookup"><span data-stu-id="36a6e-141">(For information about enumerating pins, see [Enumerating Pins](enumerating-pins.md).) Be sure to release all the interface pointers that you obtained during this step.</span></span>

<span data-ttu-id="36a6e-142">После построения графа фильтра вызовите метод [**имедиаконтрол:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) в диспетчере графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="36a6e-142">After you build the filter graph, call the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method on the filter graph manager.</span></span> <span data-ttu-id="36a6e-143">При выполнении графа фильтра данные записываются в файл.</span><span class="sxs-lookup"><span data-stu-id="36a6e-143">As the filter graph runs, it writes the data to a file.</span></span> <span data-ttu-id="36a6e-144">Используйте уведомление о событии, чтобы дождаться завершения воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="36a6e-144">Use event notification to wait for playback to complete.</span></span> <span data-ttu-id="36a6e-145">(См. раздел [реагирование на события](responding-to-events.md).) По завершении воспроизведения необходимо явно вызвать [**имедиаконтрол:: останавливаться**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) , чтобы прерывать граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="36a6e-145">(See [Responding to Events](responding-to-events.md).) When playback finishes, you must explicitly call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) to stop the filter graph.</span></span> <span data-ttu-id="36a6e-146">В противном случае файл будет записан неправильно.</span><span class="sxs-lookup"><span data-stu-id="36a6e-146">Otherwise, the file is not written correctly.</span></span>

<span data-ttu-id="36a6e-147">**Использование подсистемы интеллектуального просмотра**</span><span class="sxs-lookup"><span data-stu-id="36a6e-147">**Using the Smart Render Engine**</span></span>

<span data-ttu-id="36a6e-148">Чтобы получить преимущества интеллектуального повторного сжатия, используйте интеллектуальный механизм визуализации вместо базового механизма визуализации.</span><span class="sxs-lookup"><span data-stu-id="36a6e-148">To get the benefits of smart recompression, use the smart render engine in place of the basic render engine.</span></span> <span data-ttu-id="36a6e-149">Шаги по созданию графа практически одинаковы.</span><span class="sxs-lookup"><span data-stu-id="36a6e-149">The steps in building the graph are almost the same.</span></span> <span data-ttu-id="36a6e-150">Основное различие заключается в том, что сжатие обрабатывается на внешнем интерфейсе графа, а не в разделе, предназначенном для записи файлов.</span><span class="sxs-lookup"><span data-stu-id="36a6e-150">The major difference is that compression is handled in the front end of the graph, not in the file-writing section.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36a6e-151">Не используйте интеллектуальный модуль визуализации для чтения или записи файлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="36a6e-151">Do not use the smart render engine to read or write Windows Media files.</span></span>

 

<span data-ttu-id="36a6e-152">Каждая группа видео имеет свойство, определяющее формат сжатия для этой группы.</span><span class="sxs-lookup"><span data-stu-id="36a6e-152">Each video group has a property that specifies the compression format for that group.</span></span> <span data-ttu-id="36a6e-153">Формат сжатия должен точно совпадать с форматом несжатой группы по высоте, ширине, глубине бит и частоте кадров.</span><span class="sxs-lookup"><span data-stu-id="36a6e-153">The compression format must exactly match the group's uncompressed format in height, width, bit depth, and frame rate.</span></span> <span data-ttu-id="36a6e-154">Интеллектуальный механизм визуализации использует формат сжатия при создании графа.</span><span class="sxs-lookup"><span data-stu-id="36a6e-154">The smart render engine uses the compression format when it constructs the graph.</span></span> <span data-ttu-id="36a6e-155">Перед установкой формата сжатия обязательно задайте несжатый формат для этой группы, вызвав [**иамтимелинеграуп:: сетмедиатипе**](iamtimelinegroup-setmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="36a6e-155">Before you set the compression format, make sure to set the uncompressed format for that group by calling [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md).</span></span>

<span data-ttu-id="36a6e-156">Чтобы задать формат сжатия группы, вызовите метод [**иамтимелинеграуп:: сетсмартрекомпрессформат**](iamtimelinegroup-setsmartrecompressformat.md) .</span><span class="sxs-lookup"><span data-stu-id="36a6e-156">To set a group's compression format, call the [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method.</span></span> <span data-ttu-id="36a6e-157">Этот метод принимает указатель на структуру [**SCompFmt0**](scompfmt0.md) .</span><span class="sxs-lookup"><span data-stu-id="36a6e-157">This method takes a pointer to an [**SCompFmt0**](scompfmt0.md) structure.</span></span> <span data-ttu-id="36a6e-158">Структура **SCompFmt0** имеет два члена: **нформатид**, который должен равняться нулю, и **mediaType**, который является структурой [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="36a6e-158">The **SCompFmt0** structure has two members: **nFormatId**, which must be zero, and **MediaType**, which is an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="36a6e-159">Инициализируйте **структуру \_ \_ типа файлов мультимедиа** , используя сведения о форматировании.</span><span class="sxs-lookup"><span data-stu-id="36a6e-159">Initialize the **AM\_MEDIA\_TYPE** structure with the format information.</span></span>

> [!Note]  
> <span data-ttu-id="36a6e-160">Если вы хотите, чтобы окончательный проект имел тот же формат, что и один из исходных файлов, можно получить \_ структуру типа файлов мультимедиа, \_ непосредственно исходя из исходного файла, используя средство обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="36a6e-160">If you want the final project to have the same format as one of your source files, you can get the AM\_MEDIA\_TYPE structure directly from the source file, using the media detector.</span></span> <span data-ttu-id="36a6e-161">См. раздел [**имедиадет:: Get \_ стреаммедиатипе**](imediadet-get-streammediatype.md).</span><span class="sxs-lookup"><span data-stu-id="36a6e-161">See [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md).</span></span>

 

<span data-ttu-id="36a6e-162">Приведите переменную [**SCompFmt0**](scompfmt0.md) к указателю типа **Long**, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="36a6e-162">Cast the [**SCompFmt0**](scompfmt0.md) variable to a pointer of type **long**, as shown in the following example.</span></span>


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



<span data-ttu-id="36a6e-163">Интеллектуальный механизм визуализации автоматически ищет совместимый фильтр сжатия.</span><span class="sxs-lookup"><span data-stu-id="36a6e-163">The smart render engine automatically searches for a compatible compression filter.</span></span> <span data-ttu-id="36a6e-164">Можно также указать фильтр сжатия для группы, вызвав [**исмартрендеренгине:: сетграупкомпрессор**](ismartrenderengine-setgroupcompressor.md).</span><span class="sxs-lookup"><span data-stu-id="36a6e-164">You can also specify a compression filter for a group by calling [**ISmartRenderEngine::SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).</span></span>

<span data-ttu-id="36a6e-165">Чтобы построить граф, выполните те же действия, которые были описаны для базового механизма отрисовки в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="36a6e-165">To build the graph, use the same steps that were described for the Basic Render Engine in the previous section.</span></span> <span data-ttu-id="36a6e-166">Ниже приведены единственные отличия.</span><span class="sxs-lookup"><span data-stu-id="36a6e-166">The only differences are the following:</span></span>

-   <span data-ttu-id="36a6e-167">Используйте интеллектуальный механизм визуализации, а не базовый механизм визуализации.</span><span class="sxs-lookup"><span data-stu-id="36a6e-167">Use the smart render engine, not the basic render engine.</span></span> <span data-ttu-id="36a6e-168">Идентификатор класса — CLSID \_ смартрендеренгине.</span><span class="sxs-lookup"><span data-stu-id="36a6e-168">The class identifier is CLSID\_SmartRenderEngine.</span></span>
-   <span data-ttu-id="36a6e-169">Задайте параметры сжатия после сборки внешнего интерфейса, но перед отрисовкой выходных закрепления.</span><span class="sxs-lookup"><span data-stu-id="36a6e-169">Set compression parameters after you build the front end but before you render the output pins.</span></span> <span data-ttu-id="36a6e-170">Вызовите метод [**исмартрендеренгине:: жетграупкомпрессор**](ismartrenderengine-getgroupcompressor.md) , чтобы получить указатель на фильтр сжатия группы.</span><span class="sxs-lookup"><span data-stu-id="36a6e-170">Call the [**ISmartRenderEngine::GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) method to obtain a pointer to a group's compression filter.</span></span> <span data-ttu-id="36a6e-171">Затем запросите интерфейс [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , как описано выше.</span><span class="sxs-lookup"><span data-stu-id="36a6e-171">Then query for the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface, as described previously.</span></span>
-   <span data-ttu-id="36a6e-172">При отрисовке выходных контактов нет необходимости вставлять фильтр сжатия.</span><span class="sxs-lookup"><span data-stu-id="36a6e-172">When you render the output pins, there is no need to insert a compression filter.</span></span> <span data-ttu-id="36a6e-173">Поток уже сжат.</span><span class="sxs-lookup"><span data-stu-id="36a6e-173">The stream is already compressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36a6e-174">См. также</span><span class="sxs-lookup"><span data-stu-id="36a6e-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36a6e-175">Подготовка проекта</span><span class="sxs-lookup"><span data-stu-id="36a6e-175">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



