---
title: Событие Медиаколлектионаттрибутестрингаддед объекта Аксвиндовсмедиаплайер
description: Событие Медиаколлектионаттрибутестрингаддед возникает при добавлении значения атрибута в библиотеку. | Событие Медиаколлектионаттрибутестрингаддед объекта Аксвиндовсмедиаплайер
ms.assetid: b14db0ce-bd78-4e28-a42c-1a231c29da2b
keywords:
- событие медиаколлектионаттрибутестрингаддед объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d0612e18256f81529a8ad703ecf887ba5976ea9913e46598bc5a0fd44a903e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123944"
---
# <a name="mediacollectionattributestringadded-event-of-the-axwindowsmediaplayer-object"></a>Событие Медиаколлектионаттрибутестрингаддед объекта Аксвиндовсмедиаплайер

Событие Медиаколлектионаттрибутестрингаддед возникает при добавлении значения атрибута в библиотеку.

``` syntax
[C#]
private void player_MediaCollectionAttributeStringAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent
) Handles player.MediaCollectionAttributeStringAdded
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионаттрибутестрингаддедевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионаттрибутестрингаддедевент**, который содержит следующие свойства, связанные с этим событием.



| Свойство           | Описание                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **бстраттрибнаме** | System. СтрингспеЦифиес имя атрибута. дополнительные сведения об атрибутах, поддерживаемых проигрыватель Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).<br/> |
| бстраттрибвал      | System. СтрингспеЦифиес значение атрибута.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Remarks

При добавлении элемента мультимедиа в библиотеку его метаданные добавляются в коллекцию носителей, и это событие срабатывает для каждого добавленного атрибута.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Аксвиндовсмедиаплайер. Медиаколлектион (VB и C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиаколлектион (VB и C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





