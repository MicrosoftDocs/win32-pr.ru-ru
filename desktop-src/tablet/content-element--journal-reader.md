---
description: Содержит содержимое для страницы журнала.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Элемент Content [средство чтения журнала]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fec59601a91d63b09c703557b7c6cd28fd11620
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432156"
---
# <a name="content-element-journal-reader"></a>\[Средство чтения журнала элементов содержимого\]

Содержит содержимое для страницы журнала.

## <a name="definition"></a>Определение

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Родительские элементы

[**жаурналпаже**](journalpage-element.md)

## <a name="child-elements"></a>Дочерние элементы

[**граупноде**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**Рисование**](drawing-element.md)

[**Полнотекстовым**](text-element.md)

[**Изображение**](image-element.md)

[**Flag**](flag-element.md)

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
<th>поссиблевалуес</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Тип</strong></td>
<td><a href="contenttype-complex-type.md"><strong>ContentType, complexType</strong></a></td>
<td>Обязательно</td>
<td>Если тип — &quot; инерт &quot; , содержимое изменить нельзя.<br/></td>
<td><ul>
<li>Нормальный</li>
<li>инерт</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Сведения об элементе



|  Элемент     | Значение                                                     |
|--------------|-------------------------------------------------------------|
| Тип элемента | [**ContentType**](contenttype-complex-type.md) , complexType |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк                  |
| Имя схемы  | Средство чтения журнала                                              |



 

 

 




