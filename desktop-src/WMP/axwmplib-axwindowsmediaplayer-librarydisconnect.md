---
title: Событие Либраридисконнект объекта Аксвиндовсмедиаплайер
description: Событие Либраридисконнект возникает, когда библиотека больше недоступна.
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- событие либраридисконнект объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- LibraryDisconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a032dc95a68430768b0f2aa109a56dae80cdaecb14b67eb5dbf6b2657cdd5107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136007"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a>Событие Либраридисконнект объекта Аксвиндовсмедиаплайер

Событие Либраридисконнект возникает, когда библиотека больше недоступна.

``` syntax
[C#]
private void player_LibraryDisconnect(
  object sender,
  _WMPOCXEvents_LibraryDisconnectEvent e
)

[Visual Basic]
Private Sub player_LibraryDisconnect(  
   sender As Object,  
   e As _WMPOCXEvents_LibraryDisconnectEvent
) Handles player.LibraryDisconnect
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ либраридисконнектевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ либраридисконнектевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство | Описание                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| плибрари | **Вмплиб. ивмплибрари** Интерфейс, представляющий библиотеку, которая была отключена.<br/> |



 

## <a name="remarks"></a>Remarks

Это событие не происходит для локальной библиотеки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 11<br/>                                                                                         |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмплибрари (VB и C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





