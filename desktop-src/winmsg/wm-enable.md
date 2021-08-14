---
description: Посылается, когда приложение изменяет включенное состояние окна.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: Сообщение WM_ENABLE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e01477de7cf1b9052bba752929210a1bc7553445f81f971aec67d7b510653a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200485"
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

[**енаблевиндов**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
