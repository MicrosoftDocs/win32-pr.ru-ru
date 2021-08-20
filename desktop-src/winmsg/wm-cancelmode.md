---
description: Отправляется для отмены определенных режимов, таких как захват мыши.
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: Сообщение WM_CANCELMODE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae26cef4919ed93bb2a1c60376ab450560cd2142cef7b3040032f791c45ab09f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849303"
---
# <a name="wm_cancelmode-message"></a>\_Сообщение КАНЦЕЛМОДЕ WM

Отправляется для отмены определенных режимов, таких как захват мыши. Например, система отправляет это сообщение в активное окно, когда отображается диалоговое окно или поле сообщения. Некоторые функции также отправляют это сообщение явно в указанное окно, независимо от того, является ли оно активным. Например, функция [**енаблевиндов**](/windows/win32/api/winuser/nf-winuser-enablewindow) отправляет это сообщение при отключении указанного окна.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CANCELMODE                   0x001F
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

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Remarks

При отправке сообщения **WM \_ Канцелмоде** функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) отменяет внутреннюю обработку стандартного ввода полосы прокрутки, отменяет внутреннюю обработку меню и освобождает захват мыши.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**енаблевиндов**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[**релеасекаптуре**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
