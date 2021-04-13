---
title: Виклитригжер. DaysOfWeek, свойство
description: Для сценариев Возвращает или задает дни недели, в которые выполняется задача.
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- планировщик задач свойства DaysOfWeek
- Планировщик задач свойства DaysOfWeek, объект Виклитригжер
- Планировщик задач объекта Виклитригжер, свойство DaysOfWeek
topic_type:
- apiref
api_name:
- WeeklyTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f0a27ef031e7baf46d2d3c0e33c23fb505c7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535591"
---
# <a name="weeklytriggerdaysofweek-property"></a>Виклитригжер. DaysOfWeek, свойство

Для сценариев Возвращает или задает дни недели, в которые выполняется задача.

## <a name="syntax"></a>Синтаксис


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Значение свойства

Битовая маска, указывающая дни недели, в которые выполняется задача.

## <a name="remarks"></a>Комментарии

В следующей таблице показано сопоставление побитовой маски, используемой этим свойством.



| Месяц     | Шестнадцатеричное значение | Десятичное значение |
|-----------|-----------|---------------|
| Воскресенье    | 0X01      | 1             |
| Понедельник    | 0x02      | 2             |
| Вторник   | 0X04      | 4             |
| Среда | 0X08      | 8             |
| Четверг  | 0X10      | 16            |
| Пятница    | 0x20      | 32            |
| Суббота  | 0X40      | 64            |



 

При чтении или записи собственного XML-кода для задачи дни недели указываются с помощью элемента [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) схемы планировщик задач.

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

 

 





