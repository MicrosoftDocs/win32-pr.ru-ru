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
ms.openlocfilehash: 125b5fa2cab8bf3f9da12bd842a1a102beee3fb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071046"
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
| [**Config**](eaphostconfigschema-config-eaphostconfig-element.md)         | [**басиапмесодконфиг**](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | Используется, когда конфигурация метода находится в текстовом формате XML вместо двоичного BLOB-объекта.<br/>       |
| [**конфигблоб**](eaphostconfigschema-configblob-eaphostconfig-element.md) | hexBinary                                                                                | Используется, когда конфигурация метода находится в двоичном виде двоичного объекта, а не в виде строки текста.<br/> |
| [**еапмесод**](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [**еапмесодтипе**](eapcommonschema-eapmethodtype-complextype.md)                       | Определяет метод, на который указывает ссылка. <br/>                                                 |



## <a name="remarks"></a>Комментарии

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

[Схема еафостконфиг](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





