---
title: Код уведомления BN_HILITE (Winuser. h)
description: Посылается, когда пользователь нажимает кнопку.
ms.assetid: f20ba77e-257c-44ec-a2dd-dbf23cd78d07
keywords:
- BN_HILITE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BN_HILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5567837c9883c52d99f0ca68d450f7b3538f233b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988376"
---
# <a name="bn_hilite-notification-code"></a>\_Код уведомления млрд долл хилите

Посылается, когда пользователь нажимает кнопку.

> [!Note]  
> Этот код уведомления предоставляется только для совместимости с 16-разрядными версиями Windows, предшествующими версии 3,0. Для этой задачи приложения должны использовать стиль кнопки [**BS \_ овнердрав**](button-styles.md) и структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .

 

Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_HILITE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления кнопки. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.

</dd> <dt>

*lParam* 
</dt> <dd>

Маркер для кнопки.

</dd> </dl>

## <a name="remarks"></a>Комментарии

МЛРД долл \_ хилите совпадает с кодом [ \_ отправленного уведомления млрд долл](bn-pushed.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



 

