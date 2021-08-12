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
ms.openlocfilehash: a18922ef19bd828067ddb0153aa7c6369ecfeebd0446f5a6481f91fa64ca21b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274424"
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



## <a name="remarks"></a>Remarks

Элементы [**Credential**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) и [**кредентиалсблоб**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) нельзя одновременно использовать одновременно.

Существует точка расширения для других пространств имен.

Элемент **processContents** обеспечивает будущие улучшения схемы. Элемент **processContents** является необязательным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема еафостусеркредентиалс](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





