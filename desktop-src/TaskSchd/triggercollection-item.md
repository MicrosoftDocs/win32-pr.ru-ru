---
title: Тригжерколлектион. Item, свойство
description: Для сценариев Возвращает указанный триггер из коллекции.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- планировщик задач свойства элемента
- Свойство Item планировщик задач, объект Тригжерколлектион
- Планировщик задач объекта Тригжерколлектион, свойство Item
topic_type:
- apiref
api_name:
- TriggerCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee0460d79ef239c8dacbf7fbd45573dac8ba03ad9b53e6e9881dded1bf01030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001962"
---
# <a name="triggercollectionitem-property"></a>Тригжерколлектион. Item, свойство

Для сценариев Возвращает указанный триггер из коллекции.

## <a name="syntax"></a>Синтаксис


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a>Значение свойства

Объект [**триггера**](trigger.md) , представляющий запрошенный триггер.

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

 

 





