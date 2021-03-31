---
title: Код уведомления LVN_BEGINDRAG (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что инициируется операция перетаскивания, включающая левую кнопку мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 2b9bbff8-f5f7-47ac-b662-a327ff49caf7
keywords:
- LVN_BEGINDRAG кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69166cd38242db915f70772b5dfbd3bab6ba56df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071188"
---
# <a name="lvn_begindrag-notification-code"></a>\_Код уведомления ЛВН бегиндраг

Сообщает родительскому окну элемента управления "представление списка", что инициируется операция перетаскивания, включающая левую кнопку мыши. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_BEGINDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Элемент **Член iItem** определяет перетаскиваемый элемент, а остальные элементы равны нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





