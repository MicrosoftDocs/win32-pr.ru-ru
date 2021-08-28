---
title: Тасксеттингс. Enabled, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, что задача включена. Задачу можно выполнить, только если этот параметр имеет значение true.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Включенное свойство планировщик задач
- Включенное свойство планировщик задач, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Enabled
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7853177aecae963e4899a67d2ba5b39d1eaebdc75e25ce6e14523963a70c45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738165"
---
# <a name="tasksettingsenabled-property"></a>Тасксеттингс. Enabled, свойство

Для создания скриптов Возвращает или задает логическое значение, указывающее, что задача включена. Задачу можно выполнить, только если этот параметр имеет значение true.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a>Значение свойства

Если задано значение true, задача включена. Если задано значение false, задача не включена.

## <a name="remarks"></a>Remarks

При чтении или записи XML для задачи этот параметр указывается в элементе [**Enabled (сеттингстипе)**](taskschedulerschema-enabled-settingstype-element.md) схемы планировщик задач.

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

 

 





