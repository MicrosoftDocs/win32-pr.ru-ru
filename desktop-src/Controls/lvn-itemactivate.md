---
title: Код уведомления LVN_ITEMACTIVATE (Коммктрл. h)
description: Отправляется элементом управления "представление списка", когда пользователь активирует элемент. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- LVN_ITEMACTIVATE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9f139559b03fd82ac655381972803a288f00db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137890"
---
# <a name="lvn_itemactivate-notification-code"></a>\_Код уведомления ЛВН итемактивате

Отправляется элементом управления "представление списка", когда пользователь активирует элемент. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

[Версия 4,71](common-control-versions.md). Указатель на структуру [**нмитемактивате**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) , содержащую сведения об этом коде уведомления.

[Версия 4,70](common-control-versions.md) и более ранние версии. Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую сведения об этом коде уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение, получающее этот код уведомления, должно возвращать ноль.

## <a name="remarks"></a>Комментарии

Чтобы получить активируемые элементы, принимающее приложение должно использовать сообщение [**LVM \_ жетселектедкаунт**](lvm-getselectedcount.md) , чтобы получить количество выбранных элементов, а затем отправить сообщение [**LVM \_ жетнекститем**](lvm-getnextitem.md) с **лвни \_ Selected** , пока не будут получены все элементы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





