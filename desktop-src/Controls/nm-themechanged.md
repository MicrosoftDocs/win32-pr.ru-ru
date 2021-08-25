---
title: Код уведомления NM_THEMECHANGED (Коммктрл. h)
description: Сообщает родительскому окну элемента управления, что тема изменилась. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 5e6a039e-9c35-4476-8cf1-5aea8977ed2d
keywords:
- NM_THEMECHANGED кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- NM_THEMECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 069f4eb2b3727edc19c531f4404b723df2ea775677a25283268c1c20a978dedc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877264"
---
# <a name="nm_themechanged-notification-code"></a>\_Код уведомления семечанжед (NM)

Сообщает родительскому окну элемента управления, что тема изменилась. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_THEMECHANGED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется элементом управления.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





