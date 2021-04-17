---
title: Событие Опенстатечанже объекта Аксвиндовсмедиаплайер
description: Событие Опенстатечанже возникает при изменении значения свойства Опенстате. | Событие Опенстатечанже объекта Аксвиндовсмедиаплайер
ms.assetid: 0229f8b4-7216-44f6-9838-a640b99bd9f3
keywords:
- Событие Опенстатечанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- OpenStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcd1f2b7e59fdfd35bf31719cbb6a1a5e6c29e66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694523"
---
# <a name="openstatechange-event-of-the-axwindowsmediaplayer-object"></a>Событие Опенстатечанже объекта Аксвиндовсмедиаплайер

Событие Опенстатечанже возникает при изменении значения свойства **опенстате** .

``` syntax
[C#]
private void player_OpenStateChange(
  object sender,
  _WMPOCXEvents_OpenStateChangeEvent e
)

[Visual Basic]
Private Sub player_OpenStateChange(
  sender As Object,
  e As _WMPOCXEvents_OpenStateChangeEvent
) Handles player.OpenStateChange
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ опенстатечанжеевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ опенстатечанжеевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство | Описание                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NewState | System. Int32Specifies новое состояние открытия. Таблицу значений см. в разделе [опенстате](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).<br/> |



 

## <a name="remarks"></a>Комментарии

Проигрыватель Windows Media может пройти несколько открытых состояний при попытке открыть сетевой файл, например найти сервер, подключиться к серверу и, наконец, открыть файл. Это событие будет срабатывать каждый раз при изменении состояния открытия.

Состояния проигрывателя Windows Media не гарантированно выполняются в определенном порядке. Кроме того, не все состояния должны происходить во время последовательности событий. Не следует писать код, зависящий от порядка состояний.

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

[**Аксвиндовсмедиаплайер. Опенстате (VB и C#)**](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> </dl>

 

 





