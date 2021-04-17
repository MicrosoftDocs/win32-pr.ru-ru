---
title: Событие Медиаколлектионаттрибутестрингремовед объекта Аксвиндовсмедиаплайер
description: Событие Медиаколлектионаттрибутестрингремовед возникает при удалении значения атрибута из библиотеки. | Событие Медиаколлектионаттрибутестрингремовед объекта Аксвиндовсмедиаплайер
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- Событие Медиаколлектионаттрибутестрингремовед в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b6b028a2a47585b06159ed46b986124583950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694538"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a>Событие Медиаколлектионаттрибутестрингремовед объекта Аксвиндовсмедиаплайер

Событие Медиаколлектионаттрибутестрингремовед возникает при удалении значения атрибута из библиотеки.

``` syntax
[C#]
private void player_MediaCollectionAttributeStringRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent
) Handles player.MediaCollectionAttributeStringRemoved
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионаттрибутестрингремоведевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионаттрибутестрингремоведевент**, который содержит следующие свойства, связанные с этим событием.



| Свойство           | Описание                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **бстраттрибнаме** | System. СтрингспеЦифиес имя атрибута. Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).<br/> |
| бстраттрибвал      | System. СтрингспеЦифиес значение атрибута.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Комментарии

При удалении элемента мультимедиа из библиотеки его метаданные удаляются из **медиаколлектион** , и это событие срабатывает для каждого удаляемого атрибута.

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

[**Аксвиндовсмедиаплайер. Медиаколлектион (VB и C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиаколлектион (VB и C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





