---
title: Событие Маркерхит объекта Аксвиндовсмедиаплайер
description: Событие Маркерхит возникает при достижении маркера. | Событие Маркерхит объекта Аксвиндовсмедиаплайер
ms.assetid: 247fc22c-18c4-46b6-b42c-4882209a47f4
keywords:
- Событие Маркерхит в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- MarkerHit Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bad8d9d64b4711937cd984bbd9d335acebfe67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699022"
---
# <a name="markerhit-event-of-the-axwindowsmediaplayer-object"></a>Событие Маркерхит объекта Аксвиндовсмедиаплайер

Событие Маркерхит возникает при достижении маркера.

``` syntax
[C#]
private void player_MarkerHit(
  object sender,
  _WMPOCXEvents_MarkerHitEvent e
)

[Visual Basic]
Private Sub player_MarkerHit(  
  sender As Object,  
  e As _WMPOCXEvents_MarkerHitEvent
) Handles player.MarkerHit
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ маркерхитевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ маркерхитевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство      | Описание                                                             |
|---------------|-------------------------------------------------------------------------|
| **маркернум** | System. Int32Indicates — номер маркера, который был достигнут.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





