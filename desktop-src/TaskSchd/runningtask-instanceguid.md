---
title: Руннингтаск. Инстанцегуид, свойство
description: Для создания скриптов возвращает идентификатор GUID для этого экземпляра задачи.
ms.assetid: 35be538f-5223-4c61-9491-677953b4135a
keywords:
- планировщик задач свойства Инстанцегуид
- Планировщик задач свойства Инстанцегуид, объект Руннингтаск
- Планировщик задач объекта Руннингтаск, свойство Инстанцегуид
topic_type:
- apiref
api_name:
- RunningTask.InstanceGuid
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f3ad40eb7c8799d12ca3b4a6aaeb0b968a9229
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682032"
---
# <a name="runningtaskinstanceguid-property"></a>Руннингтаск. Инстанцегуид, свойство

Для создания скриптов возвращает идентификатор GUID для этого экземпляра задачи.

## <a name="syntax"></a>Синтаксис


```VB
RunningTask.InstanceGuid As string
```



## <a name="property-value"></a>Значение свойства

Идентификатор GUID для этого экземпляра задачи. Идентификатор создается службой планировщик задач каждый раз при выполнении задачи.

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

 

 





