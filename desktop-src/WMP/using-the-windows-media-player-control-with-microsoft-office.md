---
title: Использование элемента управления проигрывателя Windows Media с Microsoft Office
description: Использование элемента управления проигрывателя Windows Media с Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Проигрыватель Windows Media, Office
- Объектная модель проигрывателя Windows Media, Office
- Объектная модель, Office
- Проигрыватель Windows Media Mobile, Office
- Элемент управления ActiveX проигрывателя Windows Media, Office
- Мобильный элемент управления ActiveX проигрывателя Windows Media, Office
- Элемент управления ActiveX, Office
- Внедрение документов Office
- внедрение, документы Office
- Элемент управления ActiveX проигрывателя Windows Media, Excel
- Элемент управления ActiveX проигрывателя Windows Media Mobile, Excel
- Элемент управления ActiveX, Excel
- внедрение, электронные таблицы Excel
- Внедрение электронных таблиц Excel
- Элемент управления ActiveX проигрывателя Windows Media, PowerPoint
- Элемент управления ActiveX проигрывателя Windows Media Mobile, PowerPoint
- Элемент управления ActiveX, PowerPoint
- внедрение, показ слайдов PowerPoint
- Внедрение показа слайдов PowerPoint
- Элемент управления ActiveX проигрывателя Windows Media, Word
- Элемент управления ActiveX проигрывателя Windows Media Mobile, Word
- Элемент управления ActiveX, Word
- Внедрение документа Word
- внедрение, документы Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504b46b4fb409dede108c41b43014c3aaeae5ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986536"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a><span data-ttu-id="75a0f-134">Использование элемента управления проигрывателя Windows Media с Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="75a0f-134">Using the Windows Media Player Control with Microsoft Office</span></span>

<span data-ttu-id="75a0f-135">В этом разделе описывается внедрение Windows Media Player 9 Series или более поздних элементов управления ActiveX в различные документы, созданные с помощью Microsoft Office XP.</span><span class="sxs-lookup"><span data-stu-id="75a0f-135">This section describes how to embed the Windows Media Player 9 Series or later ActiveX control in various documents created using Microsoft Office XP.</span></span>

<span data-ttu-id="75a0f-136">В Microsoft Word, Excel и PowerPoint® вы внедряете элемент управления, выбрав **объект** в меню **Вставка** , а затем выбрав **проигрыватель Windows Media** из списка доступных типов объектов.</span><span class="sxs-lookup"><span data-stu-id="75a0f-136">In Microsoft Word, Excel, and PowerPoint®, you embed the control by selecting **Object** from the **Insert** menu, then choosing **Windows Media Player** from the list of available object types.</span></span> <span data-ttu-id="75a0f-137">Элемент управления проигрывателя Windows Media появится в документе в текущем расположении.</span><span class="sxs-lookup"><span data-stu-id="75a0f-137">The Windows Media Player control appears in the document at the current location.</span></span> <span data-ttu-id="75a0f-138">Затем можно выбрать пункт **Формат элемента управления** ( **Форматировать объект** в Excel) в контекстном меню для элемента управления, чтобы настроить макет, стиль обтекания текстом и другие параметры форматирования.</span><span class="sxs-lookup"><span data-stu-id="75a0f-138">You can then select **Format Control** ( **Format Object** in Excel) from the shortcut menu for the control to adjust the layout, text wrapping style, and other format options.</span></span> <span data-ttu-id="75a0f-139">Для этого в Word и Excel необходимо находиться в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="75a0f-139">In Word and Excel, you must be in design mode to do this.</span></span>

<span data-ttu-id="75a0f-140">После того как элемент управления позиционирован и отформатирован, его можно настроить с помощью диалогового окна **Свойства** , доступного из **панели элементов "элементы управления** " или из контекстного меню в режиме конструктора для Word и Excel.</span><span class="sxs-lookup"><span data-stu-id="75a0f-140">Once you have positioned and formatted the control, you can configure it using the **Properties** dialog box, which is accessible from the **Control Toolbox** or from the shortcut menu in design mode for Word and Excel.</span></span> <span data-ttu-id="75a0f-141">Здесь можно указать основные свойства управления проигрывателем, такие как имя элемента управления, URL-адрес цифрового файла мультимедиа и режим пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="75a0f-141">Here you can specify basic Player control properties such as the control name, the URL of a digital media file, and the user interface mode.</span></span> <span data-ttu-id="75a0f-142">Присвоение свойству **uiMode** значения «None» скрывает все элементы управления, за исключением окна видео или визуализации, что позволяет добавлять собственные кнопки и писать код скрипта с помощью Visual Basic для приложений (VBA) для управления нажатием кнопок и событиями элемента «управление проигрывателем».</span><span class="sxs-lookup"><span data-stu-id="75a0f-142">Setting the **uiMode** property to "none" hides everything in the control except the video or visualization window, allowing you to add your own buttons and write script code using Visual Basic for Applications (VBA) to handle the button clicks and Player control events.</span></span>

