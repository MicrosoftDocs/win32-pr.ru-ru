---
title: Скрытие элемента управления проигрывателя Windows Media
description: Скрытие элемента управления проигрывателя Windows Media
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
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
- внедрение, веб-страницы
- Проигрыватель Windows Media, скрытие элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, скрытие элемента управления ActiveX
- Объектная модель, скрытие элемента управления ActiveX
- Проигрыватель Windows Media Mobile, элемент управления Хидингактивекс
- Элемент управления ActiveX проигрывателя Windows Media, скрытие
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, скрытие
- Элемент управления ActiveX, скрытие
- Элемент управления ActiveX проигрывателя Windows Media, веб-страницы
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, веб-страницы
- Элемент управления ActiveX, веб-страницы
- Внедрение веб-страниц, скрытие элемента управления ActiveX
- Скрытие элемента управления ActiveX проигрывателя Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1add2b8f09829ad165f152c26c184d68ac183
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331456"
---
# <a name="hiding-the-windows-media-player-control"></a><span data-ttu-id="aec66-126">Скрытие элемента управления проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="aec66-126">Hiding the Windows Media Player Control</span></span>

<span data-ttu-id="aec66-127">Объект ActiveX проигрывателя Windows Media внедряется на веб-страницу с помощью элемента OBJECT.</span><span class="sxs-lookup"><span data-stu-id="aec66-127">The Windows Media Player ActiveX object is embedded in a webpage using the OBJECT element.</span></span> <span data-ttu-id="aec66-128">В отличие от более ранних версий, элемент OBJECT, определяющий проигрыватель Windows Media, должен быть помещен в раздел BODY веб-страницы между тегами <BODY> и </BODY> .</span><span class="sxs-lookup"><span data-stu-id="aec66-128">Unlike earlier versions, the OBJECT element that defines Windows Media Player must be placed in the BODY section of a webpage, between the <BODY> and </BODY> tags.</span></span> <span data-ttu-id="aec66-129">Размещение объекта ActiveX проигрывателя Windows Media в разделе HEAD веб-страницы для скрытия пользовательского интерфейса может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="aec66-129">Placing the Windows Media Player ActiveX object in the HEAD section of a webpage to hide the user interface can produce unexpected results.</span></span>

<span data-ttu-id="aec66-130">Если вы поместили элемент управления ActiveX проигрывателя Windows Media в раздел BODY веб-страницы, отобразится пользовательский интерфейс элемента управления.</span><span class="sxs-lookup"><span data-stu-id="aec66-130">If you put the Windows Media Player ActiveX control in the BODY section of a webpage, the control user interface will be displayed.</span></span> <span data-ttu-id="aec66-131">Если вы не хотите, чтобы он отображался, и хотите создать собственный пользовательский интерфейс, установите атрибуты Height и Width элемента OBJECT равными нулю.</span><span class="sxs-lookup"><span data-stu-id="aec66-131">If you do not want it to be displayed, and wish to create your own user interface, set the height and width attributes of the OBJECT element to zero.</span></span>

<span data-ttu-id="aec66-132">Элемент управления также можно сделать невидимым, установив *проигрыватель*. **uiMode** свойство в «невидимый».</span><span class="sxs-lookup"><span data-stu-id="aec66-132">The control can also be made invisible by setting the *Player*.**uiMode** property to "invisible".</span></span> <span data-ttu-id="aec66-133">Это можно сделать с помощью тега PARAM, как описано в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="aec66-133">This can be done using a PARAM tag as discussed in the next section.</span></span> <span data-ttu-id="aec66-134">В этом случае пространство зарезервировано для элемента управления с использованием высоты и ширины, но в зарезервированном пространстве ничего не отображается, пока **uiMode** не изменится на нечто, отличное от "Невидимый".</span><span class="sxs-lookup"><span data-stu-id="aec66-134">In this case, space is reserved for the control using height and width, but nothing is displayed in the reserved space until **uiMode** is changed to something other than "invisible".</span></span>

## <a name="related-topics"></a><span data-ttu-id="aec66-135">См. также</span><span class="sxs-lookup"><span data-stu-id="aec66-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aec66-136">**Использование элемента управления проигрывателя Windows Media на веб-странице**</span><span class="sxs-lookup"><span data-stu-id="aec66-136">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




