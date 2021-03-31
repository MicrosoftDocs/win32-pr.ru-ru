---
title: Код уведомления RBN_LAYOUTCHANGED (Коммктрл. h)
description: Посылается элементом управления "Главная панель", когда пользователь изменяет макет полос элемента управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: e937d151-bfaa-41c0-a134-e70ff2f75d07
keywords:
- RBN_LAYOUTCHANGED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_LAYOUTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1fc14578435fc786ecc5496cec96eb2224b4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136626"
---
# <a name="rbn_layoutchanged-notification-code"></a>\_Код уведомления РБН лайаутчанжед

Посылается элементом управления "Главная панель", когда пользователь изменяет макет полос элемента управления. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_LAYOUTCHANGED 

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого уведомления не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





