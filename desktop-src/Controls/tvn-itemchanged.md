---
title: Код уведомления TVN_ITEMCHANGED (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления о том, что атрибуты элемента изменились. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- TVN_ITEMCHANGED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d58501d02cc2058ac803c949cc7118d7f146a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892005"
---
# <a name="tvn_itemchanged-notification-code"></a>\_Код уведомления ТВН итемчанжед

Сообщает родительскому окну элемента управления иерархического представления о том, что атрибуты элемента изменились. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтвитемчанже**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) , описывающую измененный элемент. Для элемента **учанжед** задано состояние твиф \_ .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение false** , чтобы принять изменение, или **значение true** , чтобы предотвратить изменение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТВН \_ ИТЕМЧАНЖЕДВ** (Юникод) и **ТВН \_ итемчанжеда** (ANSI)<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ТВН \_ итемчангинг](tvn-itemchanging.md)
</dt> </dl>

 

 





