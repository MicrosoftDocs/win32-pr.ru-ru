---
title: Код уведомления TBN_QUERYDELETE (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, можно ли удалить кнопку с панели инструментов, пока пользователь настраивает панель инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- TBN_QUERYDELETE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a416545ecf7ad8562c1327160d683a109eccb3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533746"
---
# <a name="tbn_querydelete-notification-code"></a>\_Код уведомления ТБН куериделете

Сообщает родительскому окну панели инструментов, можно ли удалить кнопку с панели инструментов, пока пользователь настраивает панель инструментов. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтулбар**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . Член **iItem** содержит отсчитываемый от нуля индекс удаляемой кнопки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , чтобы разрешить удаление кнопки, или **значение false** , чтобы предотвратить удаление кнопки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





