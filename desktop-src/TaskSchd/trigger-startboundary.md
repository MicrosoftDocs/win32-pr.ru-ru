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
ms.openlocfilehash: 141e7e4d80d090e92ecb951917f60f972587d4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801745"
---
# <a name="triggerstartboundary-property"></a>Свойство Trigger. Стартбаундари

Для создания скриптов Возвращает или задает дату и время активации триггера.

## <a name="syntax"></a>Синтаксис


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a>Значение свойства

Дата и время активации триггера. Дата и время должны быть в следующем формате: гггг-мм-DDTHH: мм: СС (+-) чч: мм. Например, дата 11 октября 2005 по 1:21:17 в тихоокеанском часовом поясе будет записана как 2005-10-11T13:21:17-08:00. Раздел (+-) чч: мм в формате описывает часовой пояс как определенное число часов перед временем в формате UTC (время по Гринвичу).

## <a name="remarks"></a>Комментарии

При чтении или записи XML для задачи начальная граница триггера задается в элементе [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) схемы планировщик задач.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





