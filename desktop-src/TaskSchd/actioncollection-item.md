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
ms.openlocfilehash: fff95b707a4a99ce54cba4d175ce9fd094f7a6bd400147d7942a42a39d65bb7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796644"
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

## <a name="remarks"></a>Remarks

Коллекции основаны на 1. Иными словами, индекс первого элемента в коллекции равен 1.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> </dl>

 

 





