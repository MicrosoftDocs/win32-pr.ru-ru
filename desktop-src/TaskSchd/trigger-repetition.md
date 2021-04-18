---
title: Свойство Trigger. повторения
description: Для создания скриптов Возвращает или задает значение, указывающее, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- планировщик задач свойства повторения
- Планировщик задач свойства повторения, объект триггера
- Триггер объекта планировщик задач, свойство повторения
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611c7e42a14de06a8777333a6dc640781943ba06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672585"
---
# <a name="triggerrepetition-property"></a>Свойство Trigger. повторения

Для создания скриптов Возвращает или задает значение, указывающее, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.

## <a name="syntax"></a>Синтаксис


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a>Значение свойства

Объект [**репетитионпаттерн**](repetitionpattern.md) , который определяет, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.

## <a name="remarks"></a>Комментарии

При чтении или записи собственного XML-кода для задачи шаблон повторения для триггера указывается в элементе [**повторения**](taskschedulerschema-repetition-triggerbasetype-element.md) схемы планировщик задач.

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

[**репетитионпаттерн**](repetitionpattern.md)
</dt> </dl>

 

 





