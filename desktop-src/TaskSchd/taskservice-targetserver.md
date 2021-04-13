---
title: TaskService. TargetServer, свойство
description: Для создания скриптов возвращает имя компьютера, на котором запущена служба планировщик задач, к которой подключен пользователь.
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- планировщик задач свойства TargetServer
- Планировщик задач свойства TargetServer, объект TaskService
- Планировщик задач объекта TaskService, свойство TargetServer
topic_type:
- apiref
api_name:
- TaskService.TargetServer
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4347915fae57585716a64a6a4ca549ccc1c299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535471"
---
# <a name="taskservicetargetserver-property"></a>TaskService. TargetServer, свойство

Для создания скриптов возвращает имя компьютера, на котором запущена служба планировщик задач, к которой подключен пользователь.

## <a name="syntax"></a>Синтаксис


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a>Значение свойства

Имя компьютера, на котором запущена служба планировщик задач, к которой подключен пользователь.

## <a name="remarks"></a>Комментарии

Это свойство возвращает пустую строку, когда пользователь передает IP-адрес, localhost или "." в качестве параметра, и возвращает имя компьютера, на котором выполняется служба планировщик задач, когда пользователь не передает значение параметра.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





