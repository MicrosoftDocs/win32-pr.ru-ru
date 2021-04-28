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
ms.openlocfilehash: 6d850547d57596dd36b36b941d1782c2aee1f5b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092522"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылка**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ инитмену**](wm-initmenu.md)
</dt> <dt>

**Основные понятия**
</dt> <dt>

[Сочетания клавиш](keyboard-accelerators.md)
</dt> </dl>

 

