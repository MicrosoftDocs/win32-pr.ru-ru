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
ms.openlocfilehash: be89197c4ae88188fc1d2a746c40d69e385edc7ba08aaf2d3bf29067ee5f4a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516994"
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



## <a name="remarks"></a>Remarks

Если для этого элемента задано значение true, задача может быть запущена независимо от того, какие триггеры запускают задачу.

Сведения о разработке на C++ см. в описании [**Свойства алловдемандстарт объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).

Сведения о разработке сценариев см. в разделе [**тасксеттингс. алловдемандстарт**](tasksettings-allowdemandstart.md).

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, которая допускает запуск спроса, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





