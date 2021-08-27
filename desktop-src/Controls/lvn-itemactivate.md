---
title: Код уведомления LVN_ITEMACTIVATE (Коммктрл. h)
description: Отправляется элементом управления "представление списка", когда пользователь активирует элемент. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- LVN_ITEMACTIVATE кода уведомления Windows элементы управления
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
ms.openlocfilehash: f21b02406157a13d2fcf110c15e692211b26b3f9da31741489e317e6b2c68309
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105054"
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

## <a name="remarks"></a>Remarks

Чтобы получить активируемые элементы, принимающее приложение должно использовать сообщение [**LVM \_ жетселектедкаунт**](lvm-getselectedcount.md) , чтобы получить количество выбранных элементов, а затем отправить сообщение [**LVM \_ жетнекститем**](lvm-getnextitem.md) с **лвни \_ Selected** , пока не будут получены все элементы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





