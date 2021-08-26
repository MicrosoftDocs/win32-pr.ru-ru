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
ms.openlocfilehash: aab796abfdcad67a348b6d42186732d402bbe8eeeb359ac772588fe809dbf73c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991334"
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



## <a name="remarks"></a>Remarks

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
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>           |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





