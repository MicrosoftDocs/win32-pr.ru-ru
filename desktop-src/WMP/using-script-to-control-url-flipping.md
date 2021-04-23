---
title: Использование сценария для управления перелистыванием URL-адресов
description: Использование сценария для управления перелистыванием URL-адресов
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Проигрыватель Windows Media, веб-презентации
- Объектная модель проигрывателя Windows Media, веб-презентации
- Объектная модель, веб-презентации
- Проигрыватель Windows Media Mobile, веб-презентации
- Элемент управления ActiveX проигрывателя Windows Media, веб-презентации
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, веб-презентации
- Элементы управления ActiveX, веб-презентации
- Проигрыватель Windows Media, перелистывание URL-адресов
- Объектная модель проигрывателя Windows Media, перелистывание URL-адресов
- Объектная модель, перелистывание URL-адресов
- Проигрыватель Windows Media Mobile, зеркальное отображение URL-адресов
- Элемент управления ActiveX проигрывателя Windows Media, зеркальное отображение URL-адресов
- Мобильный элемент управления ActiveX проигрывателя Windows Media, зеркальное отображение URL-адресов
- Элемент управления ActiveX, перелистывание URL-адресов
- Веб-презентации, перелистывание URL-адресов
- Создание веб-презентаций, перелистывание URL-адресов
- Перелистывание URL-адресов
- Проигрыватель Windows Media, мультимедийная потоковая передача мультимедиа
- Объектная модель проигрывателя Windows Media, мультимедийная потоковая передача мультимедиа
- Объектная модель, многофункциональная потоковая передача мультимедиа
- Проигрыватель Windows Media Mobile, многофункциональная потоковая передача мультимедиа
- Элемент управления ActiveX проигрывателя Windows Media, мультимедийная потоковая передача мультимедиа
- Мобильный элемент управления ActiveX проигрывателя Windows Media, мультимедийная потоковая передача мультимедиа
- Элемент управления ActiveX, мультимедийная потоковая передача
- Веб-презентации, многофункциональная потоковая передача мультимедиа
- Создание веб-презентаций, многофункциональная потоковая передача мультимедиа
- Мультимедийная потоковая передача мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4815562bba92d67bb4b02ea0317d6c29accd9262
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "104411481"
---
# <a name="using-script-to-control-url-flipping"></a><span data-ttu-id="dbb4f-130">Использование сценария для управления перелистыванием URL-адресов</span><span class="sxs-lookup"><span data-stu-id="dbb4f-130">Using Script to Control URL Flipping</span></span>

<span data-ttu-id="dbb4f-131">Когда пользователь подключается к многофункциональному потоку мультимедиа, пока поток уже выполняется, потоковая веб-страница может отображаться до того, как все элементы будут получены и кэшированы, если проигрыватель Windows Media автоматически вызовет этот URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="dbb4f-131">When a user connects to a rich media stream while the stream is already in progress, it is possible for the streamed webpage to display before all the elements have arrived and been cached if Windows Media Player automatically invokes the URL.</span></span> <span data-ttu-id="dbb4f-132">В этом случае пользователь видит пустую или неполную веб-страницу, пока следующий набор данных не поступит в кэш.</span><span class="sxs-lookup"><span data-stu-id="dbb4f-132">When this happens, the user sees a blank or incomplete webpage until the next set of data arrives in the cache.</span></span>

<span data-ttu-id="dbb4f-133">Можно избежать отображения пустой или неполной веб-страницы, вызвав URL-адрес с помощью сценария вместо того, чтобы проигрыватель Windows Media сделает его автоматически.</span><span class="sxs-lookup"><span data-stu-id="dbb4f-133">You can avoid displaying a blank or incomplete webpage by invoking the URL using script instead of letting Windows Media Player do it automatically.</span></span> <span data-ttu-id="dbb4f-134">Таким образом, можно пропустить первый URL-адрес отражения, а затем вызвать последующие URL-адреса с помощью кода скрипта.</span><span class="sxs-lookup"><span data-stu-id="dbb4f-134">That way, you can ignore the first URL flip and then invoke subsequent URLs by using script code.</span></span>

> [!Note]  
> <span data-ttu-id="dbb4f-135">В этом разделе предполагается, что вы используете потоковую передачу HTML с помощью пакета SDK для Windows Media Encoder 9 и вы настроили поток HTML для повторения.</span><span class="sxs-lookup"><span data-stu-id="dbb4f-135">This section assumes that you are streaming HTML using the Windows Media Encoder 9 Series SDK and that you have set the HTML stream to repeat.</span></span>

 

<span data-ttu-id="dbb4f-136">Сначала необходимо создать веб-страницу набора фреймов, содержащую фрейм с внедренным проигрывателем, и фрейм, отображающий HTML-код потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="dbb4f-136">First, you must create a frameset webpage to contain the frame with the embedded Player and the frame that displays the streaming HTML.</span></span> <span data-ttu-id="dbb4f-137">Каждый из этих двух кадров изначально будет отображать отдельную веб-страницу, поэтому вы создадите всего три веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="dbb4f-137">Each of these two frames will display a separate webpage initially, so you will create a total of three webpages.</span></span> <span data-ttu-id="dbb4f-138">В следующем примере кода показана веб-страница FRAMESET:</span><span class="sxs-lookup"><span data-stu-id="dbb4f-138">The following example code demonstrates the frameset webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>

