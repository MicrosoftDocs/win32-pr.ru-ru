---
description: Фильтр мультиплексора AVI
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: Фильтр мультиплексора AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3755a4d5f63e824ae08eb736a5999dcac3d7ab32
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895089"
---
# <a name="avi-mux-filter"></a><span data-ttu-id="3c0f4-103">Фильтр мультиплексора AVI</span><span class="sxs-lookup"><span data-stu-id="3c0f4-103">AVI Mux Filter</span></span>

<span data-ttu-id="3c0f4-104">Фильтр мультиплексора AVI принимает несколько входных потоков и покидает их в формате AVI.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-104">The AVI Mux filter accepts multiple input streams and interleaves them into AVI format.</span></span> <span data-ttu-id="3c0f4-105">Фильтр использует отдельные входные сигналы для каждого входного потока и один выходной ПИН-код для потока AVI.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-105">The filter uses separate input pins for each input stream, and one output pin for the AVI stream.</span></span>

<span data-ttu-id="3c0f4-106">С помощью этого фильтра можно сохранять файлы на диск в формате AVI.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-106">Video capture or authoring applications can use this filter to save files to disk in AVI format.</span></span> <span data-ttu-id="3c0f4-107">Фильтр обычно подключается к фильтру [записи файлов](file-writer-filter.md) , но может подключаться к любому фильтру, чей входной ПИН-код поддерживает интерфейсы IStream и [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="3c0f4-107">The filter is typically connected to the [File Writer](file-writer-filter.md) filter, but it can connect to any filter whose input pin supports the IStream and [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c0f4-108">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="3c0f4-108">Filter Interfaces</span></span></td>
<td><span data-ttu-id="3c0f4-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>иконфигавимукс</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>иконфигинтерлеавинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>иперсистмедиапропертибаг</strong></a>, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="3c0f4-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c0f4-110">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="3c0f4-110">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="3c0f4-111">Любой основной тип, соответствующий старому типу FOURCC или MEDIATYPE_AUXLine21Data.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-111">Any major type that corresponds to an old-style FOURCC, or MEDIATYPE_AUXLine21Data.</span></span> <span data-ttu-id="3c0f4-112">(Дополнительные сведения см. в разделе <a href="fourccmap.md"><strong>класс фаурккмап</strong></a>.)</span><span class="sxs-lookup"><span data-stu-id="3c0f4-112">(For more information, see <a href="fourccmap.md"><strong>FOURCCMap Class</strong></a>.)</span></span>
<ul>
<li><span data-ttu-id="3c0f4-113">Если основной тип — MEDIATYPE_Audio, формат должен быть FORMAT_WaveFormatEx.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-113">If the major type is MEDIATYPE_Audio, the format must be FORMAT_WaveFormatEx.</span></span></li>
<li><span data-ttu-id="3c0f4-114">Если основной тип — MEDIATYPE_Video, формат должен быть FORMAT_VideoInfo или FORMAT_DvInfo.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-114">If the major type is MEDIATYPE_Video, the format must be FORMAT_VideoInfo or FORMAT_DvInfo.</span></span></li>
<li><span data-ttu-id="3c0f4-115">Если основной тип — MEDIATYPE_Interleaved, формат должен быть FORMAT_DvInfo.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-115">If the major type is MEDIATYPE_Interleaved, the format must be FORMAT_DvInfo.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c0f4-116">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="3c0f4-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="3c0f4-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>Иамстреамконтрол</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, ипропертибаг, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c0f4-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c0f4-118">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="3c0f4-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="3c0f4-119">MEDIATYPE_Stream, MEDIASUBTYPE_Avi</span><span class="sxs-lookup"><span data-stu-id="3c0f4-119">MEDIATYPE_Stream, MEDIASUBTYPE_Avi</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c0f4-120">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="3c0f4-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="3c0f4-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c0f4-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c0f4-122">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="3c0f4-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="3c0f4-123">CLSID_AviDest</span><span class="sxs-lookup"><span data-stu-id="3c0f4-123">CLSID_AviDest</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c0f4-124">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="3c0f4-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="3c0f4-125">CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</span><span class="sxs-lookup"><span data-stu-id="3c0f4-125">CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c0f4-126">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="3c0f4-126">Executable</span></span></td>
<td><span data-ttu-id="3c0f4-127">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="3c0f4-127">qcap.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c0f4-128"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="3c0f4-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="3c0f4-129">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="3c0f4-129">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c0f4-130"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="3c0f4-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="3c0f4-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="3c0f4-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a><span data-ttu-id="3c0f4-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c0f4-132">Remarks</span></span>

