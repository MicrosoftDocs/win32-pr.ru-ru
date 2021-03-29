---
title: Код уведомления NM_RELEASEDCAPTURE (представление списка) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что элемент управления освобождает захват мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: a43879d9-1465-4c25-936f-cda9b8b8b465
keywords:
- Элементы управления Windows для кода уведомления NM_RELEASEDCAPTURE (представление списка)
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f42af9dddf6f9864251eff5e2f5a6aebbfa9cd20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492141"
---
# <a name="nm_releasedcapture-list-view-notification-code"></a>\_Код уведомления NM релеаседкаптуре (представление списка)

Сообщает родительскому окну элемента управления "представление списка", что элемент управления освобождает захват мыши. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Элемент управления игнорирует возвращаемое значение из этого кода уведомления.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





