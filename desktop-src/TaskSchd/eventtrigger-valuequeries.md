---
title: Свойство EventTrigger. Валуекуериес
description: Для создания скриптов Возвращает или задает коллекцию именованных запросов XPath. Каждый запрос в коллекции применяется к последнему соответствующему XML-событию, возвращенному из запроса подписки, указанного в свойстве Subscription.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- планировщик задач свойства Валуекуериес
- Планировщик задач свойства Валуекуериес, объект EventTrigger
- Объект EventTrigger планировщик задач, свойство Валуекуериес
topic_type:
- apiref
api_name:
- EventTrigger.ValueQueries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8fd28cd616af56a9b51ecf4e709df5f07674c6d1f307320128645364f3bfc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253884"
---
# <a name="eventtriggervaluequeries-property"></a>Свойство EventTrigger. Валуекуериес

Для создания скриптов Возвращает или задает коллекцию именованных запросов XPath. Каждый запрос в коллекции применяется к последнему соответствующему XML-событию, возвращенному из запроса подписки, указанного в свойстве [**Subscription**](eventtrigger-subscription.md) .

## <a name="syntax"></a>Синтаксис


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a>Значение свойства

Коллекция пар "имя-значение". Каждая пара «имя-значение» в коллекции определяет уникальное имя для значения свойства события, запускающего триггер события. Значение свойства события определяется как запрос события XPath. Дополнительные сведения о запросах событий XPath см. в разделе [Выбор события](/previous-versions//aa385231(v=vs.85)).

## <a name="remarks"></a>Remarks

Имя запроса можно использовать в качестве переменной в следующих свойствах действия:

-   [**Шовмессажеактион. MessageBody**](showmessageaction-messagebody.md)
-   [**Шовмессажеактион. Title**](showmessageaction-title.md)
-   [**Ексекактион. Arguments**](execaction-arguments.md)
-   [**Ексекактион. WorkingDirectory**](execaction-workingdirectory.md)
-   [**Емаилактион. Server**](emailaction-server.md)
-   [**Емаилактион. subject**](emailaction-subject.md)
-   [**EmailAction.To**](emailaction-to.md)
-   [**EmailAction.Cc**](emailaction-cc.md)
-   [**Емаилактион. СК**](emailaction-bcc.md)
-   [**Емаилактион. ReplyTo**](emailaction-replyto.md)
-   [**Емаилактион. from**](emailaction-from.md)
-   [**Емаилактион. Body**](emailaction-body.md)
-   [**Комхандлерактион. Data**](comhandleraction-data.md)

В следующих примерах кода показаны две пары "имя-значение", которые можно использовать в коллекции "имя — значение". Значения, возвращаемые запросами XPath, могут заменять переменные в свойстве действия. Ссылки на значения указываются по имени, с помощью `$(user)` и `$(machine)` в свойстве Action. Например, если `$(user)` `$(machine)` переменные и используются в строке [**шовмессажеактион. MessageBody**](showmessageaction-messagebody.md) , то значение запросов XPath заменит переменные в строке.

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

Дополнительные сведения о записи строки запроса для определенных событий см. в разделе [Выбор событий](/previous-versions//aa385231(v=vs.85)) и [Подписка на события](../wes/subscribing-to-events.md).

## <a name="requirements"></a>Requirements (Требования)



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

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

