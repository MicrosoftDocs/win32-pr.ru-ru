---
title: Стартвхенаваилабле (Сеттингстипе), элемент
description: Указывает, что планировщик задач может запустить задачу в любое время после прохождения запланированного времени.
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- планировщик задач элемента Стартвхенаваилабле
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d86f6f6e75457d08e10ef40d728eaf3e3b00aa7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988349"
---
# <a name="startwhenavailable-settingstype-element"></a>Стартвхенаваилабле (Сеттингстипе), элемент

Указывает, что планировщик задач может запустить задачу в любое время после прохождения запланированного времени.

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Элемент **стартвхенаваилабле** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Комментарии

Это свойство применимо только к задачам с превышением времени.

Сведения о разработке на языке C++ см. в разделе [**свойство стартвхенаваилабле объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).

Сведения о разработке сценариев см. в разделе [**тасксеттингс. стартвхенаваилабле**](tasksettings-startwhenavailable.md).

## <a name="examples"></a>Примеры

Следующий XML-код определяет элемент Settings, позволяющий планировщик задач запускать задачу, когда она доступна.


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
</Settings>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





