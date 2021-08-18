---
title: Свойство Trigger. Стартбаундари
description: Для создания скриптов Возвращает или задает дату и время активации триггера.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- планировщик задач свойства Стартбаундари
- Планировщик задач свойства Стартбаундари, объект Trigger
- Планировщик задач объекта триггера, свойство Стартбаундари
topic_type:
- apiref
api_name:
- Trigger.StartBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b49fa865c215c3190b2d081390c98eec1336ffb00a4bf1e9dd9d94226105e96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002082"
---
# <a name="triggerstartboundary-property"></a>Свойство Trigger. Стартбаундари

Для создания скриптов Возвращает или задает дату и время активации триггера.

## <a name="syntax"></a>Синтаксис


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a>Значение свойства

Дата и время активации триггера. Дата и время должны быть в следующем формате: гггг-мм-DDTHH: мм: СС (+-) чч: мм. Например, дата 11 октября 2005 по 1:21:17 в тихоокеанском часовом поясе будет записана как 2005-10-11T13:21:17-08:00. Раздел (+-) чч: мм в формате описывает часовой пояс как определенное число часов перед временем в формате UTC (время по Гринвичу).

## <a name="remarks"></a>Remarks

При чтении или записи XML для задачи начальная граница триггера задается в элементе [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) схемы планировщик задач.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





