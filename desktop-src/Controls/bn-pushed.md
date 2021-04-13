---
title: Код уведомления BN_PUSHED (Winuser. h)
description: Посылается, когда для кнопки задано состояние pushd.
ms.assetid: 34000def-189c-4a37-bcef-4ca09a67df00
keywords:
- BN_PUSHED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BN_PUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18a27599c770eb55d889a21956312512ca804cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340505"
---
# <a name="bn_pushed-notification-code"></a>МЛРД долл \_ отправленный код уведомления

Посылается, когда для кнопки задано состояние pushd.

> [!Note]  
> Этот код уведомления предоставляется только для совместимости с 16-разрядными версиями Windows, предшествующими версии 3,0. Для этой задачи приложения должны использовать стиль кнопки [**BS \_ овнердрав**](button-styles.md) и структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .

 

Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_PUSHED

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

## <a name="remarks"></a>Комментарии

\_Отправленный млрд долл совпадает с кодом уведомления [ \_ хилите млрд долл](bn-hilite.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**МЛРД долл не отправлено \_**](bn-unpushed.md)
</dt> </dl>

 

