---
title: Использование сценария на веб-странице, отображаемой Firefox
description: Использование сценария на веб-странице, отображаемой Firefox
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Элемент управления ActiveX проигрывателя Windows Media, веб-страницы
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, веб-страницы
- Элемент управления ActiveX, веб-страницы
- Элемент управления ActiveX проигрывателя Windows Media, пример сценария
- Элемент управления ActiveX проигрывателя Windows Media для мобильных устройств, пример сценария
- Элемент управления ActiveX, пример сценария
- внедрение, веб-страницы
- Внедрение веб-страниц, пример сценария
- Проигрыватель Windows Media, Firefox
- Объектная модель проигрывателя Windows Media, Firefox
- Объектная модель, Firefox
- Проигрыватель Windows Media Mobile, Firefox
- Элемент управления ActiveX проигрывателя Windows Media, Firefox
- Элемент управления ActiveX проигрывателя Windows Media Mobile, Firefox
- Элемент управления ActiveX, Firefox
- Firefox, пример сценария
- Внедрение веб-страниц, Firefox
- Пример сценария для внедрения веб-страниц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8629f87f954d12602999f76483fdd36ab279290
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "105700727"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="7778c-128">Использование сценария на веб-странице, отображаемой Firefox</span><span class="sxs-lookup"><span data-stu-id="7778c-128">Using Script in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="7778c-129">Скрипт на веб-странице может использовать объектную модель проигрывателя для управления проигрывателем при взаимодействии пользователя со страницей.</span><span class="sxs-lookup"><span data-stu-id="7778c-129">Script on a webpage can use the Player object model to control the Player as the user interacts with the page.</span></span> <span data-ttu-id="7778c-130">Например, следующий элемент INPUT содержит сценарий, который задает громкость проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="7778c-130">For example, the following INPUT element has script that sets the Player volume.</span></span>


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



<span data-ttu-id="7778c-131">Многие объекты в объектной модели проигрывателя Windows Media поддерживаются Internet Explorer и подключаемым модулем Firefox.</span><span class="sxs-lookup"><span data-stu-id="7778c-131">Many of the objects in the Windows Media Player object model are supported by Internet Explorer and by the Firefox plug-in.</span></span> <span data-ttu-id="7778c-132">Тем не менее некоторые объекты не поддерживаются подключаемым модулем Firefox.</span><span class="sxs-lookup"><span data-stu-id="7778c-132">However, there are some objects that are not supported by the Firefox plug-in.</span></span> <span data-ttu-id="7778c-133">В следующей таблице перечислены все объекты в объектной модели проигрывателя и показано, какие объекты поддерживаются подключаемым модулем Firefox.</span><span class="sxs-lookup"><span data-stu-id="7778c-133">The following table lists all of the objects in the Player object model and shows which objects are supported by the Firefox plug-in.</span></span>



