---
title: Событие Кдромрипстатечанже объекта Аксвиндовсмедиаплайер
description: Событие Кдромрипстатечанже возникает при изменении состояния операции копирования компакт-диска.
ms.assetid: 0a0bd11f-a685-4c4e-8704-8eabe80d6f86
keywords:
- Событие Кдромрипстатечанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- CdromRipStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20fae9eb1fa6d5f65876e3f6758a7594f0bdbb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694383"
---
# <a name="cdromripstatechange-event-of-the-axwindowsmediaplayer-object"></a>Событие Кдромрипстатечанже объекта Аксвиндовсмедиаплайер

Событие Кдромрипстатечанже возникает при изменении состояния операции копирования компакт-диска.

``` syntax
[C#]
private void player_CdromRipStateChange(
  object sender,
  _WMPOCXEvents_CdromRipStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromRipStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromRipStateChangeEvent
) Handles player.CdromRipStateChange
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кдромрипстатечанжеевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кдромрипстатечанжеевент**, который содержит следующие свойства, связанные с этим событием.



| Свойство  | Описание                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| пкдромрип | Интерфейс Вмплиб. Ивмпкдромрипсе, представляющий операцию копирования, вызвавшую ошибку.<br/> |
| вмпрс     | Значение перечисления Вмплиб. Вмприпстатесе, указывающее новое состояние.<br/>                         |



 

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

[**Интерфейс Ивмпкдромрип (VB и C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**вмприпстате**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





