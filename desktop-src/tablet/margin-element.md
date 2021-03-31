---
description: Определяет линии полей, нарисованные на странице.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Элемент Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0500d4db165012393cb600c1e118089b68c76695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272625"
---
# <a name="margin-element"></a>Элемент Margin

Определяет линии полей, нарисованные на странице.

## <a name="definition"></a>Определение

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a>Родительские элементы

Отсутствует.

## <a name="child-elements"></a>Дочерние элементы

Нет..

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Тип</th>
<th>Обязательно</th>
<th>Описание</th>
<th>Возможные значения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Style</strong></td>
<td><a href="linelayoutstyletype-simple-type.md"><strong>Линелайаутстилетипе</strong></a> simpleType</td>
<td>Обязательно</td>
<td>Указывает тип рисуемой линии.</td>
<td><ul>
<li>Нет</li>
<li>Сплошная</li>
<li>Штрих</li>
<li>Точки</li>
<li>DashDot</li>
<li>DashDotDot</li>
<li>Double</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Цвет</strong></td>
<td><a href="colortype-simple-type.md"><strong>Колортипе</strong></a> simpleType</td>
<td>Необязательно</td>
<td>Цвет элемента.</td>
<td>Шестнадцатеричное значение RGB. Соответствует следующему регулярному выражению: # [0-9a-zA-Z] {6} . Например, #4a79B5.<br/></td>
</tr>
<tr class="odd">
<td><strong>Тип</strong></td>
<td><a href="margintypetype-simple-type.md"><strong>Маргинтипетипе</strong></a> simpleType</td>
<td>Необязательно</td>
<td>Показывает левое или правое поле.</td>
<td><ul>
<li>Левый</li>
<li>Правый</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Интервал</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Необязательно</td>
<td>Интервал между границами страницы и поля.</td>
<td>Любое неотрицательное целое число.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Сведения об элементе



|              |                                                           |
|--------------|-----------------------------------------------------------|
| Тип элемента | [**Маргинтипе**](margintype-complex-type.md) complexType |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк                |
| Имя схемы  | Средство чтения журнала                                            |



 

 

 




