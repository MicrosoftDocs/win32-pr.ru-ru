---
title: Ивмпнетворк Буфферингпрогресс, свойство
description: Свойство Буфферингпрогресс Возвращает процент завершения буферизации.
ms.assetid: 8dc9f31e-7c34-4714-a633-d92c3da3052b
keywords:
- Проигрыватель Windows Media для свойства Буфферингпрогресс
- Буфферингпрогресс свойство проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство Буфферингпрогресс
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da8a27ba41e5c4e201a5bdf0197992c30bce80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695113"
---
# <a name="iwmpnetworkbufferingprogress-property"></a><span data-ttu-id="bff6a-106">Свойство Ивмпнетворк:: Буфферингпрогресс</span><span class="sxs-lookup"><span data-stu-id="bff6a-106">IWMPNetwork::bufferingProgress property</span></span>

<span data-ttu-id="bff6a-107">Свойство **буфферингпрогресс** Возвращает процент завершения буферизации.</span><span class="sxs-lookup"><span data-stu-id="bff6a-107">The **bufferingProgress** property gets the percentage of buffering completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="bff6a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bff6a-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingProgress {get; set;}
```


```VB

Public ReadOnly Property bufferingProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="bff6a-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bff6a-109">Property value</span></span>

<span data-ttu-id="bff6a-110">Объект **System. Int32** , выполняющий буферизацию, выраженный в процентах.</span><span class="sxs-lookup"><span data-stu-id="bff6a-110">A **System.Int32** that is the buffering progress expressed as a percentage.</span></span>

## <a name="remarks"></a><span data-ttu-id="bff6a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bff6a-111">Remarks</span></span>

<span data-ttu-id="bff6a-112">Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство сбрасывается до нуля.</span><span class="sxs-lookup"><span data-stu-id="bff6a-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="bff6a-113">Если воспроизведение приостановлено, оно не сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="bff6a-113">It is not reset if playback is paused.</span></span>

<span data-ttu-id="bff6a-114">Буферизация применяется только к потоковой передаче содержимого.</span><span class="sxs-lookup"><span data-stu-id="bff6a-114">Buffering applies only to streaming content.</span></span> <span data-ttu-id="bff6a-115">Это свойство получает действительные сведения только во время выполнения, когда URL-адрес для воспроизведения задается с помощью свойства **аксвиндовсмедиаплайер. URL** .</span><span class="sxs-lookup"><span data-stu-id="bff6a-115">This property gets valid information only during run time when the URL for playback is set using the **AxWindowsMediaPlayer.URL** property.</span></span>

<span data-ttu-id="bff6a-116">Используйте **аксвиндовсмедиаплайер. \_ Вмпокксевентс \_ буфферинжевент** , чтобы определить, когда буферизация начинается или останавливается.</span><span class="sxs-lookup"><span data-stu-id="bff6a-116">Use the **AxWindowsMediaPlayer.\_WMPOCXEvents\_BufferingEvent** to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="bff6a-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="bff6a-117">Examples</span></span>

<span data-ttu-id="bff6a-118">В следующем примере **буфферингпрогресс** используется для вывода процента буферизации, завершенного в метке в ответ на событие буферизации.</span><span class="sxs-lookup"><span data-stu-id="bff6a-118">The following example uses **bufferingProgress** to display the percentage of buffering completed in a label, in response to the Buffering Event.</span></span> <span data-ttu-id="bff6a-119">В примере для обновления экрана используется таймер с интервалом в 1 секунду.</span><span class="sxs-lookup"><span data-stu-id="bff6a-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="bff6a-120">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="bff6a-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the buffering progress in a timer event handler.
private void UpdateBufferingProgress(object sender, EventArgs e)
{
    bufferingProgressLabel.Text = ("Buffering progress: " + player.network.bufferingProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

&#39; Update the buffering progress in a timer event handler.
Public Sub UpdateBufferingProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    bufferingProgressLabel.Text = (&quot;Buffering progress: &quot; + player.network.bufferingProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="bff6a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="bff6a-121">Requirements</span></span>



| <span data-ttu-id="bff6a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="bff6a-122">Requirement</span></span> | <span data-ttu-id="bff6a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="bff6a-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bff6a-124">Версия</span><span class="sxs-lookup"><span data-stu-id="bff6a-124">Version</span></span><br/>   | <span data-ttu-id="bff6a-125">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="bff6a-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="bff6a-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bff6a-126">Namespace</span></span><br/> | <span data-ttu-id="bff6a-127">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="bff6a-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bff6a-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="bff6a-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bff6a-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bff6a-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bff6a-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bff6a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bff6a-131">**Аксвиндовсмедиаплайер. URL (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bff6a-131">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bff6a-132">**Событие Аксвиндовсмедиаплайер. Buffering (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bff6a-132">**AxWindowsMediaPlayer.Buffering Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[<span data-ttu-id="bff6a-133">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bff6a-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





