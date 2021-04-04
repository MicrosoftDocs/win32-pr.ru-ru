---
title: Валуекуериес (Евенттригжертипе), элемент
description: Содержит последовательность элементов, каждая из которых содержит имя и значение запроса XPath.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- планировщик задач элемента Валуекуериес
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4448693c1c1ab19b2ea13050cc9ab817bdc25e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988347"
---
# <a name="valuequeries-eventtriggertype-element"></a>Валуекуериес (Евенттригжертипе), элемент

Содержит последовательность элементов, каждая из которых содержит имя и значение запроса XPath. Запросы применяются к событию, возвращенному из подписки на события, указанной в элементе [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) . Имя для значения запроса XPath можно использовать в качестве переменной в разделе Action задачи.

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

Элемент **валуекуериес** определяется сложным типом [**евенттригжертипе**](taskschedulerschema-eventtriggertype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                      | Унаследован от                                                                 | Описание                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger (Тригжерграуп)**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**евенттригжертипе**](taskschedulerschema-eventtriggertype-complextype.md) | Указывает триггер, который запускает задачу при возникновении системного события.<br/> |



## <a name="remarks"></a>Комментарии

Сведения о разработке на языке C++ см. в разделе [**свойство валуекуериес объекта иевенттригжер**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).

Сведения о разработке скриптов см. в разделе [**EventTrigger. валуекуериес**](eventtrigger-valuequeries.md).

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, указывающей триггер события с помощью этого элемента, см. в разделе [пример триггера события (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

