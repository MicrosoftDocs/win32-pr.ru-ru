---
title: Код уведомления TVN_ITEMEXPANDING (Коммктрл. h)
description: Сообщает родительскому окну элемента управления древовидного представления о том, что список дочерних элементов родительского элемента собирается развернуть или свернуть. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING кода уведомления элементы управления Windows
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
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989278"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТВН \_ ИТЕМЕКСПАНДИНГВ** (Юникод) и **ТВН \_ итемекспандинга** (ANSI)<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ТВН \_ итемекспандед](tvn-itemexpanded.md)
</dt> </dl>

 

 





