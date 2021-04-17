---
title: Код уведомления TVN_ITEMCHANGING (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления о том, что необходимо изменить атрибуты элементов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- TVN_ITEMCHANGING кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d258b7bf9f03b0e721e61c5da56bc915518069b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534211"
---
# <a name="tvn_itemchanging-notification-code"></a>\_Код уведомления ТВН итемчангинг

Сообщает родительскому окну элемента управления иерархического представления о том, что необходимо изменить атрибуты элементов. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтвитемчанже**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) , описывающую изменяемый элемент. Для элемента **учанжед** задано состояние твиф \_ .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение false** , чтобы принять изменение, или **значение true** , чтобы предотвратить изменение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТВН \_ ИТЕМЧАНГИНГВ** (Юникод) и **ТВН \_ итемчангинга** (ANSI)<br/>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ТВН \_ итемчанжед](tvn-itemchanged.md)
</dt> </dl>

 

 





