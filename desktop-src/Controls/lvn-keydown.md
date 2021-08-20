---
title: Код уведомления LVN_KEYDOWN (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что была нажата клавиша. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 3aa3d165-7227-41c4-8bc2-3e51a0f52ee3
keywords:
- LVN_KEYDOWN кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- LVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ebca4f615322e18cc4f86b0962414f6fe1040f486fce51ad4ec060dfebcbe38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019062"
---
# <a name="lvn_keydown-notification-code"></a>\_Код уведомления ЛВН KeyDown

Сообщает родительскому окну элемента управления "представление списка", что была нажата клавиша. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_KEYDOWN

    pnkd = (LPNMLVKEYDOWN) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмлвкэйдовн**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





