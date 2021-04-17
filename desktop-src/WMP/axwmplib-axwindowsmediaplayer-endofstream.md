---
title: Событие EndOfStream объекта Аксвиндовсмедиаплайер
description: Событие EndOfStream зарезервировано для будущего использования.
ms.assetid: 004172e0-abd4-451c-bd5c-6bf0a9277661
keywords:
- Событие EndOfStream в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- EndOfStream Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74a64eea77af43cd3b33cc7edee2177aee7d15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694457"
---
# <a name="endofstream-event-of-the-axwindowsmediaplayer-object"></a>Событие EndOfStream объекта Аксвиндовсмедиаплайер

Событие EndOfStream зарезервировано для будущего использования.

``` syntax
[C#]
private void player_EndOfStream(
  object sender,
  _WMPOCXEvents_EndOfStreamEvent e
)

[Visual Basic]
Private Sub player_EndOfStream(  
  sender As Object,  
  e As _WMPOCXEvents_EndOfStreamEvent
) Handles player.EndOfStream
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ ендофстреамевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ ендофстреамевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство | Описание                           |
|----------|---------------------------------------|
| result   | System. Int32Not поддерживается.<br/> |



 

## <a name="remarks"></a>Комментарии

Это событие зарезервировано для будущего использования.

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

 

 





