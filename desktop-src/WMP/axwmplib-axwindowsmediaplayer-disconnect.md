---
title: Событие Disconnect объекта Аксвиндовсмедиаплайер
description: Событие Disconnect зарезервировано для будущего использования.
ms.assetid: 3baecc6c-e772-4269-96c1-900be270543e
keywords:
- событие Disconnect объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Disconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0554de8fe71ae13e510733ed2204ff4ed79d575a40f23a1769a5fb36eeb560
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902702"
---
# <a name="disconnect-event-of-the-axwindowsmediaplayer-object"></a>Событие Disconnect объекта Аксвиндовсмедиаплайер

Событие Disconnect зарезервировано для будущего использования.

``` syntax
[C#]
private void player_Disconnect(
  object sender,
  _WMPOCXEvents_DisconnectEvent e
)

[Visual Basic]
Private Sub player_Disconnect(  
  sender As Object,
  e As _WMPOCXEvents_DisconnectEvent
) Handles player.Disconnect
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ дисконнектевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ дисконнектевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство | Описание                               |
|----------|-------------------------------------------|
| result   | **System. Int32** Не поддерживается.<br/> |



 

## <a name="remarks"></a>Remarks

Это событие зарезервировано для будущего использования.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





