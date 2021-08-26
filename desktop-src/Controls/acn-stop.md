---
title: Код уведомления ACN_STOP (Коммктрл. h)
description: Уведомляет родительское окно элемента управления анимации о том, что связанный ролик AVI прекратил воспроизведение. Этот код уведомления отправляется в виде \_ командного сообщения WM.
ms.assetid: 2f21a2ec-975f-4592-8b21-956bd5311ef4
keywords:
- ACN_STOP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- ACN_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ba1fe51f4ceaae6e145de43a0e1104903c90b2d573c43d7aa7904f1d8f7ae1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922094"
---
# <a name="acn_stop-notification-code"></a>АКН \_ код уведомления о прерывании

Уведомляет родительское окно элемента управления анимации о том, что связанный ролик AVI прекратил воспроизведение. Этот код уведомления отправляется в виде [**\_ командного сообщения WM**](/windows/desktop/menurc/wm-command) .


```C++
ACN_STOP     

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления анимацией. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.

</dd> <dt>

*lParam* 
</dt> <dd>

**HWND** , указывающий дескриптор для элемента управления анимации.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

