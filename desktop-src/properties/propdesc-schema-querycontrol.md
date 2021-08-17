---
description: не поддерживается в Windows 7 и более поздних версиях. Указывает, какой элемент управления следует использовать в построителе запросов.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: куериконтрол
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f05800fc026c61a4ea50098fb1d8f4deb98d971c9eecfed478d71bd3c01033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823564"
---
# <a name="querycontrol"></a>куериконтрол

не поддерживается в Windows 7 и более поздних версиях. Указывает, какой элемент управления следует использовать в построителе запросов. Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [куериконтрол]() .

При наличии нескольких элементов используется последний из них. Если элемент [куериконтрол]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.

## <a name="syntax"></a>Синтаксис


```
<!-- queryControl -->
<xs:element name="queryControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="NumericText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                   | Дочерние элементы |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | Нет           |



 

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Атрибут</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>управляющие</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot; Default &quot; . Допустимы следующие значения. 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>По умолчанию</td>
<td>По умолчанию. Использует элемент управления по умолчанию, основанный на <typeInfo type=&quot;&quot;> атрибуте. Типы по умолчанию перечислены ниже. Любой другой тип приводит к использованию &quot; &quot; элемента управления Text. 
<table>
<thead>
<tr class="header">
<th>Исключением</th>
<th>Элемент</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Строка</td>
<td>Текстовый</td>
</tr>
<tr class="even">
<td>Строка (с несколькими значениями)</td>
<td>мултивалуетекст</td>
</tr>
<tr class="odd">
<td>Число или размер</td>
<td>нумериктекст</td>
</tr>
<tr class="even">
<td>Number или size (enum)</td>
<td>Список</td>
</tr>
<tr class="odd">
<td>Дата и время</td>
<td>Календарь</td>
</tr>
<tr class="even">
<td>Логический</td>
<td>Логический</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Логическое</td>
<td>Использует логический элемент управления.</td>
</tr>
<tr class="odd">
<td>Календарь</td>
<td>Использует элемент управления "Календарь".</td>
</tr>
<tr class="even">
<td>чеккбоксдроплист</td>
<td>Использует элемент управления "список" с флажками.</td>
</tr>
<tr class="odd">
<td>дроплист</td>
<td>Использует элемент управления "раскрывающийся список".</td>
</tr>
<tr class="even">
<td>мултивалуетекст</td>
<td>Использует многозначный элемент управления "поле ввода".</td>
</tr>
<tr class="odd">
<td>нумериктекст</td>
<td>Использует элемент управления числовым текстом.</td>
</tr>
<tr class="even">
<td>Рейтинг</td>
<td>Использует элемент управления рейтингом «5 звезд».</td>
</tr>
<tr class="odd">
<td>Текст</td>
<td>Использует элемент управления редактированием текста.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
