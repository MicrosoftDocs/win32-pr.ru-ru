---
title: Код уведомления CBN_SELENDCANCEL (Winuser. h)
description: Посылается, когда пользователь выбирает элемент, а затем выбирает другой элемент управления или закрывает диалоговое окно. Указывает, что первоначальный выбор пользователя должен игнорироваться. Родительское окно поля со списком получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: ac8d6d9f-4455-42d6-b0f1-5aaa55b8ee42
keywords:
- CBN_SELENDCANCEL кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- CBN_SELENDCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 869168bfb970df9afc6399e6b1ec40e02b9ccdeaa2f2fef93fcbd86c16e9c6d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314404"
---
# <a name="cbn_selendcancel-notification-code"></a>\_Код уведомления КБН селендканцел

Посылается, когда пользователь выбирает элемент, а затем выбирает другой элемент управления или закрывает диалоговое окно. Указывает, что первоначальный выбор пользователя должен игнорироваться. Родительское окно поля со списком получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_SELENDCANCEL

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

## <a name="remarks"></a>Remarks

В поле со списком с [**\_ простым**](combo-box-styles.md) стилем CBS \_ код уведомления КБН селендканцел не отправляется. Код уведомления [КБН \_ селендок](cbn-selendok.md) отправляется непосредственно перед каждым кодом уведомления [КБН \_ селчанже](cbn-selchange.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[КБН \_ селчанже](cbn-selchange.md)
</dt> <dt>

[КБН \_ селендок](cbn-selendok.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_команда WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

