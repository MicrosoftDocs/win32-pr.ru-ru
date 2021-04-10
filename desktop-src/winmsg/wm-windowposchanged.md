---
description: Отправляются в окно, размер, расположение или место в Z-порядке изменились в результате вызова функции SetWindowPos или другой функции управления окнами.
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: Сообщение WM_WINDOWPOSCHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bda353a1c7546727818a8a3975696000da0e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144713"
---
# <a name="wm_windowposchanged-message"></a>\_Сообщение ВИНДОВПОСЧАНЖЕД WM

Отправляются в окно, размер, расположение или место в Z-порядке изменились в результате вызова функции [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) или другой функции управления окнами.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WINDOWPOSCHANGED             0x0047
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) , которая содержит сведения о новом размере и позиции окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Комментарии

По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) отправляет в окно [**сообщения \_ размером WM**](wm-size.md) и [**WM \_**](wm-move.md) . Сообщения **WM \_ size** и **WM \_ Move** не отправляются, если приложение обрабатывает сообщение **WM \_ виндовпосчанжед** без вызова **дефвиндовпрок**. Более эффективно выполнять любые операции перемещения или изменения размера во время сообщения **\_ виндовпосчанжед WM** без вызова **дефвиндовпрок**.

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

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**енддефервиндовпос**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**\_Перемещение WM**](wm-move.md)
</dt> <dt>

[**\_Размер WM**](wm-size.md)
</dt> <dt>

[**WM \_ виндовпосчангинг**](wm-windowposchanging.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
