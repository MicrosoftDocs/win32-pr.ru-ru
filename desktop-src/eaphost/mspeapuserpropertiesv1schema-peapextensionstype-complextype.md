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
ms.openlocfilehash: 9a72fa87b3f1cf5ba4a65c179895c22e5a208616ed8c9b2ffb9f046e5de9b92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983924"
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

## <a name="remarks"></a>Remarks

Сложный тип **пеапекстенсионстипе** является необязательным.

## <a name="requirements"></a>Requirements (Требования)



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Сервер<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





