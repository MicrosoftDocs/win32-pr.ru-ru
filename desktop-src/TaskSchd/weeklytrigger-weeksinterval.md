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
ms.openlocfilehash: 547ebc8617d625df3dd0e8dba167bb60682185dfb13897c49524d1894789c933
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080264"
---
# <a name="weeklytriggerweeksinterval-property"></a>Виклитригжер. Виксинтервал, свойство

Для создания скриптов Возвращает или задает интервал между неделями в расписании.

## <a name="syntax"></a>Синтаксис


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a>Значение свойства

Интервал между неделями в расписании.

## <a name="remarks"></a>Remarks

Чтобы запускать задание раз в неделю, укажите 1. Чтобы запускать задание раз в две недели, укажите 2.

При чтении или записи собственного XML-кода для задачи интервал для еженедельного расписания указывается с помощью элемента [**виксинтервал**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) схемы планировщик задач.

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

 

 





