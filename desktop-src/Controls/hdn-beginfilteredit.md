---
title: Код уведомления HDN_BEGINFILTEREDIT (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что началось изменение фильтра. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 93964453-bb94-4127-8ed4-41acb226b8e2
keywords:
- HDN_BEGINFILTEREDIT кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- HDN_BEGINFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db45027b1136e37d39caea2cfcd3fb4434362a73ab63c47f72da0b6c8fadaeea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006093"
---
# <a name="hdn_beginfilteredit-notification-code"></a>\_Код уведомления ХДН бегинфилтередит

Сообщает родительскому окну элемента управления заголовка, что началось изменение фильтра. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_BEGINFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую дополнительные сведения о редактируемом фильтре.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





