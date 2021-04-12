---
title: Использование динамического переключения потока событий
description: Использование динамического переключения потока событий
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
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
ms.openlocfilehash: fd5c586e0f1ef2b36913dee822e461daeffbfcbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252979"
---
# <a name="using-live-event-stream-switching"></a><span data-ttu-id="20ef5-118">Использование динамического переключения потока событий</span><span class="sxs-lookup"><span data-stu-id="20ef5-118">Using Live Event Stream Switching</span></span>

<span data-ttu-id="20ef5-119">Потоковая передача мультимедиа также может управляться путем взаимодействия команд сценариев, внедренных в поток мультимедиа, с элементами метафайлов Windows Media в списке воспроизведения метафайлов.</span><span class="sxs-lookup"><span data-stu-id="20ef5-119">Streaming media can also be controlled by the interaction of script commands embedded in a media stream with Windows Media metafile elements in a metafile playlist.</span></span>

<span data-ttu-id="20ef5-120">Событие — это конкретный тип команды сценария, внедренной в поток мультимедиа или файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="20ef5-120">An event is a particular type of script command embedded in a media stream or media file.</span></span> <span data-ttu-id="20ef5-121">Когда элемент управления проигрывателя Windows Media получает команду сценария, он обрабатывает событие, как определено элементом **event** в списке воспроизведения метафайла.</span><span class="sxs-lookup"><span data-stu-id="20ef5-121">When the Windows Media Player control receives the script command, it processes the event as defined by the **EVENT** element in the metafile playlist.</span></span> <span data-ttu-id="20ef5-122">Проигрыватель Windows Media переключается из текущего потока, который подготавливается к просмотру, и визуализирует содержимое, на которое ссылается элемент **события** списка воспроизведения метафайлов.</span><span class="sxs-lookup"><span data-stu-id="20ef5-122">Windows Media Player switches from the current stream it is rendering and renders the content referenced in the metafile playlist **EVENT** element.</span></span> <span data-ttu-id="20ef5-123">Элемент **event** обычно используется в реальном производстве.</span><span class="sxs-lookup"><span data-stu-id="20ef5-123">The **EVENT** element is usually used in live production.</span></span>

<span data-ttu-id="20ef5-124">Элемент **события** похож на элемент **entry** , но каждый из них обрабатывает воспроизведение потоков и файлов мультимедиа по-разному.</span><span class="sxs-lookup"><span data-stu-id="20ef5-124">An **EVENT** element looks similar to an **ENTRY** element, but each handles the playback of streams and media files differently.</span></span> <span data-ttu-id="20ef5-125">Элемент **entry** используется для создания списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="20ef5-125">The **ENTRY** element is used to create playlists.</span></span> <span data-ttu-id="20ef5-126">Поток или файл мультимедиа, на который ссылается элемент **entry** , начинает воспроизводиться, когда завершается поток или файл мультимедиа, на который ссылается Предыдущая **запись** .</span><span class="sxs-lookup"><span data-stu-id="20ef5-126">A stream or media file referenced in an **ENTRY** element starts playing when the stream or media file referenced in the previous **ENTRY** finishes.</span></span> <span data-ttu-id="20ef5-127">Поток, на который ссылается **событие** , играет роль только при получении определенной команды сценария.</span><span class="sxs-lookup"><span data-stu-id="20ef5-127">A stream referenced in an **EVENT** plays only when a specific script command is received.</span></span> <span data-ttu-id="20ef5-128">Например, когда проигрыватель Windows Media получает команду сценария со строкой типа "EVENT" и командную строку "Адлинк", она ищет в списке воспроизведения следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="20ef5-128">For example, when Windows Media Player receives a script command with type string "EVENT" and the command string "Adlink", it searches the playlist for the following elements.</span></span>


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



<span data-ttu-id="20ef5-129">Проигрыватель Windows Media переключается из активного потока для воспроизведения потока или файла мультимедиа, содержащегося в **событии**, в данном случае адлинк. WMA.</span><span class="sxs-lookup"><span data-stu-id="20ef5-129">Windows Media Player then switches from the live stream to play the stream or media file contained in the **EVENT**, in this case Adlink.wma.</span></span> <span data-ttu-id="20ef5-130">Код `WHENDONE="RESUME"` указывает проигрывателю Windows Media возобновить воспроизведение предыдущего потока при завершении адлинк. WMA.</span><span class="sxs-lookup"><span data-stu-id="20ef5-130">The code `WHENDONE="RESUME"` instructs Windows Media Player to resume playing the previous stream when Adlink.wma is finished.</span></span>

