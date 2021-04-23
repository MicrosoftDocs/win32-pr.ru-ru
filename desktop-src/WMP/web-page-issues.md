---
title: Проблемы с веб-страницей
description: Проблемы с веб-страницей
ms.assetid: fd97540e-21e9-443e-99ec-ed29f4a2570a
keywords:
- Списки воспроизведения метафайлов Windows Media, веб-страницы
- списки воспроизведения, веб-страницы
- списки воспроизведения метафайлов, веб-страницы
- Списки воспроизведения метафайлов Windows Media, Настройка Хтмлвиев
- списки воспроизведения, Настройка Хтмлвиев
- списки воспроизведения метафайлов, Настройка Хтмлвиев
- Списки воспроизведения метафайлов Windows Media, Настройка Хтмлвиев
- списки воспроизведения, Настройка Хтмлвиев
- списки воспроизведения метафайлов, Настройка Хтмлвиев
- Настройка Хтмлвиев
- Проигрыватель Windows Media, веб-страницы
- Проигрыватель Windows Media, Настройка Хтмлвиев
- Проигрыватель Windows Media, Хтмлвиев Настройка
- Хтмлвиев, Настройка
- Хтмлвиев, веб-страницы
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 882d8993ba3690cf8c4a068f9861ccf39cd1a95c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778938"
---
# <a name="web-page-issues"></a><span data-ttu-id="e5481-118">Проблемы с веб-страницей</span><span class="sxs-lookup"><span data-stu-id="e5481-118">Web Page Issues</span></span>

<span data-ttu-id="e5481-119">При создании веб-страницы, отображаемой в функции **воспроизведения** проигрывателя Windows Media, необходимо учитывать некоторые моменты.</span><span class="sxs-lookup"><span data-stu-id="e5481-119">There are some things to consider when you create a webpage to be displayed in the Windows Media Player **Now Playing** feature.</span></span> <span data-ttu-id="e5481-120">В этом разделе обсуждаются некоторые проблемы, которые могут возникнуть при создании веб-содержимого.</span><span class="sxs-lookup"><span data-stu-id="e5481-120">This section discusses some of the issues you might encounter when creating your Web-based content.</span></span>

## <a name="customizing-htmlview"></a><span data-ttu-id="e5481-121">Настройка Хтмлвиев</span><span class="sxs-lookup"><span data-stu-id="e5481-121">Customizing HTMLView</span></span>

<span data-ttu-id="e5481-122">Веб-страница Хтмлвиев может быть простой или сложной.</span><span class="sxs-lookup"><span data-stu-id="e5481-122">Your HTMLView webpage can be as simple or complex as you want.</span></span> <span data-ttu-id="e5481-123">Можно включить любой элемент, который обычно используется в веб-содержимом.</span><span class="sxs-lookup"><span data-stu-id="e5481-123">You can include any of the elements you usually use in your Web-based content.</span></span> <span data-ttu-id="e5481-124">При внедрении элемента управления проигрывателя Windows Media можно отобразить один из пользовательских интерфейсов, предоставляемых элементом управления, создать собственный пользовательский интерфейс с помощью кода HTML и скрипта или вообще не предоставлять пользовательский интерфейс (это означает, что пользователь может использовать элементы управления транспортным проигрывателем в полноэкранном режиме).</span><span class="sxs-lookup"><span data-stu-id="e5481-124">If you embed the Windows Media Player control, you can display one of the user interfaces supplied by the control, create your own user interface using HTML and script code, or provide no UI at all (which means that the user can use the transport controls of the full-mode Player).</span></span>

