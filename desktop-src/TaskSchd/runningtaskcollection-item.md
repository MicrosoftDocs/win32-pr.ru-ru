---
title: Руннингтаскколлектион. Item, свойство
description: Для сценария возвращает указанную задачу из коллекции.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- планировщик задач свойства элемента
- Свойство Item планировщик задач, объект Руннингтаскколлектион
- Планировщик задач объекта Руннингтаскколлектион, свойство Item
topic_type:
- apiref
api_name:
- RunningTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7e2ca7abf5f1daa936509d5fae71211e8b139537fa1782daac6c08bf9a1017f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866784"
---
# <a name="runningtaskcollectionitem-property"></a>Руннингтаскколлектион. Item, свойство

Для сценария возвращает указанную задачу из коллекции.

## <a name="syntax"></a>Синтаксис


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a>Значение свойства

Объект [**руннингтаск**](runningtask.md) , содержащий запрошенный контекст.

## <a name="remarks"></a>Remarks

Коллекции основаны на 1. Иными словами, индекс первого элемента в коллекции равен 1.

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

 

 





