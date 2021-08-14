---
description: Посылается окну после того, как функция SetWindowLong изменила один или несколько стилей окна.
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: Сообщение WM_STYLECHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc84d3df087cb8667367830998675903a83f633eba4797e64125269d0c937c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705944"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



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

 

 
