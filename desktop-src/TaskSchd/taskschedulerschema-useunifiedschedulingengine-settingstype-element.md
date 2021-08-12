---
title: Усеунифиедсчедулинженгине (Сеттингстипе), элемент
description: Указывает, что для выполнения этой задачи будет использоваться единый механизм планирования.
ms.assetid: 93436f14-1caf-4ec8-bf74-a198b7dcb27c
keywords:
- планировщик задач элемента Усеунифиедсчедулинженгине
topic_type:
- apiref
api_name:
- UseUnifiedSchedulingEngine
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faf27ea132fb47e35cd248e183fbec0584cb5d44414d6cacda6baac0d595c32d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610457"
---
# <a name="useunifiedschedulingengine-settingstype-element"></a>Усеунифиедсчедулинженгине (Сеттингстипе), элемент

Указывает, что для выполнения этой задачи будет использоваться единый механизм планирования.

``` syntax
<xs:element name="UseUnifiedSchedulingEngine"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

Элемент **усеунифиедсчедулинженгине** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Remarks

Значение по умолчанию для этого элемента — false.

Для разработки на C++ эта информация доступна через свойство [**ITaskSettings2:: усеунифиедсчедулинженгине**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет элемент Settings, который указывает, что для выполнения этой задачи будет использоваться единый механизм планирования.


```XML
<Settings>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
</Settings>
        
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





