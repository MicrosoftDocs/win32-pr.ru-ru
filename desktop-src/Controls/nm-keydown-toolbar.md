---
title: Код уведомления NM_KEYDOWN (Toolbar) (Коммктрл. h)
description: Код уведомления NM_KEYDOWN (панель инструментов) — отправляется элементом управления, когда элемент управления имеет фокус клавиатуры и пользователь нажимает клавишу. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- Элементы управления Windows для кода уведомления NM_KEYDOWN (панель инструментов)
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d53818cf417e1efac686e94d3b4ef5919f819ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112362"
---
# <a name="nm_keydown-toolbar-notification-code"></a>\_Код уведомления NM (панель инструментов)

Посылается элементом управления, когда элемент управления имеет фокус клавиатуры и пользователь нажимает клавишу. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмкэй**](/windows/win32/api/commctrl/ns-commctrl-nmkey) , которая содержит дополнительные сведения о ключе, вызвавшем код уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение, чтобы элемент управления не обрабатывал ключ, или ноль в противном случае.

## <a name="remarks"></a>Remarks

В настоящее время этот код уведомления отправляется только элементом управления ToolBar.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





