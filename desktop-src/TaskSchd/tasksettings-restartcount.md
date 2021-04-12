---
title: Тасксеттингс. Рестарткаунт, свойство
description: Для сценариев Возвращает или задает количество попыток перезапуска задачи планировщик задач.
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- планировщик задач свойства Рестарткаунт
- Планировщик задач свойства Рестарткаунт, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Рестарткаунт
topic_type:
- apiref
api_name:
- TaskSettings.RestartCount
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee033eebde7b085d6df40f1e5e20d6dcf640a93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415220"
---
# <a name="tasksettingsrestartcount-property"></a>Тасксеттингс. Рестарткаунт, свойство

Для сценариев Возвращает или задает количество попыток перезапуска задачи планировщик задач.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a>Значение свойства

Количество попыток перезапуска задачи планировщик задач.

## <a name="remarks"></a>Комментарии

При чтении или записи XML для задачи этот параметр указывается в элементе [**Count**](taskschedulerschema-count-restarttype-element.md) схемы планировщик задач.

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

 

 





