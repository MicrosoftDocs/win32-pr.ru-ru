---
title: Код уведомления TCN_SELCHANGE (Коммктрл. h)
description: Сообщает родительскому окну элемента управления вкладки, что выбранная в данный момент вкладка была изменена. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: f40e30f6-169b-4381-a300-12c3befb5fc5
keywords:
- TCN_SELCHANGE кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54ad012e98005e8fbf5148af58aab10d90e3127afeab6311cc8b8f3f84e2988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876184"
---
# <a name="tcn_selchange-notification-code"></a>\_Код уведомления ТКН селчанже

Сообщает родительскому окну элемента управления вкладки, что выбранная в данный момент вкладка была изменена. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TCN_SELCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Чтобы определить текущую выбранную вкладку, используйте макрос [**табктрл \_**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ТКН \_ селчангинг](tcn-selchanging.md)
</dt> </dl>

 

 





