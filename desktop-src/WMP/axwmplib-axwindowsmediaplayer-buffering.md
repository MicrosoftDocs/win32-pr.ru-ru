---
title: Буферизация события объекта Аксвиндовсмедиаплайер
description: Событие буферизации возникает, когда элемент управления проигрывателя Windows Media начинает или заканчивается буферизацией или загружается. | Буферизация события объекта Аксвиндовсмедиаплайер
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Буферизация события объекта Аксвиндовсмедиаплайер проигрывателя Windows Media
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af595443d78a311510df6a7e06b2e716da22ecae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694392"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a>Буферизация события объекта Аксвиндовсмедиаплайер

Событие буферизации возникает, когда элемент управления проигрывателя Windows Media начинает или заканчивается буферизацией или загружается.

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ буфферинжевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ буфферинжевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство | Описание                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Запуск    | System. БулеанспеЦифиес, начало или окончание буферизации. Значение true указывает, что оно началось; значение false указывает, что оно завершено.<br/> |



 

## <a name="remarks"></a>Комментарии

Это событие используется для определения времени, в течение которого буферизация или загрузка начинается или останавливается. Один и тот же блок событий можно использовать в обоих случаях и в Test *ивмпнетворк*. **буфферингпрогресс** и *ивмпнетворк*. **довнлоадпрогресс** , чтобы определить, является ли проигрыватель Windows Media в данный момент буферизацией или загрузкой содержимого.

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

[**Ивмпнетворк. Буфферингпрогресс (VB и C#)**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[**Ивмпнетворк. Довнлоадпрогресс (VB и C#)**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





