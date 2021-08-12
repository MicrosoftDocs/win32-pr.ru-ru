---
title: Код уведомления BN_UNPUSHED (Winuser. h)
description: Посылается, когда для кнопки задано значение unpushd.
ms.assetid: 1ae7311d-f067-41fe-a117-e0c70d239e9d
keywords:
- BN_UNPUSHED кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- BN_UNPUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 418cb2cacc872fd1e1dfcd86778fddf35939c8e022510a4e0df7e00cf7718bc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674118"
---
# <a name="bn_unpushed-notification-code"></a>МЛРД долл неотправленный \_ код уведомления

Посылается, когда для кнопки задано значение unpushd.

> [!Note]  
> этот код уведомления предоставляется только для обеспечения совместимости с 16-разрядными версиями Windows более ранних, чем 3,0. Для этой задачи приложения должны использовать стиль кнопки [**BS \_ овнердрав**](button-styles.md) и структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .

 

Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_UNPUSHED

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

Маркер кнопки.

</dd> </dl>

## <a name="remarks"></a>Remarks

МЛРД долл \_ UNpushd совпадает с кодом уведомления [ \_ унхилите млрд долл](bn-unhilite.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[МЛРД долл \_ отправлен](bn-pushed.md)
</dt> </dl>

 

