---
title: Сложный тип Актионбасетипе
description: Определяет атрибут ID для всех элементов этого типа.
ms.assetid: adc7117f-881f-4a32-8578-0530f2a0c179
keywords:
- планировщик задач сложного типа Актионбасетипе
topic_type:
- apiref
api_name:
- actionBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a8091456b2f09e6be5a332930d68960b2473acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137371"
---
# <a name="actionbasetype-complex-type"></a>Сложный тип Актионбасетипе

Определяет атрибут ID для всех элементов этого типа.

``` syntax
<xs:complexType name="actionBaseType"
    abstract="true"
>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a>Атрибуты



| Имя | Тип | Описание                                        |
|------|------|----------------------------------------------------|
| идентификатор   | ID   | Идентификатор действия, выполняемого задачей.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





