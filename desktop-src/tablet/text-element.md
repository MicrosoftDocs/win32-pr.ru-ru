---
description: Содержит текстовую информацию из заметки журнала.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Элемент Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c72fe584d0e796d4a6f897297aa60bbeddc5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999424"
---
# <a name="text-element"></a>Элемент Text

Содержит текстовую информацию из заметки журнала.

## <a name="definition"></a>Определение

При использовании с [**содержимым**](content-element--journal-reader.md):

``` syntax
<xs:element name="Text" type="TextType" />
```

Или при использовании с [**титлеинфо**](titleinfo-element.md) и [**граупноде**](groupnode-element.md):

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a>Родительские элементы

[**Содержани**](content-element--journal-reader.md)

[**граупноде**](groupnode-element.md)

[**титлеинфо**](titleinfo-element.md)

## <a name="child-elements"></a>Дочерние элементы

Отсутствует.

## <a name="attributes"></a>Атрибуты

При использовании с [**титлеинфо**](titleinfo-element.md) и [**граупноде**](groupnode-element.md)атрибуты не используются. При использовании с [**содержимым**](content-element--journal-reader.md)атрибуты выглядят следующим образом.



| attribute  | Тип                      | Обязательно | Описание                                                                             | Возможные значения           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Слева**   | **xs:integer**            | Обязательно | Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента. | Любое целое число.              |
| **Top**    | **xs:integer**            | Обязательно | Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.  | Любое целое число.              |
| **Width**  | **xs:nonNegativeInteger** | Обязательно | Ширина ограничивающего прямоугольника для элемента.                                          | Любое неотрицательное целое число. |
| **Height** | **xs:nonNegativeInteger** | Обязательно | Высота ограничивающего прямоугольника для элемента.                                         | Любое неотрицательное целое число. |



 

## <a name="element-information"></a>Сведения об элементе



|              |                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Тип элемента | [**Тексттипе**](texttype-complex-type.md) complexType (с элементом Content) или **xs: String** (с элементами [**граупноде**](groupnode-element.md) и [**титлеинфо**](titleinfo-element.md) ) |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк<br/>                                                                                                                                               |
| Имя схемы  | Средство чтения журнала<br/>                                                                                                                                                                           |



 

 

 




