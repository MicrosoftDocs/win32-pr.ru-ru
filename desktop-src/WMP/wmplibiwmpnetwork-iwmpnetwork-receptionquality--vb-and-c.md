---
title: Ивмпнетворк Рецептионкуалити, свойство
description: Свойство Рецептионкуалити Возвращает процент пакетов, которые не были потеряны за последние 30 секунд.
ms.assetid: 103e6b8f-e029-4f53-93ac-b516896a7594
keywords:
- проигрыватель Windows Media свойства рецептионкуалити
- проигрыватель Windows Media свойства рецептионкуалити, интерфейс ивмпнетворк
- проигрыватель Windows Media интерфейса ивмпнетворк, свойство рецептионкуалити
topic_type:
- apiref
api_name:
- IWMPNetwork.receptionQuality
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5ea62391df07ed0e5e2c27752f668fda95a19d17dc6322fb7375ef5d3ed440f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098724"
---
# <a name="iwmpnetworkreceptionquality-property"></a>Свойство Ивмпнетворк:: Рецептионкуалити

Свойство **рецептионкуалити** Возвращает процент пакетов, которые не были потеряны за последние 30 секунд.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 receptionQuality {get; set;}
```


```VB

Public ReadOnly Property receptionQuality As System.Int32
```





## <a name="property-value"></a>Значение свойства

Значение **System. Int32** , которое является качеством приема.

## <a name="remarks"></a>Remarks

Количество пакетов, полученных, потерянных и восстановленных во время потоковой передачи, отслеживается каждую секунду. Свойство **рецептионкуалити** Возвращает процент пакетов, которые не были потеряны за последние 30 секунд.

Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство сбрасывается до нуля. Значение не сбрасывается, если воспроизведение приостановлено.

Это свойство получает действительные сведения только во время выполнения, когда URL-адрес для воспроизведения задается с помощью свойства **аксвиндовсмедиаплайер. URL** .

## <a name="examples"></a>Примеры

В следующем примере используется **рецептионкуалити** , чтобы отобразить процент пакетов, полученных в метке, в ответ на событие **плайстатечанже** . В примере для обновления экрана используется таймер с интервалом в 1 секунду. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether content is playing. 
    if (e.newState == 3)
    {
        // Start the timer. Update the display every 10 seconds.
        timer.Interval = 10000;
        timer.Start();
    }
    else
    {
        // Not playing; stop the timer.
        timer.Stop();
    }
}

private void UpdateReceptionQuality(object sender, EventArgs e)
{
    receptionQualityLabel.Text = ("Packets recovered: " + player.network.receptionQuality.ToString() + "%");
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

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

Public Sub UpdateReceptionQuality(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receptionQualityLabel.Text = (&quot;Packets recovered: &quot; + player.network.receptionQuality.ToString() + &quot;%&quot;)

End Sub
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Аксвиндовсмедиаплайер. URL (VB и C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпнетворк (VB и C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





