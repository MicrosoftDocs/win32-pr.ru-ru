---
description: Содержит набор элементов&\# 8212; Абзац, Инкворд, Drawing, Text, Image или Flag&\# 8212;, которые группируются вместе в заметке журнала.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Граупноде, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ee141691ef58d14e6c08a49544e9cf3ecf7540b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647186"
---
# <a name="groupnode-element"></a>Граупноде, элемент

Содержит набор элементов ([**абзац**](paragraph-element.md), [**инкворд**](inkword-element.md), [**Рисование**](drawing-element.md), [**текст**](text-element.md), [**изображение**](image-element.md)или [**флаг**](flag-element.md)), которые группируются в заметке журнала.

## <a name="definition"></a>Определение

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a>Родительские элементы

[**Содержани**](content-element--journal-reader.md)

## <a name="child-elements"></a>Дочерние элементы

[**Paragraph**](paragraph-element.md)

[**инкворд**](inkword-element.md)

[**Рисование**](drawing-element.md)

[**Полнотекстовым**](text-element.md)

[**Образ**](docimage-element.md)

[**Flag**](flag-element.md)

## <a name="attributes"></a>Атрибуты



| attribute  | Тип                      | Обязательно | Описание                                                                             | Возможные значения           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Слева**   | **xs:integer**            | Обязательно | Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента. | Любое целое число.              |
| **Top**    | **xs:integer**            | Обязательно | Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.  | Любое целое число.              |
| **Width**  | **xs:nonNegativeInteger** | Обязательно | Ширина ограничивающего прямоугольника для элемента.                                          | Любое неотрицательное целое число. |
| **Height** | **xs:nonNegativeInteger** | Обязательно | Высота ограничивающего прямоугольника для элемента.                                         | Любое неотрицательное целое число. |



 

## <a name="element-information"></a>Сведения об элементе



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| Тип элемента | [**Граупнодетипе**](groupnodetype-complex-type.md) complexType |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк                      |
| Имя схемы  | Средство чтения журнала                                                  |



 

 

 



