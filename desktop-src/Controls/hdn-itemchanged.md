---
title: Код уведомления HDN_ITEMCHANGED (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что изменились атрибуты элемента заголовка. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ab707010-8ed2-4575-8233-8a1f5656e498
keywords:
- HDN_ITEMCHANGED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGED
- HDN_ITEMCHANGEDA
- HDN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67157ff7f775c124236b7a77a1051b7644758c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071196"
---
# <a name="hdn_itemchanged-notification-code"></a>\_Код уведомления ХДН итемчанжед

Сообщает родительскому окну элемента управления заголовка, что изменились атрибуты элемента заголовка. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_ITEMCHANGED

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую сведения о элементе управления "заголовок", включая атрибуты, которые были изменены.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ХДН \_ ИТЕМЧАНЖЕДВ** (Юникод) и **ХДН \_ итемчанжеда** (ANSI)<br/>           |



 

 





