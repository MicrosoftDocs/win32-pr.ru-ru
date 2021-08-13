---
title: Еафостконфиг, элемент
description: Содержит элемент Еапмесод и элемент конфигурации или Конфигблоб. Элементы config и Конфигблоб не могут одновременно использоваться одновременно.
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- Элемент Еафостконфиг EAPHost
topic_type:
- apiref
api_name:
- EapHostConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c34ddd1607a59c0425f7ec789bedb4981a05983ead276a14308fbf6aaadf26de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274868"
---
# <a name="eaphostconfig-element"></a>Еафостконфиг, элемент

Элемент **еафостконфиг** содержит элемент [**Еапмесод**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) и элемент [**config**](eaphostconfigschema-config-eaphostconfig-element.md) или [**конфигблоб**](eaphostconfigschema-configblob-eaphostconfig-element.md) .

Элементы [**config**](eaphostconfigschema-config-eaphostconfig-element.md) и [**конфигблоб**](eaphostconfigschema-configblob-eaphostconfig-element.md) не могут одновременно использоваться одновременно.

``` syntax
<xs:element name="EapHostConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Config"
                    type="BaseEapMethodConfig"
                 />
                <xs:element name="ConfigBlob"
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



| Элемент                                                                    | Тип                                                                                     | Описание                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Файле**](eaphostconfigschema-config-eaphostconfig-element.md)         | [**басиапмесодконфиг**](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | Используется, когда конфигурация метода находится в текстовом формате XML вместо двоичного BLOB-объекта.<br/>       |
| [**конфигблоб**](eaphostconfigschema-configblob-eaphostconfig-element.md) | hexBinary                                                                                | Используется, когда конфигурация метода находится в двоичном виде двоичного объекта, а не в виде строки текста.<br/> |
| [**еапмесод**](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [**еапмесодтипе**](eapcommonschema-eapmethodtype-complextype.md)                       | Определяет метод, на который указывает ссылка. <br/>                                                 |



## <a name="remarks"></a>Remarks

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

[Схема еафостконфиг](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





