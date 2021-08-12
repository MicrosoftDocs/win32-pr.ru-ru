---
title: Код уведомления BCN_DROPDOWN (Winuser. h)
description: Посылается, когда пользователь щелкает стрелку раскрывающегося списка на кнопке. Родительское окно элемента управления получает этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- BCN_DROPDOWN кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbacf22cdabbac7c5d2932c604fab634dbc185207acda8cee311d434478e5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674977"
---
# <a name="bcn_dropdown-notification-code"></a>\_Код уведомления для раскрывающегося списка BCN

Посылается, когда пользователь щелкает стрелку раскрывающегося списка на кнопке. Родительское окно элемента управления получает этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмбкдропдовн**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) . Для элемента **ркбуттон** задано описание раскрывающегося области.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Получатель уведомлений выполняет приведение **lParam** для получения структуры [**нмбкдропдовн**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) . **WParam** содержит идентификатор элемента управления, который отправляет это сообщение. Элемент управления "Кнопка" должен иметь стиль кнопки раскрывающегося списка.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



 

 





