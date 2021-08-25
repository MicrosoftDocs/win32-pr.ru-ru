---
title: Код уведомления BN_HILITE (Winuser. h)
description: Посылается, когда пользователь нажимает кнопку.
ms.assetid: f20ba77e-257c-44ec-a2dd-dbf23cd78d07
keywords:
- BN_HILITE кода уведомления Windows элементы управления
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
ms.openlocfilehash: e864fff01fcce9c7856ab040f66d12e08524c731b43d343a2e878e15e41e801f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827624"
---
# <a name="bn_hilite-notification-code"></a>\_Код уведомления млрд долл хилите

Посылается, когда пользователь нажимает кнопку.

> [!Note]  
> этот код уведомления предоставляется только для обеспечения совместимости с 16-разрядными версиями Windows более ранних, чем 3,0. Для этой задачи приложения должны использовать стиль кнопки [**BS \_ овнердрав**](button-styles.md) и структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .

 

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

## <a name="remarks"></a>Remarks

МЛРД долл \_ хилите совпадает с кодом [ \_ отправленного уведомления млрд долл](bn-pushed.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



 