> [!Note]  
> <span data-ttu-id="20ef5-131">Сбой при обработке каждого события, внедренного в поток мультимедиа или файл мультимедиа, может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="20ef5-131">Failure to handle every event embedded in a media stream or media file may yield unexpected results.</span></span>

 

<span data-ttu-id="20ef5-132">Если вы хотите использовать динамическое переключение потока событий, необходимо включить один элемент **события** в список воспроизведения, чтобы обрабатывалась каждая команда сценария события, встроенная в мультимедийные потоки или файлы мультимедиа в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="20ef5-132">If you want to use live event stream switching, you must include one **EVENT** element in your playlist to handle each event script command embedded in the media streams or media files in your playlist.</span></span> <span data-ttu-id="20ef5-133">Перед созданием списка воспроизведения необходимо ознакомиться с подробными сведениями о том, какие команды сценария внедряются в мультимедийное содержимое.</span><span class="sxs-lookup"><span data-stu-id="20ef5-133">Before you create your playlist, you must know the details about which script commands are embedded in your digital media content.</span></span> <span data-ttu-id="20ef5-134">Если имеется команда скрипта событий, которую проигрыватель Windows Media будет игнорировать, включите элемент **события** в список воспроизведения для обработки события, но сослаться на фиктивный URL-адрес в обработчике событий.</span><span class="sxs-lookup"><span data-stu-id="20ef5-134">If there is an event script command that you want Windows Media Player to ignore, include an **EVENT** element in your playlist to handle the event, but reference a dummy URL in the event handler.</span></span>

## <a name="ad-insertion"></a><span data-ttu-id="20ef5-135">Вставка рекламы</span><span class="sxs-lookup"><span data-stu-id="20ef5-135">Ad Insertion</span></span>

<span data-ttu-id="20ef5-136">Этот метод можно использовать для вставки рекламы.</span><span class="sxs-lookup"><span data-stu-id="20ef5-136">This technique can be used for ad insertion.</span></span> <span data-ttu-id="20ef5-137">Например, во время интерактивного Интернет-вещания шариковой игры можно отправить команду в начале каждого коммерческого перерыва, который указывает каждому клиенту (проигрывателю Windows Media), что требуется воспроизвести коммерческие списки в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="20ef5-137">For example, during a live Internet broadcast of a ball game, a command can be sent at the beginning of every commercial break that instructs each client (Windows Media Player) to play commercials listed in its playlist.</span></span> <span data-ttu-id="20ef5-138">Когда клиенты завершат воспроизведение коммерческих презентаций, список воспроизведения дает каждому клиенту возможность вернуться в вещание.</span><span class="sxs-lookup"><span data-stu-id="20ef5-138">When clients finish playing the commercials, the playlist instructs each client to cut back to the live broadcast.</span></span> <span data-ttu-id="20ef5-139">Содержимое носителя **событий** будет отображаться только в том случае, если доступ к потоковой передаче мультимедиа рассылается в виде внедренных сценариев с соответствующим именем **события** .</span><span class="sxs-lookup"><span data-stu-id="20ef5-139">The **EVENT** media content will be rendered only when the streaming media being accessed broadcasts embedded scripting with the matching **EVENT** name.</span></span>

<span data-ttu-id="20ef5-140">Возможности, характерные для переключения **событий** , наилучшим образом приводятся в пользу, чтобы сравнить, как рекламные материалы достигают посетителей через стандартную, беспроводную трансляцию с тем, как рекламные материалы могут достичь посетителей с помощью технологий Windows Media.</span><span class="sxs-lookup"><span data-stu-id="20ef5-140">The possibilities inherent in **EVENT** switching are best appreciated by contrasting how ads reach viewers through standard, over-the-air broadcasting with how ads can reach viewers using Windows Media Technologies.</span></span> <span data-ttu-id="20ef5-141">Исторически рекламные объявления могли бы приблизительно быть нацелены на средства просмотра, используя данные рейтинга в качестве основных критериев.</span><span class="sxs-lookup"><span data-stu-id="20ef5-141">Historically, broadcast ads could only be roughly targeted at viewers, using ratings data as the primary criteria.</span></span> <span data-ttu-id="20ef5-142">Реклама, отправленная с помощью технологий Windows Media, может быть нацелена непосредственно на целевой пользователь, так как **события** и списки воспроизведения можно создавать на лету на основе вводимых пользователем данных.</span><span class="sxs-lookup"><span data-stu-id="20ef5-142">Ads sent using Windows Media Technologies can be aimed directly at the target user because **EVENTs** and playlists can be built on the fly based on user input.</span></span> <span data-ttu-id="20ef5-143">Дополнительные сведения см. в разделе [Персонализация доставки мультимедиа](personalizing-media-delivery.md).</span><span class="sxs-lookup"><span data-stu-id="20ef5-143">For more information, see [Personalizing Media Delivery](personalizing-media-delivery.md).</span></span>

