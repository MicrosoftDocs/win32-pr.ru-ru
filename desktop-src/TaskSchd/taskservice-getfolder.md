---
title: TaskService. @ Folder, метод
description: Для создания скриптов Возвращает папку с зарегистрированными задачами.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- Метод onfolder планировщик задач
- Метод GetObject планировщик задач, объект TaskService
- Объект TaskService планировщик задач, метод GetObject
topic_type:
- apiref
api_name:
- TaskService.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e58f2d930a0577b6f1be620891b7ba631f18d77
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387103"
---
# <a name="taskservicegetfolder-method"></a>TaskService. @ Folder, метод

Для создания скриптов Возвращает папку с зарегистрированными задачами.

## <a name="syntax"></a>Синтаксис


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*путь* \[ окне\]
</dt> <dd>

Путь к извлекаемой папке. Не используйте обратную косую черту после имени последней папки в пути. Корневая папка задач указывается с помощью обратной косой черты ( \\ ). Примером пути к папке задачи в корневой папке задачи является \\ митаскфолдер. Символ "." нельзя использовать для указания текущей папки задач и ".." символы нельзя использовать для указания родительской папки задач в пути.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Объект [**таскфолдер**](taskfolder.md) для запрошенной папки.

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

 

 





