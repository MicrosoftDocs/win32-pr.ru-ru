---
title: Код уведомления TVN_ITEMEXPANDING (Коммктрл. h)
description: Сообщает родительскому окну элемента управления древовидного представления о том, что список дочерних элементов родительского элемента собирается развернуть или свернуть. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f4403b41682590d305b527d6445c208011b368b2d2474d66720ed32d29c80ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957793"
---
# <a name="tvn_itemexpanding-notification-code"></a>\_Код уведомления ТВН итемекспандинг

Сообщает родительскому окну элемента управления древовидного представления о том, что список дочерних элементов родительского элемента собирается развернуть или свернуть. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Элемент **итемнев** — это структура [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , которая содержит допустимые сведения о родительском элементе в членах **хитем**, **State** и **lParam** . Член **действия** указывает, следует ли развернуть или свернуть список. Список возможных значений см. в описании сообщения [**TVM \_ expand**](tvm-expand.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , чтобы предотвратить расширение или свертывание списка.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТВН \_ ИТЕМЕКСПАНДИНГВ** (Юникод) и **ТВН \_ итемекспандинга** (ANSI)<br/>       |



## <a name="see-also"></a>См. также

<dl> <dt>

[ТВН \_ итемекспандед](tvn-itemexpanded.md)
</dt> </dl>

 

 





