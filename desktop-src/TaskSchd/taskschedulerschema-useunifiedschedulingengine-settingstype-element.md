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
ms.openlocfilehash: a00798a46df3dfbb351dd8705b264192c38daff6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071408"
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



## <a name="remarks"></a>Комментарии

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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





