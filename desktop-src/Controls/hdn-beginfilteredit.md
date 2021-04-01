---
title: Код уведомления HDN_BEGINFILTEREDIT (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что началось изменение фильтра. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 93964453-bb94-4127-8ed4-41acb226b8e2
keywords:
- HDN_BEGINFILTEREDIT кода уведомления элементы управления Windows
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
ms.openlocfilehash: 0527427752b5621e626add17d61e60a675958f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989457"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





