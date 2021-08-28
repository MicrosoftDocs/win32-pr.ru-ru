---
title: Событие Либрариконнект объекта Аксвиндовсмедиаплайер
description: Событие Либрариконнект возникает, когда библиотека станет доступной.
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- событие либрариконнект объекта аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- LibraryConnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940eed16004009e928309ae1a2e5d8f792b9fd0cb36fe8e836abfefb89e3ab95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123954"
---
# <a name="libraryconnect-event-of-the-axwindowsmediaplayer-object"></a>Событие Либрариконнект объекта Аксвиндовсмедиаплайер

Событие Либрариконнект возникает, когда библиотека станет доступной.

``` syntax
[C#]
private void player_LibraryConnect(
  object sender,
  _WMPOCXEvents_LibraryConnectEvent e
)

[Visual Basic]
Private Sub player_LibraryConnect(  
  sender As Object,
  e As _WMPOCXEvents_LibraryConnectEvent
) Handles player.LibraryConnect
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ либрариконнектевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ либрариконнектевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство | Описание                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| плибрари | **Вмплиб. ивмплибрари** Интерфейс, представляющий подключаемую библиотеку.<br/> |



 

## <a name="remarks"></a>Remarks

Это событие не происходит для локальной библиотеки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 11<br/>                                                                                         |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмплибрари (VB и C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





