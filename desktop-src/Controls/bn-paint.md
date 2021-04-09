---
title: Код уведомления BN_PAINT (Winuser. h)
description: Посылается, когда кнопка должна быть окрашена.
ms.assetid: 1c742272-60bb-42f1-a9b3-974e9a8540cd
keywords:
- BN_PAINT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BN_PAINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f142c0c502d92933bf7bbc9cb01e3062c8bba96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071130"
---
# <a name="bn_paint-notification-code"></a>\_Код уведомления млрд долл Paint

Посылается, когда кнопка должна быть окрашена.

> [!Note]  
> Этот код уведомления предоставляется только для совместимости с 16-разрядными версиями Windows, предшествующими версии 3,0. Для этой задачи приложения должны использовать стиль кнопки [**BS \_ овнердрав**](button-styles.md) и структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .

 

Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_PAINT

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



 

