---
title: Использование элемента управления проигрывателя Windows Media с Microsoft Visual Studio
description: Использование элемента управления проигрывателя Windows Media с Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Проигрыватель Windows Media, .NET Framework
- Объектная модель проигрывателя Windows Media, NET Framework
- Объектная модель, .NET Framework
- Проигрыватель Windows Media Mobile, .NET Framework
- Элемент управления ActiveX проигрывателя Windows Media, .NET Framework
- Элемент управления ActiveX проигрывателя Windows Media Mobile, NET Framework
- Элемент управления ActiveX, NET Framework
- Элемент управления ActiveX проигрывателя Windows Media, Visual Studio
- Элемент управления ActiveX проигрывателя Windows Media Mobile, Visual Studio
- Элемент управления ActiveX, Visual Studio
- Платформа .NET Framework, внедрение программ Visual Studio
- внедрение, программы Visual Studio
- Visual Studio, внедрение программ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b01fecd6acdfd5ccc9a7d823740ef3915bf9c6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "104068677"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a><span data-ttu-id="f24fd-123">Использование элемента управления проигрывателя Windows Media с Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f24fd-123">Using the Windows Media Player Control with Microsoft Visual Studio</span></span>

<span data-ttu-id="f24fd-124">С помощью панели элементов в Visual Studio можно добавить элемент управления ActiveX серии 9 или более поздней версии в приложение платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f24fd-124">You can add the Windows Media Player 9 Series or later ActiveX control to a .NET Framework application through the Toolbox in Visual Studio.</span></span>

## <a name="adding-the-windows-media-player-control"></a><span data-ttu-id="f24fd-125">Добавление элемента управления проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="f24fd-125">Adding the Windows Media Player Control</span></span>

<span data-ttu-id="f24fd-126">Перед созданием нового проекта убедитесь, что на компьютере установлена последняя версия проигрывателя Windows Media и пакет SDK проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f24fd-126">Before creating a new project, make sure that the latest version of Windows Media Player and the Windows Media Player SDK is installed on your computer.</span></span>

<span data-ttu-id="f24fd-127">Запустите Visual Studio, а затем создайте новый проект.</span><span class="sxs-lookup"><span data-stu-id="f24fd-127">Start Visual Studio, then create a new project.</span></span>

<span data-ttu-id="f24fd-128">В Visual Studio откройте область элементов.</span><span class="sxs-lookup"><span data-stu-id="f24fd-128">In Visual Studio, open the Toolbox.</span></span>

<span data-ttu-id="f24fd-129">Если проигрыватель Windows Media не отображается в области **компонентов** панели элементов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f24fd-129">If Windows Media Player does not appear in the **Components** portion of the Toolbox, do the following:</span></span>

1.  <span data-ttu-id="f24fd-130">Щелкните правой кнопкой мыши в области элементов и выберите **пункт Выбрать элементы**.</span><span class="sxs-lookup"><span data-stu-id="f24fd-130">Right-click within the Toolbox, and then select **Choose Items**.</span></span> <span data-ttu-id="f24fd-131">Откроется диалоговое окно **Настройка панели элементов** .</span><span class="sxs-lookup"><span data-stu-id="f24fd-131">This opens the **Customize Toolbox** dialog box.</span></span>
2.  <span data-ttu-id="f24fd-132">На вкладке **COM-компоненты** выберите Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f24fd-132">On the **COM Components** tab, select Windows Media Player.</span></span>

    <span data-ttu-id="f24fd-133">Если проигрыватель Windows Media не отображается в списке, нажмите кнопку **Обзор**, а затем откройте Wmp.dll, который должен находиться в \\ папке Windows System32.</span><span class="sxs-lookup"><span data-stu-id="f24fd-133">If Windows Media Player does not appear in the list, click **Browse**, and then open Wmp.dll, which should be in the Windows\\System32 folder.</span></span>

3.  <span data-ttu-id="f24fd-134">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f24fd-134">Click **OK**.</span></span> <span data-ttu-id="f24fd-135">Элемент управления проигрывателя Windows Media будет помещен на текущую вкладку панели элементов.</span><span class="sxs-lookup"><span data-stu-id="f24fd-135">The Windows Media Player control will be placed on the current Toolbox tab.</span></span>

