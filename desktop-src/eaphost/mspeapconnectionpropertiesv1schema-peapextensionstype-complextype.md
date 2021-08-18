---
title: Сложный тип Пеапекстенсионстипе
description: содержит улучшения схемы, внесенные в Windows 7. Будущие улучшения схемы будут обрабатываться PeapExtensionsTypeV2.
ms.assetid: a8fb8474-a375-4401-83b0-4fa87d637209
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
ms.openlocfilehash: 212c8bf6b1421cfc461288e8f57258b40e11e9118c9ea2b2f620986e91d226f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984034"
---
# <a name="peapextensionstype-complex-type"></a>Сложный тип Пеапекстенсионстипе

сложный тип **пеапекстенсионстипе** содержит улучшения схемы, внесенные в Windows 7. Будущие улучшения схемы будут обрабатываться [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PerformServerValidation"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:AcceptServerName"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:IdentityPrivacy"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PeapExtensionsV2"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                                               | Тип | Описание                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------|------|------------------------------------------------------------------------------------------------------------|
| [**Екстендедпеап: Перформсервервалидатион**](mspeapconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |      | Windows 7 и более поздних версий: указывает, выполняется ли проверка сервера.<br/>                          |
| [**Екстендедпеап: Акцептсервернаме**](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | Windows 7 и более поздних версий: указывает, считывается ли имя сервера.<br/>                            |
| [**Екстендедпеап: Идентитиприваци**](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | Windows 7 и более поздних версий: указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение.<br/> |
| [**Екстендедпеап: PeapExtensionsV2**](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | Windows 7 и более поздних версий: включает будущие улучшения схемы.<br/>                                 |



## <a name="remarks"></a>Remarks

Элемент **пеапекстенсионстипе** является необязательным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Сложные типы схемы mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





