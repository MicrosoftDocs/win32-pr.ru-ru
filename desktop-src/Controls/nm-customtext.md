---
title: Код уведомления NM_CUSTOMTEXT (Коммктрл. h)
description: Сообщает родительскому окну элемента управления о пользовательских операциях с текстом. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b4bde648-3479-4fac-ad32-b34c7272c1fc
keywords:
- NM_CUSTOMTEXT кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- NM_CUSTOMTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512ccb6cd94ce680b9832c342696941d98c0e6543c319caeb89eb409de1fe73c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018881"
---
# <a name="nm_customtext-notification-code"></a>\_Код уведомления кустомтекст (NM)

Сообщает родительскому окну элемента управления о пользовательских операциях с текстом. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CUSTOMTEXT

    lpnmct = (NMCUSTOMTEXT) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмкустомтекст**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется элементом управления.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





