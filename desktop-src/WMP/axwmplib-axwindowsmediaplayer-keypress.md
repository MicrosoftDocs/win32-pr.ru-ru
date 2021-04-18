---
title: Событие KeyPress объекта Аксвиндовсмедиаплайер
description: Событие KeyPress возникает при нажатии и отпускании клавиши. | Событие KeyPress объекта Аксвиндовсмедиаплайер
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- Событие KeyPress объекта Аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- KeyPress Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4a01e84b8f765d024c753d08211f3bb84e7f011
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699027"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a>Событие KeyPress объекта Аксвиндовсмедиаплайер

Событие KeyPress возникает при нажатии и отпускании клавиши.

``` syntax
[C#]
private void player_KeyPressEvent(
  object sender,
  _WMPOCXEvents_KeyPressEvent e
)

[Visual Basic]
Private Sub player_KeyPressEvent(  
  sender As Object,  
  e As _WMPOCXEvents_KeyPressEvent
) Handles player.KeyPressEvent
```

## <a name="event-data"></a>Данные о событиях

Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кэйпрессевенсандлер**. Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кэйпрессевент**, который содержит следующее свойство, связанное с этим событием.



| Свойство      | Описание                                                                        |
|---------------|------------------------------------------------------------------------------------|
| **нкэйасЦии** | System. Int16Specifies — стандартный числовой код ANSI для символа.<br/> |



 

## <a name="remarks"></a>Комментарии

Это событие возникает, когда нажатие клавиши приводит к вводу любого печатного символа клавиатуры, клавиши CTRL в сочетании с символом из стандартного алфавита или одного из нескольких специальных символов, а также клавишей Ввод или BACKSPACE.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





