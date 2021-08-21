---
title: Сообщение WM_SETFOCUS (Winuser. h)
description: Посылается окну после того, как оно получило фокус клавиатуры.
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- WM_SETFOCUS ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ba202a4f0205a28d294d2d4f54372921205ebb72516f6f26c4042e08d9cfe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757377"
---
# <a name="wm_setfocus-message"></a>\_Сообщение SETFOCUS WM

Посылается окну после того, как оно получило фокус клавиатуры.


```C++
#define WM_SETFOCUS                     0x0007
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер окна, которое потеряло фокус клавиатуры. Этот параметр может принимать значение **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение должно вернуть нуль, если оно обрабатывает это сообщение.

## <a name="remarks"></a>Remarks

Чтобы отобразить курсор, приложение должно вызвать соответствующие функции курсора при получении сообщения **WM \_ SETFOCUS** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**WM \_ киллфокус**](wm-killfocus.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Ввод с клавиатуры](keyboard-input.md)
</dt> </dl>

 

