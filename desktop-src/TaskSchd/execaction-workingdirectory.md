---
title: Ексекактион. WorkingDirectory, свойство
description: Для создания скриптов Возвращает или задает каталог, содержащий исполняемый файл или файлы, используемые исполняемым файлом.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- планировщик задач свойства WorkingDirectory
- Планировщик задач свойства WorkingDirectory, объект Ексекактион
- Планировщик задач объекта Ексекактион, свойство WorkingDirectory
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d4755b6f760ed1af75c676ecb70074c3ea7c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672591"
---
# <a name="execactionworkingdirectory-property"></a>Ексекактион. WorkingDirectory, свойство

Для создания скриптов Возвращает или задает каталог, содержащий исполняемый файл или файлы, используемые исполняемым файлом.

## <a name="syntax"></a>Синтаксис


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a>Значение свойства

Каталог, содержащий исполняемый файл или файлы, используемые исполняемым файлом.

## <a name="remarks"></a>Комментарии

При чтении или записи XML рабочий каталог приложения указывается в элементе [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) схемы планировщик задач.

Путь проверяется, чтобы убедиться, что он действителен при регистрации задачи, а не когда это свойство задано.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ексекактион**](execaction.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





