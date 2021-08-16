---
title: Сообщение WM_INITMENUPOPUP (Winuser. h)
description: WM_INITMENUPOPUP сообщение — отправляется, когда раскрывающийся меню или подменю собирается стать активным. Это позволяет приложению изменять меню до его отображения, не изменяя весь меню.
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_INITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba23607dcb8da7fb282e380e87fe6a2cbb9a26a50850845a5877d036983665f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869603"
---
# <a name="wm_initmenupopup-message"></a>\_Сообщение ИНИТМЕНУПОПУП WM

Посылается, когда раскрывающееся меню или подменю станет активным. Это позволяет приложению изменять меню до его отображения, не изменяя весь меню.


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер раскрывающегося меню или подменю.

</dd> <dt>

*lParam* 
</dt> <dd>

Слово нижнего порядка указывает относительное расположение элемента меню, начинающееся с нуля, которое открывает раскрывающееся меню или подменю.

Слово высокого порядка указывает, является ли раскрывающееся меню окном. Если меню является меню окно, этот параметр имеет **значение true**; в противном случае — **false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ инитмену**](wm-initmenu.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Сочетания клавиш](keyboard-accelerators.md)
</dt> </dl>

 

