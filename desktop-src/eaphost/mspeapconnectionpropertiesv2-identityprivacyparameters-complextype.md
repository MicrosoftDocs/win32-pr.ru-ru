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
ms.openlocfilehash: 8360065e2ce124531bec63637e2b6560cfc32f54
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104133370"
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



 

## <a name="remarks"></a>Комментарии

Элемент Идентитиприваципараметерс является необязательным.

## <a name="related-topics"></a>См. также

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Сложные типы mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




