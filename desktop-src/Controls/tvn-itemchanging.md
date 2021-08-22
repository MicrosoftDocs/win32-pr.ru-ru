---
title: Код уведомления TVN_ITEMCHANGING (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления о том, что необходимо изменить атрибуты элементов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- TVN_ITEMCHANGING кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85416e22562720455da3e3c03c95b3cee25b5f0f7420a31250b244f47dab0caa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957873"
---
# <a name="tvn_itemchanging-notification-code"></a>\_Код уведомления ТВН итемчангинг

Сообщает родительскому окну элемента управления иерархического представления о том, что необходимо изменить атрибуты элементов. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтвитемчанже**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) , описывающую изменяемый элемент. Для элемента **учанжед** задано состояние твиф \_ .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение false** , чтобы принять изменение, или **значение true** , чтобы предотвратить изменение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТВН \_ ИТЕМЧАНГИНГВ** (Юникод) и **ТВН \_ итемчангинга** (ANSI)<br/>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ТВН \_ итемчанжед](tvn-itemchanged.md)
</dt> </dl>

 

 





