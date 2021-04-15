---
title: Код уведомления RBN_AUTOSIZE (Коммктрл. h)
description: Посылается элементом управления главной панели, созданным с помощью стиля автомасштабирования RBS, \_ когда Главная панель автоматически изменяет размер. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- RBN_AUTOSIZE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ecfac5a4f84d69d444c25a24956cb911fd90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654702"
---
# <a name="rbn_autosize-notification-code"></a>\_Код уведомления РБН AUTOSIZE

Посылается элементом управления главной панели, созданным с помощью стиля автомасштабирования [**RBS \_**](rebar-control-styles.md) , когда Главная панель автоматически изменяет размер. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмрбаутосизе**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) , содержащую сведения об операции изменения размера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого уведомления не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





