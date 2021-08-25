---
title: Событие Кдромбурнмедиаеррор объекта Аксвиндовсмедиаплайер
description: Событие Кдромбурнмедиаеррор возникает при возникновении ошибки при записи отдельного элемента мультимедиа на компакт-диск.
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- событие кдромбурнмедиаеррор объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba161945edcda7409b842987ab97768c30a6e1f0ba011772cf7f3757d3f61c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765273"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a>Событие Кдромбурнмедиаеррор объекта Аксвиндовсмедиаплайер

Событие Кдромбурнмедиаеррор возникает при возникновении ошибки при записи отдельного элемента мультимедиа на компакт-диск.

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кдромбурнмедиаерроревенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кдромбурнмедиаерроревент**, который содержит следующие свойства, связанные с этим событием.



| Свойство   | Описание                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| пкдромбурн | Интерфейс Вмплиб. Ивмпкдромбурнсе, представляющий операцию записи, вызвавшую ошибку.<br/>               |
| пмедиа     | Элемент мультимедиа System. Обжектсе, вызвавший ошибку. Это можно привести к интерфейсу Ивмпмедиа для доступа к нему.<br/> |



 

## <a name="remarks"></a>Remarks

Для захвата общих ошибок обрабатывайте Аксвмплиб. \_ \_Событие вмпокксевентс кдромбурнеррор.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 11<br/>                                                                                         |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Событие Аксвиндовсмедиаплайер. Кдромбурнеррор (VB и C#)**](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[**Интерфейс Ивмпкдромбурн (VB и C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





