---
title: Регистратионтригжер (Тригжерграуп), элемент
description: Указывает триггер, который запускает задачу при регистрации задачи.
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- планировщик задач триггера регистрации, XML-элемент
- планировщик задач элемента Регистратионтригжер
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90960f81d252b0b0a8d1de3ab5cc1465003467a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681983"
---
# <a name="registrationtrigger-triggergroup-element"></a>Регистратионтригжер (Тригжерграуп), элемент

Указывает триггер, который запускает задачу при регистрации задачи.

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

Элемент **регистратионтригжер** определяется сложным типом [**регистратионтригжертипе**](taskschedulerschema-registrationtriggertype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Триггеры**](taskschedulerschema-triggers-tasktype-element.md) | [**тригжерстипе**](taskschedulerschema-triggerstype-complextype.md) | Задает триггеры, которые запускают задачу.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                        | Тип                                                                     | Описание                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Задержка (Регистратионтригжертипе)**](taskschedulerschema-delay-boottriggertype-element.md)                   | длительность                                                                 | Указывает промежуток времени между регистрацией задачи и началом задачи.<br/>                          |
| [**Включено (Тригжербасетипе)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | Логическое                                                                  | Указывает, что триггер включен.<br/>                                                                                  |
| [**Ендбаундари (Тригжербасетипе)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Указывает дату и время деактивации триггера. Триггер не может запустить задачу после ее деактивации.<br/> |
| [**Ексекутионтимелимит (Тригжербасетипе)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | длительность                                                                 | Указывает максимальное время, в течение которого задача может запускаться триггером.<br/>                                   |
| [**Повторение (Тригжербасетипе)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**репетитионтипе**](taskschedulerschema-repetitiontype-complextype.md) | Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.<br/>          |
| [**Стартбаундари (Тригжербасетипе)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Указывает дату и время активации триггера.<br/>                                                              |



## <a name="attributes"></a>Атрибуты



| Имя | Тип | Описание                           |
|------|------|---------------------------------------|
| Идентификатор   | ID   | Идентификатор триггера.<br/> |



## <a name="remarks"></a>Комментарии

Для разработки сценариев триггер регистрации указывается с помощью объекта [**регистратионтригжер**](registrationtrigger.md) .

Для разработки на C++ триггер регистрации указывается с помощью интерфейса [**ирегистратионтригжер**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) .

Перечисленные выше дочерние элементы определяются сложными типами элементов [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) и [**регистратионтригжертипе**](taskschedulerschema-registrationtriggertype-complextype.md) . Эти элементы должны быть добавлены в приведенной ниже последовательности.

-   [**Стартбаундари (Тригжербасетипе)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**Ендбаундари (Тригжербасетипе)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Включено (Тригжербасетипе)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Повторение (Тригжербасетипе)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**Ексекутионтимелимит (Тригжербасетипе)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**Задержка (Регистратионтригжертипе)**](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, указывающей триггер загрузки, см. в разделе [пример триггера регистрации (XML)](registration-trigger-example--xml-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





