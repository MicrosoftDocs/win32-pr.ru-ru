---
title: Элемент volatile
description: Указывает, будет ли задача автоматически отключаться при каждом запуске Windows.
ms.assetid: E0298876-2A96-401D-B857-69758AF980E5
keywords:
- планировщик задач с временными элементами
topic_type:
- apiref
api_name:
- Volatile
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca697bd0dff3a1fffd0b92a29d2fc88f1d4ed433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803635"
---
# <a name="volatile-element"></a>Элемент volatile

Указывает, будет ли задача автоматически отключаться при каждом запуске Windows.

``` syntax
<xs:element name="Volatile"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
    default="false"
 />
```

Элемент **volatile** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от | Описание                                                                        |
|-------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) |              | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Комментарии

При программировании на C++ этот параметр простоя указывается с помощью свойства [**ITaskSettings3:: volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





