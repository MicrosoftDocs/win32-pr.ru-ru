---
title: Код уведомления NM_NCHITTEST (Коммктрл. h)
description: NM_NCHITTEST код уведомления — отправляется элементом управления главной панели, когда элемент управления получает \_ сообщение WM нчиттест. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- NM_NCHITTEST кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ede0ac017fbe5146cd68e51e2a38c7f66c7898
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112322"
---
# <a name="nm_nchittest-notification-code"></a>\_Код уведомления нчиттест (NM)

Посылается элементом управления "Главная панель", когда элемент управления получает сообщение [**WM \_ нчиттест**](/windows/desktop/inputdev/wm-nchittest) . Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нммаусе**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) , содержащую сведения о коде уведомления. Элемент *PT* содержит координаты мыши для сообщения проверки попадания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если не указано иное, возвращайте нуль, чтобы разрешить элементу управления выполнять обработку сообщения проверки попадания по умолчанию, или вернуть одно из значений НТ, \* задокументированных в [**WM \_ нчиттест**](/windows/desktop/inputdev/wm-nchittest) , чтобы переопределить обработку проверки попадания по умолчанию.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

