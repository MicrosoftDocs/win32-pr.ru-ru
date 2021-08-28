---
title: Код уведомления TVN_ITEMCHANGED (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления о том, что атрибуты элемента изменились. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- TVN_ITEMCHANGED кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d140346d66a87bd394bc5aa36555b8accedef56891e722a4b28272e22f804ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018652"
---
# <a name="tvn_itemchanged-notification-code"></a>\_Код уведомления ТВН итемчанжед

Сообщает родительскому окну элемента управления иерархического представления о том, что атрибуты элемента изменились. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтвитемчанже**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) , описывающую измененный элемент. Для элемента **учанжед** задано состояние твиф \_ .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение false** , чтобы принять изменение, или **значение true** , чтобы предотвратить изменение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТВН \_ ИТЕМЧАНЖЕДВ** (Юникод) и **ТВН \_ итемчанжеда** (ANSI)<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ТВН \_ итемчангинг](tvn-itemchanging.md)
</dt> </dl>

 

 





