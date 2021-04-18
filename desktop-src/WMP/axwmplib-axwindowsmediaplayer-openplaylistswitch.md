---
title: Событие Опенплайлистсвитч объекта Аксвиндовсмедиаплайер
description: Событие Опенплайлистсвитч возникает, когда начинается воспроизведение заголовка на DVD-диске. | Событие Опенплайлистсвитч объекта Аксвиндовсмедиаплайер
ms.assetid: 0b9c37a3-1349-48bd-8e1a-aba286c82abf
keywords:
- Событие Опенплайлистсвитч в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d360944b46555be53d5e212561cf906dd33c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694729"
---
# <a name="openplaylistswitch-event-of-the-axwindowsmediaplayer-object"></a>Событие Опенплайлистсвитч объекта Аксвиндовсмедиаплайер

Событие Опенплайлистсвитч возникает, когда начинается воспроизведение заголовка на DVD-диске.

``` syntax
[C#]
private void player_OpenPlaylistSwitch(
  object sender,
  _WMPOCXEvents_OpenPlaylistSwitchEvent e
)

[Visual Basic]
Private Sub player_OpenPlaylistSwitch(
  sender As Object,
  e As _WMPOCXEvents_OpenPlaylistSwitchEvent
) Handles player.OpenPlaylistSwitch
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ опенплайлистсвитчевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ опенплайлистсвитчевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство  | Описание                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------|
| **питем** | System. Обжектобжект, представляющий заголовок. Это можно привести к интерфейсу Ивмпплайлист для доступа к нему.<br/> |



 

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

 

 





