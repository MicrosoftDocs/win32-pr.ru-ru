---
title: TaskService. @, метод
description: Для создания скриптов возвращает пустой объект определения задачи, который должен быть заполнен параметрами и свойствами, а затем зарегистрирован с помощью метода Таскфолдер. Регистертаскдефинитион.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- планировщик задач метода "в команде"
- Метод планировщик задач, объект TaskService
- Планировщик задач объекта TaskService, метод "в команде"
topic_type:
- apiref
api_name:
- TaskService.NewTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22da6f62f59bf24ded0eed9dea21e3a1a9d1c3e7ecc36fb6f425f58124aee71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990934"
---
# <a name="taskservicenewtask-method"></a>TaskService. @, метод

Для создания скриптов возвращает пустой объект определения задачи, который должен быть заполнен параметрами и свойствами, а затем зарегистрирован с помощью метода [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md) .

## <a name="syntax"></a>Синтаксис


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Этот параметр зарезервирован для будущего использования и должен иметь значение 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Определение задачи, в которой указаны все сведения, необходимые для создания новой задачи.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





