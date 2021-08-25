---
title: Событие Кдромбурнеррор объекта Аксвиндовсмедиаплайер
description: Событие Кдромбурнеррор возникает при возникновении общей ошибки во время операции записи компакт-дисков.
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- событие кдромбурнеррор объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- CdromBurnError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ea2ca4c510685e8a9d23a3fdc507e055f30c8916c7bf8bbbfbb30a5c4591b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864744"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a>Событие Кдромбурнеррор объекта Аксвиндовсмедиаплайер

Событие Кдромбурнеррор возникает при возникновении общей ошибки во время операции записи компакт-дисков.

``` syntax
[C#]
private void player_CdromBurnError(
  object sender,
  _WMPOCXEvents_CdromBurnErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnError(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnErrorEvent
) Handles player.CdromBurnError
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кдромбурнерроревенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кдромбурнерроревент**, который содержит следующие свойства, связанные с этим событием.



| Свойство   | Описание                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| хреррор    | **System. Int32** Ошибка, вызвавшая событие.<br/>                                               |
| пкдромбурн | Интерфейс Вмплиб. Ивмпкдромбурнсе, представляющий операцию записи, вызвавшую ошибку.<br/> |



 

## <a name="remarks"></a>Remarks

Для записи ошибок, связанных с носителями, необходимо выполнить обработку Аксвмплиб. \_ \_Событие вмпокксевентс кдромбурнмедиаеррор.

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

[**Событие Аксвиндовсмедиаплайер. Кдромбурнмедиаеррор (VB и C#)**](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[**Интерфейс Ивмпкдромбурн (VB и C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





