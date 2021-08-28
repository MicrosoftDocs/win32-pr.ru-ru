---
title: Сложный тип Рекуиредпривилежестипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Рекуиредпривилежес (Рекуиредпривилежестипе).
ms.assetid: ae96282a-d167-47ea-9d37-2d682f746d23
keywords:
- планировщик задач сложного типа Рекуиредпривилежестипе
topic_type:
- apiref
api_name:
- requiredPrivilegesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d79b75a4d4bb44aded7367fd4acfd758887815bba6fc6fcfd965f9123ac58c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658794"
---
# <a name="requiredprivilegestype-complex-type"></a>Сложный тип Рекуиредпривилежестипе

Определяет дочерние элементы и сведения о последовательности для элемента [**рекуиредпривилежес (рекуиредпривилежестипе)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) .

``` syntax
<xs:complexType name="requiredPrivilegesType">
    <xs:all>
        <xs:element name="Privilege"
            type="privilegeType"
            minOccurs="1"
            maxOccurs="64"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                           | Тип                                                                  | Описание                                                |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------|
| [**Привилегия**](taskschedulerschema-privilege-requiredprivilegestype-element.md) | [**привилежетипе**](taskschedulerschema-privilegetype-simpletype.md) | Указывает необходимые привилегии для задачи. <br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





