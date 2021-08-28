---
title: Ивмпмедиа, свойство длительности
description: Свойство Duration возвращает продолжительность текущего элемента мультимедиа в секундах.
ms.assetid: f8a0bf3e-eeaf-46f5-90c8-d3b11ce4eb39
keywords:
- свойство duration проигрыватель Windows Media
- свойство duration проигрыватель Windows Media, интерфейс ивмпмедиа
- проигрыватель Windows Media интерфейса ивмпмедиа, свойство duration
topic_type:
- apiref
api_name:
- IWMPMedia.duration
- IWMPMedia.get_duration
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38703c37e73ba6312970b8e5b929441c3c5c9ccd1f034ab244dc97c36c2d2162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506024"
---
# <a name="iwmpmediaduration-property"></a>Ивмпмедиа: свойство фигурации:d

Свойство **Duration** Возвращает продолжительность текущего элемента мультимедиа в секундах.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Double duration {get;}
```


```VB

Public ReadOnly Property duration As System.Double
```





## <a name="property-value"></a>Значение свойства

Значение **System. Double** , которое является длительностью в секундах.

## <a name="remarks"></a>Remarks

Если это свойство используется с элементом мультимедиа, отличным от указанного в Аксвиндовсмедиаплайер. Куррентмедиа, он может не содержать допустимого значения.

чтобы получить длительность для файлов, которые не находятся в библиотеке пользователя, необходимо подождать, пока проигрыватель Windows Media откроет файл. то есть текущий **опенстате** должен равняться **медиаопен**. Это можно проверить, обрабатывая **аксвиндовсмедиаплайер. \_ Вмпокксевентс \_ опенстатечанже** или путем периодической проверки значения **аксвиндовсмедиаплайер. опенстате**.

Для списков воспроизведения продолжительность каждого элемента мультимедиа может быть получена при открытии отдельного элемента мультимедиа, а не при открытии списка воспроизведения.

Перед использованием этого свойства необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере используется **Длительность** для вывода времени, оставшегося в текущем элементе мультимедиа в метке. Таймер обновляет текст метки каждую секунду.


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 

private void TimerEventProcessor(object sender, System.EventArgs e)
{
    // Subtract the current position from the duration of the current media to get
    // the time remaining. Use the Math.floor method to round the result down to the
    // nearest whole number.
    double t = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition);

    // Display the time remaining in the current media.
    timeRemaining.Text = ("Seconds remaining: " + t.ToString());        
}
```


```VB

' Set the timer to fire an event every second and start the timer.
Timer.Interval = 1000
Timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a Select Case statement to
&#39; determine when to start and stop the timer. 

Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles Timer.Tick

    &#39; Subtract the current position from the duration of the current media to get
    &#39; the time remaining. Use the Math.Floor method to round the result down to the
    &#39; nearest whole number.
    Dim t As Double = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition)

    &#39; Display the time remaining in the current media.
    timeRemaining.Text = (&quot;Seconds remaining: &quot; + t.ToString())

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

[**Аксвиндовсмедиаплайер. Куррентмедиа (VB и C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**Аксвиндовсмедиаплайер. Опенстате (VB и C#)**](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> <dt>

[**Событие Аксвиндовсмедиаплайер. Опенстатечанже (VB и C#)**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиа. Дуратионстринг (VB и C#)**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)
</dt> </dl>

 

 





