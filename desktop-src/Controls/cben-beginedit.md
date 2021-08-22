---
title: Код уведомления CBEN_BEGINEDIT (Коммктрл. h)
description: Посылается, когда пользователь активирует раскрывающийся список или щелкает поле ввода элемента управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 77236471-b1c0-4679-b7b8-93e85867fe3b
keywords:
- CBEN_BEGINEDIT кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- CBEN_BEGINEDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109af3e9ccfdd7d8679ac7a5d467cafa966de6faf76adbd06450fd6ba782e80d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527904"
---
# <a name="cben_beginedit-notification-code"></a>\_Код уведомления кбен BEGINEDIT

Посылается, когда пользователь активирует раскрывающийся список или щелкает поле ввода элемента управления. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
CBEN_BEGINEDIT

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую сведения о коде уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение, обрабатывающее этот код уведомления, должно возвращать ноль.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





