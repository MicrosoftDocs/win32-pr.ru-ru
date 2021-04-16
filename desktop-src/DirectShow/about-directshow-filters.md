---
description: О фильтрах DirectShow
ms.assetid: 57b7d32e-2073-46a2-91ec-a34072134489
title: О фильтрах DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ddfb5dda550bee88c42ef70347c95ba7a2b003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104571593"
---
# <a name="about-directshow-filters"></a><span data-ttu-id="41ba3-103">О фильтрах DirectShow</span><span class="sxs-lookup"><span data-stu-id="41ba3-103">About DirectShow Filters</span></span>

<span data-ttu-id="41ba3-104">DirectShow использует модульную архитектуру, где каждый этап обработки выполняется объектом COM, называемым фильтром.</span><span class="sxs-lookup"><span data-stu-id="41ba3-104">DirectShow uses a modular architecture, where each stage of processing is done by a COM object called a filter.</span></span> <span data-ttu-id="41ba3-105">DirectShow предоставляет набор стандартных фильтров для используемых приложений, и разработчики могут писать собственные настраиваемые фильтры, расширяющие функциональные возможности DirectShow.</span><span class="sxs-lookup"><span data-stu-id="41ba3-105">DirectShow provides a set of standard filters for applications to use, and developers can write their own custom filters that extend the functionality of DirectShow.</span></span> <span data-ttu-id="41ba3-106">Ниже приведены шаги, необходимые для воспроизведения видеофайлов AVI, а также фильтры, выполняющие каждый шаг.</span><span class="sxs-lookup"><span data-stu-id="41ba3-106">To illustrate, here are the steps needed to play an AVI video file, along with the filters that perform each step:</span></span>

