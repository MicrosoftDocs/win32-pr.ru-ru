---
title: Код уведомления RBN_DELETINGBAND (Коммктрл. h)
description: Посылается элементом управления главной панели, когда удаляется полоса. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 92840cb1-375e-4c37-bde4-7ba02a1ff4f1
keywords:
- RBN_DELETINGBAND кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_DELETINGBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf810fd8800d7774a0dbf9a65cdf08c2d53d92ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988982"
---
# <a name="rbn_deletingband-notification-code"></a>\_Код уведомления РБН делетингбанд

Посылается элементом управления главной панели, когда удаляется полоса. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_DELETINGBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмребар**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) , содержащую сведения о коде уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого уведомления не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





