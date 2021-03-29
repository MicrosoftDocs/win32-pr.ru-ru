---
title: Сообщение HDN_ITEMSTATEICONCLICK (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что пользователь щелкнул значок состояния элемента. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: a1969579-3a69-49ff-b06e-4b7450146a92
keywords:
- Элементы управления Windows для HDN_ITEMSTATEICONCLICK сообщений
topic_type:
- apiref
api_name:
- HDN_ITEMSTATEICONCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e5e162b78c829e60494f6e8ff81af3ca97eee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493053"
---
# <a name="hdn_itemstateiconclick-message"></a>\_Сообщение ХДН итемстатеиконкликк

Сообщает родительскому окну элемента управления заголовка, что пользователь щелкнул значок состояния элемента. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_ITEMSTATEICONCLICK

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую дополнительные сведения о значке состояния, в котором была нажата кнопка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





