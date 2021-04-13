---
title: Использование элемента управления проигрывателя Windows Media с браузером Firefox
description: Использование элемента управления проигрывателя Windows Media с браузером Firefox
ms.assetid: a95529d6-7508-4e27-adfe-bbbf4dcaffce
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
- Проигрыватель Windows Media, Firefox
- Объектная модель проигрывателя Windows Media, Firefox
- Объектная модель, Firefox
- Проигрыватель Windows Media Mobile, Firefox
- Элемент управления ActiveX проигрывателя Windows Media, Firefox
- Элемент управления ActiveX проигрывателя Windows Media Mobile, Firefox
- Элемент управления ActiveX, Firefox
- Firefox, о внедрении веб-страниц
- внедрение, веб-страницы
- Внедрение веб-страниц, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253dd21312409fe2c97bf94c36397efed8353bdb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104413969"
---
# <a name="using-the-windows-media-player-control-with-firefox"></a><span data-ttu-id="333ec-123">Использование элемента управления проигрывателя Windows Media с браузером Firefox</span><span class="sxs-lookup"><span data-stu-id="333ec-123">Using the Windows Media Player Control with Firefox</span></span>

<span data-ttu-id="333ec-124">Корпорация Майкрософт предоставляет подключаемый модуль, который позволяет внедрить элемент управления ActiveX проигрывателя Windows Media на веб-страницу, чтобы он правильно отображался браузером Firefox.</span><span class="sxs-lookup"><span data-stu-id="333ec-124">Microsoft provides a plug-in that enables you to embed the Windows Media Player ActiveX control in a webpage so that it will be displayed correctly by a Firefox browser.</span></span> <span data-ttu-id="333ec-125">Подключаемый модуль, который должен быть установлен на клиентском компьютере, можно скачать с [веб-сайта Microsoft Port25](https://www.mozilla.org/).</span><span class="sxs-lookup"><span data-stu-id="333ec-125">The plug-in, which must be installed on the client computer, can be downloaded from the [Microsoft Port25 website](https://www.mozilla.org/).</span></span>

<span data-ttu-id="333ec-126">Сведения о браузере Firefox см. на [веб-сайте Firefox](https://www.mozilla.org/).</span><span class="sxs-lookup"><span data-stu-id="333ec-126">For information about the Firefox browser, see the [Firefox website](https://www.mozilla.org/).</span></span>

<span data-ttu-id="333ec-127">Дополнительные сведения об использовании проигрывателя Windows Media с Firefox см. в разделе Windows Media Player на [веб-сайте мозиллазине](http://kb.mozillazine.org/Windows_Media_Player).</span><span class="sxs-lookup"><span data-stu-id="333ec-127">For more information about using Windows Media Player with Firefox, see the Windows Media Player section of the [mozillaZine website](http://kb.mozillazine.org/Windows_Media_Player).</span></span>

<span data-ttu-id="333ec-128">В следующих разделах описывается внедрение элемента управления проигрывателя Windows Media на веб-страницу, которая может отображаться правильно в Internet Explorer и Firefox.</span><span class="sxs-lookup"><span data-stu-id="333ec-128">The following topics describe how to embed the Windows Media Player control in a webpage that can be displayed correctly by both Internet Explorer and Firefox.</span></span>



| <span data-ttu-id="333ec-129">Раздел</span><span class="sxs-lookup"><span data-stu-id="333ec-129">Topic</span></span>                                                                                                                                    | <span data-ttu-id="333ec-130">Описание</span><span class="sxs-lookup"><span data-stu-id="333ec-130">Description</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="333ec-131">Внедрение элемента управления игрока в веб-страницу, отображаемую в браузере Firefox</span><span class="sxs-lookup"><span data-stu-id="333ec-131">Embedding the Player Control in a Web Page Displayed by Firefox</span></span>](embedding-the-player-control-in-a-web-page-displayed-by-firefox.md)   | <span data-ttu-id="333ec-132">Описывает, как скрипт записи, создающий ОБЪЕКТный элемент, совместимый с Internet Explorer и Firefox.</span><span class="sxs-lookup"><span data-stu-id="333ec-132">Describes how write script that creates an OBJECT element that is compatible with both Internet Explorer and Firefox.</span></span> |
| [<span data-ttu-id="333ec-133">Использование элементов PARAM на веб-странице, отображаемой Firefox</span><span class="sxs-lookup"><span data-stu-id="333ec-133">Using PARAM Elements in a Web Page Displayed by Firefox</span></span>](using-param-elements-in-a-web-page-displayed-by-firefox.md)                   | <span data-ttu-id="333ec-134">Описывает элементы PARAM, поддерживаемые подключаемым модулем Firefox.</span><span class="sxs-lookup"><span data-stu-id="333ec-134">Describes the PARAM elements that are supported by the Firefox plug-in.</span></span>                                               |
| [<span data-ttu-id="333ec-135">Использование сценария на веб-странице, отображаемой Firefox</span><span class="sxs-lookup"><span data-stu-id="333ec-135">Using Script in a Web Page Displayed by Firefox</span></span>](using-script-in-a-web-page-displayed-by-firefox.md)                                   | <span data-ttu-id="333ec-136">Описывает объекты проигрывателя Windows Media, поддерживаемые подключаемым модулем Firefox.</span><span class="sxs-lookup"><span data-stu-id="333ec-136">Describes the Windows Media Player objects that are supported by the Firefox plug-in.</span></span>                                 |
| [<span data-ttu-id="333ec-137">Обработка событий на веб-странице, отображаемой Firefox</span><span class="sxs-lookup"><span data-stu-id="333ec-137">Handling Events in a Web Page Displayed by Firefox</span></span>](handling-events-in-a-web-page-displayed-by-firefox.md)                             | <span data-ttu-id="333ec-138">Описание процесса написания скрипта на веб-странице, отображаемой Firefox, которая обрабатывает события проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="333ec-138">Describes how to write script, in a webpage displayed by Firefox, that handles Windows Media Player events.</span></span>           |
| [<span data-ttu-id="333ec-139">Использование свойства Инвокеурлс на веб-странице, отображаемой в браузере Firefox</span><span class="sxs-lookup"><span data-stu-id="333ec-139">Using the invokeURLs Property in a Web Page Displayed by Firefox</span></span>](using-the-invokeurls-property-in-a-web-page-displayed-by-firefox.md) | <span data-ttu-id="333ec-140">В этой статье описывается, как реагировать на команды сценария типа URL на веб-странице, отображаемой Firefox.</span><span class="sxs-lookup"><span data-stu-id="333ec-140">Describes how to respond to URL-type script commands in a webpage displayed by Firefox.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="333ec-141">См. также</span><span class="sxs-lookup"><span data-stu-id="333ec-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="333ec-142">**Использование элемента управления проигрывателя Windows Media на веб-странице**</span><span class="sxs-lookup"><span data-stu-id="333ec-142">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




