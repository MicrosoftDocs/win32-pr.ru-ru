---
title: Сложный тип Идентитиприваципараметерс
description: Содержит сведения об использовании анонимных удостоверений во время аутентификации PEAP.
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 18bef3eb69ab2799f7139fe2886d89e996fb8fb47d178997694c568450fb8340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983904"
---
# <a name="identityprivacyparameters-complex-type"></a>Сложный тип Идентитиприваципараметерс

Сложный тип **идентитиприваципараметерс** содержит сведения об использовании анонимных удостоверений во время аутентификации PEAP.


```XML
<xs:complexType name="IdentityPrivacyParameters">
    <xs:sequence>
        <xs:element name="EnableIdentityPrivacy"
            type="xs:boolean"
            minOccurs="0"
        />
        <xs:element name="AnonymousUserName"
            type="xs:string"
            minOccurs="0"
        />
    </xs:sequence>
</xs:complexType>
```





| Элемент                                                                                                               | Тип    | Описание                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**енаблеидентитиприваци**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | Логическое | Указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение.                                                                                                                                                                                                                                                                           |
| [**анонимаусусернаме**](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | строка  | содержит анонимное удостоверение, используемое вместо истинной идентификации пользователя. Он отправляется во время первого этапа проверки подлинности PEAP, когда **удостоверение** отправляется в виде обычного текста. Использование анонимных удостоверений определяется элементом [**енаблеидентитиприваци**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) . |



 

## <a name="remarks"></a>Remarks

Элемент Идентитиприваципараметерс является необязательным.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Сложные типы mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




