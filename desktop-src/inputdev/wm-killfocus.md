---
title: Сообщение WM_KILLFOCUS (Winuser. h)
description: Посылается окну непосредственно перед тем, как оно теряет фокус клавиатуры.
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- WM_KILLFOCUS ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644ea7d82a2ae3f316985a882c284d77f3869a75341142d4372b612d66ada1ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757458"
---
# <a name="wm_killfocus-message"></a>\_Сообщение КИЛЛФОКУС WM

Посылается окну непосредственно перед тем, как оно теряет фокус клавиатуры.


```C++
#define WM_KILLFOCUS                    0x0008
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер окна, получающего фокус клавиатуры. Этот параметр может принимать значение **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение должно вернуть нуль, если оно обрабатывает это сообщение.

## <a name="remarks"></a>Remarks

Если приложение отображает курсор, в этот момент курсор должен быть разрушен.

При обработке этого сообщения не следует выполнять вызовы функций, которые отображают или активируют окно. Это приводит к тому, что поток получает управление и может привести к тому, что приложение перестает отвечать на сообщения. Дополнительные сведения см. в разделе [взаимоблокировки сообщений](/windows/desktop/winmsg/about-messages-and-message-queues).

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

[**WM \_ SETFOCUS**](wm-setfocus.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Ввод с клавиатуры](keyboard-input.md)
</dt> </dl>

 

