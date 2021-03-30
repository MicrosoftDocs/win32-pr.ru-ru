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
ms.openlocfilehash: d600418d43459d6c4cbfcb0746a378633d096c24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801732"
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

## <a name="remarks"></a>Комментарии

Коллекции основаны на 1. Иными словами, индекс первого элемента в коллекции равен 1.

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

 

 





