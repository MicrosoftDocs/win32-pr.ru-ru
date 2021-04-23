---
description: Фильтр разделителя AVI
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Фильтр разделителя AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24335511e9b7b866c85792c2036a4d4b6d089f2a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909662"
---
# <a name="avi-splitter-filter"></a><span data-ttu-id="a1860-103">Фильтр разделителя AVI</span><span class="sxs-lookup"><span data-stu-id="a1860-103">AVI Splitter Filter</span></span>

<span data-ttu-id="a1860-104">Фильтр AVI Splitter используется для воспроизведения AVI-файлов.</span><span class="sxs-lookup"><span data-stu-id="a1860-104">The AVI Splitter Filter is used for playback of AVI files.</span></span> <span data-ttu-id="a1860-105">Он принимает данные в формате AVI и разделяет их в составные потоки для дальнейшей обработки и (или) подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="a1860-105">It accepts data in AVI format and splits it into its constituent streams for further processing and/or rendering.</span></span>



| <span data-ttu-id="a1860-106">Метка</span><span class="sxs-lookup"><span data-stu-id="a1860-106">Label</span></span> | <span data-ttu-id="a1860-107">Значение</span><span class="sxs-lookup"><span data-stu-id="a1860-107">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1860-108">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="a1860-108">Filter Interfaces</span></span>                        | <span data-ttu-id="a1860-109">[**Иаммедиаконтент**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**иперсистмедиапропертибаг**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span><span class="sxs-lookup"><span data-stu-id="a1860-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span></span>                        |
| <span data-ttu-id="a1860-110">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="a1860-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="a1860-111">\_Поток MEDIATYPE, медиасубтипе \_ AVI</span><span class="sxs-lookup"><span data-stu-id="a1860-111">MEDIATYPE\_Stream, MEDIASUBTYPE\_Avi</span></span>                                                                                                                                |
| <span data-ttu-id="a1860-112">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="a1860-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="a1860-113">[**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="a1860-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                    |
| <span data-ttu-id="a1860-114">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="a1860-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="a1860-115">Обычно **это \_** аудио и **мультимедийное \_ Воспроизведение**.</span><span class="sxs-lookup"><span data-stu-id="a1860-115">Typically **MEDIATYPE\_Video** or **MEDIATYPE\_Audio**.</span></span> <span data-ttu-id="a1860-116">Точный тип зависит от содержимого файла, от сжатия файла и от того, какой кодек использовался.</span><span class="sxs-lookup"><span data-stu-id="a1860-116">The exact type depends on the content of the file, whether the file is compressed, and what codec was used.</span></span> |
| <span data-ttu-id="a1860-117">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="a1860-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="a1860-118">[**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), ипропертибаг, [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="a1860-118">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>    |
| <span data-ttu-id="a1860-119">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="a1860-119">Filter CLSID</span></span>                             | <span data-ttu-id="a1860-120">\_АВИСПЛИТТЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="a1860-120">CLSID\_AviSplitter</span></span>                                                                                                                                                  |
| <span data-ttu-id="a1860-121">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="a1860-121">Property Page CLSID</span></span>                      | <span data-ttu-id="a1860-122">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="a1860-122">No property page.</span></span>                                                                                                                                                   |
| <span data-ttu-id="a1860-123">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="a1860-123">Executable</span></span>                               | <span data-ttu-id="a1860-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="a1860-124">quartz.dll</span></span>                                                                                                                                                          |
| [<span data-ttu-id="a1860-125">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="a1860-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="a1860-126">неуспешный \_ режим</span><span class="sxs-lookup"><span data-stu-id="a1860-126">MERIT\_NORMAL</span></span>                                                                                                                                                       |
| [<span data-ttu-id="a1860-127">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="a1860-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="a1860-128">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="a1860-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="a1860-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1860-129">Remarks</span></span>

<span data-ttu-id="a1860-130">Этот фильтр обычно подключается к фильтру [асинхронного файла](file-source--async--filter.md) на его входном ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="a1860-130">This filter is typically connected to the [Async File Source](file-source--async--filter.md) filter on its input pin.</span></span> <span data-ttu-id="a1860-131">Он может подключаться к любому фильтру, чей выходной ПИН-код поддерживает [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) и предоставляет правильный тип носителя для входного ПИН-кода фильтра разделителя AVI.</span><span class="sxs-lookup"><span data-stu-id="a1860-131">It can connect to any filter whose output pin supports [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and offers the correct media type to the AVI Splitter filter's input pin.</span></span>

<span data-ttu-id="a1860-132">Выходные сигналы в разделителе AVI поддерживают метод Ипропертибаг:: Read для чтения свойств из отдельных потоков.</span><span class="sxs-lookup"><span data-stu-id="a1860-132">The output pins on the AVI Splitter support the IPropertyBag::Read method for reading properties from individual streams.</span></span> <span data-ttu-id="a1860-133">В настоящее время определено следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="a1860-133">Currently, the following property is defined.</span></span>



| <span data-ttu-id="a1860-134">Свойство</span><span class="sxs-lookup"><span data-stu-id="a1860-134">Property</span></span> | <span data-ttu-id="a1860-135">Описание</span><span class="sxs-lookup"><span data-stu-id="a1860-135">Description</span></span>                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1860-136">name</span><span class="sxs-lookup"><span data-stu-id="a1860-136">name</span></span>     | <span data-ttu-id="a1860-137">Возвращает имя потока, взятое из `'strn'` фрагмента файла AVI.</span><span class="sxs-lookup"><span data-stu-id="a1860-137">Returns the name of the stream, taken from the `'strn'` chunk in the AVI file.</span></span> <span data-ttu-id="a1860-138">Если этот блок отсутствует, метод Read возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="a1860-138">If this chunk is absent, the Read method returns E\_INVALIDARG.</span></span> |



 

<span data-ttu-id="a1860-139">Метод Ипропертибаг:: Write возвращает E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="a1860-139">The IPropertyBag::Write method returns E\_FAIL.</span></span> <span data-ttu-id="a1860-140">Фильтр [мультиплексора](avi-mux-filter.md) в формате AVI поддерживает ипропертибаг:: Write для сохранения свойств потока в файле AVI.</span><span class="sxs-lookup"><span data-stu-id="a1860-140">The [AVI Mux](avi-mux-filter.md) filter supports IPropertyBag::Write for saving stream properties into an AVI file.</span></span>

<span data-ttu-id="a1860-141">Разделитель AVI не позволяет нисходящим фильтрам использовать собственный распределитель.</span><span class="sxs-lookup"><span data-stu-id="a1860-141">The AVI Splitter does not allow downstream filters to use their own allocator.</span></span>

<span data-ttu-id="a1860-142">Продолжительность операций с выводом в файле определяет объем памяти, выделяемый разделителем AVI для его обработки.</span><span class="sxs-lookup"><span data-stu-id="a1860-142">The interleaving duration in the file determines how much memory the AVI Splitter will allocate to process it.</span></span> <span data-ttu-id="a1860-143">Для обработки файла, который помещается за один второй фрагмент, требуется гораздо больше памяти, чем для файла, длительность чередования которого равна одному или двум кадрам.</span><span class="sxs-lookup"><span data-stu-id="a1860-143">A file that is interleaved in one second chunks will require much more memory to process than a file whose interleave duration is set to one or two frames.</span></span> <span data-ttu-id="a1860-144">На современных компьютерах это, как правило, не является проблемой, если одновременно не используется несколько экземпляров одного разделителя AVI.</span><span class="sxs-lookup"><span data-stu-id="a1860-144">On modern computers, this is generally not an issue unless you are running multiple instances of the AVI Splitter simultaneously.</span></span>

### <a name="seeking"></a><span data-ttu-id="a1860-145">Нужна</span><span class="sxs-lookup"><span data-stu-id="a1860-145">Seeking</span></span>

<span data-ttu-id="a1860-146">Если файл содержит поток видео, разделитель AVI поддерживает поиск по номеру кадра.</span><span class="sxs-lookup"><span data-stu-id="a1860-146">If the file contains a video stream, the AVI Splitter supports seeking by frame number.</span></span> <span data-ttu-id="a1860-147">Чтобы включить поиск на основе кадров, вызовите [**имедиасикинг:: сеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) в [диспетчере графов фильтров](filter-graph-manager.md) со значением **\_ \_ кадр формата времени**.</span><span class="sxs-lookup"><span data-stu-id="a1860-147">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

<span data-ttu-id="a1860-148">Если файл содержит аудиопоток, разделитель AVI поддерживает поиск по образцу числа.</span><span class="sxs-lookup"><span data-stu-id="a1860-148">If the file contains an audio stream, the AVI Splitter supports seeking by sample number.</span></span> <span data-ttu-id="a1860-149">Чтобы включить поиск на основе образца, вызовите [**сеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) в диспетчере графа фильтров со значением **\_ \_ пример формата времени**.</span><span class="sxs-lookup"><span data-stu-id="a1860-149">To enable sample-based seeking, call [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the Filter Graph Manager with the value **TIME\_FORMAT\_SAMPLE**.</span></span>

<span data-ttu-id="a1860-150">В обоих случаях выходной ПИН-код для этого потока должен быть подключен к фильтру модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="a1860-150">In both cases, the output pin for that stream must be connected to a renderer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1860-151">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a1860-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1860-152">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="a1860-152">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



