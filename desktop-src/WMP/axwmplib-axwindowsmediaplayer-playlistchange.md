---
title: Событие Плайлистчанже объекта Аксвиндовсмедиаплайер
description: Событие Плайлистчанже возникает при изменении списка воспроизведения. | Событие Плайлистчанже объекта Аксвиндовсмедиаплайер
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- Событие Плайлистчанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- PlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9989b303d8e9077c158fd844c93431100205d9f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699085"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a>Событие Плайлистчанже объекта Аксвиндовсмедиаплайер

Событие Плайлистчанже возникает при изменении списка воспроизведения.

``` syntax
[C#]
private void player_PlaylistChange(
  object sender,
  _WMPOCXEvents_PlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_PlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_PlaylistChangeEvent
) Handles player.PlaylistChange
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ плайлистчанжеевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ плайлистчанжеевент**, который содержит следующие свойства, связанные с этим событием.



| Свойство     | Описание                                                                                                                   |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| **список воспроизведения** | Измененный объект System. Обжектсе. Это можно привести к интерфейсу Ивмпплайлист для доступа к нему.<br/>                |
| **change**   | Значение перечисления Вмплиб. Вмпплайлистчанжеевенттипеан, указывающее тип изменения, произошедшего в списке воспроизведения.<br/> |



 

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

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





