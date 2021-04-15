---
title: Код уведомления RBN_MINMAX (Коммктрл. h)
description: Посылается элементом управления "Главная панель" до максимизации или минимизации полосы. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 75619cb0-ef0b-44fa-83b2-15a5e5e92c60
keywords:
- RBN_MINMAX кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_MINMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3569a28d0c0a610ccccf42d11ff4b2e5b4b0007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654533"
---
# <a name="rbn_minmax-notification-code"></a>\_Код уведомления РБН MINMAX

Посылается элементом управления "Главная панель" до максимизации или минимизации полосы. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_MINMAX
```



## <a name="parameters"></a>Параметры

Этот код уведомления не содержит параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение, чтобы не допустить выполнения операции, ноль, чтобы разрешить продолжение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





