---
title: Код уведомления LVN_ODSTATECHANGED (Коммктрл. h)
description: Отправляется элементом управления "представление списка" при изменении состояния элемента или диапазона элементов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: a3aafda5-a3ec-4f84-8153-8d34097e04f1
keywords:
- LVN_ODSTATECHANGED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_ODSTATECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86de2f5e01e15d0a97c49f451914aac5b74b27e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803064"
---
# <a name="lvn_odstatechanged-notification-code"></a>\_Код уведомления ЛВН одстатечанжед

Отправляется элементом управления "представление списка" при изменении состояния элемента или диапазона элементов. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_ODSTATECHANGED

    lpStateChange = (LPNMLVODSTATECHANGE) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмлводстатечанже**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) , которая содержит сведения об измененном элементе или элементах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение, получающее этот код уведомления, должно возвращать ноль.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





