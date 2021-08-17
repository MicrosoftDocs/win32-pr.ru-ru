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
ms.openlocfilehash: 362b6cbb977e66a92425da1355f0747660d867f67aec0ad684f7e8e3956edc63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139447"
---
# <a name="execactionworkingdirectory-property"></a>Ексекактион. WorkingDirectory, свойство

Для создания скриптов Возвращает или задает каталог, содержащий исполняемый файл или файлы, используемые исполняемым файлом.

## <a name="syntax"></a>Синтаксис


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a>Значение свойства

Каталог, содержащий исполняемый файл или файлы, используемые исполняемым файлом.

## <a name="remarks"></a>Remarks

При чтении или записи XML рабочий каталог приложения указывается в элементе [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) схемы планировщик задач.

Путь проверяется, чтобы убедиться, что он действителен при регистрации задачи, а не когда это свойство задано.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ексекактион**](execaction.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





