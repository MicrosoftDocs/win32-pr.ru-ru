---
description: Контейнер для одного или нескольких отдельных элементов Пропертидескриптион.
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: пропертидескриптионлист
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd0beaf4dbbd8b71c7f4b3335c169754c704d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647263"
---
# <a name="propertydescriptionlist"></a>пропертидескриптионлист

Контейнер для одного или нескольких отдельных элементов [пропертидескриптион](./propdesc-schema-propertydescription.md) . Файл схемы описания свойства. пропдеск должен содержать хотя бы один элемент [пропертидескриптионлист]() .

## <a name="syntax"></a>Синтаксис


```
<!-- propertyDescriptionList -->
<xs:element name="propertyDescriptionList">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="s:propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string" use="required"/>
        <xs:attribute name="product"   type="xs:string" use="required"/>
    </xs:complexType>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_formatid_and_propid">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@formatID"/>
        <xs:field    xpath="@propID"/>
    </xs:unique>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_canonical_name">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@name"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                        | Дочерние элементы                                                   |
|---------------------------------------|------------------------------------------------------------------|
| [schema](./propdesc-schema-entry.md) | [пропертидескриптион](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a>Атрибуты



| Атрибут | Описание                                                               |
|-----------|---------------------------------------------------------------------------|
| publisher | Общедоступный. Обязательный. Отображаемое имя издателя, предоставляющего схему. |
| product   | Общедоступный. Обязательный. Отображаемое имя продукта, предоставляющего схему.   |



 

## <a name="remarks"></a>Комментарии

[Пропертидескриптионлист]() не следует путать с "списками свойств" и [**ипропертидескриптионлист**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), которые полностью отделены друг от друга.

 

 
