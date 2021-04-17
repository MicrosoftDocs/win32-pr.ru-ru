---
title: Виклитригжер. Виксинтервал, свойство
description: Для создания скриптов Возвращает или задает интервал между неделями в расписании.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- планировщик задач свойства Виксинтервал
- Планировщик задач свойства Виксинтервал, объект Виклитригжер
- Планировщик задач объекта Виклитригжер, свойство Виксинтервал
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4668b68d0b3f83e096284db35df799a63eb677b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681782"
---
# <a name="weeklytriggerweeksinterval-property"></a>Виклитригжер. Виксинтервал, свойство

Для создания скриптов Возвращает или задает интервал между неделями в расписании.

## <a name="syntax"></a>Синтаксис


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a>Значение свойства

Интервал между неделями в расписании.

## <a name="remarks"></a>Комментарии

Чтобы запускать задание раз в неделю, укажите 1. Чтобы запускать задание раз в две недели, укажите 2.

При чтении или записи собственного XML-кода для задачи интервал для еженедельного расписания указывается с помощью элемента [**виксинтервал**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) схемы планировщик задач.

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

 

 





