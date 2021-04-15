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
# <a name="iwmpnetworkbufferingprogress-property"></a>Свойство Ивмпнетворк:: Буфферингпрогресс

Свойство **буфферингпрогресс** Возвращает процент завершения буферизации.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 bufferingProgress {get; set;}
```


```VB

Public ReadOnly Property bufferingProgress As System.Int32
```





## <a name="property-value"></a>Значение свойства

Объект **System. Int32** , выполняющий буферизацию, выраженный в процентах.

## <a name="remarks"></a>Комментарии

Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство сбрасывается до нуля. Если воспроизведение приостановлено, оно не сбрасывается.

Буферизация применяется только к потоковой передаче содержимого. Это свойство получает действительные сведения только во время выполнения, когда URL-адрес для воспроизведения задается с помощью свойства **аксвиндовсмедиаплайер. URL** .

Используйте **аксвиндовсмедиаплайер. \_ Вмпокксевентс \_ буфферинжевент** , чтобы определить, когда буферизация начинается или останавливается.

## <a name="examples"></a>Примеры

В следующем примере **буфферингпрогресс** используется для вывода процента буферизации, завершенного в метке в ответ на событие буферизации. В примере для обновления экрана используется таймер с интервалом в 1 секунду. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


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





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Аксвиндовсмедиаплайер. URL (VB и C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Событие Аксвиндовсмедиаплайер. Buffering (VB и C#)**](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[**Интерфейс Ивмпнетворк (VB и C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





