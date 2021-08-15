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
ms.openlocfilehash: 0d97f629b5d4b0c245606b36efea9ebcb230c4c9fd14d837e18949880a7e7e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971813"
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

## <a name="remarks"></a>Remarks

Сообщение **WM \_ MENUCOMMAND** предоставляет в меню указатель, позволяющий получить доступ к данным меню в структуре [**менуинфо**](/windows/win32/api/winuser/ns-winuser-menuinfo) , а также предоставляет индекс выбранного элемента, который обычно требуется приложениям. В отличие от этого [**, \_ командное сообщение WM**](wm-command.md) предоставляет идентификатор пункта меню.

Сообщение **WM \_ MENUCOMMAND** отправляется только для меню, определенных флагом **MNS \_ нотифибипос** , установленным в элементе **двстиле** структуры [**менуинфо**](/windows/win32/api/winuser/ns-winuser-menuinfo) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о меню](menus.md)
</dt> </dl>

 

 





