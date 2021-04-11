---
title: Внедрение элемента управления проигрывателя Windows Media в решение Visual Basic .NET
description: Внедрение элемента управления проигрывателя Windows Media в решение Visual Basic .NET
ms.assetid: e6428b42-5d8b-48ef-9f7a-c90a4625b745
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Проигрыватель Windows Media, Visual Basic .NET
- Объектная модель проигрывателя Windows Media, Visual Basic .NET
- Объектная модель, Visual Basic .NET
- Проигрыватель Windows Media Mobile, Visual Basic .NET
- Элемент управления ActiveX проигрывателя Windows Media, Visual Basic .NET
- Элемент управления ActiveX проигрывателя Windows Media Mobile, Visual Basic .NET
- Элемент управления ActiveX, Visual Basic .NET
- внедрение, Visual Basic программ .NET
- Visual Basic внедрение программы .NET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d578b456a5064f1846ead7f074f178753dbc7c97
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "104332880"
---
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a><span data-ttu-id="80844-119">Внедрение элемента управления проигрывателя Windows Media в решение Visual Basic .NET</span><span class="sxs-lookup"><span data-stu-id="80844-119">Embedding the Windows Media Player Control in a Visual Basic .NET Solution</span></span>

<span data-ttu-id="80844-120">Чтобы использовать функциональные возможности серии проигрывателя Windows Media 9 или более поздней версии в Visual Basic приложении .NET, сначала добавьте компонент в форму, как описано в статье [использование элемента управления проигрывателя Windows Media с Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span><span class="sxs-lookup"><span data-stu-id="80844-120">To use the functionality of Windows Media Player 9 Series or later in a Visual Basic .NET application, first add the component to a form as described in [Using the Windows Media Player Control with Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span></span>

<span data-ttu-id="80844-121">В этом разделе описывается создание приложения, которое воспроизводит видео и содержит настраиваемые кнопки воспроизведения и отключения.</span><span class="sxs-lookup"><span data-stu-id="80844-121">This section describes how to create an application that plays video and has custom play and stop buttons.</span></span>

## <a name="add-the-video-window"></a><span data-ttu-id="80844-122">Добавление окна видео</span><span class="sxs-lookup"><span data-stu-id="80844-122">Add the Video Window</span></span>

<span data-ttu-id="80844-123">Добавление элемента управления проигрывателя Windows Media в форму.</span><span class="sxs-lookup"><span data-stu-id="80844-123">Add the Windows Media Player control to a form.</span></span> <span data-ttu-id="80844-124">Измените размер элемента управления, а затем поместите его там, где должно отображаться окно видео.</span><span class="sxs-lookup"><span data-stu-id="80844-124">Resize the control, and then place it where you want the video window to appear.</span></span>

<span data-ttu-id="80844-125">Выберите элемент управления проигрывателя Windows Media, а затем измените значение свойства **uiMode** на "нет".</span><span class="sxs-lookup"><span data-stu-id="80844-125">Select the Windows Media Player control, then change the **uiMode** property to "none".</span></span> <span data-ttu-id="80844-126">Этот параметр скрывает элементы управления пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="80844-126">This setting hides the UI controls.</span></span> <span data-ttu-id="80844-127">Когда пользователь воспроизводит видео, он появляется в окне.</span><span class="sxs-lookup"><span data-stu-id="80844-127">When the user plays a video, it will appear in the window.</span></span> <span data-ttu-id="80844-128">Для содержимого, поддерживающего только звук, отображается визуализация.</span><span class="sxs-lookup"><span data-stu-id="80844-128">For audio-only content, a visualization will appear.</span></span>

## <a name="add-two-buttons-and-adjust-the-form"></a><span data-ttu-id="80844-129">Добавление двух кнопок и настройка формы</span><span class="sxs-lookup"><span data-stu-id="80844-129">Add Two Buttons and Adjust the Form</span></span>

<span data-ttu-id="80844-130">Теперь добавьте две кнопки в форму.</span><span class="sxs-lookup"><span data-stu-id="80844-130">Now add two buttons to the form.</span></span> <span data-ttu-id="80844-131">Нажмите первую кнопку и измените свойство **Text** на Play.</span><span class="sxs-lookup"><span data-stu-id="80844-131">Select the first button and change the **Text** property to "Play".</span></span> <span data-ttu-id="80844-132">Нажмите вторую кнопку и измените ее свойство **Text** на «останавливаться».</span><span class="sxs-lookup"><span data-stu-id="80844-132">Select the second button and change its **Text** property to "Stop".</span></span>

## <a name="add-the-play-code"></a><span data-ttu-id="80844-133">Добавление кода воспроизведения</span><span class="sxs-lookup"><span data-stu-id="80844-133">Add the Play Code</span></span>

<span data-ttu-id="80844-134">Дважды щелкните кнопку **Воспроизведение** , чтобы открыть окно кода.</span><span class="sxs-lookup"><span data-stu-id="80844-134">Double-click the **Play** button to reveal the Code window.</span></span> <span data-ttu-id="80844-135">Отобразится следующий код:</span><span class="sxs-lookup"><span data-stu-id="80844-135">The following code is displayed:</span></span>


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



<span data-ttu-id="80844-136">Добавьте следующую строку в подпрограммы:</span><span class="sxs-lookup"><span data-stu-id="80844-136">Add this line to the subroutine:</span></span>


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



<span data-ttu-id="80844-137">В предыдущем примере кода "axWindowsMediaPlayer1" — это имя элемента управления проигрывателя Windows Media по умолчанию, а "c: \\ mediafile. wmv" — это имя носителя, который нужно воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="80844-137">In the preceding code example, "axWindowsMediaPlayer1" is the default name of the Windows Media Player control and "c:\\mediafile.wmv" is a placeholder for the name of the media you want to play.</span></span>

<span data-ttu-id="80844-138">Если вы добавили цифровое мультимедийное содержимое из пакета SDK проигрывателя Windows Media в библиотеку в проигрывателе Windows Media Player, можно использовать следующий код:</span><span class="sxs-lookup"><span data-stu-id="80844-138">If you have added the digital media content from the Windows Media Player SDK to the library in Windows Media Player, you can use this code instead:</span></span>


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



<span data-ttu-id="80844-139">Поскольку свойство **автозапуска** по умолчанию имеет значение true, проигрыватель Windows Media начнет играть при установке свойства **куррентплайлист** или **URL** .</span><span class="sxs-lookup"><span data-stu-id="80844-139">Because the **autoStart** property is true by default, Windows Media Player will start playing when you set the **currentPlaylist** or **URL** property.</span></span>

## <a name="add-the-stop-code"></a><span data-ttu-id="80844-140">Добавление кода завершения</span><span class="sxs-lookup"><span data-stu-id="80844-140">Add the Stop Code</span></span>

<span data-ttu-id="80844-141">Дважды щелкните кнопку " **Закрыть** ", чтобы открыть окно кода.</span><span class="sxs-lookup"><span data-stu-id="80844-141">Double-click the **Stop** button to reveal the Code window.</span></span> <span data-ttu-id="80844-142">Отобразится следующий код:</span><span class="sxs-lookup"><span data-stu-id="80844-142">The following code is displayed:</span></span>


```VB
Private Sub Button2_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub

```



<span data-ttu-id="80844-143">Добавьте следующую строку в подпрограммы:</span><span class="sxs-lookup"><span data-stu-id="80844-143">Add this line to the subroutine:</span></span>


```VB
AxWindowsMediaPlayer1.Ctlcontrols.stop()

```



> [!Note]  
> <span data-ttu-id="80844-144">Оболочка управляемого кода для элемента управления проигрывателя Windows Media предоставляет объект **Controls** как **ктлконтролс** , чтобы избежать конфликта со свойством **Controls** , унаследованным от **System. Windows. Forms. Control**.</span><span class="sxs-lookup"><span data-stu-id="80844-144">The managed-code wrapper for the Windows Media Player control exposes the **Controls** object as **Ctlcontrols** to avoid collision with the **Controls** property inherited from **System.Windows.Forms.Control**.</span></span>

 

## <a name="add-error-handling"></a><span data-ttu-id="80844-145">Добавление обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="80844-145">Add Error-handling</span></span>

<span data-ttu-id="80844-146">Элемент управления проигрывателя Windows Media не вызывает исключение, если возникает ошибка, например недопустимый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="80844-146">The Windows Media Player control does not raise an exception when it encounters an error such as an invalid URL.</span></span> <span data-ttu-id="80844-147">Вместо этого элемент управления сигнализирует о событии.</span><span class="sxs-lookup"><span data-stu-id="80844-147">Instead, the control signals an event.</span></span> <span data-ttu-id="80844-148">Приложение должно поддерживать события ошибок, отправленные проигрывателем.</span><span class="sxs-lookup"><span data-stu-id="80844-148">Your application should handle error events sent by the Player.</span></span>

<span data-ttu-id="80844-149">Чтобы создать обработчик событий, откройте окно кода для класса формы.</span><span class="sxs-lookup"><span data-stu-id="80844-149">To create an event handler, open the code window for your form class.</span></span> <span data-ttu-id="80844-150">В раскрывающемся списке в верхней части окна выберите элемент управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="80844-150">From the drop-down list at the top of the window, select the Windows Media Player control.</span></span> <span data-ttu-id="80844-151">В раскрывающемся списке справа появится список событий.</span><span class="sxs-lookup"><span data-stu-id="80844-151">A list of events appears in the drop-down list to the right.</span></span> <span data-ttu-id="80844-152">В этом списке выберите [**медиаеррор**](axwmplib-axwindowsmediaplayer-mediaerror.md).</span><span class="sxs-lookup"><span data-stu-id="80844-152">From that list, select [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md).</span></span> <span data-ttu-id="80844-153">Отобразится следующий код:</span><span class="sxs-lookup"><span data-stu-id="80844-153">The following code is displayed:</span></span>


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



<span data-ttu-id="80844-154">Следующий код можно вставить в подпрограмму, чтобы обеспечить минимальную возможность обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="80844-154">The following code could be inserted in the subroutine to provide minimal error-handling capability.</span></span> <span data-ttu-id="80844-155">Обратите внимание, что сведения об ошибке можно получить из аргумента **\_ \_ медиаерроревент вмпокксевентс** .</span><span class="sxs-lookup"><span data-stu-id="80844-155">Note that information about the error can be retrieved from the **\_WMPOCXEvents\_MediaErrorEvent** argument.</span></span>


```VB
Try
    ' If the file is corrupt or missing, show the 
    ' hexadecimal error code and URL.
    Dim errSource As WMPLib.IWMPMedia2 = e.pMediaObject
    Dim errorItem As WMPLib.IWMPErrorItem = errSource.Error
    MessageBox.Show("Media error " + errorItem.errorCode.ToString("X") _
                    + " in " + errSource.sourceURL)
Catch ex As InvalidCastException
    ' In case pMediaObject is not an IWMPMedia item.
    MessageBox.Show("Player error.")
End Try

```



## <a name="related-topics"></a><span data-ttu-id="80844-156">См. также</span><span class="sxs-lookup"><span data-stu-id="80844-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80844-157">**Внедрение элемента управления проигрывателя Windows Media в платформа .NET Framework решение**</span><span class="sxs-lookup"><span data-stu-id="80844-157">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




