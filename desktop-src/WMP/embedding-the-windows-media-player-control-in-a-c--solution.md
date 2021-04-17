---
title: Внедрение элемента управления проигрывателя Windows Media в решение C
description: Внедрение элемента управления проигрывателя Windows Media в решение C \
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Проигрыватель Windows Media, C
- Объектная модель проигрывателя Windows Media, C
- Объектная модель, C
- Проигрыватель Windows Media Mobile, C
- Элемент управления ActiveX проигрывателя Windows Media, C
- Элемент управления ActiveX проигрывателя Windows Media Mobile, C
- Элемент управления ActiveX, C
- внедрение, программы на языке C
- Внедрение программ на C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c950bed9812cea0aa6ce28995fd6998bb8417ac
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "105691396"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a><span data-ttu-id="49114-119">Внедрение элемента управления проигрывателя Windows Media в решение C#</span><span class="sxs-lookup"><span data-stu-id="49114-119">Embedding the Windows Media Player Control in a C# Solution</span></span>

<span data-ttu-id="49114-120">Чтобы использовать функциональные возможности проигрывателя Windows Media в приложении C#, сначала добавьте компонент в форму, как описано в статье [использование элемента управления проигрывателя Windows Media с Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span><span class="sxs-lookup"><span data-stu-id="49114-120">To use the functionality of Windows Media Player in a C# application, first add the component to a form as described in [Using the Windows Media Player Control with Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span></span>

<span data-ttu-id="49114-121">В следующих разделах описывается создание приложения, которое воспроизводит видео, и использование настраиваемых кнопок воспроизведения и отключения.</span><span class="sxs-lookup"><span data-stu-id="49114-121">The following sections describe how to create an application that plays video and uses custom play and stop buttons.</span></span>

## <a name="add-the-video-window"></a><span data-ttu-id="49114-122">Добавление окна видео</span><span class="sxs-lookup"><span data-stu-id="49114-122">Add the Video Window</span></span>

<span data-ttu-id="49114-123">Добавление элемента управления ActiveX проигрывателя Windows Media в форму.</span><span class="sxs-lookup"><span data-stu-id="49114-123">Add the Windows Media Player ActiveX control to a form.</span></span> <span data-ttu-id="49114-124">Измените размер элемента управления, а затем поместите его там, где должно отображаться окно видео.</span><span class="sxs-lookup"><span data-stu-id="49114-124">Resize the control, and then place it where you want the video window to appear.</span></span>

<span data-ttu-id="49114-125">Выберите элемент управления проигрывателя Windows Media, а затем измените значение свойства **uiMode** на "нет".</span><span class="sxs-lookup"><span data-stu-id="49114-125">Select the Windows Media Player control, then change the **uiMode** property to "none".</span></span> <span data-ttu-id="49114-126">Этот параметр скрывает элементы управления пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="49114-126">This setting hides the UI controls.</span></span> <span data-ttu-id="49114-127">Когда пользователь воспроизводит видео, он появляется в окне.</span><span class="sxs-lookup"><span data-stu-id="49114-127">When the user plays a video, it will appear in the window.</span></span> <span data-ttu-id="49114-128">Для содержимого, поддерживающего только звук, отображается визуализация.</span><span class="sxs-lookup"><span data-stu-id="49114-128">For audio-only content, a visualization will appear.</span></span>

## <a name="add-two-buttons-and-adjust-the-form"></a><span data-ttu-id="49114-129">Добавление двух кнопок и настройка формы</span><span class="sxs-lookup"><span data-stu-id="49114-129">Add Two Buttons and Adjust the Form</span></span>

<span data-ttu-id="49114-130">Теперь добавьте две кнопки в форму.</span><span class="sxs-lookup"><span data-stu-id="49114-130">Now, add two buttons to the form.</span></span> <span data-ttu-id="49114-131">Нажмите первую кнопку и измените свойство **Text** на Play.</span><span class="sxs-lookup"><span data-stu-id="49114-131">Select the first button and change the **Text** property to "Play".</span></span> <span data-ttu-id="49114-132">Нажмите вторую кнопку и измените ее свойство **Text** на «останавливаться».</span><span class="sxs-lookup"><span data-stu-id="49114-132">Select the second button and change its **Text** property to "Stop".</span></span>

## <a name="add-the-play-code"></a><span data-ttu-id="49114-133">Добавление кода воспроизведения</span><span class="sxs-lookup"><span data-stu-id="49114-133">Add the Play Code</span></span>

<span data-ttu-id="49114-134">Дважды щелкните кнопку **Воспроизведение** , чтобы открыть окно кода.</span><span class="sxs-lookup"><span data-stu-id="49114-134">Double-click the **Play** button to reveal the Code window.</span></span> <span data-ttu-id="49114-135">В C# отобразится следующий код:</span><span class="sxs-lookup"><span data-stu-id="49114-135">In C#, the following code will be displayed:</span></span>


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



<span data-ttu-id="49114-136">Добавьте следующую строку между двумя фигурными скобками:</span><span class="sxs-lookup"><span data-stu-id="49114-136">Add this line between the two curly braces:</span></span>


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



<span data-ttu-id="49114-137">В предыдущем примере кода "axWindowsMediaPlayer1" — это имя элемента управления проигрывателя Windows Media по умолчанию, а "c: \\ mediafile. wmv" — это имя элемента мультимедиа, который необходимо воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="49114-137">In the preceding code example, "axWindowsMediaPlayer1" is the default name of the Windows Media Player control, and "c:\\mediafile.wmv" is a placeholder for the name of the media item you want to play.</span></span> <span data-ttu-id="49114-138">Можно использовать любой допустимый путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="49114-138">Any valid file path can be used.</span></span> <span data-ttu-id="49114-139">Символ @ указывает компилятору не интерпретировать обратные косые черты как escape-символы.</span><span class="sxs-lookup"><span data-stu-id="49114-139">The @ symbol instructs the compiler to not interpret backslashes as escape characters.</span></span>

