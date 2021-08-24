---
title: Монслидовтригжер. Виксофмонс, свойство
description: Для сценариев Возвращает или задает недели месяца, в течение которых выполняется задача.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- планировщик задач свойства Виксофмонс
- Планировщик задач свойства Виксофмонс, объект Монслидовтригжер
- Планировщик задач объекта Монслидовтригжер, свойство Виксофмонс
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323ee8b93411d7ef176fa9dc2ffb3a4acfd1f902c0dc481fe48e07b82821227b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517444"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a>Монслидовтригжер. Виксофмонс, свойство

Для сценариев Возвращает или задает недели месяца, в течение которых выполняется задача.

## <a name="syntax"></a>Синтаксис


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a>Значение свойства

Битовая маска, указывающая дни недели, в течение которых выполняется задача.

## <a name="remarks"></a>Remarks

В следующей таблице показано сопоставление побитовой маски, используемой этим свойством.



| Неделя                     | Шестнадцатеричное значение | Десятичное значение |
|--------------------------|-----------|---------------|
| Первая неделя месяца  | 0X01      | 1             |
| Вторая неделя месяца | 0x02      | 2             |
| Третья неделя месяца  | 0X04      | 4             |
| Четвертая неделя месяца | 0X08      | 8             |



 

При чтении или записи XML для задачи дни недели месячного дня недели задаются элементом [**weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) .

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

 

 





