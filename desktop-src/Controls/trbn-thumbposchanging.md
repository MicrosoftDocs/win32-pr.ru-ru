---
title: Код уведомления TRBN_THUMBPOSCHANGING (Коммктрл. h)
description: Уведомляет об изменении расположения бегунка на TrackBar. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- TRBN_THUMBPOSCHANGING кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23722b68f28a5157948ac6277858193366242fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000165"
---
# <a name="trbn_thumbposchanging-notification-code"></a>\_Код уведомления трбн сумбпосчангинг

Уведомляет об изменении расположения бегунка на TrackBar. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтрбсумбпосчангинг**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) . Вызывающий объект отвечает за выделение этой структуры и задание ее членов, включая элементы содержащейся в ней структуры [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , чтобы предотвратить перемещение бегунка в указанную точку.

## <a name="remarks"></a>Комментарии

Отправьте это уведомление клиентам, которые не прослушивают сообщения [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





