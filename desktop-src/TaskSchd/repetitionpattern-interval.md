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
ms.openlocfilehash: c1e81920fffe5c9fd58dd36a028b924f54ebe6dd
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734179"
---
# <a name="repetitionpatterninterval-property"></a>Репетитионпаттерн. Interval, свойство

Для создания скриптов Возвращает или задает интервал времени между перезапусками задачи.

## <a name="syntax"></a>Синтаксис


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a>Значение свойства

Промежуток времени между перезапусками задачи. Формат этой строки — `P<days>DT<hours>H<minutes>M<seconds>S` (например, "PT5M" — 5 минут, "PT1H" — 1 час, а "PT20M" — 20 минут). Максимально допустимое время — 31 день. минимальное допустимое время — 1 минута.

## <a name="remarks"></a>Замечания

Если для задачи задана длительность повторения, необходимо также указать интервал повторения.

При чтении или записи XML для задачи интервал повтора указывается в элементе [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) схемы планировщик задач.

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

 

 





