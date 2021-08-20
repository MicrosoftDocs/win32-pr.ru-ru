---
title: Событие KeyPress объекта Аксвиндовсмедиаплайер
description: Событие KeyPress возникает при нажатии и отпускании клавиши. | Событие KeyPress объекта Аксвиндовсмедиаплайер
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- событие KeyPress объекта аксвиндовсмедиаплайер проигрыватель Windows Media
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
ms.openlocfilehash: 45b8022feacda910b28d68636c1abdcb2f6c1c9d3c2e799f762f25f5060b2b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618794"
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



 

## <a name="remarks"></a>Remarks

Это событие возникает, когда нажатие клавиши приводит к вводу любого печатного символа клавиатуры, клавиши CTRL в сочетании с символом из стандартного алфавита или одного из нескольких специальных символов, а также клавишей Ввод или BACKSPACE.

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

 

 





