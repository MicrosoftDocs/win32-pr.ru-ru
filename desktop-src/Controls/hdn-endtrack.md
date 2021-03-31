---
title: Код уведомления HDN_ENDTRACK (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что пользователь завершил перетаскивание разделителя. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: d9b25871-7bd6-439c-91b8-e8249d9be67d
keywords:
- HDN_ENDTRACK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_ENDTRACK
- HDN_ENDTRACKA
- HDN_ENDTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ab7625690a2de0414f1da391f26f919c1c2617
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071198"
---
# <a name="hdn_endtrack-notification-code"></a>\_Код уведомления ХДН ендтракк

Сообщает родительскому окну элемента управления заголовка, что пользователь завершил перетаскивание разделителя. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_ENDTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую сведения о элементе управления заголовка и элементе, разделитель которого был перетащен.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ХДН \_ ЕНДТРАККВ** (Юникод) и **ХДН \_ ендтракка** (ANSI)<br/>                 |



 

 





