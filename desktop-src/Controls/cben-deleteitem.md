---
title: Код уведомления CBEN_DELETEITEM (Коммктрл. h)
description: Отправляется при удалении элемента. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 8b0d03ff-57fa-44dc-ab3e-05089b876e3c
keywords:
- CBEN_DELETEITEM кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBEN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c7ca7329898c9dd0c6bba76cba9d3524b017e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892549"
---
# <a name="cben_deleteitem-notification-code"></a>\_Код уведомления кбен DELETEITEM

Отправляется при удалении элемента. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
CBEN_DELETEITEM

    pCBEx = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмкомбобоксекс**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) , содержащую сведения о коде уведомления и удаленном элементе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение, обрабатывающее этот код уведомления, должно возвращать ноль.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





