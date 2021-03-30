---
title: Ексекактион. Path, свойство
description: Для создания скриптов Возвращает или задает путь к исполняемому файлу.
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- Свойство пути планировщик задач
- Свойство Path планировщик задач, объект Ексекактион
- Планировщик задач объекта Ексекактион, свойство Path
topic_type:
- apiref
api_name:
- ExecAction.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20e1dcd8cd9700f961eb944c7be3168582b8c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801793"
---
# <a name="execactionpath-property"></a>Ексекактион. Path, свойство

Для создания скриптов Возвращает или задает путь к исполняемому файлу.

## <a name="syntax"></a>Синтаксис


```VB
ExecAction.Path As String
```



## <a name="property-value"></a>Значение свойства

Путь к исполняемому файлу, запускаемому действием.

## <a name="remarks"></a>Комментарии

Это действие выполняет операцию командной строки. Например, действие может выполнить сценарий или запустить исполняемый файл.

При чтении или записи XML путь операции командной строки указывается в элементе [**Command**](taskschedulerschema-command-exectype-element.md) схемы планировщик задач.

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

 

 





