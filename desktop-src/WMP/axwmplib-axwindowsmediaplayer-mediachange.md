---
title: Событие Медиачанже объекта Аксвиндовсмедиаплайер
description: Событие Медиачанже возникает при изменении элемента мультимедиа. | Событие Медиачанже объекта Аксвиндовсмедиаплайер
ms.assetid: 0a2380ff-df50-4092-a952-812184822719
keywords:
- Событие Медиачанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- MediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175a7ed6ca57e3083d307cfe218d09233410053c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695169"
---
# <a name="mediachange-event-of-the-axwindowsmediaplayer-object"></a>Событие Медиачанже объекта Аксвиндовсмедиаплайер

Событие Медиачанже возникает при изменении элемента мультимедиа.

``` syntax
[C#]
private void player_MediaChange(
  object sender,
  _WMPOCXEvents_MediaChangeEvent e
)

[Visual Basic]
Private Sub player_MediaChange(  
  sender As Object,  
  e As _WMPOCXEvents_MediaChangeEvent
) Handles player.MediaChange
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ медиачанжеевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ медиачанжеевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство | Описание                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------|
| Item     | Измененный элемент мультимедиа System. Обжектсе. Это можно привести к интерфейсу Ивмпмедиа для доступа к нему.<br/> |



 

## <a name="examples"></a>Примеры

В следующем примере для вывода имени текущего элемента мультимедиа используется метка. Код обновляет текст в метке с каждым вхождением события Медиачанже. Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.


```CSharp
// Add a delegate for the MediaChange event.
player.MediaChange += new AxWMPLib._WMPOCXEvents_MediaChangeEventHandler(player_MediaChange);

private void player_MediaChange(object sender, AxWMPLib._WMPOCXEvents_MediaChangeEvent e)
{
    // Get an interface to the changed media item that is returned in the event data. 
    WMPLib.IWMPMedia3 changedItem = (WMPLib.IWMPMedia3)e.item;

    // Display the name of the changed media item.
    mediaName.Text = changedItem.name;
}
```


```VB

Public Sub player_MediaChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_MediaChangeEvent) Handles player.MediaChange

    &#39; Get an interface to the changed media item that is returned in the event data.
    Dim changedItem As WMPLib.IWMPMedia3 = e.item

    &#39; Display the name of the changed media item.
    mediaName.Text = changedItem.name

End Sub
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





