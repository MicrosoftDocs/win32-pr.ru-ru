---
title: Событие Warning объекта Аксвиндовсмедиаплайер
description: Событие предупреждения зарезервировано для будущего использования.
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- событие предупреждения объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18925236148a508e66bb34e83f7ddb69f0cb59d87c98dfe0188f780ea2fc3605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004004"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a>Событие Warning объекта Аксвиндовсмедиаплайер

Событие предупреждения зарезервировано для будущего использования.

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ варнинжевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ варнинжевент**, который содержит следующие свойства, связанные с этим событием.



| Свойство    | Описание                                |
|-------------|--------------------------------------------|
| варнингтипе | **System. Int32** Не поддерживается.<br/>  |
| param       | **System. Int32** Не поддерживается.<br/>  |
| description | **System. String** Не поддерживается.<br/> |



 

## <a name="remarks"></a>Remarks

Это событие зарезервировано для будущего использования.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





