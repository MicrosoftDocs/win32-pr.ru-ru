---
title: EventTrigger. Delay, свойство
description: Для создания скриптов Возвращает или задает значение, указывающее промежуток времени между возникновением события и моментом запуска задачи.
ms.assetid: 6f8b5e25-ad53-466e-adab-fe3c968e941b
keywords:
- планировщик задач свойства Delay
- Свойство Delay планировщик задач, объект EventTrigger
- Объект EventTrigger планировщик задач, свойство Delay
topic_type:
- apiref
api_name:
- EventTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb67ca7ef12ca023bcb6c0d9d83880d4abb94af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672685"
---
# <a name="eventtriggerdelay-property"></a>EventTrigger. Delay, свойство

Для создания скриптов Возвращает или задает значение, указывающее промежуток времени между возникновением события и моментом запуска задачи. Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).

## <a name="syntax"></a>Синтаксис


```VB
EventTrigger.Delay As String
```



## <a name="property-value"></a>Значение свойства

Значение, указывающее промежуток времени между возникновением события и моментом запуска задачи.

## <a name="remarks"></a>Комментарии

При чтении или записи собственного XML-кода для задачи задержка события указывается с помощью элемента [**delay**](taskschedulerschema-delay-eventtriggertype-element.md) схемы планировщик задач.

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

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

 





