---
title: Событие Медиаколлектионмедиааддед объекта Аксвиндовсмедиаплайер
description: Событие Медиаколлектионмедиааддед возникает при добавлении элемента мультимедиа в локальную библиотеку. | Событие Медиаколлектионмедиааддед объекта Аксвиндовсмедиаплайер
ms.assetid: ba1779f6-a212-44f4-b52a-c88e22aebcce
keywords:
- Событие Медиаколлектионмедиааддед в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb839fccf9a5048b5647480eca36fcfcaeb904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699011"
---
# <a name="mediacollectionmediaadded-event-of-the-axwindowsmediaplayer-object"></a>Событие Медиаколлектионмедиааддед объекта Аксвиндовсмедиаплайер

Событие Медиаколлектионмедиааддед возникает при добавлении элемента мультимедиа в локальную библиотеку.

``` syntax
[C#]
private void player_MediaCollectionMediaAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionMediaAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaAddedEvent
) Handles player.MediaCollectionMediaAdded
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионмедиааддедевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионмедиааддедевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство | Описание                                                                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|
| пмедиа   | Элемент мультимедиа System. Обжектсе добавлен в локальную библиотеку. Это можно привести к интерфейсу Ивмпмедиа для доступа к нему.<br/> |



 

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

[**Аксвиндовсмедиаплайер. Медиаколлектион (VB и C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиаколлектион (VB и C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





