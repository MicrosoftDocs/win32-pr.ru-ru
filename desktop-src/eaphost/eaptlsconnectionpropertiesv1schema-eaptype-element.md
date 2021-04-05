---
title: Еаптипе, элемент
description: Является производным типом элемента Еаптипе из схемы Басиапконнектионпропертиес. | Еаптипе, элемент
ms.assetid: cf92d500-f815-48e2-a7d5-1364cb13a1f0
keywords:
- Элемент Еаптипе EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d1fdb4026c72b99bf2434a9fd6937743a9edb40
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000117"
---
# <a name="eaptype-element"></a>Еаптипе, элемент

Элемент **еаптипе** является производным типом элемента [**Еаптипе**](baseeapconnectionpropertiesv1schema-eaptype-element.md) из схемы [басиапконнектионпропертиес](baseeapconnectionpropertiesv1schema-schema.md) .

Этот производный элемент **еаптипе** содержит следующие элементы: [**кредентиалссаурце**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**сервервалидатион**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**дифферентусернаме**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**перформсервервалидатион**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)и [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="CredentialsSource"
                        type="CredentialsSourceParameters"
                        minOccurs="0"
                     />
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="DifferentUsername"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: PerformServerValidation"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: AcceptServerName"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: TLSExtensions"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                                               | Тип                                                                                                              | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Екстендедтлс: Перформсервервалидатион**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |                                                                                                                   | Windows 7 и более поздние версии: указывает, выполняется ли проверка сервера.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Екстендедтлс: Акцептсервернаме**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)              |                                                                                                                   | Windows 7 и более поздние версии: указывает, считывается ли имя сервера.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Екстендедтлс: Тлсекстенсионс**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)                  |                                                                                                                   | Windows 7 и более поздние версии: включает будущие улучшения схемы.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**кредентиалссаурце**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)                                     | [**кредентиалссаурцепараметерс**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) | Содержит сведения о расположении сертификата безопасности EAP-TLS. <br/> Элемент [**кредентиалссаурце**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) является необязательным.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**дифферентусернаме**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)                                     | Логическое                                                                                                           | Определяет, какое имя пользователя использует EAP-TLS. <br/> Если элемент [**дифферентусернаме**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) имеет **значение true**, то EAP-TLS должен использовать имя пользователя, отличное от имени, которое отображается в сертификате. Если элемент [**дифферентусернаме**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) имеет **значение false**, то EAP-TLS использует имя пользователя, которое отображается в сертификате.<br/> Элемент [**дифферентусернаме**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) является необязательным. <br/> |
| [**сервервалидатион**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)                                       | [**сервервалидатионпараметерс**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)   | Содержит сведения о выполнении проверки сервера. Элемент [**сервервалидатион**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) является необязательным. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Элементы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





