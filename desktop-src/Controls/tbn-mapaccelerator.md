---
title: Код уведомления TBN_MAPACCELERATOR (Коммктрл. h)
description: Запрашивает индекс кнопки на панели инструментов, соответствующей указанному символу ускорителя. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- TBN_MAPACCELERATOR кода уведомления Windows элементы управления
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
ms.openlocfilehash: 488c78ff00b75c42f6646e314c75d63445c7400eb9130464b126e75bcf2df942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434194"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





