---
description: Описывает одно уникальное каноническое свойство.
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: пропертидескриптион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233f6d9b1242a9f02b2edbb2bb29cefaef625c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991544"
---
# <a name="propertydescription"></a>пропертидескриптион

Описывает одно уникальное каноническое свойство. Каждое такое свойство, предназначенное для доступа в системе, должно иметь соответствующий элемент [пропертидескриптион]() .

## <a name="syntax-for-windows-7"></a>Синтаксис для Windows 7


```
<!-- propertyDescription for Windows 7-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
            <xs:element ref="relatedPropertyInfo" minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="propid" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-vista"></a>Синтаксис для Vista


```
<!-- propertyDescription for Windows Vista-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                           | Дочерние элементы                                                   |
|--------------------------------------------------------------------------|------------------------------------------------------------------|
| [пропертидескриптионлист](./propdesc-schema-propertydescriptionlist.md) | [сеарчинфо](./propdesc-schema-searchinfo.md)                   |
|                                                                          | [лабелинфо](./propdesc-schema-labelinfo.md)                     |
|                                                                          | [typeInfo](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [aliasInfo](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [displayInfo](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [релатедпропертинфо](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a>Атрибуты



| Атрибут | Описание                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name      | Обязательный. Каноническое имя свойства, уникальное для системы; Например, `System.Rating` . Эта строка имеет тип канонического типа и ограничена 64 символами. Имя чувствительно к регистру и должно использовать следующий синтаксис: Publisher. Application. PropertyName. [**Ипропертидескриптион:: жетканоникалнаме**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) возвращает это значение. |
| форматид  | Обязательный. Идентификатор формата свойства (FMTID). Значение должно включать заключенные в фигурные скобки. Например, `{64440492-4C8B-11D1-8B70-080036B11A03}` . [**Ипропертидескриптион:: жетпропертикэй**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) возвращает это значение.                                                                                                                       |
| propID    | Обязательный. Идентификатор свойства (PID); Например, `9` . [**Ипропертидескриптион:: жетпропертикэй**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) возвращает это значение. Это значение должно быть больше или равно 2. Значения 0 и 1 зарезервированы системой.                                                                                                                  |



 

 

 
