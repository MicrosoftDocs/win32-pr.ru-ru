---
title: Сообщение HDN_ITEMSTATEICONCLICK (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что пользователь щелкнул значок состояния элемента. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: a1969579-3a69-49ff-b06e-4b7450146a92
keywords:
- элементы управления Windows сообщений HDN_ITEMSTATEICONCLICK
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
ms.openlocfilehash: cba2e475ec3037ab00c379cf0c9ea371d5a336b80458c68e974a7122d9a2427a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435254"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





