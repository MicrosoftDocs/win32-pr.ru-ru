---
title: Событие Стрингколлектиончанже объекта Аксвиндовсмедиаплайер
description: Событие Стрингколлектиончанже возникает при изменении коллекции строк. | Событие Стрингколлектиончанже объекта Аксвиндовсмедиаплайер
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- событие стрингколлектиончанже объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- StringCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ceeba7942be4180d02a44ff19d63c10f9bc9df0bba745fdf69bcf10e97c3052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764663"
---
# <a name="stringcollectionchange-event-of-the-axwindowsmediaplayer-object"></a>Событие Стрингколлектиончанже объекта Аксвиндовсмедиаплайер

Событие Стрингколлектиончанже возникает при изменении коллекции строк.

``` syntax
[C#]
private void player_StringCollectionChange(
  object sender,
  _WMPOCXEvents_StringCollectionChangeEvent e
)

[Visual Basic]
Private Sub player_StringCollectionChange(
  sender As Object,
  e As _WMPOCXEvents_StringCollectionChangeEvent
) Handles player.StringCollectionChange
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ стрингколлектиончанжеевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ стрингколлектиончанжеевент**, который содержит следующие свойства, связанные с этим событием.



| Свойство              | Описание                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| пдиспстрингколлектион | Измененный элемент коллекции строк System. Обжектсе. Это можно привести к интерфейсу Ивмпстрингколлектион для доступа к нему.<br/> |
| лколлектиониндекс      | Индекс System. Int32The элемента коллекции строк, который был изменен.<br/>                                                          |
| Изменить                | Значение перечисления Вмплиб. Вмпстрингколлектиончанжеевенттипеан, указывающее тип произошедшего изменения.<br/>                 |



 

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

[**Интерфейс Ивмпстрингколлектион (VB и C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**вмпстрингколлектиончанжеевенттипе**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 





