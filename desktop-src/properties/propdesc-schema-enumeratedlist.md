---
description: 'Указывает, как Ипропертидескриптион:: Форматфордисплай должен форматировать значение свойства в виде строки.'
ms.assetid: 49ba57b8-3e08-425f-98b2-52ed2c41a488
title: енумератедлист
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d098b47463b65c483be68eb7750da929df43cee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702254"
---
# <a name="enumeratedlist"></a>енумератедлист

Указывает, как [**ипропертидескриптион:: форматфордисплай**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) должен форматировать значение свойства в виде строки. Он также влияет на то, как свойство может быть сгруппировано, или какие значения должны отображаться в списке, если "Едитконтрол" является листблокс. Это применимо только в том случае <displayInfo displayType="Enumerated"> , если. Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [енумератедлист]() .

При наличии нескольких элементов используется последний из них. Если элемент [енумератедлист]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.

## <a name="syntax"></a>Синтаксис


```
<!-- enumeratedList -->
<xs:element name="enumeratedList"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="value" type="xs:string" use="required"/>
                    <xs:attribute name="text" type="xs:string" use="required"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="minValue" type="xs:integer" use="required"/>
                    <xs:attribute name="setValue" type="xs:integer"/>
                    <xs:attribute name="text" type="xs:string"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
        <xs:attribute name="defaultText" type="xs:string"/>
        <xs:attribute name="useValueForDefault" type="xs:boolean"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                   | Дочерние элементы                               |
|--------------------------------------------------|----------------------------------------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | [enum](./propdesc-schema-enum.md)           |
|                                                  | [енумранже](./propdesc-schema-enumrange.md) |



 

## <a name="attributes"></a>Атрибуты



| Атрибут          | Описание                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| defaultText        | Общедоступный. Необязательный элемент. Укажите текст по умолчанию, который будет использоваться при присвоении значения [**ипропертидескриптион:: форматфордисплай**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) , не сопоставляемого с одним из перечисляемых элементов в списке. Синтаксис допускает прямую отображаемую строку или ссылку на непрямо отображаемую строку; Используйте ссылку, чтобы ее можно было локализовать.                              |
| усевалуефордефаулт | Общедоступный. Необязательный элемент. Если задать для этого параметра значение "true", [**ипропертидескриптион:: форматфордисплай**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) будет использовать значение "как есть", если оно не соответствует одному из перечисляемых элементов в списке. Для **ипропертидескриптион:: форматфордисплай** присвоение этому параметру значения "true" имеет приоритет над заданием "defaultText". Значение по умолчанию — «false». |



 

 

 