<span data-ttu-id="20ef5-144">Вы также можете использовать списки воспроизведения метафайлов для показа специальной графики, аудио и текста для рекламы.</span><span class="sxs-lookup"><span data-stu-id="20ef5-144">You can also use metafile playlists to display customized graphics, audio and text for advertising.</span></span> <span data-ttu-id="20ef5-145">Элемент **баннера** можно использовать как дочерний элемент **события** для отображения изображения рекламного сообщения.</span><span class="sxs-lookup"><span data-stu-id="20ef5-145">You can use the **BANNER** element as a child element of an **EVENT** to display an advertising message graphic.</span></span> <span data-ttu-id="20ef5-146">Элемент **баннера** предоставляет путь и файл, содержащий рисунки для баннера.</span><span class="sxs-lookup"><span data-stu-id="20ef5-146">The **BANNER** element provides the path and file containing the graphics for your advertising banner.</span></span> <span data-ttu-id="20ef5-147">Можно также указать ссылку на сайт или файл с помощью дочернего элемента **мореинфо** .</span><span class="sxs-lookup"><span data-stu-id="20ef5-147">You can also provide a link to a site or file using the **MOREINFO** child element.</span></span> <span data-ttu-id="20ef5-148">URL-адрес в элементе **мореинфо** может предоставить ссылку на еще больше объявлений в Интернете.</span><span class="sxs-lookup"><span data-stu-id="20ef5-148">The URL in the **MOREINFO** element can provide a link to even more advertisements on the Web.</span></span> <span data-ttu-id="20ef5-149">В следующем примере демонстрируется использование этих элементов.</span><span class="sxs-lookup"><span data-stu-id="20ef5-149">The following example demonstrates using these elements.</span></span>

<span data-ttu-id="20ef5-150">Пример кода</span><span class="sxs-lookup"><span data-stu-id="20ef5-150">Example Code</span></span>


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



<span data-ttu-id="20ef5-151">В следующем примере показано, как вставить объявление AD. wma в поток широковещательного одноадресного потока обстоятельства, когда клиент получает **событие** команды сценария с атрибутом **Name** , имеющим значение "время ожидания".</span><span class="sxs-lookup"><span data-stu-id="20ef5-151">The following example inserts the ad Advert.wma into the broadcast unicast stream BallGame when a client receives a script command **EVENT** with the **NAME** attribute set to "Time-Out".</span></span> <span data-ttu-id="20ef5-152">**Клиентскип** имеет значение No, чтобы не допустить пропуска потокового объявления.</span><span class="sxs-lookup"><span data-stu-id="20ef5-152">**CLIENTSKIP** is set to NO to prevent the streamed ad from being skipped.</span></span> <span data-ttu-id="20ef5-153">В этом примере потоковая реклама должна быть воспроизведена перед возвратом в исходный поток.</span><span class="sxs-lookup"><span data-stu-id="20ef5-153">In this example, the streamed ad must be played before returning to the original stream.</span></span> <span data-ttu-id="20ef5-154">После завершения рекламы клиент возобновляет воспроизведение исходного потока.</span><span class="sxs-lookup"><span data-stu-id="20ef5-154">When the ad is finished, the client resumes playing the original stream.</span></span>

<span data-ttu-id="20ef5-155">Пример кода</span><span class="sxs-lookup"><span data-stu-id="20ef5-155">Example Code</span></span>


```XML
<ASX VERSION="3.0">
    <ENTRY>
        <REF HREF="mms://proseware.com/BallGame" />
    </ENTRY>
    <EVENT NAME="Time-Out" WHENDONE="RESUME">
        <ENTRY>
            <REF HREF = "mms://proseware.com/Advert.wma" 
                CLIENTSKIP = "NO" />
       </ENTRY>
    </EVENT>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="20ef5-156">См. также</span><span class="sxs-lookup"><span data-stu-id="20ef5-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20ef5-157">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="20ef5-157">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="20ef5-158">**Использование списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="20ef5-158">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="20ef5-159">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="20ef5-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="20ef5-160">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="20ef5-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