<span data-ttu-id="75a0f-143">В диалоговом окне Основные **Свойства** можно также открыть диалоговое окно **свойства элемента управления проигрывателя Windows Media** , дважды щелкнув строку "(Custom)" или нажав кнопку с многоточием (...) после выбора этой строки.</span><span class="sxs-lookup"><span data-stu-id="75a0f-143">From the basic **Properties** dialog box, you can also access the more sophisticated **Windows Media Player Control Properties** dialog box by double-clicking the "(Custom)" row or by clicking the ellipsis ("...") button after selecting that row.</span></span> <span data-ttu-id="75a0f-144">В этом диалоговом окне можно изменить все доступные свойства элементов управления проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="75a0f-144">From this dialog box, you can modify all available Player control properties.</span></span>

> [!Note]  
> <span data-ttu-id="75a0f-145">Необходимо избегать выполнения действий в обработчиках событий управления проигрывателем, которые приведут к уничтожению элемента управления.</span><span class="sxs-lookup"><span data-stu-id="75a0f-145">You must be careful not to take actions in Player control event handlers that will result in the control being destroyed.</span></span> <span data-ttu-id="75a0f-146">Например, если внедрить элемент управления проигрывателя Windows Media на слайд в презентации PowerPoint, не следует вызывать метод PowerPoint **Next** из события Player **опенстатечанже** или любого другого события.</span><span class="sxs-lookup"><span data-stu-id="75a0f-146">For example, if you embed the Windows Media Player control on a slide in a PowerPoint presentation, do not call the PowerPoint **Next** method from the Player **openStateChange** event or any other event.</span></span>

 

> [!Note]  
> <span data-ttu-id="75a0f-147">Кроме того, не следует задавать свойство **Player. URL** из обработчика событий элемента управления игрока.</span><span class="sxs-lookup"><span data-stu-id="75a0f-147">In addition, you should not set the **Player.URL** property from a Player control event handler.</span></span>

 

<span data-ttu-id="75a0f-148">В приложении FrontPage добавьте элемент управления проигрывателя Windows Media на веб-страницу, выбрав в меню " **Вставка** " пункт " **Интернет-компонент** ".</span><span class="sxs-lookup"><span data-stu-id="75a0f-148">In FrontPage, add the Windows Media Player control to a webpage by selecting **Web Component** from the **Insert** menu.</span></span> <span data-ttu-id="75a0f-149">В диалоговом окне **Вставка веб-компонента** в списке **тип компонента** выберите пункт **Дополнительные элементы управления** , а затем в списке элементов управления выберите **элемент ActiveX** .</span><span class="sxs-lookup"><span data-stu-id="75a0f-149">In the **Insert Web Component** dialog box, select **Advanced Controls** from the **Component type** list, then select **ActiveX Control** from the list of control choices.</span></span> <span data-ttu-id="75a0f-150">В следующем окне диалогового окна выберите **проигрыватель Windows Media**.</span><span class="sxs-lookup"><span data-stu-id="75a0f-150">In the next window of the dialog box, select **Windows Media Player**.</span></span> <span data-ttu-id="75a0f-151">Если его нет в списке, щелкните **настроить** и установите флажок **Windows Media Player** в списке **управления** .</span><span class="sxs-lookup"><span data-stu-id="75a0f-151">If it is not listed, click **Customize** and select the **Windows Media Player** check box in the **Control** list.</span></span>

<span data-ttu-id="75a0f-152">После внедрения элемента управления проигрывателя Windows Media можно изменить его размер и свойства, выбрав **свойства элемента управления ActiveX** в контекстном меню элемента управления.</span><span class="sxs-lookup"><span data-stu-id="75a0f-152">After the Windows Media Player control is embedded, you can position and resize it, and modify its properties by selecting **ActiveX Control Properties** from the shortcut menu for the control.</span></span> <span data-ttu-id="75a0f-153">В представлении HTML заданные свойства отображаются в элементе OBJECT, представляющем элемент управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="75a0f-153">In the HTML view, the property values that you specify appear in the OBJECT element representing the Windows Media Player control.</span></span> <span data-ttu-id="75a0f-154">Имя объекта отображается в качестве атрибута ID, а свойства элемента управления — в виде тегов PARAM.</span><span class="sxs-lookup"><span data-stu-id="75a0f-154">The object name appears as the ID attribute, and the control properties appear as PARAM tags.</span></span> <span data-ttu-id="75a0f-155">Имя объекта предоставляет доступ к объектной модели управления проигрывателя Windows Media, которую можно программировать с помощью Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="75a0f-155">The object name gives you access to the Windows Media Player control object model, which you can program using Microsoft JScript.</span></span> <span data-ttu-id="75a0f-156">Дополнительные сведения см. [в разделе Использование элемента управления проигрывателя Windows Media на веб-странице](using-the-windows-media-player-control-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="75a0f-156">For more information, see [Using the Windows Media Player Control in a Web Page](using-the-windows-media-player-control-in-a-web-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="75a0f-157">См. также</span><span class="sxs-lookup"><span data-stu-id="75a0f-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75a0f-158">**Управление проигрывателем**</span><span class="sxs-lookup"><span data-stu-id="75a0f-158">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




