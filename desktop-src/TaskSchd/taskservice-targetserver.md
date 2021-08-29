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
ms.openlocfilehash: 79f68dfaf5d6000ad88dca9001102056eb349601630364105526ea0d29a8bf46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080294"
---
# <a name="taskservicetargetserver-property"></a>TaskService. TargetServer, свойство

Для создания скриптов возвращает имя компьютера, на котором запущена служба планировщик задач, к которой подключен пользователь.

## <a name="syntax"></a>Синтаксис


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a>Значение свойства

Имя компьютера, на котором запущена служба планировщик задач, к которой подключен пользователь.

## <a name="remarks"></a>Remarks

Это свойство возвращает пустую строку, когда пользователь передает IP-адрес, localhost или "." в качестве параметра, и возвращает имя компьютера, на котором выполняется служба планировщик задач, когда пользователь не передает значение параметра.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





