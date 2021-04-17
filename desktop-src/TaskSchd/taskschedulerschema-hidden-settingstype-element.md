---
title: Hidden (Сеттингстипе), элемент
description: Указывает, что задача не будет отображаться в пользовательском интерфейсе по умолчанию.
ms.assetid: a08c270f-6d4e-4473-9538-c1e1e21b3b10
keywords:
- планировщик задач скрытого элемента
topic_type:
- apiref
api_name:
- Hidden
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef5ad479fe3107ed8fa79f0f86307254a9f33c4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672903"
---
# <a name="hidden-settingstype-element"></a>Hidden (Сеттингстипе), элемент

Указывает, что задача не будет отображаться в пользовательском интерфейсе по умолчанию. Однако администраторы могут переопределить этот параметр с помощью "главного коммутатора", который делает все задачи видимыми в пользовательском интерфейсе.

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

**Скрытый** элемент определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Комментарии

Сведения о разработке с + + см. в разделе [**свойство Hidden объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).

Сведения о разработке сценариев см. в разделе [**тасксеттингс. Hidden**](tasksettings-hidden.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





