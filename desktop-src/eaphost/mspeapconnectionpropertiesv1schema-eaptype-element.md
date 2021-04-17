---
title: Элемент Еаптипе (mspeapconnectionpropertiesv1schema)
description: Этот элемент является производным типом элемента Еаптипе из схемы Басиапконнектионпропертиес. Для mspeapconnectionpropertiesv1schema.
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
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
ms.openlocfilehash: 3336e943170afa0ec1f239d4cf7a0c603a0c8e71
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187753"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a>Элемент Еаптипе (mspeapconnectionpropertiesv1schema)

Элемент **еаптипе** является производным типом элемента [**Еаптипе**](baseeapconnectionpropertiesv1schema-eaptype-element.md) из схемы [басиапконнектионпропертиес](baseeapconnectionpropertiesv1schema-schema.md) .

Этот производный элемент **еаптипе** содержит следующие элементы: [**сервервалидатион**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**идентитиприваци**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**иннереапоптионал**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md), [**енаблекуарантинечеккс**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) и [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).

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
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="IdentityPrivacy"
                        type="IdentityPrivacyParameters"
                        minOccurs="0"
                     />
                    <xs:element name="FastReconnect"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="InnerEapOptional"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="EnableQuarantineChecks"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="RequireCryptoBinding"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                     | Тип                                                                                                            | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Протокола**](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | Описывает внутренний метод и конфигурацию метода. Если элемент [**иннереапоптионал**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) имеет значение true, должен присутствовать элемент [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) . Если элемент [**иннереапоптионал**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) имеет значение false, то элемент [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) должен отсутствовать.<br/>           |
| [**енаблекуарантинечеккс**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | Логическое                                                                                                         | Указывает, следует ли выполнять проверки защиты доступа к сети (NAP). Если элемент [**енаблекуарантинечеккс**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) имеет значение true, PEAP ВЫПОЛНЯЕТ проверки NAP; Если значение FALSE PEAP не будет выполнять проверки защиты доступа к сети. Элемент [**енаблекуарантинечеккс**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) является необязательным.<br/>                                                                                |
| [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | Логическое                                                                                                         | Указывает, следует ли выполнять быстрое повторное подключение. Если элемент [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) имеет значение true, то PEAP пытается выполнить быстрое повторное подключение. Если значение равно FALSE, PEAP выполняет полную проверку подлинности. Элемент [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) является необязательным.<br/>                                                                                                                       |
| [**идентитиприваци**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [**идентитиприваципараметерс**](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | Windows 7 или более поздней версии: указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение. Элемент [**идентитиприваци**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) является необязательным.<br/>                                                                                                                                                                                                                                                                                 |
| [**иннереапоптионал**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | Логическое                                                                                                         | Указывает, следует ли выполнять гостевой доступ. Если элемент [**иннереапоптионал**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) имеет значение true, то должен присутствовать элемент [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) , описывающий внутренний метод и его конфигурацию. Если задано значение FALSE, PEAP выполняет гостевой доступ. Элемент [**иннереапоптионал**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) является необязательным.<br/>            |
| [**пеапекстенсионс**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | Элемент [**пеапекстенсионс**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) обеспечивает будущие улучшения схемы. Элемент [**пеапекстенсионс**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) является необязательным.<br/>                                                                                                                                                                                                                                    |
| [**рекуирекриптобиндинг**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | Логическое                                                                                                         | Указывает, следует ли выполнять проверку подлинности на серверах, поддерживающих криптобиндинг. Если элемент [**рекуирекриптобиндинг**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) имеет значение true, PEAP будет проходить проверку подлинности на серверах, не поддерживающих криптобиндинг. Если значение равно FALSE, PEAP будет проходить проверку подлинности только на серверах, поддерживающих криптобиндинг. Элемент [**рекуирекриптобиндинг**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) является необязательным.<br/> |
| [**сервервалидатион**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [**сервервалидатионпараметерс**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | Содержит сведения о выполнении проверки сервера. Элемент [**сервервалидатион**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) является необязательным.<br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Элементы схемы mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





