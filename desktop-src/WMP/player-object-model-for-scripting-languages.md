---
title: Объектная модель проигрывателя для языков сценариев
description: Объектная модель проигрывателя для языков сценариев
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Проигрыватель Windows Media, объектная модель
- Объектная модель проигрывателя Windows Media, о программе
- Объектная модель, сведения
- Элемент управления ActiveX проигрывателя Windows Media, объектная модель
- Элемент управления ActiveX, объектная модель
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объектная модель
- Проигрыватель Windows Media Mobile, объектная модель
- пакет средств разработки программного обеспечения (SDK), объектная модель элемента управления ActiveX проигрывателя Windows Media
- Пакет SDK (пакет средств разработки программного обеспечения), объектная модель элемента управления ActiveX проигрывателя Windows Media
- Документация, объектная модель элемента управления ActiveX проигрывателя Windows Media
- Проигрыватель Windows Media, языки сценариев
- Объектная модель проигрывателя Windows Media, языки сценариев
- Объектная модель, языки сценариев
- Элемент управления ActiveX проигрывателя Windows Media, языки сценариев
- Элемент управления ActiveX, языки сценариев
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, языки сценариев
- Проигрыватель Windows Media Mobile, языки сценариев
- Языки сценариев
- Проигрыватель Windows Media Player, объект Player
- Объектная модель проигрывателя Windows Media, объект Player
- Объектная модель, объект Player
- Элемент управления ActiveX проигрывателя Windows Media, объект Player
- Элемент управления ActiveX, объект Player
- Элемент управления ActiveX проигрывателя Windows Media Mobile, объект Player
- Проигрыватель Windows Media Mobile, объект Player
- Объект Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670bff03075fd98812dbee269115e297a137e92d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104561722"
---
# <a name="player-object-model-for-scripting-languages"></a><span data-ttu-id="06aa0-129">Объектная модель проигрывателя для языков сценариев</span><span class="sxs-lookup"><span data-stu-id="06aa0-129">Player Object Model for Scripting Languages</span></span>

<span data-ttu-id="06aa0-130">ActiveX использует концепцию объектов для хранения функциональных возможностей программирования.</span><span class="sxs-lookup"><span data-stu-id="06aa0-130">ActiveX uses the concept of objects to contain programming functionality.</span></span> <span data-ttu-id="06aa0-131">Проигрыватель Windows Media использует несколько объектов для разделения функциональных возможностей, предоставляемых элементом управления.</span><span class="sxs-lookup"><span data-stu-id="06aa0-131">Windows Media Player uses several objects to divide up the functionality the control provides.</span></span> <span data-ttu-id="06aa0-132">Корневой объект — это объект **Player** , а другие объекты присоединяются к объекту **Player** через определенные свойства.</span><span class="sxs-lookup"><span data-stu-id="06aa0-132">The root object is the **Player** object, and the other objects are attached to the **Player** object through specific properties.</span></span>

<span data-ttu-id="06aa0-133">На следующей схеме показано, как работает объектная модель элемента управления ActiveX в проигрывателе Windows Media 11 для языков сценариев.</span><span class="sxs-lookup"><span data-stu-id="06aa0-133">The following diagram shows how the Windows Media Player 11 ActiveX control object model works for scripting languages.</span></span>

![Схема объектной модели проигрывателя Windows Media 11](images/playeromdiag.png)

<span data-ttu-id="06aa0-135">В C++ и иногда в языках .NET объекты представлены COM-интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="06aa0-135">In C++, and sometimes in .NET languages, objects are represented by COM interfaces.</span></span> <span data-ttu-id="06aa0-136">В объектной модели проигрывателя Windows Media имена COM-интерфейсов совпадают с именами объектов, но начинаются с префикса "ИВМП".</span><span class="sxs-lookup"><span data-stu-id="06aa0-136">In the Windows Media Player object model, COM interface names are the same as the object name, but are prefixed with "IWMP".</span></span> <span data-ttu-id="06aa0-137">Например, объект **сети** предоставляется через интерфейс **ивмпнетворк** .</span><span class="sxs-lookup"><span data-stu-id="06aa0-137">For example, the **Network** object is exposed through the **IWMPNetwork** interface.</span></span>

<span data-ttu-id="06aa0-138">В следующих разделах приводятся общие обзоры для каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="06aa0-138">The following sections provide conceptual overviews for each object:</span></span>

