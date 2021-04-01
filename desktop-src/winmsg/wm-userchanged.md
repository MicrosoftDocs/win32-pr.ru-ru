---
description: Посылается всем окнам после входа или отключения пользователем. Когда пользователь входит в систему или выключается, система обновляет пользовательские параметры. Система отправляет это сообщение сразу после обновления параметров.
title: Сообщение WM_USERCHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_userchanged.htm
api_name:
- WM_USERCHANGED
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14458bdafa0bbf4421c67db8102491db4e1fe6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999416"
---
# <a name="wm_userchanged-message"></a>\_Сообщение УСЕРЧАНЖЕД WM

Посылается всем окнам после входа или отключения пользователем. Когда пользователь входит в систему или выключается, система обновляет пользовательские параметры. Система отправляет это сообщение сразу после обновления параметров.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> [!Note]  
> Это сообщение не поддерживается в Windows Vista.

 


```C++
#define WM_USERCHANGED                  0x0054
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

Тип: **lResult**

Приложение должно вернуть нуль, если оно обрабатывает это сообщение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                                              |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обзор Windows](windows.md)
</dt> </dl>

 

 
