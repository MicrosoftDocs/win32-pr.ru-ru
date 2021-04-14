---
title: ActionCollection. Item, свойство
description: Для скрипта возвращает указанное действие из коллекции.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- планировщик задач свойства элемента
- Свойство Item планировщик задач, объект ActionCollection
- Планировщик задач объекта ActionCollection, свойство Item
topic_type:
- apiref
api_name:
- ActionCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4853009c547f3bdfbb269e512ce5d39273726095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415888"
---
# <a name="actioncollectionitem-property"></a>ActionCollection. Item, свойство

Для скрипта возвращает указанное действие из коллекции.

## <a name="syntax"></a>Синтаксис


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a>Значение свойства

Объект [**Action**](action.md) , представляющий запрошенное действие.

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
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> </dl>

 

 





