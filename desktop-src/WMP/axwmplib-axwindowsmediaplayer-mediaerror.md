---
title: Событие Медиаеррор объекта Аксвиндовсмедиаплайер
description: Событие Медиаеррор возникает, когда объект мультимедиа имеет условие ошибки.
ms.assetid: a1fb3422-85c4-4856-951a-332517599984
keywords:
- событие медиаеррор объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- MediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83dc6bceb188ff443bfdcab904242e91b30fba80c4bae4f03cfa388cf15642b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902614"
---
# <a name="mediaerror-event-of-the-axwindowsmediaplayer-object"></a>Событие Медиаеррор объекта Аксвиндовсмедиаплайер

Событие Медиаеррор возникает, когда объект мультимедиа имеет условие ошибки.

``` syntax
[C#]
private void player_MediaError(
  object sender,
  _WMPOCXEvents_MediaErrorEvent e
)

[Visual Basic]
Private Sub player_MediaError(
  sender As Object,
  e As _WMPOCXEvents_MediaErrorEvent
) Handles player.MediaError
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ медиаерроревенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ медиаерроревент**, который содержит следующее свойство, связанное с этим событием.



| Свойство     | Описание                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| пмедиаобжект | System. Обжектобжект с условием ошибки. Это можно привести к интерфейсу Ивмпмедиа для доступа к нему.<br/> |



 

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

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





