---
title: Код уведомления TTN_NEEDTEXT (Коммктрл. h)
description: Посылается элементом управления ToolTip для получения сведений, необходимых для вывода окна подсказки. Этот код уведомления идентичен ТТН \_ жетдиспинфо. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- TTN_NEEDTEXT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31b498f48534d7f6b270027bc1279244c67e26ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136395"
---
# <a name="ttn_needtext-notification-code"></a>\_Код уведомления ТТН нидтекст

Посылается элементом управления ToolTip для получения сведений, необходимых для вывода окна подсказки. Этот код уведомления идентичен [ТТН \_ жетдиспинфо](ttn-getdispinfo.md). Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TTN_NEEDTEXT

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмттдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) , определяющую средство, которое нуждается в тексте и получает запрошенные сведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого уведомления не используется.

## <a name="remarks"></a>Комментарии

Заполните соответствующие элементы структуры, чтобы вернуть запрошенные сведения в элемент управления ToolTip. Если обработчик сообщений задает для элемента **уфлагс** структуры [**нмттдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) значение TTF \_ di \_ сетитем, элемент управления ToolTip сохраняет информацию и не запрашивает их снова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТТН \_ НИДТЕКСТВ** (Юникод) и **ТТН \_ нидтекста** (ANSI)<br/>                 |



 

 





