---
title: Событие Плайлистколлектионплайлистремовед объекта Аксвиндовсмедиаплайер
description: Событие Плайлистколлектионплайлистремовед возникает при удалении списка воспроизведения из коллекции списков воспроизведения. | Событие Плайлистколлектионплайлистремовед объекта Аксвиндовсмедиаплайер
ms.assetid: 96935a9e-4c08-42e9-a63f-7b6cda41b243
keywords:
- событие плайлистколлектионплайлистремовед объекта аксвиндовсмедиаплайер проигрыватель Windows Media
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
ms.openlocfilehash: 170dd4291c1c60f0e20c548c611485cddd50f5ec51d3f244d21f3e046e5c0d4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864576"
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



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлистколлектион. Жетбинаме (VB и C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





