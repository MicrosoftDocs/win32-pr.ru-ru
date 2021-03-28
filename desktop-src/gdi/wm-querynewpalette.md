---
description: Сообщение WM \_ куериневпалетте информирует окно о том, что он собирается получить фокус клавиатуры, давая окну возможность реализовать логическую палитру при получении фокуса.
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: Сообщение WM_QUERYNEWPALETTE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985337"
---
# <a name="wm_querynewpalette-message"></a>\_Сообщение КУЕРИНЕВПАЛЕТТЕ WM

Сообщение **WM \_ куериневпалетте** информирует окно о том, что он собирается получить фокус клавиатуры, давая окну возможность реализовать логическую палитру при получении фокуса.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если окно реализует логическую палитру, оно должно возвращать **значение true**. в противном случае он должен вернуть **значение false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о цветах](colors.md)
</dt> <dt>

[Цветные сообщения](color-messages.md)
</dt> <dt>

[**WM \_ палеттечанжед**](wm-palettechanged.md)
</dt> <dt>

[**WM \_ палеттеисчангинг**](wm-paletteischanging.md)
</dt> </dl>

 

 
