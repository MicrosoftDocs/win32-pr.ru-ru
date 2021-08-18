---
title: Код уведомления CBEN_INSERTITEM (Коммктрл. h)
description: Посылается при вставке нового элемента в элемент управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: caf60156-10d2-4cfb-91c4-def6ee99c471
keywords:
- CBEN_INSERTITEM кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- CBEN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a58c1f8b14f4983e2f7e7444a8110f0407220b0c5bc682cfc73f72bee078ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413670"
---
# <a name="cben_insertitem-notification-code"></a>\_Код уведомления кбен INSERTITEM

Посылается при вставке нового элемента в элемент управления. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
CBEN_INSERTITEM

    pNMInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмкомбобоксекс**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) , содержащую сведения о коде уведомления и вставленном элементе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение, обрабатывающее этот код уведомления, должно возвращать ноль.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





