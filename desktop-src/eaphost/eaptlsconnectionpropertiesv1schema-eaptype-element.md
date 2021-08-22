---
title: Элемент Еаптипе (eaptlsconnectionpropertiesv1schema)
description: Этот элемент является производным типом элемента Еаптипе из схемы Басиапконнектионпропертиес. Для eaptlsconnectionpropertiesv1schema.
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
ms.openlocfilehash: b7d448524c65e53ad9142d52786a651e085eddcfc7f3eb28bff558a38fc619fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785209"
---
# <a name="eaptype-element-eaptlsconnectionpropertiesv1schema"></a>Элемент Еаптипе (eaptlsconnectionpropertiesv1schema)

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
| [**Екстендедтлс: Перформсервервалидатион**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |                                                                                                                   | Windows 7 и более поздних версий: указывает, выполняется ли проверка сервера.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Екстендедтлс: Акцептсервернаме**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)              |                                                                                                                   | Windows 7 и более поздних версий: указывает, считывается ли имя сервера.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Екстендедтлс: Тлсекстенсионс**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)                  |                                                                                                                   | Windows 7 и более поздних версий: включает будущие улучшения схемы.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**кредентиалссаурце**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)                                     | [**кредентиалссаурцепараметерс**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) | Содержит сведения о расположении сертификата безопасности EAP-TLS. <br/> Элемент [**кредентиалссаурце**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) является необязательным.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**дифферентусернаме**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)                                     | Логическое                                                                                                           | Определяет, какое имя пользователя использует EAP-TLS. <br/> Если элемент [**дифферентусернаме**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) имеет **значение true**, то EAP-TLS должен использовать имя пользователя, отличное от имени, которое отображается в сертификате. Если элемент [**дифферентусернаме**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) имеет **значение false**, то EAP-TLS использует имя пользователя, которое отображается в сертификате.<br/> Элемент [**дифферентусернаме**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) является необязательным. <br/> |
| [**сервервалидатион**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)                                       | [**сервервалидатионпараметерс**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)   | Содержит сведения о выполнении проверки сервера. Элемент [**сервервалидатион**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) является необязательным. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Элементы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





