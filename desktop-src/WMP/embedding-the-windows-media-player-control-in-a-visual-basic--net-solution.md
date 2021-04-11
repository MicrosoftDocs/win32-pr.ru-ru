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
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a>Внедрение элемента управления проигрывателя Windows Media в решение Visual Basic .NET

Чтобы использовать функциональные возможности серии проигрывателя Windows Media 9 или более поздней версии в Visual Basic приложении .NET, сначала добавьте компонент в форму, как описано в статье [использование элемента управления проигрывателя Windows Media с Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

В этом разделе описывается создание приложения, которое воспроизводит видео и содержит настраиваемые кнопки воспроизведения и отключения.

## <a name="add-the-video-window"></a>Добавление окна видео

Добавление элемента управления проигрывателя Windows Media в форму. Измените размер элемента управления, а затем поместите его там, где должно отображаться окно видео.

Выберите элемент управления проигрывателя Windows Media, а затем измените значение свойства **uiMode** на "нет". Этот параметр скрывает элементы управления пользовательского интерфейса. Когда пользователь воспроизводит видео, он появляется в окне. Для содержимого, поддерживающего только звук, отображается визуализация.

## <a name="add-two-buttons-and-adjust-the-form"></a>Добавление двух кнопок и настройка формы

Теперь добавьте две кнопки в форму. Нажмите первую кнопку и измените свойство **Text** на Play. Нажмите вторую кнопку и измените ее свойство **Text** на «останавливаться».

## <a name="add-the-play-code"></a>Добавление кода воспроизведения

Дважды щелкните кнопку **Воспроизведение** , чтобы открыть окно кода. Отобразится следующий код:


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



Добавьте следующую строку в подпрограммы:


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



В предыдущем примере кода "axWindowsMediaPlayer1" — это имя элемента управления проигрывателя Windows Media по умолчанию, а "c: \\ mediafile. wmv" — это имя носителя, который нужно воспроизвести.

Если вы добавили цифровое мультимедийное содержимое из пакета SDK проигрывателя Windows Media в библиотеку в проигрывателе Windows Media Player, можно использовать следующий код:


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



Поскольку свойство **автозапуска** по умолчанию имеет значение true, проигрыватель Windows Media начнет играть при установке свойства **куррентплайлист** или **URL** .

## <a name="add-the-stop-code"></a>Добавление кода завершения

Дважды щелкните кнопку " **Закрыть** ", чтобы открыть окно кода. Отобразится следующий код:


```VB
Private Sub Button2_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub

```



Добавьте следующую строку в подпрограммы:


```VB
AxWindowsMediaPlayer1.Ctlcontrols.stop()

```



> [!Note]  
> Оболочка управляемого кода для элемента управления проигрывателя Windows Media предоставляет объект **Controls** как **ктлконтролс** , чтобы избежать конфликта со свойством **Controls** , унаследованным от **System. Windows. Forms. Control**.

 

## <a name="add-error-handling"></a>Добавление обработки ошибок

Элемент управления проигрывателя Windows Media не вызывает исключение, если возникает ошибка, например недопустимый URL-адрес. Вместо этого элемент управления сигнализирует о событии. Приложение должно поддерживать события ошибок, отправленные проигрывателем.

Чтобы создать обработчик событий, откройте окно кода для класса формы. В раскрывающемся списке в верхней части окна выберите элемент управления проигрывателя Windows Media. В раскрывающемся списке справа появится список событий. В этом списке выберите [**медиаеррор**](axwmplib-axwindowsmediaplayer-mediaerror.md). Отобразится следующий код:


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



Следующий код можно вставить в подпрограмму, чтобы обеспечить минимальную возможность обработки ошибок. Обратите внимание, что сведения об ошибке можно получить из аргумента **\_ \_ медиаерроревент вмпокксевентс** .


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Внедрение элемента управления проигрывателя Windows Media в платформа .NET Framework решение**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




