---
title: Код уведомления LVN_SETDISPINFO (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что оно должно обновлять сведения, которые он поддерживает для элемента. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- LVN_SETDISPINFO кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4827d37a115f2bd1bb523f78bdb5975de4314056a174be4bfa886e1a076497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915064"
---
# <a name="lvn_setdispinfo-notification-code"></a>\_Код уведомления ЛВН сетдиспинфо

Сообщает родительскому окну элемента управления "представление списка", что оно должно обновлять сведения, которые он поддерживает для элемента. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмлвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) , которая задает сведения для измененного элемента. **Элемент** этой структуры является структурой [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , содержащей сведения об измененном элементе. Элемент **псзтекст** **элемента** содержит допустимое значение, независимо от того, \_ установлен ли флаг текста лвиф в элементе **Mask** этой структуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Получатель уведомлений выполняет приведение *lParam* для получения структуры [**нмлвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . Параметр *wParam* содержит код сообщения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ЛВН \_ СЕТДИСПИНФОВ** (Юникод) и **ЛВН \_ сетдиспинфоа** (ANSI)<br/>           |



## <a name="see-also"></a>См. также

<dl> <dt>

[ЛВН \_ жетдиспинфо](lvn-getdispinfo.md)
</dt> </dl>

 

 