<span data-ttu-id="3c0f4-133">В следующих примечаниях описаны различные аспекты функциональности фильтра мультиплексора AVI.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-133">The following remarks describe various aspects of the AVI Mux filter's functionality.</span></span>

<span data-ttu-id="3c0f4-134">Маркеры</span><span class="sxs-lookup"><span data-stu-id="3c0f4-134">Pins</span></span>

<span data-ttu-id="3c0f4-135">При создании фильтра мультиплексора формата AVI он имеет один входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-135">When the AVI Mux filter is created, it has one input pin.</span></span> <span data-ttu-id="3c0f4-136">При подключении каждого входного ПИН-кода фильтр создает новый входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-136">As each input pin is connected, the filter creates a new input pin.</span></span>

<span data-ttu-id="3c0f4-137">Свойства потока</span><span class="sxs-lookup"><span data-stu-id="3c0f4-137">Stream Properties</span></span>

<span data-ttu-id="3c0f4-138">Входные контакты поддерживают интерфейс Ипропертибаг для установки свойств отдельных потоков.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-138">The input pins support the IPropertyBag interface for setting properties on individual streams.</span></span> <span data-ttu-id="3c0f4-139">В настоящее время определено следующее свойство:</span><span class="sxs-lookup"><span data-stu-id="3c0f4-139">Currently, the following property is defined:</span></span>



| <span data-ttu-id="3c0f4-140">Свойство</span><span class="sxs-lookup"><span data-stu-id="3c0f4-140">Property</span></span> | <span data-ttu-id="3c0f4-141">Описание</span><span class="sxs-lookup"><span data-stu-id="3c0f4-141">Description</span></span>                                                           |
|----------|-----------------------------------------------------------------------|
| <span data-ttu-id="3c0f4-142">name</span><span class="sxs-lookup"><span data-stu-id="3c0f4-142">name</span></span>     | <span data-ttu-id="3c0f4-143">Имя потока.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-143">The name of the stream.</span></span> <span data-ttu-id="3c0f4-144">Это свойство записывается как `'strn'` фрагмент.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-144">This property is written as a `'strn'` chunk.</span></span> |



 

<span data-ttu-id="3c0f4-145">Если фильтр запущен или приостановлен, метод Ипропертибаг:: Write возвращает \_ \_ неправильное состояние VFW E \_ .</span><span class="sxs-lookup"><span data-stu-id="3c0f4-145">If the filter is running or paused, the IPropertyBag::Write method returns VFW\_E\_WRONG\_STATE.</span></span>

<span data-ttu-id="3c0f4-146">Частота кадров</span><span class="sxs-lookup"><span data-stu-id="3c0f4-146">Frame Rates</span></span>

<span data-ttu-id="3c0f4-147">Если вышестоящий фильтр не задает частоту кадров в элементе **авгтимеперфраме** структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , то компонент AVI мультиплексор использует метки времени в первом кадре видео.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-147">If the upstream filter does not specify a frame rate in the **AvgTimePerFrame** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, the AVI Mux uses the time stamps on the first video frame.</span></span> <span data-ttu-id="3c0f4-148">Формат файла AVI не поддерживает переменные частоты кадров.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-148">The AVI file format does not support variable frame rates.</span></span>

<span data-ttu-id="3c0f4-149">Удаленные кадры</span><span class="sxs-lookup"><span data-stu-id="3c0f4-149">Dropped Frames</span></span>

<span data-ttu-id="3c0f4-150">Фильтр мультиплексора AVI рассчитывает пропущенные кадры на основе значений времени каждого образца, если они доступны, или в качестве штампов времени образца.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-150">The AVI Mux filter calculates dropped frames based on each sample's media times, if available, or else the sample's time stamps.</span></span> <span data-ttu-id="3c0f4-151">Он записывает запись индекса нулевой длины для каждого удаленного кадра.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-151">It writes a zero-length index entry for every dropped frame.</span></span>

