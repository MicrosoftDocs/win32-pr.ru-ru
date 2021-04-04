---
title: Код уведомления NM_KILLFOCUS (в виде дерева) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления древовидного представления о том, что элемент управления потерял фокус ввода. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: f6646a39-6480-4417-9c1c-ffd2417ca7dd
keywords:
- Элементы управления Windows для кода уведомления NM_KILLFOCUS (представление в виде дерева)
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7123f47469a02fcec92805a27d81e173c5e1d10a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988190"
---
# <a name="nm_killfocus-tree-view-notification-code"></a>\_Код уведомления NM киллфокус (в виде дерева)

Сообщает родительскому окну элемента управления древовидного представления о том, что элемент управления потерял фокус ввода. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_KILLFOCUS

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



 

 





