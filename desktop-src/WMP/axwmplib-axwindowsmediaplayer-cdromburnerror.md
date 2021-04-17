---
title: Событие Кдромбурнеррор объекта Аксвиндовсмедиаплайер
description: Событие Кдромбурнеррор возникает при возникновении общей ошибки во время операции записи компакт-дисков.
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- Событие Кдромбурнеррор в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
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
ms.openlocfilehash: 7c27969ea83089b225ba92eb93854fc1dcde9bde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694390"
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



 

## <a name="remarks"></a>Комментарии

Для записи ошибок, связанных с носителями, необходимо выполнить обработку Аксвмплиб. \_ \_Событие вмпокксевентс кдромбурнмедиаеррор.

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

[**Событие Аксвиндовсмедиаплайер. Кдромбурнмедиаеррор (VB и C#)**](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[**Интерфейс Ивмпкдромбурн (VB и C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





