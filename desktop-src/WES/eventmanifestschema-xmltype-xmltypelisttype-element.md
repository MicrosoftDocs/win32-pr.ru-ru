---
title: xmlType (Ксмлтипелисттипе), элемент
description: Определяет тип XML.
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- Журнал событий элемента xmlType
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 119ebe7f09f86aa46d9e80380670309fe8734fa818b48049d5dffc29e6a2ebb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863284"
---
# <a name="xmltype-xmltypelisttype-element"></a>xmlType (Ксмлтипелисттипе), элемент

Определяет тип XML.

``` syntax
<xs:element name="xmlType">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="XmlType"
            >
                <xs:attribute name="name"
                    type="QName"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="symbol"
                    type="string"
                    use="required"
                 />
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

Элемент **xmlType** определяется сложным типом [**ксмлтипелисттипе**](eventmanifestschema-xmltypelisttype-complextype.md) .

## <a name="attributes"></a>Атрибуты



| Имя   | Тип      | Описание                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName** | Имя типа выходных данных.<br/>                                                                                                                                                                                                                    |
| символ | строка    | Символ, используемый для ссылки на тип выходных данных в приложении. [**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ, чтобы создать константу для типа выходных данных в файле заголовка, создаваемом компилятором.<br/> |
| value  | строка    | Целочисленное значение, уникально идентифицирующее тип вывода в списке определяемых типов выходных данных.<br/>                                                                                                                                          |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**Ксмлтипес (Типелисттипе)**](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