<span data-ttu-id="e5481-125">Рекомендуемый размер веб-страниц, отображаемых при использовании функции Хтмлвиев, составляет 575 x 345 пикселей.</span><span class="sxs-lookup"><span data-stu-id="e5481-125">The recommended size for webpages displayed by using the HTMLView feature is 575 x 345 pixels.</span></span> <span data-ttu-id="e5481-126">Однако у пользователя есть возможность изменить размер проигрывателя Windows Media и выбрать разрешение экрана.</span><span class="sxs-lookup"><span data-stu-id="e5481-126">The user, however, has the ability to resize Windows Media Player and choose the screen resolution.</span></span> <span data-ttu-id="e5481-127">Если веб-страница Хтмлвиев больше, чем размер, заданный сейчас функцией **воспроизведения** , игрок отображает горизонтальные и вертикальные полосы прокрутки, позволяющие пользователю видеть всю страницу.</span><span class="sxs-lookup"><span data-stu-id="e5481-127">If the HTMLView webpage is larger than the size accommodated by the **Now Playing** feature, the Player displays horizontal and vertical scroll bars that enable the user to see the entire page.</span></span> <span data-ttu-id="e5481-128">Вы должны протестировать содержимое Хтмлвиев, используя разнообразные разрешения экрана и размеры проигрывателя, чтобы определить оптимальный размер веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="e5481-128">You should test your HTMLView content using a variety of screen resolutions and Player sizes to determine the best size for your webpage.</span></span>

<span data-ttu-id="e5481-129">Проигрыватель Windows Media не предоставляет метод, позволяющий указать размер для проигрывателя в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="e5481-129">Windows Media Player does not provide a method that enables you to specify a size for the full-mode Player.</span></span>

## <a name="web-page-navigation"></a><span data-ttu-id="e5481-130">Навигация по веб-страницам</span><span class="sxs-lookup"><span data-stu-id="e5481-130">Web page navigation</span></span>

<span data-ttu-id="e5481-131">Проигрыватель Windows Media не предоставляет панель навигации для веб-страниц, отображаемых в **воспроизводимой** функции.</span><span class="sxs-lookup"><span data-stu-id="e5481-131">Windows Media Player does not provide a navigation toolbar for webpages displayed in the **Now Playing** feature.</span></span> <span data-ttu-id="e5481-132">Это означает, что вы можете полностью контролировать, могут ли пользователи переходить с веб-страницы Хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="e5481-132">This means that you have complete control over whether users can navigate away from your HTMLView webpage.</span></span> <span data-ttu-id="e5481-133">Если вы хотите разрешить пользователям переходить на другие веб-страницы, необходимо включить в код HTML элементы, чтобы обеспечить эту функциональность.</span><span class="sxs-lookup"><span data-stu-id="e5481-133">If you want to enable users to navigate to other webpages, you must include elements in your HTML code to provide that functionality.</span></span>

## <a name="retrieving-the-parent-window"></a><span data-ttu-id="e5481-134">Получение родительского окна</span><span class="sxs-lookup"><span data-stu-id="e5481-134">Retrieving the parent window</span></span>

<span data-ttu-id="e5481-135">Если существующий код скрипта использует **Window. Parent** для получения объекта родительского окна, этот код не будет работать на веб-странице хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="e5481-135">If your existing script code uses **window.parent** to retrieve the parent window object, this code will not work in your HTMLView webpage.</span></span> <span data-ttu-id="e5481-136">При использовании Хтмлвиев отсутствует объект родительского окна; Поэтому эта функция сценариев недоступна.</span><span class="sxs-lookup"><span data-stu-id="e5481-136">When you use HTMLView, there is no parent window object; therefore, this scripting feature is unavailable.</span></span>

## <a name="about-the-embedded-browser"></a><span data-ttu-id="e5481-137">Сведения о встроенном браузере</span><span class="sxs-lookup"><span data-stu-id="e5481-137">About the embedded browser</span></span>

<span data-ttu-id="e5481-138">Поскольку проигрыватель Windows Media использует встроенный экземпляр Internet Explorer для отображения содержимого Хтмлвиев, параметры пользователя и политики для Internet Explorer применяются ко всем веб-страницам, отображаемым в проигрывателе.</span><span class="sxs-lookup"><span data-stu-id="e5481-138">Because Windows Media Player uses an embedded instance of Internet Explorer to display HTMLView content, the user settings and policies for Internet Explorer apply to any webpages displayed in the Player.</span></span> <span data-ttu-id="e5481-139">Например, если пользователь настроил Internet Explorer так, чтобы веб-страницы не загружали файлы cookie на компьютер, веб-страница Хтмлвиев также не сможет сделать это.</span><span class="sxs-lookup"><span data-stu-id="e5481-139">For example, if the user has configured Internet Explorer to prevent webpages from downloading cookies to the computer, your HTMLView webpage is also prevented from doing this.</span></span>

