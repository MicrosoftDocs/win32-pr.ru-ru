---
title: Фильтр чтения WM ASF (пакет SDK для формата Windows Media 11)
description: Фильтр чтения WM ASF
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Пакет SDK для Windows Media Format, средство чтения WM ASF
- DirectShow, средство чтения WM ASF
- Фильтры КАСФ, средство чтения WM ASF
- Средство чтения WM ASF
- Расширенный формат систем (ASF), читатель WM ASF
- ASF (Расширенный системный формат), читатель WM ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13b7944f45b850a158c9832e174ae5ec7dce4d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800688"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="fb0a5-109">Фильтр чтения WM ASF (пакет SDK для формата Windows Media 11)</span><span class="sxs-lookup"><span data-stu-id="fb0a5-109">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="fb0a5-110">При наличии имени файла ASF или URL-адреса средство чтения WM ASF считывает сжатое содержимое, анализирует потоки и предоставляет закрепление вывода для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="fb0a5-110">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="fb0a5-111">Этот фильтр подключается к Windows Media Audio или Windows Media Video дмос, который выполняет распаковку.</span><span class="sxs-lookup"><span data-stu-id="fb0a5-111">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="fb0a5-112">Поиск поддерживается, если ASF-файл доступен для поиска.</span><span class="sxs-lookup"><span data-stu-id="fb0a5-112">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="fb0a5-113">Модуль чтения WM ASF применяет штампы времени к примерам мультимедиа на основе метки времени в файле ASF, но не изменяет метки времени каким бы то ни было образом.</span><span class="sxs-lookup"><span data-stu-id="fb0a5-113">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="fb0a5-114">На внутреннем уровне фильтр использует объект чтения формата Windows Media для чтения содержимого на основе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fb0a5-114">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="fb0a5-115">В пакете SDK для DirectX этот фильтр не является фильтром источника по умолчанию для файлов ASF, поэтому с этим пакетом SDK этот фильтр нельзя использовать с методом **RenderFile** . необходимо явно добавить его в граф фильтра с помощью идентификатора класса (CLSID).</span><span class="sxs-lookup"><span data-stu-id="fb0a5-115">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="fb0a5-116">Это поведение отличается от пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="fb0a5-116">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="fb0a5-117">При установке библиотек среды выполнения пакета SDK для Windows Media Format средство чтения WM ASF регистрируется в качестве фильтра по умолчанию для файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="fb0a5-117">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="fb0a5-118">В следующей таблице содержатся сведения о фильтре чтения WM ASF, например интерфейсах и типах носителей, которые он поддерживает.</span><span class="sxs-lookup"><span data-stu-id="fb0a5-118">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|                        |                                                                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb0a5-119">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="fb0a5-119">Filter interfaces</span></span>      | <span data-ttu-id="fb0a5-120">**Ибасефилтер**, **ифилесаурцефилтер**, **IServiceProvider**, **ивмхеадеринфо**, **ивмреадерадванцед** (частично реализовано).</span><span class="sxs-lookup"><span data-stu-id="fb0a5-120">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="fb0a5-121">См. примечания.), **IWMReaderAdvanced2** (частично реализован), **Ивмдрмреадер** (через **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="fb0a5-121">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="fb0a5-122">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="fb0a5-122">Input pin media types</span></span>  | <span data-ttu-id="fb0a5-123">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fb0a5-123">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="fb0a5-124">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="fb0a5-124">Input pin interfaces</span></span>   | <span data-ttu-id="fb0a5-125">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fb0a5-125">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="fb0a5-126">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="fb0a5-126">Output pin media types</span></span> | <span data-ttu-id="fb0a5-127">МУЛЬТИМЕДИЙное \_ видео, MediaType \_ Audio, MediaType \_ команду скрипта, MediaType \_ филетрансфер</span><span class="sxs-lookup"><span data-stu-id="fb0a5-127">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="fb0a5-128">Тип формата</span><span class="sxs-lookup"><span data-stu-id="fb0a5-128">Format type</span></span>            | <span data-ttu-id="fb0a5-129">**VIDEOINFOHEADER2** , если содержимое [*чередуются*](wmformat-glossary.md), в противном случае **видеоинфохеадер**</span><span class="sxs-lookup"><span data-stu-id="fb0a5-129">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="fb0a5-130">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="fb0a5-130">Output pin interfaces</span></span>  | <span data-ttu-id="fb0a5-131">**Имедиасикинг**, **иамвмбуфферпасс**, **IServiceProvider**, **IWMStreamConfig2** (через **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="fb0a5-131">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="fb0a5-132">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="fb0a5-132">Filter CLSID</span></span>           | <span data-ttu-id="fb0a5-133">\_ВМАСФРЕАДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="fb0a5-133">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="fb0a5-134">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="fb0a5-134">Property Page CLSID</span></span>    | <span data-ttu-id="fb0a5-135">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="fb0a5-135">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="fb0a5-136">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="fb0a5-136">Executable</span></span>             | <span data-ttu-id="fb0a5-137">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="fb0a5-137">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="fb0a5-138">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="fb0a5-138">Merit</span></span>                  | <span data-ttu-id="fb0a5-139">\_маловероятно</span><span class="sxs-lookup"><span data-stu-id="fb0a5-139">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="fb0a5-140">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="fb0a5-140">Filter Category</span></span>        | <span data-ttu-id="fb0a5-141">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="fb0a5-141">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="fb0a5-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb0a5-142">Remarks</span></span>

