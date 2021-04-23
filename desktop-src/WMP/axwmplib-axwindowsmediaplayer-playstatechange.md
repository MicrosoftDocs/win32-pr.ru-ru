---
title: Событие Плайстатечанже объекта Аксвиндовсмедиаплайер
description: Событие Плайстатечанже возникает при изменении состояния воспроизведения элемента управления проигрывателя Windows Media.
ms.assetid: f8823c90-2084-4771-a2fe-7081d4e49e63
keywords:
- Событие Плайстатечанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- PlayStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af97803224df89287847ee2b9ef83d8e976d91b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694801"
---
# <a name="playstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="5c5bd-104">Событие Плайстатечанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="5c5bd-104">PlayStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="5c5bd-105">Событие Плайстатечанже возникает при изменении состояния воспроизведения элемента управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5c5bd-105">The PlayStateChange event occurs when the play state of the Windows Media Player control changes.</span></span>

``` syntax
[C#]
private void player_PlayStateChange(
  object sender,
  _WMPOCXEvents_PlayStateChangeEvent e
)

[Visual Basic]
 Private Sub player_PlayStateChange(   
 sender As Object,  
 e As _WMPOCXEvents_PlayStateChangeEvent 
 ) Handles player.PlayStateChange
 
```

## <a name="event-data"></a><span data-ttu-id="5c5bd-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="5c5bd-106">Event Data</span></span>

<span data-ttu-id="5c5bd-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ плайстатечанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="5c5bd-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlayStateChangeEventHandler**.</span></span> <span data-ttu-id="5c5bd-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ плайстатечанжеевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="5c5bd-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlayStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="5c5bd-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="5c5bd-109">Property</span></span>     | <span data-ttu-id="5c5bd-110">Описание</span><span class="sxs-lookup"><span data-stu-id="5c5bd-110">Description</span></span>                                     |
|--------------|-------------------------------------------------|
| <span data-ttu-id="5c5bd-111">**Новое_состояние**</span><span class="sxs-lookup"><span data-stu-id="5c5bd-111">**newState**</span></span> | <span data-ttu-id="5c5bd-112">System. Int32Specifies новое состояние.</span><span class="sxs-lookup"><span data-stu-id="5c5bd-112">System.Int32Specifies the new state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c5bd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c5bd-113">Remarks</span></span>

<span data-ttu-id="5c5bd-114">Состояния проигрывателя Windows Media не гарантированно выполняются в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="5c5bd-114">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="5c5bd-115">Кроме того, не все состояния должны происходить во время последовательности событий.</span><span class="sxs-lookup"><span data-stu-id="5c5bd-115">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="5c5bd-116">Не следует писать код, зависящий от порядка состояний.</span><span class="sxs-lookup"><span data-stu-id="5c5bd-116">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="5c5bd-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="5c5bd-117">Examples</span></span>

<span data-ttu-id="5c5bd-118">В следующем примере показан обработчик события Плайстатечанже, отображающий текущее состояние воспроизведения в метке.</span><span class="sxs-lookup"><span data-stu-id="5c5bd-118">The following example demonstrates an event handler for the PlayStateChange Event that displays the current play state in a label.</span></span> <span data-ttu-id="5c5bd-119">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="5c5bd-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test the current state of the player and display a message for each state.
    switch (e.newState)
    {
        case 0:    // Undefined
            currentStateLabel.Text = "Undefined";
            break;

        case 1:    // Stopped
            currentStateLabel.Text = "Stopped";
            break;

        case 2:    // Paused
            currentStateLabel.Text = "Paused";
            break;

        case 3:    // Playing
            currentStateLabel.Text = "Playing";
            break;

        case 4:    // ScanForward
            currentStateLabel.Text = "ScanForward";
            break;

        case 5:    // ScanReverse
            currentStateLabel.Text = "ScanReverse";
            break;

        case 6:    // Buffering
            currentStateLabel.Text = "Buffering";
            break;

        case 7:    // Waiting
            currentStateLabel.Text = "Waiting";
            break;

        case 8:    // MediaEnded
            currentStateLabel.Text = "MediaEnded";
            break;

        case 9:    // Transitioning
            currentStateLabel.Text = "Transitioning";
            break;

        case 10:   // Ready
            currentStateLabel.Text = "Ready";
            break;

        case 11:   // Reconnecting
            currentStateLabel.Text = "Reconnecting";
            break;

        case 12:   // Last
            currentStateLabel.Text = "Last";
            break;

        default:
            currentStateLabel.Text = ("Unknown State: " + e.newState.ToString());
            break;
    }
}
```




```VB
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    ' Test the current state of the player, display a message for each state.
    Select Case e.newState

        Case 0 ' Undefined
            currentStateLabel.Text = "Undefined"

        Case 1 ' Stopped
            currentStateLabel.Text = "Stopped"

        Case 2 ' Paused
            currentStateLabel.Text = "Paused"

        Case 3 ' Playing
            currentStateLabel.Text = "Playing"

        Case 4 ' ScanForward
            currentStateLabel.Text = "ScanForward"

        Case 5 ' ScanReverse
            currentStateLabel.Text = "ScanReverse"

        Case 6 ' Buffering
            currentStateLabel.Text = "Buffering"

        Case 7 ' Waiting
            currentStateLabel.Text = "Waiting"

        Case 8 ' MediaEnded
            currentStateLabel.Text = "MediaEnded"

        Case 9 ' Transitioning
            currentStateLabel.Text = "Transitioning"

        Case 10 ' Ready
            currentStateLabel.Text = "Ready"

        Case 11 ' Reconnecting
            currentStateLabel.Text = "Reconnecting"

        Case 12 ' Last
            currentStateLabel.Text = "Last"

        Case Else
            currentStateLabel.Text = ("Unknown State: " + e.newState.ToString())

    End Select

End Sub
```



## <a name="requirements"></a><span data-ttu-id="5c5bd-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5c5bd-120">Requirements</span></span>



| <span data-ttu-id="5c5bd-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5c5bd-121">Requirement</span></span> | <span data-ttu-id="5c5bd-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5c5bd-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c5bd-123">Версия</span><span class="sxs-lookup"><span data-stu-id="5c5bd-123">Version</span></span><br/>   | <span data-ttu-id="5c5bd-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5c5bd-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="5c5bd-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5c5bd-125">Namespace</span></span><br/> | <span data-ttu-id="5c5bd-126">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="5c5bd-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="5c5bd-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="5c5bd-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5c5bd-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5c5bd-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c5bd-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c5bd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c5bd-130">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="5c5bd-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5c5bd-131">**Аксвиндовсмедиаплайер. Плайстате (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="5c5bd-131">**AxWindowsMediaPlayer.playState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> </dl>

 

 





