---
title: Код уведомления TBN_MAPACCELERATOR (Коммктрл. h)
description: Запрашивает индекс кнопки на панели инструментов, соответствующей указанному символу ускорителя. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- TBN_MAPACCELERATOR кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_MAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b20f1908f441c38e23aa7428f8c8edb8a192c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988186"
---
# <a name="tbn_mapaccelerator-notification-code"></a>\_Код уведомления ТБН мапакцелератор

Запрашивает индекс кнопки на панели инструментов, соответствующей указанному символу ускорителя. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмчар**](/windows/win32/api/commctrl/ns-commctrl-nmchar) , содержащую символ клавиши быстрого вызова и принимающий индекс соответствующей кнопки. Поле **двитемнекст** имеет значение-1, если ускоритель не соответствует команде.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если для **нмчар. двитемнекст** задано значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





