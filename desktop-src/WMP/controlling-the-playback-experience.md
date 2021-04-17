---
title: Управление процессом воспроизведения
description: Управление процессом воспроизведения
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Списки воспроизведения метафайлов Windows Media, Управление воспроизведением
- списки воспроизведения, Управление воспроизведением
- списки воспроизведения метафайлов, Управление воспроизведением
- Списки воспроизведения метафайлов Windows Media, проблемы воспроизведения
- списки воспроизведения, проблемы воспроизведения
- списки воспроизведения метафайлов, проблемы воспроизведения
- Управление воспроизведением
- Проигрыватель Windows Media, Управление воспроизведением
- Проигрыватель Windows Media, проблемы воспроизведения
- Хтмлвиев, проблемы воспроизведения
- Хтмлвиев, Управление воспроизведением
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6877b869be8ca38ef9266aedf9318103d0e547ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691290"
---
# <a name="controlling-the-playback-experience"></a><span data-ttu-id="97d08-114">Управление процессом воспроизведения</span><span class="sxs-lookup"><span data-stu-id="97d08-114">Controlling the Playback Experience</span></span>

<span data-ttu-id="97d08-115">В этом разделе рассматриваются некоторые проблемы воспроизведения, которые могут возникнуть при использовании функции Хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="97d08-115">This section discusses some of the playback issues you may encounter when using the HTMLView feature.</span></span>

## <a name="requiring-the-user-to-view-web-based-content"></a><span data-ttu-id="97d08-116">Запрос на просмотр веб-содержимого пользователем</span><span class="sxs-lookup"><span data-stu-id="97d08-116">Requiring the user to view Web-based content</span></span>

<span data-ttu-id="97d08-117">Вы можете решить, что пользователи должны иметь возможность работать с цифровым содержимым мультимедиа, когда также отображается веб-содержимое Хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="97d08-117">You may decide that you only want users to be able to enjoy your digital media content when the HTMLView Web-based content is also displayed.</span></span> <span data-ttu-id="97d08-118">Вы можете включить код скрипта на веб-странице Хтмлвиев, которая останавливает воспроизведение мультимедийного содержимого, если пользователь перейдет из функции **Now (воспроизведение** ).</span><span class="sxs-lookup"><span data-stu-id="97d08-118">You can include script code in your HTMLView webpage that stops playback of the digital media content if the user switches away from the **Now Playing** feature.</span></span> <span data-ttu-id="97d08-119">Для этого можно указать обработчик событий для события **выгрузки** как часть элемента **Body** , как показано в следующем коде HTML:</span><span class="sxs-lookup"><span data-stu-id="97d08-119">To do this, you can specify an event handler for the **unload** event as part of the **BODY** element, as the following HTML code demonstrates:</span></span>


```XML
<BODY onunload = "UnloadMe();">

```



<span data-ttu-id="97d08-120">Затем можно включить код скрипта в функцию обработчика событий, чтобы закрыть файл в проигрывателе.</span><span class="sxs-lookup"><span data-stu-id="97d08-120">Then you can include script code in your event handler function to close the file in the Player.</span></span> <span data-ttu-id="97d08-121">В следующем примере кода выполняется следующее:</span><span class="sxs-lookup"><span data-stu-id="97d08-121">The following example code does this:</span></span>


```XML
function UnloadMe()
{
   Player.close();
}

```



<span data-ttu-id="97d08-122">Когда пользователь переключается из **игры** , нажав кнопку, чтобы открыть другой компонент проигрывателя Windows Media, например библиотеку, проигрыватель закрывает встроенный браузер.</span><span class="sxs-lookup"><span data-stu-id="97d08-122">When the user switches away from **Now Playing** by clicking a button to open another Windows Media Player feature, such as the library, the Player closes the embedded browser.</span></span> <span data-ttu-id="97d08-123">Это приводит к возникновению события **OnUnload** с выполнением скрипта в функции с именем **унлоадме**.</span><span class="sxs-lookup"><span data-stu-id="97d08-123">This causes the **onunload** event to occur, running the script in the function named **UnloadMe**.</span></span> <span data-ttu-id="97d08-124">Метод [Player. Close](player-close.md) останавливает воспроизведение и выгружает текущий файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="97d08-124">The [Player.close](player-close.md) method stops playback and unloads the current digital media file.</span></span> <span data-ttu-id="97d08-125">Чтобы снова просмотреть содержимое, пользователь должен снова открыть исходный файл. ASX.</span><span class="sxs-lookup"><span data-stu-id="97d08-125">To view the content again, the user must reopen the original .asx file.</span></span> <span data-ttu-id="97d08-126">Этот метод также останавливает воспроизведение, когда пользователь выходит за пределы веб-страницы Хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="97d08-126">This technique also stops playback when the user navigates away from the HTMLView webpage.</span></span> <span data-ttu-id="97d08-127">Обратите внимание, что этот метод не может помешать пользователю просматривать мультимедийное содержимое при переключении в режим обложки.</span><span class="sxs-lookup"><span data-stu-id="97d08-127">Note that this technique cannot prevent the user from viewing the digital media content when he or she switches to skin mode.</span></span>

