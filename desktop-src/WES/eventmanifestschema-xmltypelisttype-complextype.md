---
title: Сложный тип Ксмлтипелисттипе
description: Определяет выходные типы списка, которые служба использует для определения способа визуализации входного типа данных.
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- Журнал событий сложных типов Ксмлтипелисттипе
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 388161572ec9c84ed46d5b40987df5fb8d1ed077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340795"
---
# <a name="xmltypelisttype-complex-type"></a>Сложный тип Ксмлтипелисттипе

Определяет выходные типы списка, которые служба использует для определения способа визуализации входного типа данных.

``` syntax
<xs:complexType name="XmlTypeListType">
    <xs:sequence>
        <xs:element name="xmlType"
            minOccurs="0"
            maxOccurs="unbounded"
        >
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
                            type="CSymbolType"
                            use="required"
                         />
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                | Тип | Описание                      |
|------------------------------------------------------------------------|------|----------------------------------|
| [**xmlType**](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | Определяет тип XML. <br/> |



## <a name="attributes"></a>Атрибуты



| Имя   | Тип                                                              | Описание                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName**                                                         | Имя типа выходных данных.<br/>                                                                                                                                                                                                                    |
| символ | [**ксимболтипе**](eventmanifestschema-csymboltype-simpletype.md) | Символ, используемый для ссылки на тип выходных данных в приложении. [**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ, чтобы создать константу для типа выходных данных в файле заголовка, создаваемом компилятором.<br/> |
| value  | строка                                                            | Целочисленное значение, уникально идентифицирующее тип вывода в списке определяемых типов выходных данных.<br/>                                                                                                                                          |



## <a name="remarks"></a>Комментарии

\\Файл Include \\Winmeta.xml, включенный в Windows SDK, содержит список предопределенных типов вывода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





