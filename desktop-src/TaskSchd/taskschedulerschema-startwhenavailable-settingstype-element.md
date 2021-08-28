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
ms.openlocfilehash: aa87fe438cb2916757e5ad9ecf88e08ce944eb6c71749c116afc75b253da6f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401764"
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



## <a name="remarks"></a>Remarks

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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





