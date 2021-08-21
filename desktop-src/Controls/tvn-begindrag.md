---
title: Код уведомления TVN_BEGINDRAG (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления, что инициируется операция перетаскивания с использованием левой кнопки мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- TVN_BEGINDRAG кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TVN_BEGINDRAG
- TVN_BEGINDRAGA
- TVN_BEGINDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95952ee42dfe8eb8dd1a46c66dcd452f41cbc9723fa175c2a0d1fc75056c31ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957923"
---
# <a name="tvn_begindrag-notification-code"></a>\_Код уведомления ТВН бегиндраг

Сообщает родительскому окну элемента управления иерархического представления, что инициируется операция перетаскивания с использованием левой кнопки мыши. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_BEGINDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Элемент **итемнев** — это структура [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , которая содержит допустимые сведения об элементе, который перетаскивается в элементы **хитем**, **State** и **lParam** . Элемент **птдраг** указывает текущие экранные координаты мыши.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="remarks"></a>Remarks

Элемент управления "дерево-представление", имеющий стиль [**\_ Дисабледрагдроп "телевизоры**](tree-view-control-window-styles.md) ", не отправляет этот код уведомления.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТВН \_ БЕГИНДРАГВ** (Юникод) и **ТВН \_ бегиндрага** (ANSI)<br/>               |



 

 





