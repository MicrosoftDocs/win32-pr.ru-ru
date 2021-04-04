---
title: Сложный тип Пеапекстенсионстипе
description: Содержит улучшения схемы, вносимые в Windows 7. Будущие улучшения схемы будут обрабатываться PeapExtensionsTypeV2.
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
ms.openlocfilehash: 7cb8c698122c5a466ae95f728838425a5f10c665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803281"
---
# <a name="peapextensionstype-complex-type"></a>Сложный тип Пеапекстенсионстипе

Сложный тип **пеапекстенсионстипе** содержит улучшения схемы, вносимые в Windows 7. Будущие улучшения схемы будут обрабатываться [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).

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
| [**Екстендедпеап: Перформсервервалидатион**](mspeapconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |      | Windows 7 и более поздние версии: указывает, выполняется ли проверка сервера.<br/>                          |
| [**Екстендедпеап: Акцептсервернаме**](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | Windows 7 и более поздние версии: указывает, считывается ли имя сервера.<br/>                            |
| [**Екстендедпеап: Идентитиприваци**](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | Windows 7 и более поздние версии: указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение.<br/> |
| [**Екстендедпеап: PeapExtensionsV2**](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | Windows 7 и более поздние версии: включает будущие улучшения схемы.<br/>                                 |



## <a name="remarks"></a>Комментарии

Элемент **пеапекстенсионстипе** является необязательным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Сложные типы схемы mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





