---
description: Указывает, какой элемент управления следует использовать при изменении свойства.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: едитконтрол
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966f9742082fd6b5f939941a956eaae1ac4e427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998592"
---
# <a name="editcontrol"></a>едитконтрол

Указывает, какой элемент управления следует использовать при изменении свойства. Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [едитконтрол]() .

При наличии нескольких элементов используется последний из них. Если элемент [едитконтрол]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.

Если <typeInfo isInnate="true"> значение равно, этот элемент игнорируется, так как свойство присущей не может быть изменено.

## <a name="syntax"></a>Синтаксис


```
<!-- editControl -->
<xs:element name="editControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                    <xs:enumeration value="IconList"/>
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
<td>Значение по умолчанию</td>
<td>По умолчанию. Использует элемент управления по умолчанию, основанный на <typeInfo type=&quot;&quot;> атрибуте. Типы по умолчанию перечислены ниже. Любой другой тип приводит к использованию &quot; &quot; элемента управления Text. 
<table>
<thead>
<tr class="header">
<th>Тип</th>
<th>Control</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Строка</td>
<td>Текст</td>
</tr>
<tr class="even">
<td>Строка (с несколькими значениями)</td>
<td>мултивалуетекст</td>
</tr>
<tr class="odd">
<td>Дата/время</td>
<td>Календарь</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Календарь</td>
<td>Использует элемент управления Calendar.</td>
</tr>
<tr class="odd">
<td>чеккбоксдроплист</td>
<td>Использует элемент управления "список" с флажками.</td>
</tr>
<tr class="even">
<td>дроплист</td>
<td>Использует элемент управления "раскрывающийся список".</td>
</tr>
<tr class="odd">
<td>мултилинетекст</td>
<td>Использует многострочный элемент управления "поле ввода".</td>
</tr>
<tr class="even">
<td>мултивалуетекст</td>
<td>Использует многозначный элемент управления "поле ввода".</td>
</tr>
<tr class="odd">
<td>Рейтинг</td>
<td>Использует элемент управления рейтингом «5 звезд».</td>
</tr>
<tr class="even">
<td>Текст</td>
<td>Использует элемент управления редактированием текста.</td>
</tr>
<tr class="odd">
<td>иконлист</td>
<td><strong>Windows 7 и более поздние версии.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
