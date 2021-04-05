---
description: Фильтр разделителя AVI
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Фильтр разделителя AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61b9a60c4c42aafa875c166ae08ccdf337793c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140531"
---
# <a name="avi-splitter-filter"></a><span data-ttu-id="92fff-103">Фильтр разделителя AVI</span><span class="sxs-lookup"><span data-stu-id="92fff-103">AVI Splitter Filter</span></span>

<span data-ttu-id="92fff-104">Фильтр AVI Splitter используется для воспроизведения AVI-файлов.</span><span class="sxs-lookup"><span data-stu-id="92fff-104">The AVI Splitter Filter is used for playback of AVI files.</span></span> <span data-ttu-id="92fff-105">Он принимает данные в формате AVI и разделяет их в составные потоки для дальнейшей обработки и (или) подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="92fff-105">It accepts data in AVI format and splits it into its constituent streams for further processing and/or rendering.</span></span>



|                                          |                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92fff-106">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="92fff-106">Filter Interfaces</span></span>                        | <span data-ttu-id="92fff-107">[**Иаммедиаконтент**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**иперсистмедиапропертибаг**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span><span class="sxs-lookup"><span data-stu-id="92fff-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span></span>                        |
| <span data-ttu-id="92fff-108">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="92fff-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="92fff-109">\_Поток MEDIATYPE, медиасубтипе \_ AVI</span><span class="sxs-lookup"><span data-stu-id="92fff-109">MEDIATYPE\_Stream, MEDIASUBTYPE\_Avi</span></span>                                                                                                                                |
| <span data-ttu-id="92fff-110">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="92fff-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="92fff-111">[**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="92fff-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                    |
| <span data-ttu-id="92fff-112">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="92fff-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="92fff-113">Обычно **это \_** аудио и **мультимедийное \_ Воспроизведение**.</span><span class="sxs-lookup"><span data-stu-id="92fff-113">Typically **MEDIATYPE\_Video** or **MEDIATYPE\_Audio**.</span></span> <span data-ttu-id="92fff-114">Точный тип зависит от содержимого файла, от сжатия файла и от того, какой кодек использовался.</span><span class="sxs-lookup"><span data-stu-id="92fff-114">The exact type depends on the content of the file, whether the file is compressed, and what codec was used.</span></span> |
| <span data-ttu-id="92fff-115">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="92fff-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="92fff-116">[**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), ипропертибаг, [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="92fff-116">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>    |
| <span data-ttu-id="92fff-117">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="92fff-117">Filter CLSID</span></span>                             | <span data-ttu-id="92fff-118">\_АВИСПЛИТТЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="92fff-118">CLSID\_AviSplitter</span></span>                                                                                                                                                  |
| <span data-ttu-id="92fff-119">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="92fff-119">Property Page CLSID</span></span>                      | <span data-ttu-id="92fff-120">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="92fff-120">No property page.</span></span>                                                                                                                                                   |
| <span data-ttu-id="92fff-121">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="92fff-121">Executable</span></span>                               | <span data-ttu-id="92fff-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="92fff-122">quartz.dll</span></span>                                                                                                                                                          |
| [<span data-ttu-id="92fff-123">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="92fff-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="92fff-124">неуспешный \_ режим</span><span class="sxs-lookup"><span data-stu-id="92fff-124">MERIT\_NORMAL</span></span>                                                                                                                                                       |
| [<span data-ttu-id="92fff-125">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="92fff-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="92fff-126">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="92fff-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="92fff-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92fff-127">Remarks</span></span>

<span data-ttu-id="92fff-128">Этот фильтр обычно подключается к фильтру [асинхронного файла](file-source--async--filter.md) на его входном ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="92fff-128">This filter is typically connected to the [Async File Source](file-source--async--filter.md) filter on its input pin.</span></span> <span data-ttu-id="92fff-129">Он может подключаться к любому фильтру, чей выходной ПИН-код поддерживает [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) и предоставляет правильный тип носителя для входного ПИН-кода фильтра разделителя AVI.</span><span class="sxs-lookup"><span data-stu-id="92fff-129">It can connect to any filter whose output pin supports [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and offers the correct media type to the AVI Splitter filter's input pin.</span></span>

<span data-ttu-id="92fff-130">Выходные сигналы в разделителе AVI поддерживают метод Ипропертибаг:: Read для чтения свойств из отдельных потоков.</span><span class="sxs-lookup"><span data-stu-id="92fff-130">The output pins on the AVI Splitter support the IPropertyBag::Read method for reading properties from individual streams.</span></span> <span data-ttu-id="92fff-131">В настоящее время определено следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="92fff-131">Currently, the following property is defined.</span></span>



| <span data-ttu-id="92fff-132">Свойство</span><span class="sxs-lookup"><span data-stu-id="92fff-132">Property</span></span> | <span data-ttu-id="92fff-133">Описание</span><span class="sxs-lookup"><span data-stu-id="92fff-133">Description</span></span>                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92fff-134">name</span><span class="sxs-lookup"><span data-stu-id="92fff-134">name</span></span>     | <span data-ttu-id="92fff-135">Возвращает имя потока, взятое из `'strn'` фрагмента файла AVI.</span><span class="sxs-lookup"><span data-stu-id="92fff-135">Returns the name of the stream, taken from the `'strn'` chunk in the AVI file.</span></span> <span data-ttu-id="92fff-136">Если этот блок отсутствует, метод Read возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="92fff-136">If this chunk is absent, the Read method returns E\_INVALIDARG.</span></span> |



 

<span data-ttu-id="92fff-137">Метод Ипропертибаг:: Write возвращает E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="92fff-137">The IPropertyBag::Write method returns E\_FAIL.</span></span> <span data-ttu-id="92fff-138">Фильтр [мультиплексора](avi-mux-filter.md) в формате AVI поддерживает ипропертибаг:: Write для сохранения свойств потока в файле AVI.</span><span class="sxs-lookup"><span data-stu-id="92fff-138">The [AVI Mux](avi-mux-filter.md) filter supports IPropertyBag::Write for saving stream properties into an AVI file.</span></span>

<span data-ttu-id="92fff-139">Разделитель AVI не позволяет нисходящим фильтрам использовать собственный распределитель.</span><span class="sxs-lookup"><span data-stu-id="92fff-139">The AVI Splitter does not allow downstream filters to use their own allocator.</span></span>

<span data-ttu-id="92fff-140">Продолжительность операций с выводом в файле определяет объем памяти, выделяемый разделителем AVI для его обработки.</span><span class="sxs-lookup"><span data-stu-id="92fff-140">The interleaving duration in the file determines how much memory the AVI Splitter will allocate to process it.</span></span> <span data-ttu-id="92fff-141">Для обработки файла, который помещается за один второй фрагмент, требуется гораздо больше памяти, чем для файла, длительность чередования которого равна одному или двум кадрам.</span><span class="sxs-lookup"><span data-stu-id="92fff-141">A file that is interleaved in one second chunks will require much more memory to process than a file whose interleave duration is set to one or two frames.</span></span> <span data-ttu-id="92fff-142">На современных компьютерах это, как правило, не является проблемой, если одновременно не используется несколько экземпляров одного разделителя AVI.</span><span class="sxs-lookup"><span data-stu-id="92fff-142">On modern computers, this is generally not an issue unless you are running multiple instances of the AVI Splitter simultaneously.</span></span>

### <a name="seeking"></a><span data-ttu-id="92fff-143">Нужна</span><span class="sxs-lookup"><span data-stu-id="92fff-143">Seeking</span></span>

<span data-ttu-id="92fff-144">Если файл содержит поток видео, разделитель AVI поддерживает поиск по номеру кадра.</span><span class="sxs-lookup"><span data-stu-id="92fff-144">If the file contains a video stream, the AVI Splitter supports seeking by frame number.</span></span> <span data-ttu-id="92fff-145">Чтобы включить поиск на основе кадров, вызовите [**имедиасикинг:: сеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) в [диспетчере графов фильтров](filter-graph-manager.md) со значением **\_ \_ кадр формата времени**.</span><span class="sxs-lookup"><span data-stu-id="92fff-145">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

<span data-ttu-id="92fff-146">Если файл содержит аудиопоток, разделитель AVI поддерживает поиск по образцу числа.</span><span class="sxs-lookup"><span data-stu-id="92fff-146">If the file contains an audio stream, the AVI Splitter supports seeking by sample number.</span></span> <span data-ttu-id="92fff-147">Чтобы включить поиск на основе образца, вызовите [**сеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) в диспетчере графа фильтров со значением **\_ \_ пример формата времени**.</span><span class="sxs-lookup"><span data-stu-id="92fff-147">To enable sample-based seeking, call [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the Filter Graph Manager with the value **TIME\_FORMAT\_SAMPLE**.</span></span>

<span data-ttu-id="92fff-148">В обоих случаях выходной ПИН-код для этого потока должен быть подключен к фильтру модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="92fff-148">In both cases, the output pin for that stream must be connected to a renderer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92fff-149">См. также</span><span class="sxs-lookup"><span data-stu-id="92fff-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92fff-150">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="92fff-150">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



