---
title: Код уведомления NM_CLICK (TAB) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "Вкладка", что пользователь щелкнул левой кнопкой мыши в элементе управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b892aded-d6b8-4a04-bfdd-0153b65eaccc
keywords:
- NM_CLICK (вкладка) код уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab8291ff1c003850c8fc89859eac3f09cda664cd37e04f43c7e353b9051017a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078938"
---
# <a name="nm_click-tab-notification-code"></a>\_Код уведомления Click (TAB) NM

Сообщает родительскому окну элемента управления "Вкладка", что пользователь щелкнул левой кнопкой мыши в элементе управления. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CLICK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется элементом управления "Вкладка".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





