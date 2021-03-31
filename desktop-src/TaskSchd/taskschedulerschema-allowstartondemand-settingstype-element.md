---
title: Алловстартондеманд (Сеттингстипе), элемент
description: Указывает, что задача может быть запущена либо с помощью команды выполнить, либо из контекстного меню.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- планировщик задач элемента Алловстартондеманд
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec396bf10efbd11024fe39e57bdf05025db0e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988352"
---
# <a name="allowstartondemand-settingstype-element"></a>Алловстартондеманд (Сеттингстипе), элемент

Указывает, что задача может быть запущена либо с помощью команды выполнить, либо из контекстного меню.

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

Элемент **алловстартондеманд** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Комментарии

Если для этого элемента задано значение true, задача может быть запущена независимо от того, какие триггеры запускают задачу.

Сведения о разработке на C++ см. в описании [**Свойства алловдемандстарт объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).

Сведения о разработке сценариев см. в разделе [**тасксеттингс. алловдемандстарт**](tasksettings-allowdemandstart.md).

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, которая допускает запуск спроса, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





