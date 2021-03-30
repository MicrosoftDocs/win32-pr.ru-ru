---
title: Сообщение WM_INITMENUPOPUP (Winuser. h)
description: Посылается, когда раскрывающееся меню или подменю станет активным. Это позволяет приложению изменять меню до его отображения, не изменяя весь меню.
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
ms.openlocfilehash: e02bf0f9b8e196c27990cc1bc839daed4c92f8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071340"
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

 

