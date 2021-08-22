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
ms.openlocfilehash: e30ca23a0e4ab0168ff7479a5246acfb4b34e3a43bc62886d988d5f54549672b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620324"
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



## <a name="remarks"></a>Remarks

\\файл Include \\Winmeta.xml, включенный в Windows SDK, содержит список предопределенных типов вывода.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





