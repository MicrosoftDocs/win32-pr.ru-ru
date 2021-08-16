---
description: Приложение отправляет \_ сообщение WM мдирефрешмену в окно клиента многодокументного интерфейса (MDI) для обновления меню окна фрейма окна MDI.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: Сообщение WM_MDIREFRESHMENU (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 707059d3cc51703819968f929f9692dbb2422ee3f9fa77e2edb697f12257faf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200070"
---
# <a name="wm_mdirefreshmenu-message"></a>\_Сообщение МДИРЕФРЕШМЕНУ WM

Приложение отправляет сообщение **WM \_ мдирефрешмену** в окно клиента многодокументного интерфейса (MDI) для обновления меню окна фрейма окна MDI.


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется и должен быть равен нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется и должен быть равен нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HMENU**

Если сообщение прошло удачно, возвращаемое значение является маркером меню окна фрейма.

Если сообщение не выполняется, возвращается значение **null**.

## <a name="remarks"></a>Remarks

После отправки этого сообщения приложение должно вызвать функцию [**дравменубар**](/windows/win32/api/winuser/nf-winuser-drawmenubar) для обновления строки меню.

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

[**дравменубар**](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[**WM \_ мдисетмену**](wm-mdisetmenu.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Интерфейс с несколькими документами](multiple-document-interface.md)
</dt> </dl>

 

 