-   [<span data-ttu-id="06aa0-139">Сведения об объектах CDROM и Кдромколлектион</span><span class="sxs-lookup"><span data-stu-id="06aa0-139">About the Cdrom and CdromCollection Objects</span></span>](about-the-cdrom-and-cdromcollection-objects.md)
-   [<span data-ttu-id="06aa0-140">Сведения об объекте Клоседкаптион</span><span class="sxs-lookup"><span data-stu-id="06aa0-140">About the ClosedCaption Object</span></span>](about-the-closedcaption-object.md)
-   [<span data-ttu-id="06aa0-141">Об объекте Controls</span><span class="sxs-lookup"><span data-stu-id="06aa0-141">About the Controls Object</span></span>](about-the-controls-object.md)
-   [<span data-ttu-id="06aa0-142">Об объекте DVD</span><span class="sxs-lookup"><span data-stu-id="06aa0-142">About the DVD Object</span></span>](about-the-dvd-object.md)
-   [<span data-ttu-id="06aa0-143">Об ошибках и объектах Ерроритем</span><span class="sxs-lookup"><span data-stu-id="06aa0-143">About the Error and ErrorItem Objects</span></span>](about-the-error-and-erroritem-objects.md)
-   [<span data-ttu-id="06aa0-144">Сведения об объектах Медиаколлектион и Media</span><span class="sxs-lookup"><span data-stu-id="06aa0-144">About the MediaCollection and Media Objects</span></span>](about-the-mediacollection-and-media-objects.md)
-   [<span data-ttu-id="06aa0-145">Сведения об объекте Метадатапиктуре</span><span class="sxs-lookup"><span data-stu-id="06aa0-145">About the MetadataPicture Object</span></span>](about-the-metadatapicture-object.md)
-   [<span data-ttu-id="06aa0-146">Сведения об объекте Метадататекст</span><span class="sxs-lookup"><span data-stu-id="06aa0-146">About the MetadataText Object</span></span>](about-the-metadatatext-object.md)
-   [<span data-ttu-id="06aa0-147">О сетевом объекте</span><span class="sxs-lookup"><span data-stu-id="06aa0-147">About the Network Object</span></span>](about-the-network-object.md)
-   [<span data-ttu-id="06aa0-148">Сведения об объекте Player</span><span class="sxs-lookup"><span data-stu-id="06aa0-148">About the Player Object</span></span>](about-the-player-object.md)
-   [<span data-ttu-id="06aa0-149">Сведения об объекте Плайераппликатион</span><span class="sxs-lookup"><span data-stu-id="06aa0-149">About the PlayerApplication Object</span></span>](about-the-playerapplication-object.md)
-   [<span data-ttu-id="06aa0-150">Сведения об объектах списков воспроизведения, Плайлистколлектион и Плайлистаррай</span><span class="sxs-lookup"><span data-stu-id="06aa0-150">About the Playlist, PlaylistCollection, and PlaylistArray Objects</span></span>](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [<span data-ttu-id="06aa0-151">Сведения об объекте Query</span><span class="sxs-lookup"><span data-stu-id="06aa0-151">About the Query Object</span></span>](about-the-query-object.md)
-   [<span data-ttu-id="06aa0-152">Сведения об объекте Settings</span><span class="sxs-lookup"><span data-stu-id="06aa0-152">About the Settings Object</span></span>](about-the-settings-object.md)
-   [<span data-ttu-id="06aa0-153">Сведения об объекте StringCollection</span><span class="sxs-lookup"><span data-stu-id="06aa0-153">About the StringCollection Object</span></span>](about-the-stringcollection-object.md)

<span data-ttu-id="06aa0-154">Дополнительные функциональные возможности доступны через определенные COM-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="06aa0-154">Additional functionality is available through certain COM interfaces.</span></span> <span data-ttu-id="06aa0-155">Доступность этих интерфейсов может зависеть от языка, используемого для программирования, и других факторов, таких как режим, используемый для создания экземпляра элемента управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="06aa0-155">Whether you can access these interfaces may depend on the language you use for programming and other factors, such as the mode used to create the instance of the Windows Media Player control.</span></span> <span data-ttu-id="06aa0-156">Полный список COM-интерфейсов, предоставляемых элементом управления проигрывателя Windows Media, см. в [справочнике по объектной модели для C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="06aa0-156">For a complete list of COM interfaces exposed by the Windows Media Player control, see the [Object Model Reference for C++](object-model-reference-for-c.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06aa0-157">См. также</span><span class="sxs-lookup"><span data-stu-id="06aa0-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06aa0-158">**Сведения об объектной модели проигрывателя**</span><span class="sxs-lookup"><span data-stu-id="06aa0-158">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="06aa0-159">**Использование элемента управления проигрывателя Windows Media в платформа .NET Framework решении**</span><span class="sxs-lookup"><span data-stu-id="06aa0-159">**Using the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




