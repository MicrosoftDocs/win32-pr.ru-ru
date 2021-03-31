---
title: Код уведомления TBN_ENDADJUST (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что пользователь остановил настройку панели инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 9a7496ec-787d-4571-8eca-50d60383519b
keywords:
- TBN_ENDADJUST кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_ENDADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ec420c535a207f02d12e17901efab1c18a11bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071514"
---
# <a name="tbn_endadjust-notification-code"></a>\_Код уведомления ТБН ендаджуст

Сообщает родительскому окну панели инструментов, что пользователь остановил настройку панели инструментов. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_ENDADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую сведения о коде уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





