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
ms.openlocfilehash: fecf58696618f1f0f359754bc29aa10680dd1717fe55ffe9fc3e87d0b361b76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355347"
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



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**свойство валуекуериес объекта иевенттригжер**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).

Сведения о разработке скриптов см. в разделе [**EventTrigger. валуекуериес**](eventtrigger-valuequeries.md).

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, указывающей триггер события с помощью этого элемента, см. в разделе [пример триггера события (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