<span data-ttu-id="f24fd-136">Теперь можно выбрать проигрыватель Windows Media на панели элементов и добавить его в форму.</span><span class="sxs-lookup"><span data-stu-id="f24fd-136">You can now select Windows Media Player in the Toolbox and add it to a form.</span></span>

<span data-ttu-id="f24fd-137">Visual Studio предоставляет проигрывателю Windows Media имя по умолчанию, например "axWindowsMediaPlayer1".</span><span class="sxs-lookup"><span data-stu-id="f24fd-137">Visual Studio gives the Windows Media Player control a default name such as "axWindowsMediaPlayer1".</span></span> <span data-ttu-id="f24fd-138">Может потребоваться изменить имя на что-нибудь более легкое, например "Player".</span><span class="sxs-lookup"><span data-stu-id="f24fd-138">You may want to change the name to something more easily remembered, such as "Player".</span></span>

<span data-ttu-id="f24fd-139">При добавлении элемента управления проигрывателя Windows Media из панели элементов также добавляются ссылки на две библиотеки, созданные Visual Studio, Аксвмплиб и Вмплиб.</span><span class="sxs-lookup"><span data-stu-id="f24fd-139">Adding the Windows Media Player control from the Toolbox also adds references to two libraries created by Visual Studio, AxWMPLib and WMPLib.</span></span> <span data-ttu-id="f24fd-140">Их можно найти в обозреватель решений в разделе **ссылки**.</span><span class="sxs-lookup"><span data-stu-id="f24fd-140">You can find them in the Solution Explorer under **References**.</span></span>

<span data-ttu-id="f24fd-141">Чтобы упростить использование объектов в пространстве имен Player, следует включить пространство имен в директивы using или Import файлов следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f24fd-141">To make using the objects in the Player namespace easier, you should include the namespace in the using or imports directives of your files, as follows:</span></span>


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



<span data-ttu-id="f24fd-142">Директива гарантирует, что вы можете ссылаться на объекты **Player** , не указывая полные имена.</span><span class="sxs-lookup"><span data-stu-id="f24fd-142">The directive ensures that you can refer to **Player** objects without fully qualifying their names.</span></span>

> [!Note]  
> <span data-ttu-id="f24fd-143">Элемент управления проигрывателя Windows Media является объектом **аксвиндовсмедиаплайер** из пространства имен **аксвмплиб** .</span><span class="sxs-lookup"><span data-stu-id="f24fd-143">The Windows Media Player control is an **AxWindowsMediaPlayer** object from the **AxWMPLib** namespace.</span></span> <span data-ttu-id="f24fd-144">Однако класс **аксвиндовсмедиаплайер** использует типы данных, интерфейсы и другие элементы из пространства имен **вмплиб** .</span><span class="sxs-lookup"><span data-stu-id="f24fd-144">However, the **AxWindowsMediaPlayer** class uses data types, interfaces, and other elements from the **WMPLib** namespace.</span></span>

 

## <a name="configuring-visibility-of-the-control"></a><span data-ttu-id="f24fd-145">Настройка видимости элемента управления</span><span class="sxs-lookup"><span data-stu-id="f24fd-145">Configuring Visibility of the Control</span></span>

<span data-ttu-id="f24fd-146">При первом добавлении элемента управления проигрывателя Windows Media в форму он будет виден.</span><span class="sxs-lookup"><span data-stu-id="f24fd-146">When you first add the Windows Media Player control to a form, it will be visible.</span></span> <span data-ttu-id="f24fd-147">Если вы не хотите использовать видимое изображение проигрывателя в приложении, скройте проигрыватель по умолчанию, задав одно из следующих свойств:</span><span class="sxs-lookup"><span data-stu-id="f24fd-147">If you do not want to use the visible image of the Player in your application, hide the default Player by setting any one of the following properties:</span></span>



