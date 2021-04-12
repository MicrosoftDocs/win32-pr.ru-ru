---
title: Сложный тип Пеапекстенсионстипе (свойства соединения)
description: Сведения о сложном типе Пеапекстенсионстипе. Этот тип обеспечивает будущие улучшения схемы.
ms.assetid: d4f7784d-d426-4da6-bf81-40716f185416
keywords:
- Пеапекстенсионстипе сложный тип EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bf7e22a013bbd7a931b61b55ae0013bb42f4e41
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339276"
---
# <a name="peapextensionstype-complex-type-connection-properties"></a>Сложный тип Пеапекстенсионстипе (свойства соединения)

Сложный тип **пеапекстенсионстипе** обеспечивает будущие улучшения схемы.

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>Комментарии

Сложный тип **пеапекстенсионстипе** является необязательным.

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





