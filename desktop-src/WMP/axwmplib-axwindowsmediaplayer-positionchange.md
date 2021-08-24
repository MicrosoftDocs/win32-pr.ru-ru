---
title: Событие Поситиончанже объекта Аксвиндовсмедиаплайер
description: Событие Поситиончанже возникает при изменении текущей позиции воспроизведения в элементе мультимедиа.
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- событие поситиончанже объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- PositionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269d83c92687b5debda8b70fb4d6710b55eebd5476153759ebad36e5d17657d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764684"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a>Событие Поситиончанже объекта Аксвиндовсмедиаплайер

Событие Поситиончанже возникает при изменении текущей позиции воспроизведения в элементе мультимедиа.

``` syntax
[C#]
private void player_PositionChange(
  object sender,
  _WMPOCXEvents_PositionChangeEvent e
)

[Visual Basic]
Private Sub player_PositionChange(  
  sender As Object,
  e As _WMPOCXEvents_PositionChangeEvent
) Handles player.PositionChange
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ поситиончанжеевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ поситиончанжеевент**, который содержит следующие свойства, связанные с этим событием.



| Свойство    | Описание                                         |
|-------------|-----------------------------------------------------|
| олдпоситион | Старое расположение System. ДаублеспеЦифиес.<br/> |
| невпоситион | System. ДаублеспеЦифиес новое расположение.<br/> |



 

## <a name="remarks"></a>Remarks

Это событие не вызывается во время воспроизведения. Это происходит только тогда, когда что-то активно изменяет текущее положение воспроизводимого элемента мультимедиа, например, когда пользователь перемещает маркер поиска или когда выполняется код, указывающий значение для Ивмпконтролс. **CurrentPosition**.

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

[**Ивмпконтролс. currentPosition (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





