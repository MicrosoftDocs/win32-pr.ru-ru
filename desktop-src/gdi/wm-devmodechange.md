---
description: Сообщение WM \_ девмодечанже отправляется всем окнам верхнего уровня каждый раз, когда пользователь изменяет параметры режима устройства.
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: Сообщение WM_DEVMODECHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985805"
---
# <a name="wm_devmodechange-message"></a>\_Сообщение ДЕВМОДЕЧАНЖЕ WM

Сообщение **WM \_ девмодечанже** отправляется всем окнам верхнего уровня каждый раз, когда пользователь изменяет параметры режима устройства.

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

*HWND* 
</dt> <dd>

Дескриптор окна.

</dd> <dt>

*Uiacp* 
</dt> <dd>

WM \_ девмодечанже

</dd> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на строку, указывающую имя устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение должно вернуть нуль, если оно обрабатывает это сообщение.

## <a name="remarks"></a>Примечания

Это сообщение не может быть отправлено непосредственно в окно. Чтобы отправить сообщение **WM \_ девмодечанже** всем окнам верхнего уровня, используйте функцию [**функции sendmessagetimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) с параметром *HWND* , имеющим значение HWND \_ Broadcast.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о контекстах устройств](device-contexts.md)
</dt> <dt>

[Сообщения контекста устройства](device-context-messages.md)
</dt> </dl>

 

 