| <span data-ttu-id="7778c-134">Объект</span><span class="sxs-lookup"><span data-stu-id="7778c-134">Object</span></span>                                              | <span data-ttu-id="7778c-135">Поддержка Firefox</span><span class="sxs-lookup"><span data-stu-id="7778c-135">Firefox support</span></span> |
|-----------------------------------------------------|-----------------|
| [<span data-ttu-id="7778c-136">ROM</span><span class="sxs-lookup"><span data-stu-id="7778c-136">Cdrom</span></span>](cdrom-object.md)                           | <span data-ttu-id="7778c-137">Нет</span><span class="sxs-lookup"><span data-stu-id="7778c-137">no</span></span>              |
| [<span data-ttu-id="7778c-138">кдромколлектион</span><span class="sxs-lookup"><span data-stu-id="7778c-138">CdromCollection</span></span>](cdromcollection-object.md)       | <span data-ttu-id="7778c-139">Нет</span><span class="sxs-lookup"><span data-stu-id="7778c-139">no</span></span>              |
| [<span data-ttu-id="7778c-140">клоседкаптион</span><span class="sxs-lookup"><span data-stu-id="7778c-140">ClosedCaption</span></span>](closedcaption-object.md)           | <span data-ttu-id="7778c-141">да</span><span class="sxs-lookup"><span data-stu-id="7778c-141">yes</span></span>             |
| [<span data-ttu-id="7778c-142">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="7778c-142">Controls</span></span>](controls-object.md)                     | <span data-ttu-id="7778c-143">Нет</span><span class="sxs-lookup"><span data-stu-id="7778c-143">no</span></span>              |
| [<span data-ttu-id="7778c-144">ОПТИЧЕСКИ</span><span class="sxs-lookup"><span data-stu-id="7778c-144">DVD</span></span>](dvd-object.md)                               | <span data-ttu-id="7778c-145">Нет</span><span class="sxs-lookup"><span data-stu-id="7778c-145">no</span></span>              |
| [<span data-ttu-id="7778c-146">Ошибка</span><span class="sxs-lookup"><span data-stu-id="7778c-146">Error</span></span>](error-object.md)                           | <span data-ttu-id="7778c-147">да</span><span class="sxs-lookup"><span data-stu-id="7778c-147">yes</span></span>             |
| [<span data-ttu-id="7778c-148">ерроритем</span><span class="sxs-lookup"><span data-stu-id="7778c-148">ErrorItem</span></span>](erroritem-object.md)                   | <span data-ttu-id="7778c-149">да</span><span class="sxs-lookup"><span data-stu-id="7778c-149">yes</span></span>             |
| [<span data-ttu-id="7778c-150">Носитель</span><span class="sxs-lookup"><span data-stu-id="7778c-150">Media</span></span>](media-object.md)                           | <span data-ttu-id="7778c-151">да</span><span class="sxs-lookup"><span data-stu-id="7778c-151">yes</span></span>             |
| [<span data-ttu-id="7778c-152">медиаколлектион</span><span class="sxs-lookup"><span data-stu-id="7778c-152">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="7778c-153">Нет</span><span class="sxs-lookup"><span data-stu-id="7778c-153">no</span></span>              |
| [<span data-ttu-id="7778c-154">метадатапиктуре</span><span class="sxs-lookup"><span data-stu-id="7778c-154">MetadataPicture</span></span>](metadatapicture-object.md)       | <span data-ttu-id="7778c-155">Нет</span><span class="sxs-lookup"><span data-stu-id="7778c-155">no</span></span>              |
| [<span data-ttu-id="7778c-156">метадататекст</span><span class="sxs-lookup"><span data-stu-id="7778c-156">MetadataText</span></span>](metadatatext-object.md)             | <span data-ttu-id="7778c-157">Нет</span><span class="sxs-lookup"><span data-stu-id="7778c-157">no</span></span>              |
| [<span data-ttu-id="7778c-158">Network</span><span class="sxs-lookup"><span data-stu-id="7778c-158">Network</span></span>](network-object.md)                       | <span data-ttu-id="7778c-159">да</span><span class="sxs-lookup"><span data-stu-id="7778c-159">yes</span></span>             |
| [<span data-ttu-id="7778c-160">Игрок</span><span class="sxs-lookup"><span data-stu-id="7778c-160">Player</span></span>](player-object.md)                         | <span data-ttu-id="7778c-161">да</span><span class="sxs-lookup"><span data-stu-id="7778c-161">yes</span></span>             |
| [<span data-ttu-id="7778c-162">PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="7778c-162">PlayerApplication</span></span>](playerapplication-object.md)   | <span data-ttu-id="7778c-163">Нет</span><span class="sxs-lookup"><span data-stu-id="7778c-163">no</span></span>              |
| [<span data-ttu-id="7778c-164">Списком</span><span class="sxs-lookup"><span data-stu-id="7778c-164">Playlist</span></span>](playlist-object.md)                     | <span data-ttu-id="7778c-165">да</span><span class="sxs-lookup"><span data-stu-id="7778c-165">yes</span></span>             |
| [<span data-ttu-id="7778c-166">плайлистаррай</span><span class="sxs-lookup"><span data-stu-id="7778c-166">PlaylistArray</span></span>](playlistarray-object.md)           | <span data-ttu-id="7778c-167">Нет</span><span class="sxs-lookup"><span data-stu-id="7778c-167">no</span></span>              |
| [<span data-ttu-id="7778c-168">плайлистколлектион</span><span class="sxs-lookup"><span data-stu-id="7778c-168">PlaylistCollection</span></span>](playlistcollection-object.md) | <span data-ttu-id="7778c-169">Нет</span><span class="sxs-lookup"><span data-stu-id="7778c-169">no</span></span>              |
| [<span data-ttu-id="7778c-170">Запрос</span><span class="sxs-lookup"><span data-stu-id="7778c-170">Query</span></span>](query-object.md)                           | <span data-ttu-id="7778c-171">Нет</span><span class="sxs-lookup"><span data-stu-id="7778c-171">no</span></span>              |
| [<span data-ttu-id="7778c-172">Параметры</span><span class="sxs-lookup"><span data-stu-id="7778c-172">Settings</span></span>](settings-object.md)                     | <span data-ttu-id="7778c-173">да</span><span class="sxs-lookup"><span data-stu-id="7778c-173">yes</span></span>             |
| [<span data-ttu-id="7778c-174">StringCollection</span><span class="sxs-lookup"><span data-stu-id="7778c-174">StringCollection</span></span>](stringcollection-object.md)     | <span data-ttu-id="7778c-175">Нет</span><span class="sxs-lookup"><span data-stu-id="7778c-175">no</span></span>              |



 

<span data-ttu-id="7778c-176">Подключаемый модуль Firefox поддерживает объект **Player** , но некоторые свойства объекта **Player** возвращают **значение NULL** в браузере Firefox.</span><span class="sxs-lookup"><span data-stu-id="7778c-176">The Firefox plug-in supports the **Player** object, but certain properties of the **Player** object return **NULL** in a Firefox browser.</span></span> <span data-ttu-id="7778c-177">Например, свойство [кдромколлектион](player-cdromcollection.md) объекта **Player** возвращает **значение NULL** , так как подключаемый модуль Firefox не поддерживает объект **CDROM** .</span><span class="sxs-lookup"><span data-stu-id="7778c-177">For example, the [cdromCollection](player-cdromcollection.md) property of the **Player** object returns **NULL** because the Firefox plug-in does not support the **Cdrom** object.</span></span> <span data-ttu-id="7778c-178">Аналогичным образом, свойства [DVD](player-dvd.md), [медиаколлектион](player-mediacollection.md), [плайераппликатион](player-playerapplication.md)и [плайлистколлектион](player-playlistcollection.md) объекта **Player** возвращают **значение NULL** в браузере Firefox.</span><span class="sxs-lookup"><span data-stu-id="7778c-178">Similarly, the [dvd](player-dvd.md), [mediaCollection](player-mediacollection.md), [playerApplication](player-playerapplication.md), and [playlistCollection](player-playlistcollection.md) properties of the **Player** object return **NULL** in a Firefox browser.</span></span>

<span data-ttu-id="7778c-179">Свойство **Player. плугинверсионинфо** поддерживается подключаемым модулем Firefox, но не Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="7778c-179">The **Player.pluginVersionInfo** property is supported by the Firefox plug-in but not by Internet Explorer.</span></span> <span data-ttu-id="7778c-180">Это свойство возвращает версию подключаемого модуля Firefox.</span><span class="sxs-lookup"><span data-stu-id="7778c-180">This property returns the version of the Firefox plug-in.</span></span>

<span data-ttu-id="7778c-181">Подключаемый модуль Firefox поддерживает объект **мультимедиа** , включая свойство [жетитеминфобитипе](media-getiteminfobytype.md) .</span><span class="sxs-lookup"><span data-stu-id="7778c-181">The Firefox plug-in supports the **Media** object, including the [getItemInfoByType](media-getiteminfobytype.md) property.</span></span> <span data-ttu-id="7778c-182">Однако в браузере Firefox свойство **жетитеминфобитипе** не поддерживает возвращаемые типы **метадататекст** и **метадатапиктуре** .</span><span class="sxs-lookup"><span data-stu-id="7778c-182">However, in a Firefox browser, the **getItemInfoByType** property does not support the **MetadataText** and **MetadataPicture** return types.</span></span>

<span data-ttu-id="7778c-183">Подключаемый модуль Firefox поддерживает объект [Settings](settings-object.md) , за исключением метода [SetMode](settings-setmode.md) и свойства [рекуестмедиаакцессригхтс](settings-requestmediaaccessrights.md) .</span><span class="sxs-lookup"><span data-stu-id="7778c-183">The Firefox plug-in supports the [Settings](settings-object.md) object except for the [setMode](settings-setmode.md) method and the [requestMediaAccessRights](settings-requestmediaaccessrights.md) property.</span></span> <span data-ttu-id="7778c-184">В браузере Firefox свойство **рекуестмедиаакцессригхт** всегда возвращает значение false.</span><span class="sxs-lookup"><span data-stu-id="7778c-184">In a Firefox browser, the **requestMediaAccessRight** property always returns false.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7778c-185">См. также</span><span class="sxs-lookup"><span data-stu-id="7778c-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7778c-186">**Использование элемента управления проигрывателя Windows Media с браузером Firefox**</span><span class="sxs-lookup"><span data-stu-id="7778c-186">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




