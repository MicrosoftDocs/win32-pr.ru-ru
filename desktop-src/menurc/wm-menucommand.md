---
title: Сообщение WM_MENUCOMMAND (Winuser. h)
description: Посылается, когда пользователь делает выбор из меню.
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- WM_MENUCOMMAND меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_MENUCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13288c49327b536db6ebef8a41526facd3fb2d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416153"
---
# <a name="wm_menucommand-message"></a>\_Сообщение MENUCOMMAND WM

Посылается, когда пользователь делает выбор из меню.


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс выбранного элемента.

</dd> <dt>

*lParam* 
</dt> <dd>

Маркер меню для выбранного элемента.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Сообщение **WM \_ MENUCOMMAND** предоставляет в меню указатель, позволяющий получить доступ к данным меню в структуре [**менуинфо**](/windows/win32/api/winuser/ns-winuser-menuinfo) , а также предоставляет индекс выбранного элемента, который обычно требуется приложениям. В отличие от этого [**, \_ командное сообщение WM**](wm-command.md) предоставляет идентификатор пункта меню.

Сообщение **WM \_ MENUCOMMAND** отправляется только для меню, определенных флагом **MNS \_ нотифибипос** , установленным в элементе **двстиле** структуры [**менуинфо**](/windows/win32/api/winuser/ns-winuser-menuinfo) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о меню](menus.md)
</dt> </dl>

 

 





