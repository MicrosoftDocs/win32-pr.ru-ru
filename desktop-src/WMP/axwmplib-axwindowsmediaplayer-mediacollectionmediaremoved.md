---
title: Событие Медиаколлектионмедиаремовед объекта Аксвиндовсмедиаплайер
description: Событие Медиаколлектионмедиаремовед возникает при удалении элемента мультимедиа из локальной библиотеки. | Событие Медиаколлектионмедиаремовед объекта Аксвиндовсмедиаплайер
ms.assetid: 66dae2be-2a71-4d53-b2e2-f106426d4eea
keywords:
- Событие Медиаколлектионмедиаремовед в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea15ff63fb913cd399a152913a27ffda1090d9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699010"
---
# <a name="mediacollectionmediaremoved-event-of-the-axwindowsmediaplayer-object"></a>Событие Медиаколлектионмедиаремовед объекта Аксвиндовсмедиаплайер

Событие Медиаколлектионмедиаремовед возникает при удалении элемента мультимедиа из локальной библиотеки.

``` syntax
[C#]
private void player_MediaCollectionMediaRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaRemovedEvent e
)
        
[Visual Basic]
Private Sub player_MediaCollectionMediaRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaRemovedEvent
) Handles player.MediaCollectionMediaRemoved
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионмедиаремоведевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионмедиаремоведевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство | Описание                                                                                                                      |
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| пмедиа   | Элемент мультимедиа System. Обжектсе удален из локальной библиотеки. Это можно привести к интерфейсу Ивмпмедиа для доступа к нему.<br/> |



 

## <a name="remarks"></a>Комментарии

Это событие возникает только для локальной библиотеки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11<br/>                                                                                         |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





