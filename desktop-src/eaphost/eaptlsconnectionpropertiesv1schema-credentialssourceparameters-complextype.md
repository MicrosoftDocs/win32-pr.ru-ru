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
ms.openlocfilehash: 881cd4225c0e7e2f557ad7206176224a0b3929cdac7398b29f30382506f816ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274011"
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



## <a name="remarks"></a>Remarks

Элементы [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) и [**смарт-карты**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) не могут одновременно использоваться одновременно.

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

[Сложные типы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





