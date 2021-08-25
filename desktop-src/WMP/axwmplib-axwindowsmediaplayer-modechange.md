---
title: Событие Модечанже объекта Аксвиндовсмедиаплайер
description: событие модечанже возникает при изменении режима проигрыватель Windows Media. | Событие Модечанже объекта Аксвиндовсмедиаплайер
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- событие модечанже объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- ModeChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3b81ce7c48fd34f03131c7ed3f6cafed1029b103f218842a70ecaade08f1af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764844"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a>Событие Модечанже объекта Аксвиндовсмедиаплайер

событие модечанже возникает при изменении режима проигрыватель Windows Media.

``` syntax
[C#]
private void player_ModeChange(
  object sender,
  _WMPOCXEvents_ModeChangeEvent e
)

[Visual Basic]
Private Sub player_ModeChange( 
  sender As Object,
  e As _WMPOCXEvents_ModeChangeEvent
) Handles player.ModeChange
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ модечанжеевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ модечанжеевент**, который содержит следующие свойства, связанные с этим событием.



| Свойство | Описание                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| моденаме | System. Стрингиндикатес режим, который был изменен. Возможные значения см. в разделе Примечания.<br/> |
| newValue | System. Булеаниндикатес новое состояние указанного режима.<br/>                        |



 

## <a name="remarks"></a>Remarks

В следующей таблице приведены возможные значения для свойства Моденаме.



| Строка  | Описание                                         |
|---------|-----------------------------------------------------|
| shuffle | Дорожки воспроизводятся в случайном порядке.                  |
| loop    | Все последовательности дорожек воспроизводятся постоянно. |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. мода (VB и C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. setMode (VB и C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





