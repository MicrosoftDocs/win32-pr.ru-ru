---
title: Код уведомления NM_RELEASEDCAPTURE (представление списка) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что элемент управления освобождает захват мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: a43879d9-1465-4c25-936f-cda9b8b8b465
keywords:
- NM_RELEASEDCAPTURE (представление списка) код уведомления Windows элементы управления
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
ms.openlocfilehash: d75717f937c94b4ba19cd78490b0cf9254394dfc7a6766352a9a535ee7405275
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319074"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





