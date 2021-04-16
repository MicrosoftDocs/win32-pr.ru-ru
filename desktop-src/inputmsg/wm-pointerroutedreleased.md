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
ms.openlocfilehash: 8e24a0df1a2bbdf2b0a9df97057686aa6045eff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415560"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сообщения](messages.md)
</dt> </dl>

 