<span data-ttu-id="e5481-140">Веб-страницы, открытые с помощью функции Хтмлвиев, всегда выполняются в зоне Internet Explorer **Интернет** -безопасности.</span><span class="sxs-lookup"><span data-stu-id="e5481-140">Web pages opened by using the HTMLView feature always run in the Internet Explorer **Internet** security zone.</span></span>

<span data-ttu-id="e5481-141">Внедренный элемент управления веб-браузера использует те же правила для кэширования веб-страниц в качестве изолированной версии Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e5481-141">The embedded Web browser control uses the same rules to cache webpages as the stand-alone version of Internet Explorer.</span></span> <span data-ttu-id="e5481-142">Рекомендуется использовать Active Server страниц (ASP) при создании содержимого, чтобы гарантировать доставку содержимого с веб-сервера каждый раз, когда проигрыватель Windows Media обращается к странице Хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="e5481-142">It's a good idea to use Active Server Pages (ASP) when creating your content to ensure that the content is delivered from your web server each time Windows Media Player accesses the HTMLView webpage.</span></span> <span data-ttu-id="e5481-143">Использование ASP-страниц может быть простым, так же как переименование страницы для использования расширения имени файла. ASP.</span><span class="sxs-lookup"><span data-stu-id="e5481-143">Using ASP pages can be as simple as renaming your webpage to use an .asp file name extension.</span></span>

## <a name="about-local-web-content"></a><span data-ttu-id="e5481-144">Сведения о локальном веб-содержимом</span><span class="sxs-lookup"><span data-stu-id="e5481-144">About local Web content</span></span>

<span data-ttu-id="e5481-145">Функция Хтмлвиев не позволяет открывать веб-страницы, хранящиеся на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="e5481-145">The HTMLView feature does not allow you to open webpages that are stored on the user's computer.</span></span>

## <a name="prompting-the-user"></a><span data-ttu-id="e5481-146">Отправление запроса пользователю</span><span class="sxs-lookup"><span data-stu-id="e5481-146">Prompting the user</span></span>

<span data-ttu-id="e5481-147">Вы можете использовать **Window. prompt** , чтобы запросить у пользователя сведения.</span><span class="sxs-lookup"><span data-stu-id="e5481-147">You can use **window.prompt** to prompt the user for information.</span></span> <span data-ttu-id="e5481-148">Однако **Window. Alert** и **Window. Confirm** недоступны при использовании хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="e5481-148">However, **window.alert** and **window.confirm** are not available when using HTMLView.</span></span>

## <a name="timing-issues"></a><span data-ttu-id="e5481-149">Временные проблемы</span><span class="sxs-lookup"><span data-stu-id="e5481-149">Timing issues</span></span>

<span data-ttu-id="e5481-150">При использовании встроенного элемента управления проигрывателя Windows Media на веб-странице Хтмлвиев могут возникнуть проблемы с временем.</span><span class="sxs-lookup"><span data-stu-id="e5481-150">You may encounter timing issues when using an embedded Windows Media Player control in your HTMLView webpage.</span></span> <span data-ttu-id="e5481-151">В Хтмлвиев встроенный элемент управления Player использует свой модуль воспроизведения с автономным проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e5481-151">In HTMLView, an embedded Player control shares its playback engine with the stand-alone Windows Media Player.</span></span> <span data-ttu-id="e5481-152">Возможно, что автономный проигрыватель может открыться и начать воспроизведение первой записи списка воспроизведения, прежде чем веб-страница (и, следовательно, элемент управления проигрывателя) закончит загрузку.</span><span class="sxs-lookup"><span data-stu-id="e5481-152">It is possible that the stand-alone Player may open and begin playing the first playlist entry before the webpage (and, therefore, the Player control) finishes loading.</span></span> <span data-ttu-id="e5481-153">Это означает, что при обработке событий **опенстатечанже** или **плайстатечанже** код скрипта не будет получать уведомления о событиях для этих событий, пока не будут загружены элемент управления проигрывателя и связанные с ним объекты.</span><span class="sxs-lookup"><span data-stu-id="e5481-153">This means that if you handle the **OpenStateChange** or **PlayStateChange** events, the script code will not receive event notifications for these events until the Player control and its associated objects are loaded.</span></span>

