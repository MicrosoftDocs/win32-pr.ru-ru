---
title: Событие Плайлистколлектионплайлистремовед объекта Аксвиндовсмедиаплайер
description: Событие Плайлистколлектионплайлистремовед возникает при удалении списка воспроизведения из коллекции списков воспроизведения. | Событие Плайлистколлектионплайлистремовед объекта Аксвиндовсмедиаплайер
ms.assetid: 96935a9e-4c08-42e9-a63f-7b6cda41b243
keywords:
- Событие Плайлистколлектионплайлистремовед в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b982ff566380a7aa5bf4d0b1a1219739b52dd35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699080"
---
# <a name="playlistcollectionplaylistremoved-event-of-the-axwindowsmediaplayer-object"></a>Событие Плайлистколлектионплайлистремовед объекта Аксвиндовсмедиаплайер

Событие Плайлистколлектионплайлистремовед возникает при удалении списка воспроизведения из коллекции списков воспроизведения.

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistRemoved(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistRemoved(  
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent
) Handles player.PlaylistCollectionPlaylistRemoved
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ плайлистколлектионплайлистремоведевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ плайлистколлектионплайлистремоведевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство             | Описание                                                                  |
|----------------------|------------------------------------------------------------------------------|
| **бстрплайлистнаме** | System. СтрингспеЦифиес имя списка воспроизведения, который был удален.<br/> |



 

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

[**Ивмпплайлистколлектион. Жетбинаме (VB и C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





