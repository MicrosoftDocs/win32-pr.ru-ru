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
ms.openlocfilehash: a3a34e8eef84575548998e39ab47bc5492baca368f7012d5fa096c831539ceb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072414"
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

## <a name="remarks"></a>Remarks

При чтении или записи XML для задачи этот параметр указывается в элементе [**Count**](taskschedulerschema-count-restarttype-element.md) схемы планировщик задач.

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

 

 





