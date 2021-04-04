---
title: Код уведомления TBN_QUERYINSERT (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, можно ли вставить кнопку слева от указанной кнопки, пока пользователь настраивает панель инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- TBN_QUERYINSERT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a21e9ade8f54ffe27ebffdfc2a8b535b4b3630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989288"
---
# <a name="tbn_queryinsert-notification-code"></a>\_Код уведомления ТБН куеринсерт

Сообщает родительскому окну панели инструментов, можно ли вставить кнопку слева от указанной кнопки, пока пользователь настраивает панель инструментов. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтулбар**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . Член **iItem** содержит отсчитываемый от нуля индекс вставляемой кнопки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , чтобы разрешить вставку кнопки перед заданной кнопкой, или **значение false** , чтобы запретить вставку кнопки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





