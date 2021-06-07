---
description: Содержит сведения, описывающие вертикальный компонент линий в бланке, который используется в заметке журнала. Используется, например, если в заметке есть линии сетки.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Вертикальный элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42565e6f2828c4ef27d1b28830502303a03e6f13
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432126"
---
# <a name="vertical-element"></a>Вертикальный элемент

Содержит сведения, описывающие вертикальный компонент линий в бланке, который используется в заметке журнала. Используется, например, если в заметке есть линии сетки.

## <a name="definition"></a>Определение

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Родительские элементы

[**линелайаут**](linelayout-element.md)

## <a name="child-elements"></a>Дочерние элементы

Отсутствует.

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
<td><strong>Стиль</strong></td>
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
<td><strong>спаЦингбефоре</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Необязательно</td>
<td>Отступ перед элементом.</td>
<td>Любое неотрицательное целое число.</td>
</tr>
<tr class="even">
<td><strong>спаЦингбетвин</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Необязательно</td>
<td>Интервал между этим элементом и окружающими его элементами.</td>
<td>Любое неотрицательное целое число.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Сведения об элементе



|  Элемент     | Значение                                                         |
|--------------|---------------------------------------------------------------|
| Тип элемента | [**Вертикалтипе**](verticaltype-complex-type.md) complexType |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк                    |
| Имя схемы  | Средство чтения журнала                                                |



 

 

 