<span data-ttu-id="97d08-128">Вы помните, что параметр Хтмлвиев можно применить к каждому элементу **entry** в файле. ASX.</span><span class="sxs-lookup"><span data-stu-id="97d08-128">You will recall that the HTMLView parameter can be applied to each **ENTRY** element in an .asx file.</span></span> <span data-ttu-id="97d08-129">Эту функцию можно использовать для того, чтобы содержимое Хтмлвиев отображалось при каждом запуске нового файла цифрового носителя.</span><span class="sxs-lookup"><span data-stu-id="97d08-129">You can take advantage of this feature to ensure that your HTMLView content is displayed each time a new digital media file starts.</span></span> <span data-ttu-id="97d08-130">Для этого свяжите элемент **param** для хтмлвиев с каждой записью в списке воспроизведения ASX.</span><span class="sxs-lookup"><span data-stu-id="97d08-130">To do this, associate a **PARAM** element for HTMLView with each entry in your .asx playlist.</span></span> <span data-ttu-id="97d08-131">При каждом воспроизведении записи проигрыватель возвращается в полноэкранный режим и отображает содержимое Хтмлвиев, указанное в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="97d08-131">When each entry plays, the Player returns to full mode and displays the HTMLView content you specified in the playlist.</span></span>

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a><span data-ttu-id="97d08-132">Типы команд сценария "URL-адрес" и "файл" по умолчанию отключены</span><span class="sxs-lookup"><span data-stu-id="97d08-132">URL and FILE script command types are disabled by default</span></span>

<span data-ttu-id="97d08-133">Проигрыватель Windows Media 9 Series или более поздней версии предоставляет параметры, позволяющие пользователю указать, могут ли запускаться команды сценариев для URL-адресов и типов файлов.</span><span class="sxs-lookup"><span data-stu-id="97d08-133">Windows Media Player 9 Series or later provides settings that enable the user to specify whether URL and FILE type script commands are able to run.</span></span> <span data-ttu-id="97d08-134">По умолчанию оба типа команд сценария не выполняются.</span><span class="sxs-lookup"><span data-stu-id="97d08-134">By default, both of these script command types do not run.</span></span> <span data-ttu-id="97d08-135">Если используются пользовательские типы команд сценария, они будут продолжать работать независимо от параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="97d08-135">If you use custom script command types, they will continue to run, regardless of the user setting.</span></span> <span data-ttu-id="97d08-136">Если необходимо использовать команды сценария "URL-адрес" и "тип файла", необходимо предложить пользователю изменить параметры.</span><span class="sxs-lookup"><span data-stu-id="97d08-136">If you must use URL and FILE type script commands, you must prompt the user to change the settings.</span></span> <span data-ttu-id="97d08-137">Чтобы изменить параметры, щелкните **Сервис**, **Параметры** и **Безопасность**.</span><span class="sxs-lookup"><span data-stu-id="97d08-137">To change the settings, click **Tools**, then **Options**, and then **Security**.</span></span>

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a><span data-ttu-id="97d08-138">Повторное открытие Хтмлвиев не приводит к перезагрузке веб-страницы</span><span class="sxs-lookup"><span data-stu-id="97d08-138">Reopening an HTMLView does not reload the webpage</span></span>

<span data-ttu-id="97d08-139">Когда пользователь открывает ASX-файл, содержащий параметр Хтмлвиев, и впоследствии повторно открывает тот же файл, проигрыватель Windows Media не обновляет страницу Хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="97d08-139">When the user opens an .asx file that includes an HTMLView parameter and subsequently reopens the same file, Windows Media Player does not refresh the HTMLView webpage.</span></span> <span data-ttu-id="97d08-140">Это также означает, что если вы разрешили пользователям переходить с веб-страницы Хтмлвиев, проигрыватель не вернет встроенный браузер на веб-страницу начальной Хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="97d08-140">This also means that if you have allowed users to navigate away from your HTMLView webpage, the Player does not return the embedded browser to the initial HTMLView webpage.</span></span>

## <a name="hiding-the-content-location"></a><span data-ttu-id="97d08-141">Скрытие расположения содержимого</span><span class="sxs-lookup"><span data-stu-id="97d08-141">Hiding the content location</span></span>

<span data-ttu-id="97d08-142">Возможно, вы не хотите, чтобы проигрыватель Windows Media отображал расположение цифрового мультимедиа при воспроизведении файла. ASX.</span><span class="sxs-lookup"><span data-stu-id="97d08-142">You might decide that you don't want Windows Media Player to display the location of your digital media content while it is playing an .asx file.</span></span> <span data-ttu-id="97d08-143">Как правило, проигрыватель Windows Media отображает сведения о самом списке воспроизведения при потоковой передаче содержимого из Интернета.</span><span class="sxs-lookup"><span data-stu-id="97d08-143">Usually, Windows Media Player only shows information about the playlist itself when streaming content from the Internet.</span></span> <span data-ttu-id="97d08-144">Однако существуют дальнейшие действия, которые можно предпринять, чтобы запретить пользователям определять расположение содержимого.</span><span class="sxs-lookup"><span data-stu-id="97d08-144">However, there are further steps you can take to prevent users from determining the location of your content.</span></span> <span data-ttu-id="97d08-145">Например, один из способов убедиться, что проигрыватель не отображает путь к содержимому, — потоковая передача содержимого с помощью списков воспроизведения на стороне сервера Windows Media Services.</span><span class="sxs-lookup"><span data-stu-id="97d08-145">For example, one way to ensure that the Player does not display the path to your content is to stream your content using Windows Media Services server-side playlists.</span></span> <span data-ttu-id="97d08-146">Таким образом, когда пользователь просматривает свойства содержимого, он видит URL-адрес сервера, а не URL-адрес содержимого.</span><span class="sxs-lookup"><span data-stu-id="97d08-146">That way, when the user views the properties for the content, he or she sees the URL of the server and not the URL of your content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97d08-147">См. также</span><span class="sxs-lookup"><span data-stu-id="97d08-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97d08-148">**Отображение веб-страниц в проигрывателе Windows Media**</span><span class="sxs-lookup"><span data-stu-id="97d08-148">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="97d08-149">**PARAM, элемент**</span><span class="sxs-lookup"><span data-stu-id="97d08-149">**PARAM Element**</span></span>](param-element.md)
</dt> </dl>

 

 




