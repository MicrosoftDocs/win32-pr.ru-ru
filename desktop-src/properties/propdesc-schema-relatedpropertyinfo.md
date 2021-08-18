---
description: новое для Windows 7. Элемент container для элементов relatedProperty.
ms.assetid: F8BAAE5C-A7EA-487a-B829-91A27E24B58D
title: релатедпропертинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 203c6e0e65943e90c6106f5e49e1792e6b47345a930f5368bd22df3a1c03885d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970963"
---
# <a name="relatedpropertyinfo"></a>релатедпропертинфо

новое для Windows 7. Элемент container для элементов [relatedProperty](./propdesc-schema-relatedproperty.md) . Для каждого элемента [пропертидескриптион](./propdesc-schema-propertydescription.md) должен быть только один элемент [релатедпропертинфо]() .

## <a name="syntax"></a>Синтаксис


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedPropertyInfo">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
                    <xs:attribute name="propertyName" type="canonical-name" use="required"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:unique name="No_two_relatedProperties_can_have_the_same_relationship_name">
        <xs:selector xpath="s:relatedProperty"/>
        <xs:field    xpath="@relationshipName"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                   | Дочерние элементы                                           |
|------------------------------------------------------------------|----------------------------------------------------------|
| [пропертидескриптион](./propdesc-schema-propertydescription.md) | [relatedProperty](./propdesc-schema-relatedproperty.md) |



 

## <a name="attributes"></a>Атрибуты

Этот элемент не содержит атрибуты.

 

 
