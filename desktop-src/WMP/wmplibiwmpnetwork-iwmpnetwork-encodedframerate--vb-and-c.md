---
title: Ивмпнетворк Енкодедфрамерате, свойство
description: Свойство Енкодедфрамерате возвращает частоту кадров видео, указанную автором содержимого.
ms.assetid: 4faf5675-5bf3-485d-802f-a1f900ddae63
keywords:
- проигрыватель Windows Media свойства енкодедфрамерате
- проигрыватель Windows Media свойства енкодедфрамерате, интерфейс ивмпнетворк
- проигрыватель Windows Media интерфейса ивмпнетворк, свойство енкодедфрамерате
topic_type:
- apiref
api_name:
- IWMPNetwork.encodedFrameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f8a08572f65e1e44027ed25d84acfe7d917f92bf4bb63d5d9b8cca1e1201d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000014"
---
# <a name="iwmpnetworkencodedframerate-property"></a>Свойство Ивмпнетворк:: Енкодедфрамерате

Свойство **енкодедфрамерате** возвращает частоту кадров видео, указанную автором содержимого.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 encodedFrameRate {get; set;}
```


```VB

Public ReadOnly Property encodedFrameRate As System.Int32
```





## <a name="property-value"></a>Значение свойства

Значение **System. Int32** , которое является закодированной частотой кадров в кадрах в секунду (кадров/с).

> [!Note]  
> Несмотря на то, что свойство **енкодедфрамерате** измеряет частоту закодированных кадров в кадрах в секунду, свойство **Частота** кадров измеряет текущую частоту кадров в кадрах за сотни секунд.

 

## <a name="examples"></a>Примеры

В следующем примере кода используется **енкодедфрамерате** для вывода частоты кадров, указанной при кодировании файла. Сведения отображаются в метке в ответ на событие **плайстатечанже** . Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the encodedFrameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.encodedFrameRate != 0)
            {
                encodedFrameRateLabel.Text = "Current Encoded Frame Rate: " + player.network.encodedFrameRate + " K bits/second";
            }
            break;

        default:
            break;
    }
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the encodedFrameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.encodedFrameRate <> 0) Then

                encodedFrameRateLabel.Text = &quot;Current Encoded Frame Rate: &quot; + player.network.encodedFrameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмпнетворк (VB и C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**Ивмпнетворк. частота (VB и C#)**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)
</dt> </dl>

 

 





