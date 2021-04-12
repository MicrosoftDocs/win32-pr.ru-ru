---
title: Создание элемента управления проигрывателя Windows Media программным способом
description: Создание элемента управления проигрывателя Windows Media программным способом
ms.assetid: 9a4856ce-6a44-47fb-b863-59ce4deb0597
keywords:
- Проигрыватель Windows Media, создание элемента управления ActiveX программным способом
- Объектная модель проигрывателя Windows Media, создание элемента управления ActiveX программным способом
- Объектная модель, создание элемента управления ActiveX программным способом
- Проигрыватель Windows Media Mobile, создание элемента управления ActiveX программным способом
- Элемент управления ActiveX проигрывателя Windows Media, создание программными средствами
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, создание программными средствами
- Элемент управления ActiveX, создание программными средствами
- Создание элемента управления ActiveX программным способом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222c207b33dcc13a5392f79dad267d6ee82a677c
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "104332872"
---
# <a name="creating-the-windows-media-player-control-programmatically"></a>Создание элемента управления проигрывателя Windows Media программным способом

При добавлении элемента управления проигрывателя Windows Media в форму из панели элементов создается объект класса **аксвмплиб. аксвиндовсмедиаплайер** . Этот класс-оболочка предоставляет проигрывателю все функциональные возможности элемента управления ActiveX, включая доступ к свойствам пользовательского интерфейса, таким как **Расположение** и **Размер**.

Если не требуются свойства, предоставляемые **аксвиндовсмедиаплайер**, или если приложение не имеет графического пользовательского интерфейса, можно создать управляющий элемент программным способом. В этом случае создается объект класса **вмплиб. виндовсмедиаплайер** .

> [!Note]  
> Поскольку объект **виндовсмедиаплайер** не упакован как элемент управления ActiveX, он не имеет свойств, унаследованных от **System. Windows. Forms. Control**. В результате свойство **Controls** не переименовывается в **ктлконтролс**, так как оно находится в **аксвиндовсмедиаплайер**.

 

Чтобы создать элемент управления проигрывателя Windows Media программно, необходимо сначала добавить ссылку на wmp.dll, которая находится в \\ \\ папке Windows System32. Добавление этой ссылки приведет к созданию WMPLib.dll в папке проекта, а ссылка на Вмплиб появится в обозреватель решений.

В следующем примере кода, который является частью класса Form1, показано, как создать объект **Player** и воспроизвести файл. Когда воспроизведение завершается или файл не может быть воспроизведен, форма закрывается.


```VB
Dim WithEvents Player As WMPLib.WindowsMediaPlayer

Private Sub PlayFile(ByVal url As String)
    Player = New WMPLib.WindowsMediaPlayer
    Player.URL = url
    Player.controls.play()
End Sub

Private Sub Form1_Load(ByVal sender As Object, ByVal e As System.EventArgs) _
                       Handles MyBase.Load
    ' TODO  Insert a valid path in the line below.
    PlayFile("c:\media\myaudio.wma")
End Sub

Private Sub Player_MediaError(ByVal pMediaObject As Object) _
                              Handles Player.MediaError
    MessageBox.Show("Cannot play media file.")
    Me.Close()
End Sub

Private Sub Player_PlayStateChange(ByVal NewState As Integer) _
                                   Handles Player.PlayStateChange
    If NewState = WMPLib.WMPPlayState.wmppsStopped Then
        Me.Close()
    End If
End Sub

```




```CSharp
WMPLib.WindowsMediaPlayer Player;

private void PlayFile(String url)
{
    Player = new WMPLib.WindowsMediaPlayer();
    Player.PlayStateChange += 
        new WMPLib._WMPOCXEvents_PlayStateChangeEventHandler(Player_PlayStateChange);
    Player.MediaError += 
        new WMPLib._WMPOCXEvents_MediaErrorEventHandler(Player_MediaError);
    Player.URL = url;
    Player.controls.play();
}

private void Form1_Load(object sender, System.EventArgs e)
{
    // TODO  Insert a valid path in the line below.
    PlayFile(@"c:\myaudio.wma");
}

private void Player_PlayStateChange(int NewState)
{
    if ((WMPLib.WMPPlayState)NewState == WMPLib.WMPPlayState.wmppsStopped)
    {
        this.Close();
    }
}

private void Player_MediaError(object pMediaObject)
{
    MessageBox.Show("Cannot play media file.");
    this.Close();
}


```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Внедрение элемента управления проигрывателя Windows Media в платформа .NET Framework решение**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




