---
description: Отправляются в окно, размер, расположение или место в Z-порядке которого собирается измениться в результате вызова функции SetWindowPos или другой функции управления окнами.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: Сообщение WM_WINDOWPOSCHANGING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015a31aac31d38506d1798f83c8dd7f9aa646f85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816305"
---
# <a name="wm_windowposchanging-message"></a>\_Сообщение ВИНДОВПОСЧАНГИНГ WM

Отправляются в окно, размер, расположение или место в Z-порядке которого собирается измениться в результате вызова функции [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) или другой функции управления окнами.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WINDOWPOSCHANGING            0x0046
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

Для окна с стилем [**WS \_ OVERLAPPED**](window-styles.md) или **WS \_ Сиккфраме** функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) отправляет сообщение [**WM \_ жетминмаксинфо**](wm-getminmaxinfo.md) в окно. Это делается для проверки нового размера и расположения окна, а также для применения стилей клиента [CS \_ БИТЕАЛИГНКЛИЕНТ](about-window-classes.md) и CS \_ битеалигнвиндов. Если не передать сообщение **WM \_ виндовпосчангинг** в функцию **дефвиндовпрок** , приложение может переопределить эти значения по умолчанию.

Во время обработки этого сообщения изменение любого значения в [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) влияет на новый размер, позицию или место в Z-порядке окна. Приложение может препятствовать изменениям в окне, установив или сняв соответствующие биты в элементе **flags** элемента **WINDOWPOS**.

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

[**WM \_ жетминмаксинфо**](wm-getminmaxinfo.md)
</dt> <dt>

[**\_Перемещение WM**](wm-move.md)
</dt> <dt>

[**\_Размер WM**](wm-size.md)
</dt> <dt>

[**WM \_ виндовпосчанжед**](wm-windowposchanged.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
