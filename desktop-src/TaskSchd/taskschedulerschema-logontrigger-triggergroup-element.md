---
title: Логонтригжер (Тригжерграуп), элемент
description: Указывает триггер, который запускает задачу при входе пользователя в систему.
ms.assetid: c3edee50-e053-4813-a1b2-bf1e7b575ff7
keywords:
- триггер LOGON, XML-элемент
- планировщик задач элемента Логонтригжер
topic_type:
- apiref
api_name:
- LogonTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a42aa17ae4cb5ca9177c5ff068745d506d89e0db8d71253148ab5adafa39baea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758906"
---
# <a name="logontrigger-triggergroup-element"></a>Логонтригжер (Тригжерграуп), элемент

Указывает триггер, который запускает задачу при входе пользователя в систему.

``` syntax
<xs:element name="LogonTrigger"
    type="logonTriggerType"
 />
```

Элемент **логонтригжер** определяется параметром [**тригжерграуп**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**План**](taskschedulerschema-triggers-tasktype-element.md) | [**тригжерстипе**](taskschedulerschema-triggerstype-complextype.md) | Задает триггеры, которые запускают задачу.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                        | Тип                                                                     | Описание                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Задержка (Логонтригжертипе)**](taskschedulerschema-delay-logontriggertype-element.md)                         | длительность                                                                 | Промежуток времени между входом пользователя в систему и запуском задачи.<br/>                                              |
| [**Включено (Тригжербасетипе)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | Логическое                                                                  | Указывает, что триггер включен.<br/>                                                                                  |
| [**Ендбаундари (Тригжербасетипе)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Указывает дату и время деактивации триггера. Триггер не может запустить задачу после ее деактивации.<br/> |
| [**Ексекутионтимелимит (Тригжербасетипе)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | длительность                                                                 | Указывает максимальное время, в течение которого задача может запускаться триггером.<br/>                                   |
| [**Повторение (Тригжербасетипе)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**репетитионтипе**](taskschedulerschema-repetitiontype-complextype.md) | Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.<br/>          |
| [**Стартбаундари (Тригжербасетипе)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Указывает дату и время активации триггера.<br/>                                                              |
| [**UserId (Логонтригжертипе)**](taskschedulerschema-userid-logontriggertype-element.md)                       | строка                                                                   | Идентификатор пользователя. Задача запускается, когда пользователь входит в систему на компьютере.<br/>                                      |



## <a name="remarks"></a>Remarks

Для разработки сценариев триггер входа задается с помощью объекта [**логонтригжер**](logontrigger.md) .

Для разработки на C++ триггер входа указывается с помощью интерфейса [**илогонтригжер**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) .

Перечисленные выше дочерние элементы определяются сложными типами элементов [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) и [**логонтригжертипе**](taskschedulerschema-logontriggertype-complextype.md) . Эти элементы должны быть добавлены в приведенной ниже последовательности.

-   [**Стартбаундари (Тригжербасетипе)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**Ендбаундари (Тригжербасетипе)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Включено (Тригжербасетипе)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Повторение (Тригжербасетипе)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**Ексекутионтимелимит (Тригжербасетипе)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**UserId (Логонтригжертипе)**](taskschedulerschema-userid-logontriggertype-element.md)
-   [**Задержка (Логонтригжертипе)**](taskschedulerschema-delay-logontriggertype-element.md)

### <a name="attributes"></a>Атрибуты

Приведенный ниже атрибут определяется сложными типами элементов [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .

-   ID: Идентификатор триггера.

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, использующей триггер входа, см. в разделе [пример триггера LOGON (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





