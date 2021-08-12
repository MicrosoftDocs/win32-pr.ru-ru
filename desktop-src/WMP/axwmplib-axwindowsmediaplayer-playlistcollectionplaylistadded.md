---
title: Событие Плайлистколлектионплайлистаддед объекта Аксвиндовсмедиаплайер
description: Событие Плайлистколлектионплайлистаддед возникает при добавлении списка воспроизведения в коллекцию списков воспроизведения. | Событие Плайлистколлектионплайлистаддед объекта Аксвиндовсмедиаплайер
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- событие плайлистколлектионплайлистаддед объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5223d5864aa8be9019b2219ef09917a1c63cf16d87a48aef9543246d5197a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581829"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a>Событие Плайлистколлектионплайлистаддед объекта Аксвиндовсмедиаплайер

Событие Плайлистколлектионплайлистаддед возникает при добавлении списка воспроизведения в коллекцию списков воспроизведения.

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistAdded(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistAdded(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent
) Handles player.PlaylistCollectionPlaylistAdded
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ плайлистколлектионплайлистаддедевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ плайлистколлектионплайлистаддедевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство             | Описание                                                                |
|----------------------|----------------------------------------------------------------------------|
| **бстрплайлистнаме** | System. СтрингспеЦифиес. имя добавленного списка воспроизведения.<br/> |



 

## <a name="remarks"></a>Remarks

Имя добавленного списка воспроизведения можно использовать для получения соответствующего списка воспроизведения с помощью Ивмпплайлистколлектион. метод **жетбинаме** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлистколлектион. Жетбинаме (VB и C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





