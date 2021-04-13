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
ms.openlocfilehash: 2a5ce81d96858488395e34f84232ca758ddabc59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493119"
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
| [**Правом**](taskschedulerschema-privilege-requiredprivilegestype-element.md) | [**привилежетипе**](taskschedulerschema-privilegetype-simpletype.md) | Указывает необходимые привилегии для задачи. <br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





