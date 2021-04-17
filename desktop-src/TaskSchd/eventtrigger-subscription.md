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
ms.openlocfilehash: 68ad05576e248d3ad6c2551a8654a9198ca3c0f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682034"
---
# <a name="eventtriggersubscription-property"></a>EventTrigger. Subscription, свойство

Для создания скриптов Возвращает или задает строку запроса, определяющую событие, вызвавшее срабатывание триггера.

## <a name="syntax"></a>Синтаксис


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a>Значение свойства

Строка запроса, определяющая событие, вызвавшее срабатывание триггера.

## <a name="remarks"></a>Комментарии

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

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

