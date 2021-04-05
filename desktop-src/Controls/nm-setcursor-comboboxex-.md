---
title: Код уведомления NM_SETCURSOR (ComboBoxEx) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления ComboBoxEx, что элемент управления устанавливает курсор в ответ на \_ сообщение СЕТКУРСОР WM. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- Элементы управления Windows для кода уведомления NM_SETCURSOR (ComboBoxEx)
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
ms.openlocfilehash: 5fbd5e10f06e74af0778521d31c69e63586a6476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803149"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

