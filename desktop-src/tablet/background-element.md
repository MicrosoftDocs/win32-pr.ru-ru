---
description: Содержит фон элемента Жаурналдокумент или элемента Жаурналпаже.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Элемент Background
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46388d56c04fc24ecd578788eecf9926ef01a301
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436589"
---
# <a name="background-element"></a>Элемент Background

Содержит фон элемента [**жаурналдокумент**](journaldocument-element.md) или элемента [**жаурналпаже**](journalpage-element.md) .

## <a name="definition"></a>Определение

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a>Родительские элементы

[**Stationery**](stationery-element.md)

## <a name="child-elements"></a>Дочерние элементы

[**Изображение**](image-element.md)

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
<td><strong>xs:string</strong></td>
<td>Обязательно</td>
<td>Задает стиль фона.</td>
<td><ul>
<li>Нет</li>
<li>Сплошная</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Цвет</strong></td>
<td><a href="colortype-simple-type.md"><strong>Колортипе</strong></a> simpleType</td>
<td>Необязательный</td>
<td>Указывает цвет фона.</td>
<td>См. <a href="colortype-simple-type.md"><strong>колортипе</strong></a> simpleType.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Сведения об элементе



|                  | Значение                                                             |
|------------------|-------------------------------------------------------------------|
| **Тип элемента** | [**Баккграундтипе**](backgroundtype-complex-type.md) complexType |
| **Пространство имен**    | urn: schemas-microsoft-com: TabletPC: ричинк                        |
| **Имя схемы**  | Средство чтения журнала                                                    |



 

 

 