<span data-ttu-id="fb0a5-143">Читатель WM ASF частично реализует интерфейсы **ивмреадерадванцед** и **IWMReaderAdvanced2** , чтобы предоставить приложениям доступ к информационным методам объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="fb0a5-143">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="fb0a5-144">Реализация фильтра просто передает вызовы в интерфейс объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="fb0a5-144">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="fb0a5-145">Методы потоковой передачи не реализованы, поскольку фильтр должен иметь полный контроль над процессом потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="fb0a5-145">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="fb0a5-146">Реализуются следующие методы **ивмреадерадванцед** и **IWMReaderAdvanced2** :</span><span class="sxs-lookup"><span data-stu-id="fb0a5-146">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="fb0a5-147">**Ивмреадерадванцед:: Statistics**</span><span class="sxs-lookup"><span data-stu-id="fb0a5-147">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="fb0a5-148">**Ивмреадерадванцед:: SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="fb0a5-148">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="fb0a5-149">**IWMReaderAdvanced2:: Жетбуфферпрогресс**</span><span class="sxs-lookup"><span data-stu-id="fb0a5-149">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="fb0a5-150">**IWMReaderAdvanced2:: Жетдовнлоадпрогресс**</span><span class="sxs-lookup"><span data-stu-id="fb0a5-150">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="fb0a5-151">**IWMReaderAdvanced2:: Жетплаймоде**</span><span class="sxs-lookup"><span data-stu-id="fb0a5-151">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="fb0a5-152">**IWMReaderAdvanced2:: Жетпротоколнаме**</span><span class="sxs-lookup"><span data-stu-id="fb0a5-152">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="fb0a5-153">**IWMReaderAdvanced2:: Сетлогклиентид**</span><span class="sxs-lookup"><span data-stu-id="fb0a5-153">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="fb0a5-154">**IWMReaderAdvanced2:: Сетплаймоде**</span><span class="sxs-lookup"><span data-stu-id="fb0a5-154">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="fb0a5-155">См. также</span><span class="sxs-lookup"><span data-stu-id="fb0a5-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb0a5-156">**Справочник по КАСФ DirectShow**</span><span class="sxs-lookup"><span data-stu-id="fb0a5-156">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="fb0a5-157">**Чтение файлов ASF в DirectShow**</span><span class="sxs-lookup"><span data-stu-id="fb0a5-157">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




