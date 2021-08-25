---
description: Содержит сведения о форматировании горизонтальных линий, используемых для бланков в заметке журнала.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Горизонтальный элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacadf35cca5e5f14f413ac857c4a6f3421d7ee8f5f2dc95d24cea9c7f0f6bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940647"
---
# <a name="horizontal-element"></a>Горизонтальный элемент

Содержит сведения о форматировании горизонтальных линий, используемых для бланков в заметке журнала.

## <a name="definition"></a>Определение

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
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
<li>Тип Double</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Цвет</strong></td>
<td><a href="colortype-simple-type.md"><strong>Колортипе</strong></a> simpleType</td>
<td>Необязательный</td>
<td>Цвет элемента.</td>
<td>Шестнадцатеричное значение RGB. Соответствует следующему регулярному выражению: # [0-9a-zA-Z] {6} . Например, #4a79B5.<br/></td>
</tr>
<tr class="odd">
<td><strong>спаЦингбефоре</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Необязательный</td>
<td>Отступ перед элементом.</td>
<td>Любое неотрицательное целое число.</td>
</tr>
<tr class="even">
<td><strong>спаЦингбетвин</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Необязательный</td>
<td>Интервал между этим элементом и окружающими его элементами.</td>
<td>Любое неотрицательное целое число.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Сведения об элементе



|  Элемент     | Значение                                                     |
|--------------|-------------------------------------------------------------------|
| Тип элемента | [**Хоризонталтипе complexType**](horizontaltype-complex-type.md) |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк                        |
| Имя схемы  | Средство чтения журнала                                                    |



 

 

 




