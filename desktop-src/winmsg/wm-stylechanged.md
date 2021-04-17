---
description: Посылается окну после того, как функция SetWindowLong изменила один или несколько стилей окна.
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: Сообщение WM_STYLECHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5429db06dea95dbbc003e432a2b619c5cf8d056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546471"
---
# <a name="wm_stylechanged-message"></a>\_Сообщение СТИЛЕЧАНЖЕД WM

Посылается окну после того, как функция [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) изменила один или несколько стилей окна.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает, изменились ли стили окна или расширенные стили окна. Этот параметр может принимать одно или несколько следующих значений.



| Значение                                                                                                                                                                                                            | Значение                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**ГВЛ \_ ОПЕРАТОРЕ EXSTYLE**</dt> <dt>-20</dt> </dl> | Изменены стили расширенного окна.<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**ГВЛ \_ СТИЛЬ**</dt> <dt>— 16</dt> </dl>       | Стили окна изменились.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**стилеструкт**](/windows/win32/api/winuser/ns-winuser-stylestruct) , содержащую новые стили для окна. Приложение может проверять стили, но не может их изменять.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Приложение должно вернуть нуль, если оно обрабатывает это сообщение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[**стилеструкт**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**WM \_ стилечангинг**](wm-stylechanging.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
