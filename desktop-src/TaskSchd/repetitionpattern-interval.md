---
title: Репетитионпаттерн. Interval, свойство
description: Для создания скриптов Возвращает или задает интервал времени между перезапусками задачи.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Свойство Interval планировщик задач
- Свойство Interval планировщик задач, объект Репетитионпаттерн
- Планировщик задач объекта Репетитионпаттерн, свойство Interval
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc6efcaa56d2c251b5e044c87091bc646c21f8691aa384ad522b6062014fd496
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072624"
---
# <a name="repetitionpatterninterval-property"></a>Репетитионпаттерн. Interval, свойство

Для создания скриптов Возвращает или задает интервал времени между перезапусками задачи.

## <a name="syntax"></a>Синтаксис


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a>Значение свойства

Промежуток времени между перезапусками задачи. Формат этой строки — `P<days>DT<hours>H<minutes>M<seconds>S` (например, "PT5M" — 5 минут, "PT1H" — 1 час, а "PT20M" — 20 минут). Максимально допустимое время — 31 день. минимальное допустимое время — 1 минута.

## <a name="remarks"></a>Remarks

Если для задачи задана длительность повторения, необходимо также указать интервал повторения.

При чтении или записи XML для задачи интервал повтора указывается в элементе [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) схемы планировщик задач.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





