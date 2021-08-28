---
description: Указывает, какой элемент управления следует использовать при изменении свойства.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: едитконтрол
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213d6fba3f03f90e0d5a2702226dd8596462b289
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626819"
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
| [displayInfo](./propdesc-schema-displayinfo.md) | None           |



 

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Атрибут</th>
<th>Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>управляющие</td>
<td>Общедоступный. Необязательный элемент. Значение по умолчанию — &quot; Default &quot; . Допустимы следующие значения. 
<table>
<colgroup>
<col  />
<col  />
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
<th>Тип</th>
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
<td>Дата и время</td>
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
<td>текст</td>
<td>Использует элемент управления редактированием текста.</td>
</tr>
<tr class="odd">
<td>иконлист</td>
<td><strong>Windows 7 и более поздней версии.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
