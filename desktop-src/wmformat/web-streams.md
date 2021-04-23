---
title: Веб-потоки
description: Веб-потоки
ms.assetid: 78a2c703-a3f8-4afc-85d3-1c0a8f5a52b5
keywords:
- Windows Media Format SDK, веб-потоки
- Расширенный системный формат (ASF), веб-потоки
- ASF (Расширенный системный формат), веб-потоки
- Windows Media Format SDK, потоки
- Расширенный системный формат (ASF), потоки
- ASF (Расширенный системный формат), потоки
- Веб-потоки, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710eb9903662d9707d575a09b55ec8e99a224c38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067903"
---
# <a name="web-streams"></a><span data-ttu-id="6113a-110">Веб-потоки</span><span class="sxs-lookup"><span data-stu-id="6113a-110">Web Streams</span></span>

<span data-ttu-id="6113a-111">Веб-поток подобен файловому потоку в том, что он содержит файлы данных.</span><span class="sxs-lookup"><span data-stu-id="6113a-111">A Web stream is like a file stream in that it contains data files.</span></span> <span data-ttu-id="6113a-112">В веб-потоке эти файлы обычно являются HTML-страницами и связанными графическими изображениями в формате GIF или JPEG.</span><span class="sxs-lookup"><span data-stu-id="6113a-112">In a Web stream, these files are typically HTML pages and associated graphics in GIF or JPEG format.</span></span>

<span data-ttu-id="6113a-113">Веб-потоки могут быть особенно полезны для файлов ASF, которые используются в качестве презентаций.</span><span class="sxs-lookup"><span data-stu-id="6113a-113">Web streams can be particularly useful for ASF files that are used as presentations.</span></span> <span data-ttu-id="6113a-114">До поддержки веб-потоков презентации будут иметь URL-адреса в потоках сценариев в файле, чтобы веб-страница загружалась в заранее заданное время.</span><span class="sxs-lookup"><span data-stu-id="6113a-114">Prior to the support of Web streams, presentations would have URLs in script streams within a file so that a Web page would load at a predetermined time.</span></span> <span data-ttu-id="6113a-115">Сложность заключается в том, что перегрузка сети может вызвать задержки и создать неплохое взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="6113a-115">The difficulty was that network congestion could cause delays and create a poor viewing experience.</span></span>

<span data-ttu-id="6113a-116">С помощью веб-потоков составные части веб-страниц могут быть добавлены в файл ASF в виде потока.</span><span class="sxs-lookup"><span data-stu-id="6113a-116">With Web streams, the constituent parts of Web pages can be included in the ASF file as a stream.</span></span> <span data-ttu-id="6113a-117">По мере получения файлов их можно кэшировать таким образом, чтобы при отображении (или отображении) URL-адреса можно было мгновенно получить к ним доступ через браузер.</span><span class="sxs-lookup"><span data-stu-id="6113a-117">As the files are received, they can be cached so that, when the command to display (or render) a URL is delivered, they can be instantly accessed by a browser.</span></span> <span data-ttu-id="6113a-118">Это обеспечивает гладкое и последовательное воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="6113a-118">This enables smooth, consistent playback.</span></span> <span data-ttu-id="6113a-119">Команда Render доставляется в самом веб-потоке, а не в виде команды скрипта в отдельном потоке.</span><span class="sxs-lookup"><span data-stu-id="6113a-119">The render command is delivered in the Web stream itself, not as a script command in a separate stream.</span></span>

<span data-ttu-id="6113a-120">Рекомендуется, чтобы веб-потоки, созданные с помощью пакета SDK для серии Windows Media 9 Series, или более поздних версий были получили номер версии 1.</span><span class="sxs-lookup"><span data-stu-id="6113a-120">It is recommended that Web streams created by using the Windows Media Format 9 Series SDK, or later be given the version number 1.</span></span> <span data-ttu-id="6113a-121">Это значение указывается в структуре [**\_ \_ формата ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) в элементе **вверсион** .</span><span class="sxs-lookup"><span data-stu-id="6113a-121">This value is specified in the [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure in the **wVersion** member.</span></span> <span data-ttu-id="6113a-122">Сам пакет SDK не выполняет никаких действий для принудительного применения этой версии.</span><span class="sxs-lookup"><span data-stu-id="6113a-122">The SDK itself does nothing to enforce this version.</span></span>

> [!Note]  
> <span data-ttu-id="6113a-123">При подключении к потокам Live Broadcast, имеющим веб-потоки, возможно, что пользователь может получить команду прорисовки, прежде чем указанный файл будет находиться в локальном кэше.</span><span class="sxs-lookup"><span data-stu-id="6113a-123">When connecting to live broadcast streams that have Web streams, it is possible that the user may receive a render command before the specified file is actually in the local cache.</span></span> <span data-ttu-id="6113a-124">Если приложение не обрабатывает это условие, в браузере отобразится сообщение об ошибке "страница не найдена".</span><span class="sxs-lookup"><span data-stu-id="6113a-124">Unless your application handles this condition, the browser will display a "Page not found" error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6113a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="6113a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6113a-126">**Произвольные потоки**</span><span class="sxs-lookup"><span data-stu-id="6113a-126">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="6113a-127">**Настройка веб-потоков**</span><span class="sxs-lookup"><span data-stu-id="6113a-127">**Configuring Web Streams**</span></span>](configuring-web-streams.md)
</dt> </dl>

 

 




