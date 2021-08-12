---
title: Сложный тип Евенттригжертипе
description: Определяет дочерние элементы и сведения о последовательности для элемента EventTrigger.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- планировщик задач сложного типа Евенттригжертипе
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0acd4bafa6033e461b69180862a8302e76f363b581d7f06b0812824f2031780b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612057"
---
# <a name="eventtriggertype-complex-type"></a>Сложный тип Евенттригжертипе

Определяет дочерние элементы и сведения о последовательности для элемента [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="eventTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Subscription"
                    type="nonEmptyString"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="ValueQueries"
                    type="namedValues"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                           | Тип                                                                    | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Задержка**](taskschedulerschema-delay-eventtriggertype-element.md)               | длительность                                                                | Указывает промежуток времени между моментом возникновения события и моментом запуска задачи.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Подписка**](taskschedulerschema-subscription-eventtriggertype-element.md) | [**нонемптистринг**](taskschedulerschema-nonemptystring-simpletype.md) | Указывает запрос XPath, определяющий событие, вызвавшее срабатывание триггера.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**валуекуериес**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**намедвалуес**](taskschedulerschema-namedvalues-complextype.md)      | Задает последовательность элементов, каждая из которых содержит имя и значение запроса XPath. Запросы применяются к событию, возвращенному из подписки на события, указанной в элементе [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) . Имя для значения запроса XPath можно использовать в качестве переменной в элементе [**Body**](taskschedulerschema-body-showmessagetype-element.md) в разделе действия [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) задачи. <br/> |



## <a name="remarks"></a>Remarks

Помимо дочернего элемента, определенного здесь, элемент [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) также использует дочерние элементы, определенные сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





