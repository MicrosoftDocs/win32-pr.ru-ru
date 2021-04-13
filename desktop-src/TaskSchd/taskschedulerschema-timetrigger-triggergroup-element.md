---
title: Тиметригжер (Тригжерграуп), элемент
description: Указывает триггер, который запускает задачу при активации триггера.
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- планировщик задач элемента Тиметригжер
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83d3b0a63a8be70af7eba4edb90e49db71892f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492054"
---
# <a name="timetrigger-triggergroup-element"></a>Тиметригжер (Тригжерграуп), элемент

Указывает триггер, который запускает задачу при активации триггера.

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

Элемент **тиметригжер** определяется параметром [**тригжерграуп**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Триггеры**](taskschedulerschema-triggers-tasktype-element.md) | [**тригжерстипе**](taskschedulerschema-triggerstype-complextype.md) | Задает триггеры, которые запускают задачу.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                        | Тип                                                                     | Описание                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Включено (Тригжербасетипе)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | Логическое                                                                  | Указывает, что триггер включен.<br/>                                                                                  |
| [**Ендбаундари (Тригжербасетипе)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Указывает дату и время деактивации триггера. Триггер не может запустить задачу после ее деактивации.<br/> |
| [**Ексекутионтимелимит (Тригжербасетипе)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | длительность                                                                 | Указывает максимальное время, в течение которого задача может запускаться триггером.<br/>                                   |
| [**Повторение (Тригжербасетипе)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**репетитионтипе**](taskschedulerschema-repetitiontype-complextype.md) | Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.<br/>          |
| [**Стартбаундари (Тригжербасетипе)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Указывает дату и время активации триггера. Этот элемент является обязательным.<br/>                                    |



## <a name="attributes"></a>Атрибуты



| Имя | Тип       | Описание                               |
|------|------------|-------------------------------------------|
| Идентификатор   | **string** | Идентификатор триггера.<br/> |



## <a name="remarks"></a>Комментарии

Элемент [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) является обязательным элементом для триггеров времени и календаря (**тиметригжер** и [**календартригжер**](taskschedulerschema-calendartrigger-triggergroup-element.md)).

Для разработки сценариев триггер времени указывается с помощью объекта [**тиметригжер**](timetrigger.md) .

Для разработки на C++ триггер времени указывается с помощью интерфейса [**итиметригжер**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) .

Перечисленные выше дочерние элементы определяются сложными типами элементов [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) . Эти элементы должны быть добавлены в приведенной ниже последовательности.

-   [**Стартбаундари (Тригжербасетипе)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**Ендбаундари (Тригжербасетипе)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Включено (Тригжербасетипе)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Повторение (Тригжербасетипе)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**Ексекутионтимелимит (Тригжербасетипе)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, указывающей триггер времени, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