<FRAMESET cols = "350, *">
  <FRAME  name = "player" src = "embed_player.htm">
  <FRAME  name = "content" src = "blank.htm">

  <NOFRAMES>
  <BODY>

  <P>This page uses frames, but your browser doesn't support them.</P>

  </BODY>
  </NOFRAMES>

</FRAMESET>
</HTML>

```



<span data-ttu-id="dbb4f-139">Предыдущий пример веб-страницы включает два кадра.</span><span class="sxs-lookup"><span data-stu-id="dbb4f-139">The preceding webpage example incorporates two frames.</span></span> <span data-ttu-id="dbb4f-140">Первый кадр отображается в левой половине окна браузера и отображает веб-страницу с именем embed \_player.htm.</span><span class="sxs-lookup"><span data-stu-id="dbb4f-140">The first frame displays in the left half of the browser window and displays the webpage named embed\_player.htm.</span></span> <span data-ttu-id="dbb4f-141">В следующем примере кода создается эта веб-страница:</span><span class="sxs-lookup"><span data-stu-id="dbb4f-141">The following example code creates this webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

<!-- Embed Windows Media Player and disable the invokeURLs parameter -->
<OBJECT CLASSID = "CLSID:6BF52A52-394A-11D3-B153-00C04F79FAA6" ID = "Player">
  <PARAM name = "URL"  value = "https://www.proseware.com/Media/video.wmv">
  <PARAM name = "invokeURLs"  value = "false">
</OBJECT>

<SCRIPT LANGUAGE = "JScript">
  var bFirstURL = true; // Global flag for first URL flip.
</SCRIPT>

<!-- Create an event handler for script commands. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player" EVENT = "ScriptCommand(scType, scParam)">

  if("URL" == scType)
  {
    if ( bFirstURL == false )
    {
      // Show the next URL flip.
      parent.content.location = scParam;
    }
    else
    {
      bFirstURL = false; // Set the flag.
    }
  }

</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="dbb4f-142">Второй кадр в наборе фреймов отображается в правой половине окна браузера и отображает веб-страницу с именем "blank.htm".</span><span class="sxs-lookup"><span data-stu-id="dbb4f-142">The second frame in the frameset displays in the right half of the browser window and displays a webpage named "blank.htm".</span></span> <span data-ttu-id="dbb4f-143">В следующем примере кода создается эта веб-страница:</span><span class="sxs-lookup"><span data-stu-id="dbb4f-143">The following example code creates this webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



<span data-ttu-id="dbb4f-144">Когда страница набора фреймов загружается в браузере, в левом фрейме отображается встроенный проигрыватель, а в правой — текст "Загрузка...". для информирования пользователя о том, что повышены дополнительные данные.</span><span class="sxs-lookup"><span data-stu-id="dbb4f-144">When the frameset page loads in the browser, the left frame shows the embedded Player and the right frame shows the text "Loading..." to inform the user that more data is forthcoming.</span></span> <span data-ttu-id="dbb4f-145">Когда команда сценария First URL поступает из потока HTML, обработчик событий просто изменяет значение **логического** флага.</span><span class="sxs-lookup"><span data-stu-id="dbb4f-145">When the first URL script command arrives from the HTML stream, the event handler simply changes the value of the **Boolean** flag.</span></span> <span data-ttu-id="dbb4f-146">При появлении каждой последующей команды сценария URL-адреса из потока HTML скрипт в обработчике событий загружает новый URL-адрес в кадр с именем "содержимое", а вся веб-страница отображается в рамке, расположенной в правой половине окна браузера.</span><span class="sxs-lookup"><span data-stu-id="dbb4f-146">When each subsequent URL script command arrives from the HTML stream, the script in the event handler loads the new URL into the frame named "content", and the complete webpage displays in the frame located in the right half of the browser window.</span></span>

<span data-ttu-id="dbb4f-147">Дополнительные сведения о потоковой передаче HTML-кода с помощью Windows Media см. в разделе пакет SDK для кодировщика Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dbb4f-147">For more information about streaming HTML using Windows Media, see the Windows Media Encoder SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbb4f-148">См. также</span><span class="sxs-lookup"><span data-stu-id="dbb4f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbb4f-149">**Мультимедийная потоковая передача мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="dbb4f-149">**Rich Media Streaming**</span></span>](rich-media-streaming.md)
</dt> <dt>

[<span data-ttu-id="dbb4f-150">**Перелистывание URL-адресов**</span><span class="sxs-lookup"><span data-stu-id="dbb4f-150">**URL Flipping**</span></span>](url-flipping.md)
</dt> </dl>

 

 




