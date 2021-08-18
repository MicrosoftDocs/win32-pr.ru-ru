---
title: Даилитригжер. Дайсинтервал, свойство
description: Для создания скриптов Возвращает или задает интервал между днями в расписании.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- планировщик задач свойства Дайсинтервал
- Планировщик задач свойства Дайсинтервал, объект Даилитригжер
- Планировщик задач объекта Даилитригжер, свойство Дайсинтервал
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4355e6c2a26b197224141018fa5a1d85e7d31e211ac47dc84a9e8c9ef3750fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139497"
---
# <a name="dailytriggerdaysinterval-property"></a>Даилитригжер. Дайсинтервал, свойство

Для создания скриптов Возвращает или задает интервал между днями в расписании.

## <a name="syntax"></a>Синтаксис


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a>Значение свойства

Интервал между днями в расписании.

## <a name="remarks"></a>Remarks

Интервал 1 создает ежедневное расписание. Интервал 2 создает расписание для каждого дня.

При чтении или записи собственного XML-кода для задачи интервал ежедневного расписания указывается с помощью элемента [**дайсинтервал**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) схемы планировщик задач.

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
</dt> <dt>

[**даилитригжер**](dailytrigger.md)
</dt> </dl>

 

 