<span data-ttu-id="e5481-154">Можно выполнить действия в коде, чтобы отложить воспроизведение до создания экземпляра элемента управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e5481-154">You can take steps in your code to delay playback until the Windows Media Player control is instantiated.</span></span> <span data-ttu-id="e5481-155">Один из способов сделать это — сделать первую запись в списке воспроизведения метафайла точкой в файле изображения и установить длительность файла в течение времени, в течение которого может загружаться элемент управления проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="e5481-155">One way to do this is to make the first entry in your metafile playlist point to an image file and set the duration of the file to a length of time that allows the Player control to load.</span></span> <span data-ttu-id="e5481-156">Этот параметр показан в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="e5481-156">The following example code demonstrates this option:</span></span>


```XML
<ASX version="3.0">
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>

<ENTRY>
   <REF href="https://www.proseware.com/blank.jpg"/>
   <DURATION  VALUE = "1:00"/>
</ENTRY>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="e5481-157">Когда откроется предыдущий список воспроизведения, проигрыватель Windows Media ждет первую запись в списке воспроизведения до одной минуты, пока проигрыватель загрузит веб-страницу Хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="e5481-157">When the preceding playlist opens, Windows Media Player waits at the first entry in the playlist for up to one minute while the Player loads the HTMLView webpage.</span></span>

<span data-ttu-id="e5481-158">Затем на веб-странице Хтмлвиев напишите код скрипта, обрабатывающий событие **OnLoad** для элемента **Body** .</span><span class="sxs-lookup"><span data-stu-id="e5481-158">Next, in your HTMLView webpage, write script code to handle the **onload** event for the **BODY** element.</span></span> <span data-ttu-id="e5481-159">В функции обработчика событий вызовите метод Player **Controls. Next** , чтобы начать воспроизведение второй записи в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e5481-159">In the event handler function, call the Player **Controls.Next** method to begin playback of the second entry in the playlist.</span></span>


```XML
<HTML>
<!-- Define the event handler function. -->
<BODY  onload = "OnLoad();">

<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">

</OBJECT>

<!-- Handle the BODY onload event. -->
<SCRIPT>
function OnLoad()
{
   // Advance to the second entry in the playlist.
   Player.controls.next();
}
</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="e5481-160">Когда веб-страница в предыдущем примере закончит загрузку, проигрыватель Windows Media немедленно переходит к второй записи в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e5481-160">When the webpage in the preceding example finishes loading, Windows Media Player immediately advances to the second entry in the playlist.</span></span> <span data-ttu-id="e5481-161">Это переопределяет продолжительность, указанную для первого элемента в списке воспроизведения, что означает, что пользователю не нужно ждать полной минуты перед просмотром нужного содержимого; Он должен дождаться завершения загрузки веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="e5481-161">This overrides the duration specified for the first element in the playlist, meaning that the user doesn't have to wait the full one minute before seeing the desired content; he or she only has to wait for the webpage to finish loading.</span></span> <span data-ttu-id="e5481-162">Так как на этом этапе экземпляр элемента управления Player полностью создан, события **опенстатечанже** и **плайстатечанже** могут быть обработаны обычным способом.</span><span class="sxs-lookup"><span data-stu-id="e5481-162">Because the Player control is completely instantiated at this point, the **OpenStateChange** and **PlayStateChange** events can be handled in the usual manner.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5481-163">См. также</span><span class="sxs-lookup"><span data-stu-id="e5481-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5481-164">**Отображение веб-страниц в проигрывателе Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e5481-164">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="e5481-165">**Событие Player. Плайстатечанже**</span><span class="sxs-lookup"><span data-stu-id="e5481-165">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="e5481-166">**Событие Player. Опенстатечанже**</span><span class="sxs-lookup"><span data-stu-id="e5481-166">**Player.OpenStateChange Event**</span></span>](player-player-openstatechange.md)
</dt> </dl>

 

 




