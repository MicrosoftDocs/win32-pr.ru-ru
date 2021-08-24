---
title: Тасксеттингс. Рунонлифнетворкаваилабле, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, что планировщик задач будет выполнять задачу только при доступности сети.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- планировщик задач свойства Рунонлифнетворкаваилабле
- Планировщик задач свойства Рунонлифнетворкаваилабле, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Рунонлифнетворкаваилабле
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 193d235276ffc37513c95b5ae0a4cef5a6e84cd0bc7d8bea7fab67a262110080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354851"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a>Тасксеттингс. Рунонлифнетворкаваилабле, свойство

Для создания скриптов Возвращает или задает логическое значение, указывающее, что планировщик задач будет выполнять задачу только при доступности сети.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a>Значение свойства

Если значение — true, свойство указывает, что планировщик задач будет выполнять задачу только при доступности сети. Значение по умолчанию — False.

## <a name="remarks"></a>Remarks

При чтении или записи XML для задачи этот параметр указывается в элементе [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) схемы планировщик задач.

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

 

 





