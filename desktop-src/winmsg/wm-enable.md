---
description: Посылается, когда приложение изменяет включенное состояние окна.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: Сообщение WM_ENABLE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc83b84cbbf8e0c0145ef7d2730179cab54a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693280"
---
# <a name="wm_enable-message"></a>\_Сообщение о включении WM

Посылается, когда приложение изменяет включенное состояние окна. Он отправляется в окно, состояние которого разрешено изменить. Это сообщение отправляется перед возвратом функции [**енаблевиндов**](/windows/win32/api/winuser/nf-winuser-enablewindow) , но после изменения включенного состояния (бит [**\_ отключенного типа WS**](window-styles.md) ) окна.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает, было ли окно включено или отключено. Этот параметр имеет **значение true** , если окно было включено, или **значение false** , если окно было отключено.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

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

[**енаблевиндов**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
