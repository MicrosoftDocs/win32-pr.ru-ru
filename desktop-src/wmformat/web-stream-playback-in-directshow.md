---
title: Воспроизведение веб-потока в DirectShow
description: Воспроизведение веб-потока в DirectShow
ms.assetid: cc307c24-2bd2-43de-ba81-1cf5b05524b2
keywords:
- Пакет SDK для Windows Media Format, DirectShow
- Windows Media Format SDK, воспроизведение веб-потока
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный формат систем (ASF), воспроизведение веб-потока
- ASF (Расширенный системный формат), воспроизведение веб-потока
- DirectShow, воспроизведение веб-потока
- Веб-потоки, DirectShow
- Веб-потоки, воспроизведение в DirectShow
- потоки, воспроизведение веб-потока в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a696e8184554195cf6e9c841b2fb59c4281e377a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986297"
---
# <a name="web-stream-playback-in-directshow"></a><span data-ttu-id="89d4b-113">Воспроизведение веб-потока в DirectShow</span><span class="sxs-lookup"><span data-stu-id="89d4b-113">Web Stream Playback in DirectShow</span></span>

<span data-ttu-id="89d4b-114">Microsoft DirectShow поддерживает веб-потоки (см. [веб-потоки](web-streams.md) для получения дополнительных сведений) в сценариях воспроизведения файлов с помощью фильтра [чтения WM ASF](wm-asf-reader-filter.md) , но для записи и сохранения потока необходимо написать собственный фильтр DirectShow.</span><span class="sxs-lookup"><span data-stu-id="89d4b-114">Microsoft DirectShow supports Web streams (see [Web Streams](web-streams.md) for more information) in file playback scenarios through the [WM ASF Reader](wm-asf-reader-filter.md) filter, but you must write your own DirectShow filter to capture and persist the stream.</span></span>

> [!Note]  
> <span data-ttu-id="89d4b-115">Для воспроизведения веб-потоков в содержимом, которое передается с сервера, на котором работают службы Windows Media, используйте элемент управления ActiveX® Windows Media 9 Series, внедренный в веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="89d4b-115">To play back Web streams in content that is being streamed from a server running Windows Media Services, use the Windows Media Player 9 Series ActiveX® control embedded in a Web page.</span></span>

 

<span data-ttu-id="89d4b-116">При наличии файла, содержащего потоки типа ВММЕДИАТИПЕ \_ филетрансфер, средство чтения WM ASF создаст для него закрепление вывода.</span><span class="sxs-lookup"><span data-stu-id="89d4b-116">When given a file containing streams of type WMMEDIATYPE\_FileTransfer, the WM ASF Reader will create an output pin for it.</span></span> <span data-ttu-id="89d4b-117">Блоком формата будет структура [**\_ \_ формата ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) в виде потока.</span><span class="sxs-lookup"><span data-stu-id="89d4b-117">The format block will be a [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure.</span></span> <span data-ttu-id="89d4b-118">Если подчиненный фильтр недоступен для работы с этим типом мультимедиа, ПИН-код останется неподключенным, но он по-прежнему будет воспроизводить аудио-и видеопотоки.</span><span class="sxs-lookup"><span data-stu-id="89d4b-118">If no downstream filter is available that can handle that media type, then the pin will remain unconnected, but the file will still play the audio and/or video streams.</span></span>

<span data-ttu-id="89d4b-119">Важно понимать, что каждый пример мультимедийных данных в веб-потоке содержит [**структуру \_ \_ \_ заголовка ВМТ для примера**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) , имеющую переменную длину в зависимости от длины его элемента **всзурл** .</span><span class="sxs-lookup"><span data-stu-id="89d4b-119">It is important to understand that each media sample in a Web stream contains a [**WMT\_WEBSTREAM\_SAMPLE\_HEADER**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) structure, which has a variable length depending on the length of its **wszURL** member.</span></span> <span data-ttu-id="89d4b-120">Указатель на образец данных изначально указывает на эту структуру, и необходимо передвинуть указатель за пределы структуры, чтобы получить доступ к реальным данным в потоке.</span><span class="sxs-lookup"><span data-stu-id="89d4b-120">The pointer to the sample data initially points to this structure, and you must advance the pointer past the structure in order to access the actual data in the stream.</span></span> <span data-ttu-id="89d4b-121">Фильтр обработчика веб-потока должен основываться на классе **кбасерендерер** .</span><span class="sxs-lookup"><span data-stu-id="89d4b-121">Your Web stream handler filter should be based on the **CBaseRenderer** class.</span></span> <span data-ttu-id="89d4b-122">В методе **дорендерсампле** фильтру необходимо будет проанализировать структуру для получения сведений о веб-потоке, а затем выполнить соответствующее действие.</span><span class="sxs-lookup"><span data-stu-id="89d4b-122">In the **DoRenderSample** method, the filter will need to parse the structure for information about the Web stream, and then perform the appropriate action.</span></span> <span data-ttu-id="89d4b-123">Как правило, это предполагает сохранение файла на диск, а затем вызов **коммитурлкачинтри** и **креатеурлкачинтри** для размещения файлов в кэше Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="89d4b-123">Typically, this will involve saving the file to disk, and then calling **CommitUrlCacheEntry** and **CreateUrlCacheEntry** to place the files into the Internet Explorer cache.</span></span> <span data-ttu-id="89d4b-124">Фильтр должен обрабатывать составные файлы, то есть файлы, размер которых больше одного образца, а также обрабатывать команды рендеринга, которые задаются членом **ВМТ \_ \_ \_ . ВСАМПЛЕТИПЕ в образце потока** .</span><span class="sxs-lookup"><span data-stu-id="89d4b-124">The filter must handle multipart files, that is, files that are larger than one sample, and also must handle render commands, which are specified by the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wSampleType** member.</span></span> <span data-ttu-id="89d4b-125">Фильтр отправляет в приложение **\_ \_ событие EC OLE** , а также текст **\_ заголовка ВМТ \_ \_ . всзурл** , который содержит имя файла для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="89d4b-125">The filter sends an **EC\_OLE\_EVENT** to the application, along with the text of the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wszURL** string which contains the name of the file to be rendered.</span></span> <span data-ttu-id="89d4b-126">Затем приложение вызывает отображение указанной страницы в браузере.</span><span class="sxs-lookup"><span data-stu-id="89d4b-126">The application then causes the browser to display the specified page.</span></span> <span data-ttu-id="89d4b-127">Если веб-поток создан правильно, файл должен уже находиться в кэше.</span><span class="sxs-lookup"><span data-stu-id="89d4b-127">If the Web stream has been authored correctly, the file should already be in the cache.</span></span>

<span data-ttu-id="89d4b-128">Дополнительные сведения о событиях **кбасерендерер**, **дорендерсампле** и **EC \_ OLE \_** см. в документации по пакету SDK для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="89d4b-128">For more information on **CBaseRenderer**, **DoRenderSample**, and **EC\_OLE\_EVENT**, see the DirectShow SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89d4b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="89d4b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89d4b-130">**Веб-потоки**</span><span class="sxs-lookup"><span data-stu-id="89d4b-130">**Web Streams**</span></span>](web-streams.md)
</dt> </dl>

 

 




