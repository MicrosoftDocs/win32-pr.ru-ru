---
title: Код уведомления NM_OUTOFMEMORY (Коммктрл. h)
description: Сообщает родительскому окну элемента управления, что элементу управления не удалось выполнить операцию из-за нехватки памяти. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: d7d80515-ae6c-4817-a698-d486a9d86c4a
keywords:
- NM_OUTOFMEMORY кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_OUTOFMEMORY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1321f88360d168b13d16b36f984d9b797dc094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071184"
---
# <a name="nm_outofmemory-notification-code"></a>\_Код уведомления OUTOFMEMORY (NM)

Сообщает родительскому окну элемента управления, что элементу управления не удалось выполнить операцию из-за нехватки памяти. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_OUTOFMEMORY

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется элементом управления.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





