---
title: Эксклюзивный элемент
description: Указывает, должна ли планировщик задач запускать задачу во время автоматического обслуживания в монопольном режиме.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- планировщик задач исключающих элементов
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e0cd7cf5b2a5ce3aa68f92834aa45563000945d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681790"
---
# <a name="exclusive-element"></a>Эксклюзивный элемент

Указывает, должна ли планировщик задач запускать задачу во время автоматического обслуживания в монопольном режиме.

Исключительные права гарантируется только между другими задачами обслуживания и не предоставляет приоритет выполнения задачи. Если исключительные права не указан, задача запускается параллельно с другими задачами обслуживания.

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

**Эксклюзивный** элемент определяется сложным типом [**маинтенанцесеттингстипе**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                                                          | Унаследован от                                                                               | Описание                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**Маинтенанцесеттингс (Маинтенанцесеттингстипе)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**маинтенанцесеттингстипе**](taskschedulerschema-maintenancesettingstype-complextype.md) | Задает параметры задачи, которые планировщик задач будет использовать для запуска задачи во время автоматического обслуживания.<br/> |



## <a name="remarks"></a>Комментарии

При программировании на C++ этот параметр простоя указывается с помощью свойства [**имаинтенанцесеттингс:: Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) .

## <a name="examples"></a>Примеры

Следующий код XML определяет задачу обслуживания с требованием крайнего срока, равным 15 дням.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
    <Exclusive>true</Exclusive>
</MaintenanceSettings>
```



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

 

 





