---
title: программное создание элемента управления проигрыватель Windows Media
description: программное создание элемента управления проигрыватель Windows Media
ms.assetid: 9a4856ce-6a44-47fb-b863-59ce4deb0597
keywords:
- проигрыватель Windows Media, создание ActiveX управления программным способом
- проигрыватель Windows Media объектной модели, создание ActiveX управления программным способом
- объектная модель, создание ActiveX управления программным способом
- проигрыватель Windows Media мобильный, создание ActiveX управления программным способом
- проигрыватель Windows Media ActiveX элемент управления, создание программными средствами
- проигрыватель Windows Media управление мобильными ActiveXми, создание программными средствами
- ActiveX управления, создание программными средствами
- программное создание ActiveX управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57b3f4ba9d8c297aee9feb14fc05a35306e1a85d8a718aef6721b92475e19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340967"
---
# <a name="creating-the-windows-media-player-control-programmatically"></a>программное создание элемента управления проигрыватель Windows Media

при добавлении проигрыватель Windows Media элемента управления в форму из панели элементов создается объект класса **аксвмплиб. аксвиндовсмедиаплайер** . этот класс-оболочка предоставляет проигрывателю все функциональные возможности элемента управления ActiveX, включая доступ к свойствам пользовательского интерфейса, таким как **расположение** и **размер**.

Если не требуются свойства, предоставляемые **аксвиндовсмедиаплайер**, или если приложение не имеет графического пользовательского интерфейса, можно создать управляющий элемент программным способом. В этом случае создается объект класса **вмплиб. виндовсмедиаплайер** .

> [!Note]  
> поскольку объект **виндовсмедиаплайер** не упакован как элемент управления ActiveX, он не имеет свойств, наследуемых от **System. Windows. Forms. Control**. В результате свойство **Controls** не переименовывается в **ктлконтролс**, так как оно находится в **аксвиндовсмедиаплайер**.

 

чтобы создать элемент управления проигрыватель Windows Media программным способом, необходимо сначала добавить ссылку на wmp.dll, который находится в \\ \\ папке Windows system32. Добавление этой ссылки приведет к созданию WMPLib.dll в папке проекта, а ссылка на Вмплиб появится в обозреватель решений.

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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**внедрение элемента управления проигрыватель Windows Media в платформа .NET Framework решение**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




