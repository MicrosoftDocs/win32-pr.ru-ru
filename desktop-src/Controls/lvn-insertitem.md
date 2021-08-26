---
title: Код уведомления LVN_INSERTITEM (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что был вставлен новый элемент. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 8d368fb2-e4fc-4dc4-a89e-872ba1278b75
keywords:
- LVN_INSERTITEM кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- LVN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1c706c7329e192559cb307962e293f0bbf02109c81fcde177eb36d8d39e37e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062154"
---
# <a name="lvn_insertitem-notification-code"></a>\_Код уведомления ЛВН INSERTITEM

Сообщает родительскому окну элемента управления "представление списка", что был вставлен новый элемент. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_INSERTITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Член **Член iItem** определяет новый элемент, а остальные члены равны нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





