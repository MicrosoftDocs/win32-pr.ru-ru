---
title: Код уведомления NM_SETCURSOR (ComboBoxEx) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления ComboBoxEx, что элемент управления устанавливает курсор в ответ на \_ сообщение СЕТКУРСОР WM. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- NM_SETCURSOR (ComboBoxEx) код уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0f7c7ffc8459ae1da279b6e53329f894662dd6ae6f30888fd9bdbdf631fa8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798994"
---
# <a name="nm_setcursor-comboboxex-notification-code"></a>\_Код уведомления NM сеткурсор (ComboBoxEx)

Сообщает родительскому окну элемента управления ComboBoxEx, что элемент управления устанавливает курсор в ответ на сообщение [**\_ сеткурсор WM**](/windows/desktop/menurc/wm-setcursor) . Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нммаусе**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль, чтобы позволить элементу управления установить курсор или ненулевой нуль, чтобы запретить элементу управления устанавливать курсор.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

