---
title: Еафостусеркредентиалс, элемент
description: Содержит элемент Еапмесод, а также учетные данные или элемент Кредентиалсблоб.
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- Элемент Еафостусеркредентиалс EAPHost
topic_type:
- apiref
api_name:
- EapHostUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 690770091219e51b3ebb550a1a72e50f76b20542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136694"
---
# <a name="eaphostusercredentials-element"></a>Еафостусеркредентиалс, элемент

Элемент **еафостусеркредентиалс** содержит элемент [**еапмесод**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) , а также [**учетные данные**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) или элемент [**кредентиалсблоб**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) .

``` syntax
<xs:element name="EapHostUserCredentials">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Credentials"
                    type="BaseEapMethodUserCredentials"
                 />
                <xs:element name="CredentialsBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                | Тип                                                                                                                | Описание                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Учетные данные**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [**басиапмесодусеркредентиалс**](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | Используется, когда конфигурация метода находится в текстовом формате XML вместо двоичного BLOB-объекта.<br/>   |
| [**кредентиалсблоб**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | hexBinary                                                                                                           | Используется, когда конфигурация метода является двоичным BLOB-объектом, а не в текстовом формате XML.<br/> |
| [**еапмесод**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [**еапмесодтипе**](eapcommonschema-eapmethodtype-complextype.md)                                                  | Определяет метод, на который указывает ссылка. <br/>                                             |



## <a name="remarks"></a>Комментарии

Элементы [**Credential**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) и [**кредентиалсблоб**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) нельзя одновременно использовать одновременно.

Существует точка расширения для других пространств имен.

Элемент **processContents** обеспечивает будущие улучшения схемы. Элемент **processContents** является необязательным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема еафостусеркредентиалс](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





