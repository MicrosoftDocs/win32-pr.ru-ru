---
title: Событие Медиаколлектионаттрибутестрингчанжед объекта Аксвиндовсмедиаплайер
description: Событие Медиаколлектионаттрибутестрингчанжед возникает при изменении значения атрибута в библиотеке. | Событие Медиаколлектионаттрибутестрингчанжед объекта Аксвиндовсмедиаплайер
ms.assetid: f5b91399-42b7-4202-9b65-caa9b15847b9
keywords:
- событие медиаколлектионаттрибутестрингчанжед объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dcc755d1a183525923b91ce2de7937860582c3cf795d13cbf4a8c22d7c9c37f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618784"
---
# <a name="mediacollectionattributestringchanged-event-of-the-axwindowsmediaplayer-object"></a>Событие Медиаколлектионаттрибутестрингчанжед объекта Аксвиндовсмедиаплайер

Событие Медиаколлектионаттрибутестрингчанжед возникает при изменении значения атрибута в библиотеке.

``` syntax
[C#]
private void player_MediaCollectionAttributeStringChanged(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringChanged(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent
) Handles player.MediaCollectionAttributeStringChanged
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионаттрибутестрингчанжедевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионаттрибутестрингчанжедевент**, который содержит следующие свойства, связанные с этим событием.



| Свойство         | Описание                                                                                                                                                                                  |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| бстраттрибнаме   | System. СтрингспеЦифиес имя атрибута. дополнительные сведения об атрибутах, поддерживаемых проигрыватель Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).<br/> |
| бстролдаттрибвал | System. СтрингспеЦифиес старое значение атрибута.<br/>                                                                                                                            |
| бстрневаттрибвал | System. СтрингспеЦифиес новое значение атрибута.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Remarks

Когда пользователь изменяет метаданные библиотеки, коллекция носителей обновляется, и это событие срабатывает для каждого измененного атрибута.

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

[**Аксвиндовсмедиаплайер. Медиаколлектион (VB и C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиаколлектион (VB и C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





