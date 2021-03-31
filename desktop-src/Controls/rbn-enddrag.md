---
title: Код уведомления RBN_ENDDRAG (Коммктрл. h)
description: Посылается элементом управления главной панели, когда пользователь перестает перетаскивать полосу. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 24b06144-6a4c-46a4-bef1-d6592f72a2c0
keywords:
- RBN_ENDDRAG кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb6c538679d793ed2407775b4238cea475ba4ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071807"
---
# <a name="rbn_enddrag-notification-code"></a>\_Код уведомления РБН енддраг

Посылается элементом управления главной панели, когда пользователь перестает перетаскивать полосу. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_ENDDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмребар**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) , содержащую сведения о коде уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого кода уведомления не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





