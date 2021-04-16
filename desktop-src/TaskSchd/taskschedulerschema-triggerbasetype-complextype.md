---
title: Сложный тип Тригжербасетипе
description: Определяет атрибут, базовые дочерние элементы и сведения о последовательности для всех сложных типов триггеров.
ms.assetid: 1a2d004a-6f52-42b7-b0d0-ace8d27e9166
keywords:
- планировщик задач сложного типа Тригжербасетипе
topic_type:
- apiref
api_name:
- triggerBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56602e4a7e6599b7b756ff6bc109376dddc63ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341295"
---
# <a name="triggerbasetype-complex-type"></a>Сложный тип Тригжербасетипе

Определяет атрибут, базовые дочерние элементы и сведения о последовательности для всех сложных типов триггеров.

``` syntax
<xs:complexType name="triggerBaseType"
    abstract="true"
>
    <xs:sequence>
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="EndBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Repetition"
            type="repetitionType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                      | Тип                                                                     | Описание                                                                                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**Активировано**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | Логическое                                                                  | Указывает, что триггер включен.<br/>                                                                      |
| [**ендбаундари**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Дата и время деактивации триггера.<br/>                                                          |
| [**ексекутионтимелимит**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | длительность                                                                 | Указывает интервал, в течение которого триггер может запустить задачу.<br/>                                                 |
| [**Повторение**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**репетитионтипе**](taskschedulerschema-repetitiontype-complextype.md) | Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после срабатывания триггера.<br/> |
| [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Дата и время активации триггера.<br/>                                                            |



## <a name="attributes"></a>Атрибуты



| Имя | Тип | Описание                           |
|------|------|---------------------------------------|
| идентификатор   | ID   | Идентификатор триггера.<br/> |



## <a name="remarks"></a>Комментарии

К сложным типам триггеров относятся следующие.

-   [**буттригжертипе**](taskschedulerschema-boottriggertype-complextype.md)
-   [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md)
-   [**евенттригжертипе**](taskschedulerschema-eventtriggertype-complextype.md)
-   [**идлетригжертипе**](taskschedulerschema-idletriggertype-complextype.md)
-   [**логонтригжертипе**](taskschedulerschema-logontriggertype-complextype.md)
-   [**регистратионтригжертипе**](taskschedulerschema-registrationtriggertype-complextype.md)
-   [**тиметригжертипе**](taskschedulerschema-timetriggertype-complextype.md)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