-   <span data-ttu-id="41ba3-107">Чтение необработанных данных из файла в виде потока байтов (фильтр источника файла).</span><span class="sxs-lookup"><span data-stu-id="41ba3-107">Read the raw data from the file as a byte stream (File Source filter).</span></span>
-   <span data-ttu-id="41ba3-108">Изучите заголовки AVI и проанализируйте поток байтов в отдельные видеоматериалы и образцы звука (фильтр AVI-разделителя).</span><span class="sxs-lookup"><span data-stu-id="41ba3-108">Examine the AVI headers, and parse the byte stream into separate video frames and audio samples (AVI Splitter filter).</span></span>
-   <span data-ttu-id="41ba3-109">Декодирование кадров видео (различные фильтры декодера в зависимости от формата сжатия).</span><span class="sxs-lookup"><span data-stu-id="41ba3-109">Decode the video frames (various decoder filters, depending on the compression format).</span></span>
-   <span data-ttu-id="41ba3-110">Нарисуйте видеокадры (фильтр модуля обработки видео).</span><span class="sxs-lookup"><span data-stu-id="41ba3-110">Draw the video frames (Video Renderer filter).</span></span>
-   <span data-ttu-id="41ba3-111">Отправьте звуковые образцы на звуковую карту (фильтр устройства DirectSound по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="41ba3-111">Send the audio samples to the sound card (Default DirectSound Device filter).</span></span>

<span data-ttu-id="41ba3-112">Эти фильтры показаны на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="41ba3-112">These filters are shown in the following diagram.</span></span>

![граф фильтра для воспроизведения файла AVI с помощью сжатого видео](images/avi-filter-graph.png)

<span data-ttu-id="41ba3-114">Как видно на диаграмме, каждый фильтр подключен к одному или нескольким из других фильтров.</span><span class="sxs-lookup"><span data-stu-id="41ba3-114">As the diagram shows, each filter is connected to one or more other filters.</span></span> <span data-ttu-id="41ba3-115">Точки соединения также являются COM-объектами, называемыми *закреплениями*.</span><span class="sxs-lookup"><span data-stu-id="41ba3-115">The connection points are also COM objects, called *pins*.</span></span> <span data-ttu-id="41ba3-116">Фильтры используют ПИН-коды для перемещения данных из одного фильтра в другой.</span><span class="sxs-lookup"><span data-stu-id="41ba3-116">Filters use pins to move data from one filter the next.</span></span> <span data-ttu-id="41ba3-117">Стрелки на схеме показывают направление, в котором передаются данные.</span><span class="sxs-lookup"><span data-stu-id="41ba3-117">The arrows in the diagram show the direction in which the data travels.</span></span> <span data-ttu-id="41ba3-118">В DirectShow набор фильтров называется *графом фильтра*.</span><span class="sxs-lookup"><span data-stu-id="41ba3-118">In DirectShow, a set of filters is called a *filter graph*.</span></span>

<span data-ttu-id="41ba3-119">Фильтры имеют три возможных состояния: запущено, остановлено и приостановлено.</span><span class="sxs-lookup"><span data-stu-id="41ba3-119">Filters have three possible states: running, stopped, and paused.</span></span> <span data-ttu-id="41ba3-120">При выполнении фильтра он обрабатывает данные мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="41ba3-120">When a filter is running, it processes media data.</span></span> <span data-ttu-id="41ba3-121">После остановки обработка данных прекращается.</span><span class="sxs-lookup"><span data-stu-id="41ba3-121">When it is stopped, it stops processing data.</span></span> <span data-ttu-id="41ba3-122">Приостановленное состояние используется для данных подсказки перед запуском; Этот принцип подробно описан в разделе [поток данных на графе фильтра](data-flow-in-the-filter-graph.md) .</span><span class="sxs-lookup"><span data-stu-id="41ba3-122">The paused state is used to cue data before running; the section [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md) describes this concept in more detail.</span></span> <span data-ttu-id="41ba3-123">При очень редких исключениях изменения состояния согласовываются по всему графу фильтра; все фильтры в параметре Graph имеют состояние в одновременном.</span><span class="sxs-lookup"><span data-stu-id="41ba3-123">With very rare exceptions, state changes are coordinated throughout the entire filter graph; all the filters in the graph switch states in unison.</span></span> <span data-ttu-id="41ba3-124">Таким образом, весь граф фильтра также называется запуском, остановкой или приостановкой.</span><span class="sxs-lookup"><span data-stu-id="41ba3-124">Thus, the entire filter graph is also said to be running, stopped, or paused.</span></span>

<span data-ttu-id="41ba3-125">Фильтры можно группировать по нескольким широким категориям:</span><span class="sxs-lookup"><span data-stu-id="41ba3-125">Filters can be grouped into several broad categories:</span></span>

-   <span data-ttu-id="41ba3-126">Фильтр *источника* вводит данные в граф.</span><span class="sxs-lookup"><span data-stu-id="41ba3-126">A *source* filter introduces data into the graph.</span></span> <span data-ttu-id="41ba3-127">Данные могут поступать из файла, из сети, с камеры или в другом месте.</span><span class="sxs-lookup"><span data-stu-id="41ba3-127">The data might come from a file, a network, a camera, or anywhere else.</span></span> <span data-ttu-id="41ba3-128">Каждый фильтр источника обрабатывает другой тип источника данных.</span><span class="sxs-lookup"><span data-stu-id="41ba3-128">Each source filter handles a different type of data source.</span></span>
-   <span data-ttu-id="41ba3-129">Фильтр *преобразования* принимает входной поток, обрабатывает данные и создает поток вывода.</span><span class="sxs-lookup"><span data-stu-id="41ba3-129">A *transform* filter takes an input stream, processes the data, and creates an output stream.</span></span> <span data-ttu-id="41ba3-130">Примерами фильтров преобразования являются кодировщики и декодеры.</span><span class="sxs-lookup"><span data-stu-id="41ba3-130">Encoders and decoders are examples of transform filters.</span></span>
-   <span data-ttu-id="41ba3-131">Фильтры модуля *подготовки* отчетов располагаются в конце цепочки.</span><span class="sxs-lookup"><span data-stu-id="41ba3-131">*Renderer* filters sit at the end of the chain.</span></span> <span data-ttu-id="41ba3-132">Они получают данные и представляют их пользователю.</span><span class="sxs-lookup"><span data-stu-id="41ba3-132">They receive data and present it to the user.</span></span> <span data-ttu-id="41ba3-133">Например, модуль подготовки видео рисует видеокадры на экране; модуль подготовки звука отправляет звуковые данные на звуковую карту; и фильтр записи файла записывает данные в файл.</span><span class="sxs-lookup"><span data-stu-id="41ba3-133">For example, a video renderer draws video frames on the display; an audio renderer sends audio data to the sound card; and a file-writer filter writes data to a file.</span></span>
-   <span data-ttu-id="41ba3-134">Фильтр *разделителя* разделяет входной поток на два или более выходов, обычно анализируя входной поток по своему пути.</span><span class="sxs-lookup"><span data-stu-id="41ba3-134">A *splitter* filter splits an input stream into two or more outputs, typically parsing the input stream along the way.</span></span> <span data-ttu-id="41ba3-135">Например, разделитель AVI анализирует поток байтов в отдельные видео-и звуковые потоки.</span><span class="sxs-lookup"><span data-stu-id="41ba3-135">For example, the AVI Splitter parses a byte stream into separate video and audio streams.</span></span>
-   <span data-ttu-id="41ba3-136">Фильтр *мультиплексора* принимает несколько входов и объединяет их в один поток.</span><span class="sxs-lookup"><span data-stu-id="41ba3-136">A *mux* filter takes multiple inputs and combines them into a single stream.</span></span> <span data-ttu-id="41ba3-137">Например, мультиплексор AVI выполняет обратную операцию разделителя AVI.</span><span class="sxs-lookup"><span data-stu-id="41ba3-137">For example, the AVI Mux performs the inverse operation of the AVI Splitter.</span></span> <span data-ttu-id="41ba3-138">Он использует поток аудио и видео и создает поток байтов в формате AVI.</span><span class="sxs-lookup"><span data-stu-id="41ba3-138">It takes audio and video streams and produces an AVI-formatted byte stream.</span></span>

<span data-ttu-id="41ba3-139">Различия между этими категориями не являются абсолютными.</span><span class="sxs-lookup"><span data-stu-id="41ba3-139">The distinctions between these categories are not absolute.</span></span> <span data-ttu-id="41ba3-140">Например, фильтр чтения ASF выступает в качестве фильтра источника и фильтра разделителя.</span><span class="sxs-lookup"><span data-stu-id="41ba3-140">For example, the ASF Reader filter acts as both a source filter and a splitter filter.</span></span>

<span data-ttu-id="41ba3-141">Все фильтры DirectShow предоставляют интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) , а все ПИН-коды предоставляют интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="41ba3-141">All DirectShow filters expose the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface, and all pins expose the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="41ba3-142">DirectShow также определяет множество других интерфейсов, которые поддерживают более конкретные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="41ba3-142">DirectShow also defines many other interfaces that support more specific functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41ba3-143">См. также</span><span class="sxs-lookup"><span data-stu-id="41ba3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41ba3-144">О диспетчере графов фильтров</span><span class="sxs-lookup"><span data-stu-id="41ba3-144">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)
</dt> <dt>

[<span data-ttu-id="41ba3-145">Поток данных в графе фильтра</span><span class="sxs-lookup"><span data-stu-id="41ba3-145">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="41ba3-146">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="41ba3-146">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



