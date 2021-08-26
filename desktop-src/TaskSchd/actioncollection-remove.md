---
title: ActionCollection. Remove, метод
description: Для сценариев удаляет указанное действие из коллекции.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Удалить метод планировщик задач
- Метод Remove планировщик задач, объект ActionCollection
- Планировщик задач объекта ActionCollection, метод Remove
topic_type:
- apiref
api_name:
- ActionCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c176f41c59bd473e25e82082ada1934a25641e6144f4187e7f25075779b25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011744"
---
# <a name="actioncollectionremove-method"></a>ActionCollection. Remove, метод

Для сценариев удаляет указанное действие из коллекции.

## <a name="syntax"></a>Синтаксис


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

Индекс удаляемого действия.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

При удалении элементов Обратите внимание, что индекс для первого элемента в коллекции равен 1, а индекс последнего элемента — значение свойства [**ActionCollection. Count**](actioncollection-count.md) .

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
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> </dl>

 

 





