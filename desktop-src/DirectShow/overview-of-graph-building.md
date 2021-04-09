---
description: Общие сведения о построении графов
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Общие сведения о построении графов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69ef9ea0f4f9e21d33372ad2a37a59b512d5dcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139895"
---
# <a name="overview-of-graph-building"></a><span data-ttu-id="9121c-103">Общие сведения о построении графов</span><span class="sxs-lookup"><span data-stu-id="9121c-103">Overview of Graph Building</span></span>

<span data-ttu-id="9121c-104">Чтобы создать граф фильтра, начните с создания экземпляра диспетчера графа фильтров:</span><span class="sxs-lookup"><span data-stu-id="9121c-104">To create a filter graph, begin by creating an instance of the Filter Graph Manager:</span></span>


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



<span data-ttu-id="9121c-105">Диспетчер графов фильтров поддерживает следующие методы построения диаграмм:</span><span class="sxs-lookup"><span data-stu-id="9121c-105">The Filter Graph Manager supports the following graph-building methods:</span></span>

-   <span data-ttu-id="9121c-106">[**Ифилтерграф:: коннектдирект**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) пытается установить прямое соединение между двумя контактами.</span><span class="sxs-lookup"><span data-stu-id="9121c-106">[**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) tries to make a direct connection between two pins.</span></span> <span data-ttu-id="9121c-107">Если ПИН-коды не могут подключиться, метод завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="9121c-107">If the pins cannot connect, the method fails.</span></span>
-   <span data-ttu-id="9121c-108">[**Играфбуилдер:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) соединяет два контакта.</span><span class="sxs-lookup"><span data-stu-id="9121c-108">[**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connects two pins.</span></span> <span data-ttu-id="9121c-109">По возможности он устанавливает прямое соединение.</span><span class="sxs-lookup"><span data-stu-id="9121c-109">If possible, it makes a direct connection.</span></span> <span data-ttu-id="9121c-110">В противном случае для завершения подключения используются промежуточные фильтры.</span><span class="sxs-lookup"><span data-stu-id="9121c-110">Otherwise, it uses intermediate filters to complete the connection.</span></span>
-   <span data-ttu-id="9121c-111">[**Играфбуилдер:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) начинается с выходного ПИН-кода и создает оставшуюся часть графа.</span><span class="sxs-lookup"><span data-stu-id="9121c-111">[**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) starts from an output pin and builds the rest of the graph.</span></span> <span data-ttu-id="9121c-112">Эти методы добавляют фильтры по мере необходимости, работают нисходящими, пока не достигнет фильтра модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="9121c-112">This methods adds filters as needed, working downstream, until it reaches a renderer filter.</span></span>
-   <span data-ttu-id="9121c-113">[**Играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) создает полный граф воспроизведения файлов.</span><span class="sxs-lookup"><span data-stu-id="9121c-113">[**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) builds a complete file-playback graph.</span></span>
-   <span data-ttu-id="9121c-114">[**Ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) добавляет фильтр в граф.</span><span class="sxs-lookup"><span data-stu-id="9121c-114">[**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) adds a filter to the graph.</span></span> <span data-ttu-id="9121c-115">Он не подключается к фильтру.</span><span class="sxs-lookup"><span data-stu-id="9121c-115">It does not connect the filter.</span></span> <span data-ttu-id="9121c-116">Перед вызовом этого метода необходимо создать фильтр, вызвав **CoCreateInstance** или перечислителя фильтров или перечислитель системных устройств.</span><span class="sxs-lookup"><span data-stu-id="9121c-116">You must create the filter before calling this method, either by calling **CoCreateInstance** or by using the Filter Mapper or System Device Enumerator.</span></span>

<span data-ttu-id="9121c-117">Эти методы предоставляют три основных подхода к построению графа:</span><span class="sxs-lookup"><span data-stu-id="9121c-117">These methods provide three basic approaches to building the graph:</span></span>

1.  <span data-ttu-id="9121c-118">Диспетчер графов фильтров строит весь граф.</span><span class="sxs-lookup"><span data-stu-id="9121c-118">The Filter Graph Manager builds the entire graph.</span></span>
2.  <span data-ttu-id="9121c-119">Диспетчер графов фильтров строит часть графа.</span><span class="sxs-lookup"><span data-stu-id="9121c-119">The Filter Graph Manager builds part of the graph.</span></span>
3.  <span data-ttu-id="9121c-120">Приложение создает весь граф.</span><span class="sxs-lookup"><span data-stu-id="9121c-120">The application builds the entire graph.</span></span>

<span data-ttu-id="9121c-121">**Диспетчер графов фильтров строит весь граф**</span><span class="sxs-lookup"><span data-stu-id="9121c-121">**The Filter Graph Manager Builds the Entire Graph**</span></span>

<span data-ttu-id="9121c-122">Если нужно просто воспроизвести файл, созданный в известном формате, например AVI, MPEG, WAV или MP3, используйте метод **RenderFile** .</span><span class="sxs-lookup"><span data-stu-id="9121c-122">If you simply want to play a file that is authored in a recognized format, such as AVI, MPEG, WAV, or MP3, use the **RenderFile** method.</span></span> <span data-ttu-id="9121c-123">В статье [как воспроизвести файл](how-to-play-a-file.md) показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="9121c-123">The article [How To Play a File](how-to-play-a-file.md) shows how to do this.</span></span>

<span data-ttu-id="9121c-124">Метод **RenderFile** начинается с просмотра в реестре исходного фильтра, который может проанализировать файл.</span><span class="sxs-lookup"><span data-stu-id="9121c-124">The **RenderFile** method starts by looking in the registry for a source filter that can parse the file.</span></span> <span data-ttu-id="9121c-125">Он использует протокол (например `https://` , в URL-адресе), расширение файла или предварительно определенные шаблоны байтов в файле для определения фильтра источника.</span><span class="sxs-lookup"><span data-stu-id="9121c-125">It uses the protocol (such as " `https://` " in the URL), the file extension, or pre-defined byte patterns in the file to determine the source filter.</span></span> <span data-ttu-id="9121c-126">Дополнительные сведения см. [в разделе Регистрация пользовательского типа файлов](registering-a-custom-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="9121c-126">For details, see [Registering a Custom File Type](registering-a-custom-file-type.md).</span></span>

<span data-ttu-id="9121c-127">Чтобы построить остальную часть графа, диспетчер графов фильтров использует итеративный процесс, где он принимает типы мультимедиа, поддерживаемые фильтром, на закреплениях вывода, а также выполняет поиск фильтров в реестре, которые принимают этот тип мультимедиа в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="9121c-127">To build the rest of the graph, the Filter Graph Manager uses an iterative process wherein it takes the media types that a filter supports on its output pins, and searches the registry for filters that will accept that media type as input.</span></span> <span data-ttu-id="9121c-128">Он использует несколько критериев, чтобы сократить количество фильтров поиска и приоритизации:</span><span class="sxs-lookup"><span data-stu-id="9121c-128">It uses several criteria to narrow the search and prioritize filters:</span></span>

-   <span data-ttu-id="9121c-129">*Категория фильтра* определяет общие функциональные возможности фильтра.</span><span class="sxs-lookup"><span data-stu-id="9121c-129">The *filter category* identifies the general functionality of the filter.</span></span>
-   <span data-ttu-id="9121c-130">Тип носителя описывает, какие данные может принимать фильтр в качестве входных данных или доставки в качестве выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9121c-130">The media type describes what kind of data the filter can accept as input or deliver as output.</span></span>
-   <span data-ttu-id="9121c-131">Неудача *определяет порядок* , в котором будут применяться фильтры.</span><span class="sxs-lookup"><span data-stu-id="9121c-131">The *merit* determines the order in which filters are tried.</span></span> <span data-ttu-id="9121c-132">Если два фильтра в одной и той же категории фильтров поддерживают одни и те же типы входных данных, диспетчер графа фильтров выбирает один из них с наибольшим значением.</span><span class="sxs-lookup"><span data-stu-id="9121c-132">If two filters in the same filter category both support the same input types, the Filter Graph Manager selects the one with the highest merit value.</span></span> <span data-ttu-id="9121c-133">Некоторым фильтрам назначено небольшое значение, поскольку они предназначены для специализированных целей и должны добавляться только в граф приложения.</span><span class="sxs-lookup"><span data-stu-id="9121c-133">Some filters are purposely given a low merit value because they are designed for specialized purposes and should only be added to the graph by the application.</span></span>

<span data-ttu-id="9121c-134">Диспетчер графов фильтров использует объект [сопоставителя фильтров](filter-mapper.md) для поиска в реестре.</span><span class="sxs-lookup"><span data-stu-id="9121c-134">The Filter Graph Manager uses the [Filter Mapper](filter-mapper.md) object to search the registry.</span></span>

<span data-ttu-id="9121c-135">При добавлении каждого фильтра диспетчер графа фильтров пытается подключить его к выходному ПИН-коду предыдущего фильтра.</span><span class="sxs-lookup"><span data-stu-id="9121c-135">As each filter is added, the Filter Graph Manager tries to connect it to the previous filter's output pin.</span></span> <span data-ttu-id="9121c-136">Фильтры согласовываются, чтобы определить, могут ли они подключаться, и, если да, какой тип носителя использовать для соединения.</span><span class="sxs-lookup"><span data-stu-id="9121c-136">The filters negotiate to determine whether they can connect, and if so, what media type to use for the connection.</span></span> <span data-ttu-id="9121c-137">Если новый фильтр не может подключиться, диспетчер графа фильтра отклоняет его и пытается выполнить другой фильтр.</span><span class="sxs-lookup"><span data-stu-id="9121c-137">If the new filter cannot connect, the Filter Graph Manager discards it and tries another filter.</span></span> <span data-ttu-id="9121c-138">Этот процесс продолжится до подготовки каждого потока.</span><span class="sxs-lookup"><span data-stu-id="9121c-138">This process continues until every stream is rendered.</span></span>

<span data-ttu-id="9121c-139">**Диспетчер графов фильтров строит часть графа**</span><span class="sxs-lookup"><span data-stu-id="9121c-139">**The Filter Graph Manager Builds Part of the Graph**</span></span>

<span data-ttu-id="9121c-140">Чтобы сделать что-то, помимо простого воспроизведения файла, приложение должно выполнить по крайней мере некоторые операции построения графа.</span><span class="sxs-lookup"><span data-stu-id="9121c-140">To do something beyond simply playing a file, your application must perform at least some of the graph building work.</span></span> <span data-ttu-id="9121c-141">Например, приложение для записи видео должно выбрать фильтр источника захвата и добавить его в граф.</span><span class="sxs-lookup"><span data-stu-id="9121c-141">For example, a video capture application must select a capture source filter and add it to the graph.</span></span> <span data-ttu-id="9121c-142">Если данные записываются в файл AVI, на диаграмму необходимо добавить фильтры мультиплексора и модуль записи файлов AVI.</span><span class="sxs-lookup"><span data-stu-id="9121c-142">If you are writing data to an AVI file, you must add the AVI Mux and File Writer filters to the graph.</span></span> <span data-ttu-id="9121c-143">Однако часто можно позволить диспетчеру графа фильтров завершить график.</span><span class="sxs-lookup"><span data-stu-id="9121c-143">However, it is often possible to let the Filter Graph Manager complete the graph.</span></span> <span data-ttu-id="9121c-144">Например, можно отобразить ПИН-код для предварительного просмотра, вызвав метод **Render** .</span><span class="sxs-lookup"><span data-stu-id="9121c-144">For example, you can render a pin for preview by calling the **Render** method.</span></span>

<span data-ttu-id="9121c-145">**Приложение создает весь граф**</span><span class="sxs-lookup"><span data-stu-id="9121c-145">**The Application Builds the Entire Graph**</span></span>

<span data-ttu-id="9121c-146">В некоторых сценариях приложению может потребоваться построить граф, добавив и подключив каждый фильтр.</span><span class="sxs-lookup"><span data-stu-id="9121c-146">In some scenarios, your application may need to build the graph by adding and connecting each filter.</span></span> <span data-ttu-id="9121c-147">В этом случае, возможно, вам известно, какие фильтры следует добавить к диаграмме.</span><span class="sxs-lookup"><span data-stu-id="9121c-147">In this case, you probably know specifically which filters should be added to the graph.</span></span> <span data-ttu-id="9121c-148">При таком подходе приложение добавляет каждый фильтр путем вызова **аддфилтер**, перечисляет контакты в фильтрах и подключает их, вызывая **Connect** или **коннектдирект**.</span><span class="sxs-lookup"><span data-stu-id="9121c-148">With this approach, the application adds each filter by calling **AddFilter**, enumerates the pins on the filters, and connects them by calling either **Connect** or **ConnectDirect**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9121c-149">См. также</span><span class="sxs-lookup"><span data-stu-id="9121c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9121c-150">Построение диаграмм с помощью построителя графа записи</span><span class="sxs-lookup"><span data-stu-id="9121c-150">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[<span data-ttu-id="9121c-151">Перечисление устройств и фильтров</span><span class="sxs-lookup"><span data-stu-id="9121c-151">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="9121c-152">Перечисление объектов в графе фильтра</span><span class="sxs-lookup"><span data-stu-id="9121c-152">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="9121c-153">Общие методы Graph-Building</span><span class="sxs-lookup"><span data-stu-id="9121c-153">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="9121c-154">Построение графа фильтра</span><span class="sxs-lookup"><span data-stu-id="9121c-154">Building the Filter Graph</span></span>](building-the-filter-graph.md)
</dt> </dl>

 

 



