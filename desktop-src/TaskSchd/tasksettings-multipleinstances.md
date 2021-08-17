---
title: Тасксеттингс. Мултиплеинстанцес, свойство
description: Для создания скриптов Возвращает или задает политику, определяющую, как планировщик задач работает с несколькими экземплярами задачи.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- планировщик задач свойства Мултиплеинстанцес
- Планировщик задач свойства Мултиплеинстанцес, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Мултиплеинстанцес
topic_type:
- apiref
api_name:
- TaskSettings.MultipleInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff0091b9051840fea4c37869b51902f0c5f4c7cfed43a47c4f3924b398fe3e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059692"
---
# <a name="tasksettingsmultipleinstances-property"></a>Тасксеттингс. Мултиплеинстанцес, свойство

Для создания скриптов Возвращает или задает политику, определяющую, как планировщик задач работает с несколькими экземплярами задачи.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a>Значение свойства

[**Задача \_ Константы \_ политики экземпляров**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) .



| Значение                                                                                                                                                                                                                                                               | Значение                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <dt>**Задача \_ \_Параллельные экземпляры**</dt> <dt>0</dt> </dl>                 | Запускает новый экземпляр, пока запущен существующий экземпляр задачи.<br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <dt>**Задача \_ \_Очередь экземпляров**</dt> <dt>1</dt> </dl>                          | Запускает новый экземпляр задачи после завершения всех остальных экземпляров задачи.<br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <dt>**Задача \_ ЭКЗЕМПЛЯРЫ, не \_ пропускаемые \_ New**</dt> <dt>2</dt> </dl>          | Не запускает новый экземпляр, если запущен существующий экземпляр задачи.<br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <dt>**Задача \_ ЭКЗЕМПЛЯРЫ \_ прекращают \_ существующие**</dt> <dt>3</dt> </dl> | Останавливает существующий экземпляр задачи перед запуском нового экземпляра.<br/>                 |



 

## <a name="remarks"></a>Remarks

При чтении или записи XML для задачи этот параметр указывается в элементе [**мултиплеинстанцесполици**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) схемы планировщик задач.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_политика экземпляров \_ задач**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





