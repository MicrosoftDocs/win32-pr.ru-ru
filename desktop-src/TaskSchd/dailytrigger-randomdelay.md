---
title: Даилитригжер. Рандомделай, свойство
description: Для создания скриптов Возвращает или задает время задержки, которое добавляется случайным образом к времени начала триггера. | Даилитригжер. Рандомделай, свойство
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- планировщик задач свойства Рандомделай
- Планировщик задач свойства Рандомделай, объект Даилитригжер
- Планировщик задач объекта Даилитригжер, свойство Рандомделай
topic_type:
- apiref
api_name:
- DailyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303192d578a2681e250784c1e1eb2831c98482cc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734109"
---
# <a name="dailytriggerrandomdelay-property"></a>Даилитригжер. Рандомделай, свойство

Для создания скриптов Возвращает или задает время задержки, которое добавляется случайным образом к времени начала триггера.

## <a name="syntax"></a>Синтаксис


```VB
DailyTrigger.RandomDelay As String
```



## <a name="property-value"></a>Значение свойства

Время задержки, которое случайным образом добавляется к времени начала триггера. Формат этой строки — `P<days>DT<hours>H<minutes>M<seconds>S` (например, P2DT5S имеет 2 дня, 5 секунд задержки).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**даилитригжер**](dailytrigger.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





