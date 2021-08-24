---
title: Сообщение WM_POINTERROUTEDRELEASED
description: Посылается всем процессам (настроенным для межпроцессных цепочек через Аддконтентвискросспроцессчаининг, которые в настоящее время не обрабатывают ввод указателя) при получении сообщения WM_POINTERUP в текущем процессе.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- WM_POINTERROUTEDRELEASED сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDRELEASED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 318134779d94824daef0b05903f45121665892fbcafbeb48589ef150f324d2b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611294"
---
# <a name="wm_pointerroutedreleased-message"></a>Сообщение WM_POINTERROUTEDRELEASED

Посылается всем процессам (настроенным для межпроцессных цепочек через [**аддконтентвискросспроцессчаининг**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) , которые в настоящее время не обрабатывают ввод указателя) при получении сообщения [**WM_POINTERUP**](wm-pointerup.md) в текущем процессе.


```C++
#define WM_POINTERROUTEDRELEASED       0x0253
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

NULL

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Сообщения](messages.md)
</dt> </dl>

 

