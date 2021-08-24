---
title: Код уведомления NM_RETURN (представление списка) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что элемент управления имеет фокус ввода и что пользователь нажал клавишу ВВОД. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 21a8d308-d747-4020-8925-d982234bcf81
keywords:
- NM_RETURN (представление списка) код уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d230315d09bf56a7a139b5cb089cdcd177bf21128f2407859e1c010abc6d6766
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816374"
---
# <a name="nm_return-list-view-notification-code"></a>\_Код уведомления "NM return" (представление списка)

Сообщает родительскому окну элемента управления "представление списка", что элемент управления имеет фокус ввода и что пользователь нажал клавишу ВВОД. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого уведомления не используется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





