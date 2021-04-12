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
# <a name="creating-the-windows-media-player-control-programmatically"></a><span data-ttu-id="d5f96-111">Создание элемента управления проигрывателя Windows Media программным способом</span><span class="sxs-lookup"><span data-stu-id="d5f96-111">Creating the Windows Media Player Control Programmatically</span></span>

<span data-ttu-id="d5f96-112">При добавлении элемента управления проигрывателя Windows Media в форму из панели элементов создается объект класса **аксвмплиб. аксвиндовсмедиаплайер** .</span><span class="sxs-lookup"><span data-stu-id="d5f96-112">When you add the Windows Media Player control to a form from the Toolbox, an object of the class **AxWMPLib.AxWindowsMediaPlayer** is created.</span></span> <span data-ttu-id="d5f96-113">Этот класс-оболочка предоставляет проигрывателю все функциональные возможности элемента управления ActiveX, включая доступ к свойствам пользовательского интерфейса, таким как **Расположение** и **Размер**.</span><span class="sxs-lookup"><span data-stu-id="d5f96-113">This wrapper class gives the Player all the functionality of an ActiveX control, including access to UI properties such as **Location** and **Size**.</span></span>

<span data-ttu-id="d5f96-114">Если не требуются свойства, предоставляемые **аксвиндовсмедиаплайер**, или если приложение не имеет графического пользовательского интерфейса, можно создать управляющий элемент программным способом.</span><span class="sxs-lookup"><span data-stu-id="d5f96-114">If you do not require the properties exposed by **AxWindowsMediaPlayer**, or if your application does not have a graphical user interface, you can create a Player control programmatically.</span></span> <span data-ttu-id="d5f96-115">В этом случае создается объект класса **вмплиб. виндовсмедиаплайер** .</span><span class="sxs-lookup"><span data-stu-id="d5f96-115">In this case, you create an object of the **WMPLib.WindowsMediaPlayer** class.</span></span>

> [!Note]  
> <span data-ttu-id="d5f96-116">Поскольку объект **виндовсмедиаплайер** не упакован как элемент управления ActiveX, он не имеет свойств, унаследованных от **System. Windows. Forms. Control**.</span><span class="sxs-lookup"><span data-stu-id="d5f96-116">Because the **WindowsMediaPlayer** object is not wrapped as an ActiveX control, it does not have any properties inherited from **System.Windows.Forms.Control**.</span></span> <span data-ttu-id="d5f96-117">В результате свойство **Controls** не переименовывается в **ктлконтролс**, так как оно находится в **аксвиндовсмедиаплайер**.</span><span class="sxs-lookup"><span data-stu-id="d5f96-117">As a result, the **Controls** property is not renamed to **CtlControls**, as it is in **AxWindowsMediaPlayer**.</span></span>

 

<span data-ttu-id="d5f96-118">Чтобы создать элемент управления проигрывателя Windows Media программно, необходимо сначала добавить ссылку на wmp.dll, которая находится в \\ \\ папке Windows System32.</span><span class="sxs-lookup"><span data-stu-id="d5f96-118">To create the Windows Media Player control programmatically, you must first add a reference to wmp.dll, which is found in the \\Windows\\system32 folder.</span></span> <span data-ttu-id="d5f96-119">Добавление этой ссылки приведет к созданию WMPLib.dll в папке проекта, а ссылка на Вмплиб появится в обозреватель решений.</span><span class="sxs-lookup"><span data-stu-id="d5f96-119">Adding this reference creates WMPLib.dll in your project folder, and a reference to WMPLib appears in Solution Explorer.</span></span>

<span data-ttu-id="d5f96-120">В следующем примере кода, который является частью класса Form1, показано, как создать объект **Player** и воспроизвести файл.</span><span class="sxs-lookup"><span data-stu-id="d5f96-120">The following example code, part of a Form1 class, shows how to create a **Player** object and play a file.</span></span> <span data-ttu-id="d5f96-121">Когда воспроизведение завершается или файл не может быть воспроизведен, форма закрывается.</span><span class="sxs-lookup"><span data-stu-id="d5f96-121">When playback ends, or if the file cannot be played, the form is closed.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d5f96-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d5f96-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5f96-123">**Внедрение элемента управления проигрывателя Windows Media в платформа .NET Framework решение**</span><span class="sxs-lookup"><span data-stu-id="d5f96-123">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




