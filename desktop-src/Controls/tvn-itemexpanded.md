---
title: Код уведомления TVN_ITEMEXPANDED (Коммктрл. h)
description: Сообщает родительскому окну элемента управления древовидного представления о том, что список дочерних элементов родительского элемента развернут или свернут. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- TVN_ITEMEXPANDED кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDED
- TVN_ITEMEXPANDEDA
- TVN_ITEMEXPANDEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18af761c7580707bfd0926874e25069ca15b564bf6ef205cd6dc7aaaecb6a772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018632"
---
# <a name="tvn_itemexpanded-notification-code"></a>\_Код уведомления ТВН итемекспандед

Сообщает родительскому окну элемента управления древовидного представления о том, что список дочерних элементов родительского элемента развернут или свернут. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Элемент **итемнев** — это структура [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , которая содержит допустимые сведения о родительском элементе в членах **хитем**, **State** и **lParam** . Член **действия** указывает, развернут ли список или свернут. Список возможных значений см. в описании сообщения [**TVM \_ expand**](tvm-expand.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТВН \_ ИТЕМЕКСПАНДЕДВ** (Юникод) и **ТВН \_ итемекспандеда** (ANSI)<br/>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ТВН \_ итемекспандинг](tvn-itemexpanding.md)
</dt> </dl>

 

 





