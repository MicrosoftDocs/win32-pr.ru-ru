---
title: Рунонлифнетворкаваилабле (Сеттингстипе), элемент
description: Указывает, что планировщик задач будет выполнять задачу только при доступности сети.
ms.assetid: b7b804d3-b31a-4d70-9ba5-805a285e278e
keywords:
- планировщик задач элемента Рунонлифнетворкаваилабле
topic_type:
- apiref
api_name:
- RunOnlyIfNetworkAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3680ba3c29dc0d258a48aa16ae7923e3761eda30f198384fecfbf238e2933cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991034"
---
# <a name="runonlyifnetworkavailable-settingstype-element"></a>Рунонлифнетворкаваилабле (Сеттингстипе), элемент

Указывает, что планировщик задач будет выполнять задачу только при доступности сети.

``` syntax
<xs:element name="RunOnlyIfNetworkAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Элемент **рунонлифнетворкаваилабле** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**свойство рунонлифнетворкаваилабле объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).

Сведения о разработке сценариев см. в разделе [**тасксеттингс. рунонлифнетворкаваилабле**](tasksettings-runonlyifnetworkavailable.md).

## <a name="examples"></a>Примеры

Следующий XML-код определяет элемент Settings, который позволяет задаче запускаться только в случае доступности сети.


```XML
<Settings>
    <RunOnlyIfNetworkAvailable>true</RunOnlyIfNetworkAvailable>
</Settings>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





