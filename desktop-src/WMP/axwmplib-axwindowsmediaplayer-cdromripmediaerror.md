---
title: Событие Кдромрипмедиаеррор объекта Аксвиндовсмедиаплайер
description: Событие Кдромрипмедиаеррор возникает при возникновении ошибки при копировании отдельной дорожки с компакт-диска.
ms.assetid: 542d0184-d893-4b98-903e-339909276fd6
keywords:
- Событие Кдромрипмедиаеррор в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- CdromRipMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39b429505996cd5e85bc1e0e2e85c3f47103d244
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694385"
---
# <a name="cdromripmediaerror-event-of-the-axwindowsmediaplayer-object"></a>Событие Кдромрипмедиаеррор объекта Аксвиндовсмедиаплайер

Событие Кдромрипмедиаеррор возникает при возникновении ошибки при копировании отдельной дорожки с компакт-диска.

``` syntax
[C#]
private void player_CdromRipMediaError(
  object sender,
  _WMPOCXEvents_CdromRipMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromRipMediaError( 
  sender As Object,
  e As _WMPOCXEvents_CdromRipMediaErrorEvent
) Handles player.CdromRipMediaError
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кдромрипмедиаерроревенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кдромрипмедиаерроревент**, который содержит следующие свойства, связанные с этим событием.



| Свойство  | Описание                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| пкдромрип | Интерфейс Вмплиб. Ивмпкдромрипсе, представляющий операцию копирования, вызвавшую ошибку.<br/>                |
| пмедиа    | Элемент мультимедиа System. Обжектсе, вызвавший ошибку. Это можно привести к интерфейсу Ивмпмедиа для доступа к нему.<br/> |



 

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

[**Интерфейс Ивмпкдромрип (VB и C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





