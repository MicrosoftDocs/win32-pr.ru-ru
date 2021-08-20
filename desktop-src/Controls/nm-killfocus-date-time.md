---
title: Код уведомления NM_KILLFOCUS (Дата и время) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "Выбор даты и времени", что элемент управления потерял фокус ввода. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 33d6b88b-9608-4227-a822-1dc7a77d3a3f
keywords:
- NM_KILLFOCUS (дата и время) код уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0147fd5d79998024df8c12d9be4a9a71ee3c1751a3f31d21d090ea2c7e9a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018842"
---
# <a name="nm_killfocus-date-time-notification-code"></a>\_Код уведомления NM киллфокус (Дата и время)

Сообщает родительскому окну элемента управления "Выбор даты и времени", что элемент управления потерял фокус ввода. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Адрес структуры [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащей дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





