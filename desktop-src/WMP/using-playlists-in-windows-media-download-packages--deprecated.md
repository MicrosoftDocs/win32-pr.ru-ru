---
title: Использование списков воспроизведения в пакетах загрузки Windows Media (устарело)
description: Использование списков воспроизведения в пакетах загрузки Windows Media (устарело)
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Метафайлы Windows Media, пакеты загрузки Windows Media
- Проигрыватель Windows Media, пакеты загрузки Windows Media
- Метафайлы, пакеты загрузки Windows Media
- Windows Media, Загрузка пакетов Windows Media
- списки воспроизведения, пакеты загрузки Windows Media
- списки воспроизведения метафайлов, пакеты загрузки Windows Media
- Списки воспроизведения метафайлов Windows Media, пакеты загрузки Windows Media
- Пакеты загрузки Windows Media, списки воспроизведения
- Пакеты загрузки Windows Media, списки воспроизведения метафайлов
- Пакеты загрузки Windows Media, списки воспроизведения метафайлов Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00c4daa26d18294c00aad7b4926a017d2f3f6343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411208"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a><span data-ttu-id="c1555-113">Использование списков воспроизведения в пакетах загрузки Windows Media (устарело)</span><span class="sxs-lookup"><span data-stu-id="c1555-113">Using Playlists in Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="c1555-114">Эта страница описывает функцию, которая может быть недоступна в будущих версиях проигрывателя Windows Media и Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="c1555-114">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="c1555-115">Списки воспроизведения — это метафайлы Windows Media с расширением. ASX, содержащие сведения о том, как воспроизвести упакованное содержимое в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c1555-115">Playlists are Windows Media metafiles with an .asx file name extension that provide information that tells Windows Media Player how to play the packaged content.</span></span> <span data-ttu-id="c1555-116">Объединяя несколько файлов содержимого в один пакет загрузки Windows Media, вы можете управлять пакетом загрузки Windows Media и настраивать его с помощью списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c1555-116">By combining multiple content files into a single Windows Media Download package, you can control and customize your Windows Media Download package by using the playlist.</span></span>

> [!Note]  
> <span data-ttu-id="c1555-117">Как правило, списки воспроизведения метафайлов используются пакетами загрузки Windows Media для ссылки на мультимедийное содержимое в пакете, а не на поток с сервера в интрасети или Интернете.</span><span class="sxs-lookup"><span data-stu-id="c1555-117">In general, metafile playlists are used by Windows Media Download packages to reference the multimedia content in the package rather than a stream from a server on an intranet or the Internet.</span></span> <span data-ttu-id="c1555-118">Однако поддерживаются ссылки на URL-адреса в файле ASX.</span><span class="sxs-lookup"><span data-stu-id="c1555-118">However, URL references within the .asx file are supported.</span></span>

 

<span data-ttu-id="c1555-119">С помощью XML метафайл предоставляет сведения, которые проигрыватель Windows Media использует для воспроизведения и вывода содержимого.</span><span class="sxs-lookup"><span data-stu-id="c1555-119">Using XML, the metafile provides the information Windows Media Player uses to play and display content.</span></span> <span data-ttu-id="c1555-120">Списки воспроизведения состоят из различных элементов кода XML со связанными тегами и атрибутами.</span><span class="sxs-lookup"><span data-stu-id="c1555-120">Playlists are made up of various XML code elements with their associated tags and attributes.</span></span> <span data-ttu-id="c1555-121">Каждый элемент в списке воспроизведения метафайлов Windows Media определяет конкретный параметр или действие в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c1555-121">Each element in a Windows Media metafile playlist defines a particular setting or action in Windows Media Player.</span></span>

<span data-ttu-id="c1555-122">Компьютер пользователя связывает метафайл Windows Media с расширением файла. ASX с проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c1555-122">The user's computer associates a Windows Media metafile that has an .asx file name extension with Windows Media Player.</span></span> <span data-ttu-id="c1555-123">Проигрыватель Windows Media открывает и анализирует XML-код в метафайле, который содержит путь для поиска упакованных аудио-или видеофайлов.</span><span class="sxs-lookup"><span data-stu-id="c1555-123">Windows Media Player opens and parses the XML code in the metafile, which contains the path for locating the packaged audio or video files.</span></span> <span data-ttu-id="c1555-124">Затем сценарий метафайлов управляет аудио, видео и графическим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="c1555-124">The metafile script then controls the audio, video, and graphical experience.</span></span> <span data-ttu-id="c1555-125">Метафайл также содержит сведения, которые проигрыватель Windows Media обрабатывает и отображает в раскрывающемся списке Список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c1555-125">The metafile also contains information that Windows Media Player processes and displays in the playlist drop-down box.</span></span> <span data-ttu-id="c1555-126">Сразу после отображения списка выполняется воспроизведение первого элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="c1555-126">Immediately after the list is displayed, the first item in the list is played.</span></span>

<span data-ttu-id="c1555-127">Список воспроизведения метафайлов — это ярлык файлов, содержащих упакованное содержимое.</span><span class="sxs-lookup"><span data-stu-id="c1555-127">A metafile playlist is a shortcut to the files that contain your packaged content.</span></span> <span data-ttu-id="c1555-128">Следующий код является примером метафайла, который задает границу для вывода с помощью элемента **Skin** , двух песен для воспроизведения и сведений о списках воспроизведения для каждой песни.</span><span class="sxs-lookup"><span data-stu-id="c1555-128">The following code is an example of a metafile that specifies the border to display by using the **SKIN** element, two songs to be played, and the playlist information for each song.</span></span>


```XML
<ASX Version="3.0">
<AUTHOR>Name of content creator goes here</AUTHOR>
<TITLE>Album Title goes here</TITLE>
<PARAM name="Album" value="Album Title "/>
<PARAM name="Artist" value="Artist Name"/>
<PARAM name="Genre" value="Genre"/>
<SKIN HREF="myborder.wmz"/>
    <ENTRY>
        <REF HREF="song1.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #1 title</TITLE>
    </ENTRY>
    <ENTRY>
        <REF HREF="song2.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #2 name</TITLE>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="c1555-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c1555-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1555-130">**Границы для проигрывателя Windows Media (не рекомендуется)**</span><span class="sxs-lookup"><span data-stu-id="c1555-130">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="c1555-131">**Пакеты загрузки Windows Media (устарели)**</span><span class="sxs-lookup"><span data-stu-id="c1555-131">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> <dt>

[<span data-ttu-id="c1555-132">**Метафайлы Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c1555-132">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




