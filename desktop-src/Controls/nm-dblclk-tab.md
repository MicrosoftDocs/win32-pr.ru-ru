---
title: Код уведомления NM_DBLCLK (TAB) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "Вкладка", что пользователь дважды щелкнул левую кнопку мыши в элементе управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: fd99f195-ceac-47e8-b584-d814b055fa21
keywords:
- Элементы управления Windows для кода уведомления NM_DBLCLK (TAB)
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c8171696e57684be55e6e42792666ae206d890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137082"
---
# <a name="nm_dblclk-tab-notification-code"></a>\_Код уведомления "NM дблклк (вкладка)"

Сообщает родительскому окну элемента управления "Вкладка", что пользователь дважды щелкнул левую кнопку мыши в элементе управления. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение, чтобы не разрешать обработку по умолчанию, или нуль, чтобы разрешить обработку по умолчанию.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





