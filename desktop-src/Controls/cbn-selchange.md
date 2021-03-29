---
title: Код уведомления CBN_SELCHANGE (Winuser. h)
description: Посылается, когда пользователь изменяет текущее выделение в списке поля со списком.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- CBN_SELCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e921b7856780763923a448e42de072476cc02f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989377"
---
# <a name="cbn_selchange-notification-code"></a>\_Код уведомления КБН селчанже

Посылается, когда пользователь изменяет текущее выделение в списке поля со списком. Пользователь может изменить выбор, щелкнув в списке или используя клавиши со стрелками. Родительское окно поля со списком получает этот код уведомления в виде [**\_ командного сообщения WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления поля со списком. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.

</dd> <dt>

*lParam* 
</dt> <dd>

Обработайте с полем со списком.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы получить индекс текущего выделения, отправьте в элемент управления сообщение с параметром [**CB \_**](cb-getcursel.md) .

\_Код уведомления КБН селчанже не отправляется, если текущий выбор задается с помощью [**сообщения \_ сеткурсел CB**](cb-setcursel.md) .

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

[КБН \_ крупный план](cbn-closeup.md)
</dt> <dt>

[КБН \_ дблклк](cbn-dblclk.md)
</dt> <dt>

[**CB \_**](cb-getcursel.md)
</dt> <dt>

[**\_СЕТКУРСЕЛ CB**](cb-setcursel.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_команда WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

