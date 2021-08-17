---
title: Код уведомления NM_TOOLTIPSCREATED (Коммктрл. h)
description: Сообщает родительскому окну элемента управления, что элемент управления создал элемент управления ToolTip. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 8108f084-212d-4a16-b604-1ec134b1bb43
keywords:
- NM_TOOLTIPSCREATED кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35006c7c7f4cc66cc9ce5e387a362f423db43b6b7aab914d26360dd08d13b37b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410317"
---
# <a name="nm_tooltipscreated-notification-code"></a>\_Код уведомления тултипскреатед (NM)

Сообщает родительскому окну элемента управления, что элемент управления создал элемент управления ToolTip. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтултипскреатед**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если не указано иное, элемент управления игнорирует возвращаемое значение из этого кода уведомления.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





