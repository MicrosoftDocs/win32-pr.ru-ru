---
title: Код уведомления DTN_DATETIMECHANGE (Коммктрл. h)
description: Отправляется элементом управления "Выбор даты и времени" каждый раз, когда происходит изменение. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- DTN_DATETIMECHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40072a54732a0a3575e3153ddb901ca1df291b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892290"
---
# <a name="dtn_datetimechange-notification-code"></a>\_Код уведомления ДТН датетимечанже

Отправляется элементом управления "Выбор даты и времени" каждый раз, когда происходит изменение. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмдатетимечанже**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) , содержащую сведения об изменении, которое произошло в элементе управления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Владелец элемента управления должен возвращать ноль.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





