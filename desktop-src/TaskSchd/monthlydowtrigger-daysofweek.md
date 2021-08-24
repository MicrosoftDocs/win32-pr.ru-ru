---
title: Монслидовтригжер. DaysOfWeek, свойство
description: Для сценариев Возвращает или задает дни недели, в которые выполняется задача.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- планировщик задач свойства DaysOfWeek
- Планировщик задач свойства DaysOfWeek, объект Монслидовтригжер
- Планировщик задач объекта Монслидовтригжер, свойство DaysOfWeek
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b9abf5dcd33c92d402f8ed6047a2fd80a0d5905bae075110931cfb8f83aa10a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517464"
---
# <a name="monthlydowtriggerdaysofweek-property"></a>Монслидовтригжер. DaysOfWeek, свойство

Для сценариев Возвращает или задает дни недели, в которые выполняется задача.

## <a name="syntax"></a>Синтаксис


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Значение свойства

Битовая маска, указывающая дни недели, в течение которых выполняется задача.

## <a name="remarks"></a>Remarks

В следующей таблице показано сопоставление побитовой маски, используемой этим свойством.



| День недели | Шестнадцатеричное значение | Десятичное значение |
|-------------|-----------|---------------|
| Воскресенье      | 0x01      | 1             |
| Понедельник      | 0x02      | 2             |
| Вторник     | 0x04      | 4             |
| Среда   | 0x08      | 8             |
| Четверг    | 0x10      | 16            |
| Пятница      | 0x20      | 32            |
| Суббота    | 0x40      | 64            |



 

При чтении или записи XML для задачи дни недели месячного дня недели задаются элементом [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**монслидовтригжер**](monthlydowtrigger.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





