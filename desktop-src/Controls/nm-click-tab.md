---
title: Код уведомления NM_CLICK (TAB) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "Вкладка", что пользователь щелкнул левой кнопкой мыши в элементе управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b892aded-d6b8-4a04-bfdd-0153b65eaccc
keywords:
- Элементы управления Windows для кода уведомления NM_CLICK (TAB)
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
ms.openlocfilehash: e451a7a87d1b02140f59797c7485b8eb250dad13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137871"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





