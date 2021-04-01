---
description: Отправляется в окно, когда функция SetWindowLong собирается изменить один или несколько стилей окна.
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: Сообщение WM_STYLECHANGING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e587797404bb361a443a60750d4de5ea6a8924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909852"
---
# <a name="wm_stylechanging-message"></a>\_Сообщение СТИЛЕЧАНГИНГ WM

Отправляется в окно, когда функция [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) собирается изменить один или несколько стилей окна.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает, изменяются ли стили окна или расширенные стили окна. Этот параметр может принимать одно или несколько следующих значений.



| Значение                                                                                                                                                                                                            | Значение                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**ГВЛ \_ ОПЕРАТОРЕ EXSTYLE**</dt> <dt>-20</dt> </dl> | Изменяются расширенные стили окна.<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**ГВЛ \_ СТИЛЬ**</dt> <dt>— 16</dt> </dl>       | Стили окна меняются.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**стилеструкт**](/windows/win32/api/winuser/ns-winuser-stylestruct) , которая содержит предложенные новые стили для окна. Приложение может проверить стили и при необходимости изменить их.

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

[**стилеструкт**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**WM \_ стилечанжед**](wm-stylechanged.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
