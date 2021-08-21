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
ms.openlocfilehash: 21eed68ff260d199a46adabc0e560533658c6cc1398d00f9507b80b40fb69955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611015"
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



## <a name="remarks"></a>Remarks

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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