<span data-ttu-id="3c0f4-152">имедиасикинг</span><span class="sxs-lookup"><span data-stu-id="3c0f4-152">IMediaSeeking</span></span>

<span data-ttu-id="3c0f4-153">Фильтр мультиплексора AVI реализует интерфейс [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3c0f4-153">The AVI Mux filter implements the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface as follows:</span></span>

-   <span data-ttu-id="3c0f4-154">Метод [**жеткуррентпоситион**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) возвращает текущий ход выполнения мультиплексирования.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-154">The [**GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method returns the current progress of the multiplexing.</span></span> <span data-ttu-id="3c0f4-155">Если вы перекодируете файл (медленнее, чем в реальном времени), это значение становится более точным, чем значение, возвращенное диспетчером графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-155">If you are transcoding a file (slower than real time), this value is more accurate than the value returned by the Filter Graph Manager.</span></span> <span data-ttu-id="3c0f4-156">Дополнительные сведения см. в разделе "Примечания" на странице справочника по Жеткуррентпоситион.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-156">For more information, see the Remarks section of the GetCurrentPosition reference page.</span></span>
-   <span data-ttu-id="3c0f4-157">Метод [**WebMethod**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) запрашивает каждый вышестоящий фильтр и возвращает длительность самого длинного потока.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-157">The [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method queries each upstream filter and returns the duration of the longest stream.</span></span> <span data-ttu-id="3c0f4-158">Если какой-либо из этих фильтров не выполняет вызов методаической длительности (или не поддерживает Имедиасикинг), то мультиплексор AVI возвращает код ошибки и заполняет параметр *пдуратион* наиболее длинной длительностью.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-158">If any of these filters fails the GetDuration call (or does not support IMediaSeeking), the AVI Mux returns a failure code and fills in the *pDuration* parameter with the longest duration found.</span></span> <span data-ttu-id="3c0f4-159">Однако значение *пдуратион* в этом случае не обязательно является длиной самого длинного входного потока.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-159">However, the value of *pDuration* in this case is not necessarily the length of the longest input stream.</span></span>
-   <span data-ttu-id="3c0f4-160">Мультиплексор AVI не реализует методы Жетстоппоситион, Disposition, Жетпреролл, методомического и недоступности. и не реализует какие бы то ни было \* методы Set для поиска.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-160">The AVI Mux does not implement the GetStopPosition, GetPositions, GetAvailable, GetRate, or GetPreroll methods; nor does it implement any Set\* methods for seeking.</span></span>

<span data-ttu-id="3c0f4-161">Расширения формата файлов AVI 2,0</span><span class="sxs-lookup"><span data-stu-id="3c0f4-161">AVI 2.0 File Format Extensions</span></span>

<span data-ttu-id="3c0f4-162">В настоящее время DirectShow поддерживает следующие расширения формата файлов AVI 2,0:</span><span class="sxs-lookup"><span data-stu-id="3c0f4-162">DirectShow currently supports the following AVI 2.0 file format extensions:</span></span>

-   <span data-ttu-id="3c0f4-163">Увеличен размер AVI-файла (более 1 ГБ)</span><span class="sxs-lookup"><span data-stu-id="3c0f4-163">Increased AVI file size (greater than 1 GB)</span></span>
-   <span data-ttu-id="3c0f4-164">Иерархическое индексирование</span><span class="sxs-lookup"><span data-stu-id="3c0f4-164">Hierarchical indexing</span></span>

<span data-ttu-id="3c0f4-165">Дополнительные сведения см. в статье версия 1,02 для расширений формата AVI-файлов Опендмл, опубликованных в Подкомитете формат файла Опендмл AVI M – JPEG.</span><span class="sxs-lookup"><span data-stu-id="3c0f4-165">For more information, see version 1.02 of the "OpenDML AVI File Format Extensions" published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c0f4-166">См. также</span><span class="sxs-lookup"><span data-stu-id="3c0f4-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c0f4-167">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="3c0f4-167">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