| <span data-ttu-id="f24fd-148">Свойство</span><span class="sxs-lookup"><span data-stu-id="f24fd-148">Property</span></span>        | <span data-ttu-id="f24fd-149">Значение</span><span class="sxs-lookup"><span data-stu-id="f24fd-149">Value</span></span>                                                 |
|-----------------|-------------------------------------------------------|
| <span data-ttu-id="f24fd-150">**uiMode**</span><span class="sxs-lookup"><span data-stu-id="f24fd-150">**uiMode**</span></span>      | <span data-ttu-id="f24fd-151">"Невидимый" (см. [Player. uiMode](player-uimode.md).)</span><span class="sxs-lookup"><span data-stu-id="f24fd-151">"invisible" (See [Player.uiMode](player-uimode.md).)</span></span> |
| <span data-ttu-id="f24fd-152">**Visible**</span><span class="sxs-lookup"><span data-stu-id="f24fd-152">**Visible**</span></span>     | <span data-ttu-id="f24fd-153">"false"</span><span class="sxs-lookup"><span data-stu-id="f24fd-153">"false"</span></span>                                               |
| <span data-ttu-id="f24fd-154">**Размер. ширина**</span><span class="sxs-lookup"><span data-stu-id="f24fd-154">**Size.Width**</span></span>  | <span data-ttu-id="f24fd-155">0</span><span class="sxs-lookup"><span data-stu-id="f24fd-155">0</span></span>                                                     |
| <span data-ttu-id="f24fd-156">**Размер. Высота**</span><span class="sxs-lookup"><span data-stu-id="f24fd-156">**Size.Height**</span></span> | <span data-ttu-id="f24fd-157">0</span><span class="sxs-lookup"><span data-stu-id="f24fd-157">0</span></span>                                                     |



 

<span data-ttu-id="f24fd-158">Эти свойства можно задать либо в коде, либо в окне **Свойства** при выборе элемента управления проигрывателя Windows Media в конструкторе форм.</span><span class="sxs-lookup"><span data-stu-id="f24fd-158">You can set these properties either in code or in the **Properties** window when the Windows Media Player control is selected in the form designer.</span></span>

## <a name="object-model-compatibility-of-the-control"></a><span data-ttu-id="f24fd-159">Совместимость объектной модели с элементом управления</span><span class="sxs-lookup"><span data-stu-id="f24fd-159">Object Model Compatibility of the Control</span></span>

<span data-ttu-id="f24fd-160">Объектная модель для элемента управления проигрывателя Windows Media практически одинакова в платформа .NET Framework, как в неуправляемом коде и сценарии.</span><span class="sxs-lookup"><span data-stu-id="f24fd-160">The object model for the Windows Media Player control is basically the same in the .NET Framework as in unmanaged code and script.</span></span> <span data-ttu-id="f24fd-161">Однако существуют различия в предоставлении элементов:</span><span class="sxs-lookup"><span data-stu-id="f24fd-161">However, there are differences in how elements are exposed:</span></span>

