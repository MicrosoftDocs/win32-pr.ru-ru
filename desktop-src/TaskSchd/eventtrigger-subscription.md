---
title: EventTrigger. Subscription, свойство
description: Для создания скриптов Возвращает или задает строку запроса, определяющую событие, вызвавшее срабатывание триггера.
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- планировщик задач Свойства подписки
- Свойство подписки планировщик задач, объект EventTrigger
- Объект EventTrigger планировщик задач, свойство подписки
topic_type:
- apiref
api_name:
- EventTrigger.Subscription
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d83225faa022de6e4a0823be3db971c71da503a885a46c1941fc1e5578f711b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100234"
---
# <a name="eventtriggersubscription-property"></a>EventTrigger. Subscription, свойство

Для создания скриптов Возвращает или задает строку запроса, определяющую событие, вызвавшее срабатывание триггера.

## <a name="syntax"></a>Синтаксис


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a>Значение свойства

Строка запроса, определяющая событие, вызвавшее срабатывание триггера.

## <a name="remarks"></a>Remarks

При чтении или записи собственного XML-кода для задачи подписка на событие указывается с помощью элемента [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) схемы планировщик задач.

Дополнительные сведения о записи строки запроса для определенных событий см. в разделе [Выбор событий](/previous-versions//aa385231(v=vs.85)) и [Подписка на события](../wes/subscribing-to-events.md).

## <a name="examples"></a>Примеры

Следующая строка запроса определяет подписку на все события уровня 2 в системном канале:


```XML
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>" 
```



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

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

