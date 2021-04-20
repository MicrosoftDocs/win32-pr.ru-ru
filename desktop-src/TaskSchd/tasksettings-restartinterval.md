---
title: Тасксеттингс. Рестартинтервал, свойство
description: Для создания скриптов Возвращает или задает значение, указывающее, как долго планировщик задач будет пытаться перезапустить задачу.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- планировщик задач свойства Рестартинтервал
- Планировщик задач свойства Рестартинтервал, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Рестартинтервал
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f127c5d434b5cb1e6dec6d8a3c68ee343fa00ffc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734149"
---
# <a name="tasksettingsrestartinterval-property"></a>Тасксеттингс. Рестартинтервал, свойство

Для создания скриптов Возвращает или задает значение, указывающее, как долго планировщик задач будет пытаться перезапустить задачу.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a>Значение свойства

Значение, указывающее, как долго планировщик задач будет пытаться перезапустить задачу. Если это свойство задано, также должно быть задано свойство [**рестарткаунт**](tasksettings-restartcount.md) . Формат этой строки — `P<days>DT<hours>H<minutes>M<seconds>S` (например, "PT5M" — 5 минут, "PT1H" — 1 час, а "PT20M" — 20 минут). Максимально допустимое время — 31 день. минимальное допустимое время — 1 минута.

## <a name="remarks"></a>Замечания

При чтении или записи XML для задачи этот параметр указывается в элементе [**Interval**](taskschedulerschema-interval-restarttype-element.md) схемы планировщик задач.

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

 

 