-   <span data-ttu-id="f24fd-162">Большинство объектов предоставляются под именем своего базового COM-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f24fd-162">Most objects are exposed under the name of their underlying COM interface.</span></span> <span data-ttu-id="f24fd-163">Например, объект **списка воспроизведения** предоставляется как **ивмпплайлист**.</span><span class="sxs-lookup"><span data-stu-id="f24fd-163">For example, the **Playlist** object is exposed as **IWMPPlaylist**.</span></span>
-   <span data-ttu-id="f24fd-164">Некоторые интерфейсы имеют более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="f24fd-164">Some interfaces have later versions.</span></span> <span data-ttu-id="f24fd-165">Например, **ивмпмедиа** была предоставлена дополнительная функциональность в **IWMPMedia2** и **IWMPMedia3**.</span><span class="sxs-lookup"><span data-stu-id="f24fd-165">For example, **IWMPMedia** was given additional functionality in **IWMPMedia2** and **IWMPMedia3**.</span></span> <span data-ttu-id="f24fd-166">Если вы объявили объект как **ивмпмедиа**, у вас обычно есть доступ к функциональным возможностям всех версий интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f24fd-166">If you declare an object as **IWMPMedia**, you usually have access to the functionality of all versions of the interface.</span></span> <span data-ttu-id="f24fd-167">Однако® IntelliSense не распознает методы или свойства интерфейсов более поздней версии, и Visual Basic редактор .NET не будет автоматически исправлять прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="f24fd-167">However, IntelliSense® will not recognize the methods or properties of the later-version interfaces, and the Visual Basic .NET editor will not automatically correct capitalization.</span></span> <span data-ttu-id="f24fd-168">Чтобы получить полное преимущество IntelliSense и других функций Visual Studio, объявите объект с помощью последней версии интерфейса, например **IWMPMedia3**.</span><span class="sxs-lookup"><span data-stu-id="f24fd-168">To get the full benefit of IntelliSense and other features of Visual Studio, declare the object by using the latest version of the interface, such as **IWMPMedia3**.</span></span>
-   <span data-ttu-id="f24fd-169">Нет индексированных свойств (C#) или свойств по умолчанию (Visual Basic .NET).</span><span class="sxs-lookup"><span data-stu-id="f24fd-169">There are no indexed properties (C#) or default properties (Visual Basic .NET).</span></span> <span data-ttu-id="f24fd-170">Например, чтобы получить **список воспроизведения. Item**, необходимо вызвать метод доступа **ивмплайлист. Get \_ Item** в C# или получить свойство **ивмплайист. Item** в Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="f24fd-170">For example, to retrieve a **Playlist.item**, you must call the **IWMPlaylist.get\_Item** accessor method in C# or retrieve the **IWMPlayist.Item** property in Visual Basic .NET.</span></span>
-   <span data-ttu-id="f24fd-171">Из-за конфликта имен между свойством **Controls** проигрывателя Windows Media и свойством **Controls** , предоставляемым каждым элементом управления, версия проигрывателя этого свойства называется **Ктлконтролс** в контексте элемента управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="f24fd-171">Because of a naming conflict between the Windows Media Player **Controls** property and the **Controls** property exposed by every control, the Player version of this property is called **CtlControls** in the context of the ActiveX control.</span></span> <span data-ttu-id="f24fd-172">(Однако это не так, когда вы создаете проигрыватель программным способом, а не как элемент управления ActiveX.)</span><span class="sxs-lookup"><span data-stu-id="f24fd-172">(However, this is not the case when you create the Player programmatically rather than as an ActiveX control.)</span></span>

<span data-ttu-id="f24fd-173">Используйте обозреватель объектов в Visual Studio для нахождение правильных имен API для методов и объектов в пространствах имен **аксвмплиб** и **вмплиб** .</span><span class="sxs-lookup"><span data-stu-id="f24fd-173">Use the Object Browser in Visual Studio to locate the correct API names for methods and objects in the **AxWMPLib** and **WMPLib** namespaces.</span></span>

## <a name="distributing-your-application"></a><span data-ttu-id="f24fd-174">Распространение приложения</span><span class="sxs-lookup"><span data-stu-id="f24fd-174">Distributing Your Application</span></span>

<span data-ttu-id="f24fd-175">При распространении приложения не забудьте установить AxInterop.WMPLib.dll и Interop.WMPLib.dll в папке приложения.</span><span class="sxs-lookup"><span data-stu-id="f24fd-175">When you distribute your application, be sure to install AxInterop.WMPLib.dll and Interop.WMPLib.dll in the application folder.</span></span> <span data-ttu-id="f24fd-176">Также необходимо убедиться, что на компьютере пользователя установлена требуемая версия проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f24fd-176">You will also need to make sure that the required Windows Media Player version is installed on the user's computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f24fd-177">См. также</span><span class="sxs-lookup"><span data-stu-id="f24fd-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f24fd-178">**Создание элемента управления проигрывателя Windows Media программным способом**</span><span class="sxs-lookup"><span data-stu-id="f24fd-178">**Creating the Windows Media Player Control Programmatically**</span></span>](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[<span data-ttu-id="f24fd-179">**Внедрение элемента управления проигрывателя Windows Media в решение C#**</span><span class="sxs-lookup"><span data-stu-id="f24fd-179">**Embedding the Windows Media Player Control in a C# Solution**</span></span>](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[<span data-ttu-id="f24fd-180">**Внедрение элемента управления проигрывателя Windows Media в решение Visual Basic .NET**</span><span class="sxs-lookup"><span data-stu-id="f24fd-180">**Embedding the Windows Media Player Control in a Visual Basic .NET Solution**</span></span>](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




