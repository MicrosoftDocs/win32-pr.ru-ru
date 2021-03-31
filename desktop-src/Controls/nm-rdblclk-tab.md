---
title: Код уведомления NM_RDBLCLK (TAB) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "Вкладка", что пользователь дважды щелкнул правой кнопкой мыши в элементе управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: cdf0df70-e30b-4353-8c2a-26fffa0596c4
keywords:
- Элементы управления Windows для кода уведомления NM_RDBLCLK (TAB)
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4e159e64780f21576aa9e936379c881b32153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071107"
---
# <a name="nm_rdblclk-tab-notification-code"></a>\_Код уведомления "NM рдблклк (вкладка)"

Сообщает родительскому окну элемента управления "Вкладка", что пользователь дважды щелкнул правой кнопкой мыши в элементе управления. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_RDBLCLK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение, чтобы не разрешать обработку по умолчанию, или нуль, чтобы разрешить обработку по умолчанию.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





