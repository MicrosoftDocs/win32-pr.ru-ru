---
title: Код уведомления NM_SETFOCUS (Дата и время) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "Выбор даты и времени", что элемент управления получил фокус ввода. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 61c62fb2-bc79-404b-9958-7208d1c781fa
keywords:
- NM_SETFOCUS (Дата и время) коды уведомлений элементы управления Windows
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba80ea119056c131f1dd94cdf1f39a84371b7052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489960"
---
# <a name="nm_setfocus-date-time-notification-code"></a>\_Код уведомления для NM (Дата и время)

Сообщает родительскому окну элемента управления "Выбор даты и времени", что элемент управления получил фокус ввода. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





