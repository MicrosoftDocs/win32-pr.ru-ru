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
ms.openlocfilehash: 6499f3b900fe10b2a2527c2e2ee675cca3151204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534301"
---
# <a name="dailytriggerdaysinterval-property"></a>Даилитригжер. Дайсинтервал, свойство

Для создания скриптов Возвращает или задает интервал между днями в расписании.

## <a name="syntax"></a>Синтаксис


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a>Значение свойства

Интервал между днями в расписании.

## <a name="remarks"></a>Комментарии

Интервал 1 создает ежедневное расписание. Интервал 2 создает расписание для каждого дня.

При чтении или записи собственного XML-кода для задачи интервал ежедневного расписания указывается с помощью элемента [**дайсинтервал**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) схемы планировщик задач.

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
</dt> <dt>

[**даилитригжер**](dailytrigger.md)
</dt> </dl>

 

 





