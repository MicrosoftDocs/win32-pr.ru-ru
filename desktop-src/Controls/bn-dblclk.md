---
title: Код уведомления BN_DBLCLK (Winuser. h)
description: Посылается, когда пользователь дважды нажимает кнопку.
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- BN_DBLCLK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04c6bf52e213056d85d3a6d038bedb83754a27e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071389"
---
# <a name="bn_dblclk-notification-code"></a>\_Код уведомления млрд долл дблклк

Посылается, когда пользователь дважды нажимает кнопку. Этот код уведомления отправляется автоматически для кнопок [**BS \_ усербуттон**](button-styles.md), [**BS \_**](button-styles.md)и [**BS \_ овнердрав**](button-styles.md) . Другие типы кнопок отправляют млрд долл \_ дблклк только в том случае, если они имеют стиль " [**BS \_**](button-styles.md) ".

Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_DBLCLK

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

МЛРД долл \_ дблклк совпадает с кодом уведомления [млрд долл \_ даублекликкед](bn-doubleclicked.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[\_щелчок млрд долл](bn-clicked.md)
</dt> <dt>

[МЛРД долл \_ даублекликкед](bn-doubleclicked.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**\_команда WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