<span data-ttu-id="49114-140">Если вы добавили цифровое мультимедийное содержимое из пакета SDK проигрывателя Windows Media в библиотеку в проигрывателе Windows Media Player, можно использовать следующий код:</span><span class="sxs-lookup"><span data-stu-id="49114-140">If you have added the digital media content from the Windows Media Player SDK to the library in Windows Media Player, you can use this code instead:</span></span>


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



<span data-ttu-id="49114-141">Поскольку свойство **автозапуска** по умолчанию имеет значение true, проигрыватель Windows Media начнет играть при установке свойства **куррентплайлист** или **URL** .</span><span class="sxs-lookup"><span data-stu-id="49114-141">Because the **autoStart** property is true by default, Windows Media Player will start playing when you set the **currentPlaylist** or **URL** property.</span></span>

## <a name="add-the-stop-code"></a><span data-ttu-id="49114-142">Добавление кода завершения</span><span class="sxs-lookup"><span data-stu-id="49114-142">Add the Stop Code</span></span>

<span data-ttu-id="49114-143">Дважды щелкните кнопку " **Закрыть** ", чтобы открыть окно кода.</span><span class="sxs-lookup"><span data-stu-id="49114-143">Double-click the **Stop** button to reveal the Code window.</span></span> <span data-ttu-id="49114-144">В C# отобразится следующий код:</span><span class="sxs-lookup"><span data-stu-id="49114-144">In C#, the following code will be displayed:</span></span>


```CSharp
private void button2_Click(object sender, System.EventArgs e)
{

}

```



<span data-ttu-id="49114-145">Добавьте следующую строку между двумя фигурными скобками:</span><span class="sxs-lookup"><span data-stu-id="49114-145">Add this line between the two curly braces:</span></span>


```CSharp
axWindowsMediaPlayer1.Ctlcontrols.stop();

```



> [!Note]  
> <span data-ttu-id="49114-146">Оболочка управляемого кода для элемента управления проигрывателя Windows Media предоставляет объект **Controls** как **ктлконтролс** , чтобы избежать конфликта со свойством **Controls** , унаследованным от **System. Windows. Forms. Control**.</span><span class="sxs-lookup"><span data-stu-id="49114-146">The managed-code wrapper for the Windows Media Player control exposes the **Controls** object as **Ctlcontrols** to avoid collision with the **Controls** property inherited from **System.Windows.Forms.Control**.</span></span>

 

## <a name="add-error-handling"></a><span data-ttu-id="49114-147">Добавление обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="49114-147">Add Error-handling</span></span>

<span data-ttu-id="49114-148">Элемент управления проигрывателя Windows Media не вызывает исключение, если возникает ошибка, например недопустимый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="49114-148">The Windows Media Player control does not raise an exception when it encounters an error such as an invalid URL.</span></span> <span data-ttu-id="49114-149">Вместо этого он сигнализирует о событии.</span><span class="sxs-lookup"><span data-stu-id="49114-149">Instead, it signals an event.</span></span> <span data-ttu-id="49114-150">Приложение должно поддерживать события ошибок, отправленные проигрывателем.</span><span class="sxs-lookup"><span data-stu-id="49114-150">Your application should handle error events sent by the Player.</span></span>

<span data-ttu-id="49114-151">Чтобы создать обработчик событий, сначала откройте окно свойств для элемента управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="49114-151">To create an event handler, first open the Properties window for the Windows Media Player control.</span></span> <span data-ttu-id="49114-152">В списке событий дважды щелкните **медиаеррор**.</span><span class="sxs-lookup"><span data-stu-id="49114-152">In the list of events, double-click **MediaError**.</span></span> <span data-ttu-id="49114-153">Отобразится следующий код:</span><span class="sxs-lookup"><span data-stu-id="49114-153">The following code is displayed:</span></span>


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



<span data-ttu-id="49114-154">Следующий код можно вставить в метод, чтобы обеспечить минимальную возможность обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="49114-154">The following code could be inserted in the method to provide minimal error-handling capability.</span></span> <span data-ttu-id="49114-155">Обратите внимание, что сведения об ошибке можно получить из аргумента **\_ \_ медиаерроревент вмпокксевентс** .</span><span class="sxs-lookup"><span data-stu-id="49114-155">Note that information about the error can be retrieved from the **\_WMPOCXEvents\_MediaErrorEvent** argument.</span></span>


```CSharp
try
// If the Player encounters a corrupt or missing file, 
// show the hexadecimal error code and URL.
{
    IWMPMedia2 errSource = e.pMediaObject as IWMPMedia2;
    IWMPErrorItem errorItem = errSource.Error;
    MessageBox.Show("Error " + errorItem.errorCode.ToString("X") 
                    + " in " + errSource.sourceURL);
}
catch(InvalidCastException)
// In case pMediaObject is not an IWMPMedia item.
{
    MessageBox.Show("Error.");
} 

```



## <a name="related-topics"></a><span data-ttu-id="49114-156">См. также</span><span class="sxs-lookup"><span data-stu-id="49114-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49114-157">**Внедрение элемента управления проигрывателя Windows Media в платформа .NET Framework решение**</span><span class="sxs-lookup"><span data-stu-id="49114-157">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




