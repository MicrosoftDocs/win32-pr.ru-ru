---
title: Сложный тип Кредентиалссаурцепараметерс
description: Определяет элемент, необходимый для указания источника сертификата, используемого с проверкой подлинности EAP-TLS.
ms.assetid: 1482694e-3025-4231-8154-4be0301fe5ce
keywords:
- Кредентиалссаурцепараметерс сложный тип EAPHost
topic_type:
- apiref
api_name:
- CredentialsSourceParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 912faa4a388d9a57225991959625a978ca0921f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136691"
---
# <a name="credentialssourceparameters-complex-type"></a>Сложный тип Кредентиалссаурцепараметерс

Сложный тип **кредентиалссаурцепараметерс** определяет элемент, необходимый для указания источника сертификата, который будет использоваться с проверкой подлинности EAP-TLS.

Существует возможность выбора между элементом [**смарт-карты**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) или элементом [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) .

``` syntax
<xs:complexType name="CredentialsSourceParameters">
    <xs:choice>
        <xs:element name="SmartCard"
            type="emptyString"
         />
        <xs:element name="CertificateStore"
            type="CertSelection"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                             | Тип                                                                                  | Описание                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ИмяХранилищаСертификатов**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) | [**цертселектион**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) | Указывает, что EAP-TLS должен прочитать сертификат из моего хранилища пользователя или проверить подлинность компьютера. <br/> |
| [**Карте**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)               | [**emptyString**](eaptlsconnectionpropertiesv1schema-emptystring-simpletype.md)      | Указывает, что EAP-TLS должен считывать сертификат из смарт-карты. <br/>                                          |



## <a name="remarks"></a>Комментарии

Элементы [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) и [**смарт-карты**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) не могут одновременно использоваться одновременно.

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

[Сложные типы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





