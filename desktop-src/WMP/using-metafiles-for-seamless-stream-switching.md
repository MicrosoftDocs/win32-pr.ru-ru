---
title: Использование метафайлов для простого переключения потоков
description: Использование метафайлов для простого переключения потоков
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
keywords:
- Списки воспроизведения метафайлов Windows Media, динамическое переключение потоков событий
- списки воспроизведения, динамическое переключение потоков событий
- списки воспроизведения метафайлов, динамическое переключение потоков событий
- Списки воспроизведения метафайлов Windows Media, переключение потока событий
- списки воспроизведения, переключение потоков событий
- списки воспроизведения метафайлов, переключение потоков событий
- Списки воспроизведения метафайлов Windows Media, вставка рекламы
- списки воспроизведения, вставка рекламы
- списки воспроизведения метафайлов, вставка рекламы
- Проигрыватель Windows Media, динамическое переключение потоков событий
- Проигрыватель Windows Media, переключение потока событий
- Проигрыватель Windows Media, вставка рекламы
- Динамическое переключение потоков событий
- Переключение потока событий
- Вставка рекламы
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29496c71c0c849480bae029f246bfd544667071e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700499"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a><span data-ttu-id="801f6-118">Использование метафайлов для простого переключения потоков</span><span class="sxs-lookup"><span data-stu-id="801f6-118">Using Metafiles for Seamless Stream Switching</span></span>

<span data-ttu-id="801f6-119">Вы можете легко переключаться между потоками с помощью списков воспроизведения метафайлов.</span><span class="sxs-lookup"><span data-stu-id="801f6-119">You can facilitate seamless stream switching using metafile playlists.</span></span> <span data-ttu-id="801f6-120">Обычно при завершении фрагмента содержимого буферизация выполняется для следующего клипа или потока перед открытием (если это содержимое получено с сервера потокового мультимедиа).</span><span class="sxs-lookup"><span data-stu-id="801f6-120">Usually, when a piece of content ends, buffering occurs for the next clip or stream before it opens (if it is content received from a streaming media server).</span></span> <span data-ttu-id="801f6-121">Службы Microsoft Windows Media Services позволяют устранять или по крайней мере свести к минимуму минимальное время буферизации, а другую часть потокового содержимого начать воспроизведение практически сразу же.</span><span class="sxs-lookup"><span data-stu-id="801f6-121">Microsoft Windows Media Services enables you to eliminate, or at least minimize, this buffering time and have another piece of streamed content begin playing nearly immediately.</span></span> <span data-ttu-id="801f6-122">Обычным режимом работы проигрывателя Windows Media является открытие следующего потока мультимедиа, на который ссылается список воспроизведения за 20 секунд до конца текущего потока.</span><span class="sxs-lookup"><span data-stu-id="801f6-122">The normal mode of operation for Windows Media Player is to open the next media stream referenced by the playlist 20 seconds before the end of the currently rendered stream.</span></span> <span data-ttu-id="801f6-123">Обычно это обеспечивает простой переход между потоками мультимедиа в зависимости от других факторов, таких как время веб-доступа.</span><span class="sxs-lookup"><span data-stu-id="801f6-123">This generally provides a seamless transition between media streams, depending on other factors such as Web access times.</span></span>

<span data-ttu-id="801f6-124">Используйте элемент **event** в списке воспроизведения в сочетании с командами опеневент из кодировщика, чтобы упростить переключение между потоками или файлами.</span><span class="sxs-lookup"><span data-stu-id="801f6-124">Use the **EVENT** element in a playlist in conjunction with OPENEVENT commands from the encoder to facilitate seamless switching between streams or files.</span></span> <span data-ttu-id="801f6-125">Отправка команды ОПЕНЕВЕНТ 20 секунд или более перед выполнением команды события может привести к уменьшению задержек при переключении потока.</span><span class="sxs-lookup"><span data-stu-id="801f6-125">Sending an OPENEVENT command 20 seconds or more prior to the EVENT command can minimize delays in stream switching.</span></span> <span data-ttu-id="801f6-126">Затем проигрыватель Windows Media может загрузить часть предстоящего потокового содержимого в буфер.</span><span class="sxs-lookup"><span data-stu-id="801f6-126">Then Windows Media Player is able to preload a portion of the upcoming streaming content into a buffer.</span></span>

<span data-ttu-id="801f6-127">Используйте кодировщик Windows Media для отправки команды сценария в потоке в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="801f6-127">Use Windows Media Encoder to send a script command in the stream using the following format:</span></span>


```XML
OPENEVENT eventname 

```



<span data-ttu-id="801f6-128">Имя события должно быть задано в элементе **event** в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="801f6-128">The event name must be the one defined in the **EVENT** element in the playlist.</span></span> <span data-ttu-id="801f6-129">Когда проигрыватель Windows Media получает команду сценария ОПЕНЕВЕНТ из кодировщика, он выполняет поиск элемента **event** в списке воспроизведения и начинает буферизацию клипа или потока, определенного в элементе **event** .</span><span class="sxs-lookup"><span data-stu-id="801f6-129">When Windows Media Player receives an OPENEVENT script command from the encoder, it looks to the **EVENT** element in the playlist and begins buffering the clip or stream defined in the **EVENT** element.</span></span> <span data-ttu-id="801f6-130">Проигрыватель Windows Media сохраняет эти сведения до наступления фактического события с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="801f6-130">Windows Media Player then holds this information until the actual event of the same name.</span></span> <span data-ttu-id="801f6-131">При получении именованного события проигрыватель Windows Media переключается на ранее буферизованное содержимое.</span><span class="sxs-lookup"><span data-stu-id="801f6-131">When the named event is received, Windows Media Player switches to that previously buffered content.</span></span>

> [!Note]  
> <span data-ttu-id="801f6-132">Нельзя использовать символы Юникода для команды сценария ОПЕНЕВЕНТ в файле мультимедиа или в элементе **event** в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="801f6-132">You cannot use Unicode characters for the OPENEVENT script command in the media file or the **EVENT** element in the playlist.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="801f6-133">См. также</span><span class="sxs-lookup"><span data-stu-id="801f6-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="801f6-134">**Создание списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="801f6-134">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="801f6-135">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="801f6-135">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="801f6-136">**Событие Player. команду скрипта**</span><span class="sxs-lookup"><span data-stu-id="801f6-136">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="801f6-137">**Использование списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="801f6-137">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="801f6-138">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="801f6-138">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="801f6-139">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="801f6-139">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




