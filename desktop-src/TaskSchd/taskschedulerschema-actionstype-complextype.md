---
title: Сложный тип Актионстипе
description: Определяет дочерние элементы и атрибут для элемента Actions.
ms.assetid: 01577b65-4bfa-4b9f-b9b9-6b2b0dbd582a
keywords:
- планировщик задач сложного типа Актионстипе
topic_type:
- apiref
api_name:
- actionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d84cab2f0977a3b5bf980f594f1b26b543d8e5e7de000959488e874e640dc9d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010934"
---
# <a name="actionstype-complex-type"></a>Сложный тип Актионстипе

Определяет дочерние элементы и атрибут для элемента [**Actions**](taskschedulerschema-actions-tasktype-element.md) .

``` syntax
<xs:complexType name="actionsType">
    <xs:sequence>
        <xs:group
            maxOccurs="32"
            ref="actionGroup"
         />
    </xs:sequence>
    <xs:attribute name="Context"
        type="IDREF"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a>Атрибуты



| Имя    | Тип  | Описание                                                                                          |
|---------|-------|------------------------------------------------------------------------------------------------------|
| Контекст | IDREF | Идентификатор субъекта используемого, который является контекстом безопасности для действий задачи.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





