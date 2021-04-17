---
description: Содержит сведения о названии заметки журнала.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Элемент Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2362e286482b329c50788b8eae4b4a30cbd1a125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693658"
---
# <a name="title-element"></a>Элемент Title

Содержит сведения о названии заметки журнала.

## <a name="definition"></a>Определение

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>Родительские элементы

[**Stationery**](stationery-element.md)

## <a name="child-elements"></a>Дочерние элементы

[**титлеареа**](titlearea-element.md)

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
<td><strong>xs:string</strong></td>
<td>Обязательно</td>
<td>Задает тип границы, окружающей заголовок примечания.</td>
<td><ul>
<li>Нет</li>
<li>солидскуаре</li>
<li>аутлинескуаре</li>
<li>солидраундрект</li>
<li>аутлинераундрект</li>
<li>солидраундректдоттедбаселине</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>датестиле</strong></td>
<td><strong>xs:string</strong></td>
<td>Обязательно</td>
<td>Определяет, содержит ли заголовок дату или нет.</td>
<td><ul>
<li>Нет</li>
<li>Short</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Цвет</strong></td>
<td><a href="colortype-simple-type.md"><strong>Колортипе simpleType</strong></a></td>
<td>Необязательно</td>
<td>Указывает цвет фона.</td>
<td>См. <a href="colortype-simple-type.md"><strong>Колортипе simpleType</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Сведения об элементе



|              |                                                         |
|--------------|---------------------------------------------------------|
| Тип элемента | [**Титлетипе**](titletype-complex-type.md) complexType |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк              |
| Имя схемы  | Средство чтения журнала                                          |



 

 

 



