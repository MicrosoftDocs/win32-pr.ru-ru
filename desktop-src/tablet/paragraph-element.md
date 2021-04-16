---
description: Содержит абзац.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Элемент абзаца (Windows.ui.xaml.docументс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Paragraph
api_type:
- HeaderDef
api_location:
- windows.ui.xaml.documents.h
ms.openlocfilehash: bfe3752541bb54571e9802f557e83dcc7632f845
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656879"
---
# <a name="paragraph-element"></a>Элемент абзаца

Содержит абзац.

## <a name="definition"></a>Определение

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Родительские элементы

[**Содержани**](content-element--journal-reader.md)

[**граупноде**](groupnode-element.md)

## <a name="child-elements"></a>Дочерние элементы

[**Штрих**](line-element.md)

[**параграфлинеметрикс**](paragraphlinemetrics-element.md)

## <a name="attributes"></a>Атрибуты



| attribute       | Тип                      | Обязательно | Описание                                                                             | Возможные значения           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Слева**        | **xs:integer**            | Обязательно | Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента. | Любое целое число.              |
| **Top**         | **xs:integer**            | Обязательно | Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.  | Любое целое число.              |
| **Width**       | **xs:nonNegativeInteger** | Обязательно | Ширина ограничивающего прямоугольника для элемента.                                          | Любое неотрицательное целое число. |
| **Height**      | **xs:nonNegativeInteger** | Обязательно | Высота ограничивающего прямоугольника для элемента.                                         | Любое неотрицательное целое число. |
| **блоккнумбер** | **xs:nonNegativeInteger** | Обязательно | Номер блока.                                                                           | Любое неотрицательное целое число. |
| **LineNumber**  | **xs:nonNegativeInteger** | Обязательно | Строка, с которой начинается абзац.                                                 | Любое неотрицательное целое число. |



 

## <a name="element-information"></a>Сведения об элементе



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| Тип элемента | [**Параграфтипе**](paragraphtype-complex-type.md) complexType |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк                      |
| Имя схемы  | Средство чтения журнала                                                  |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Windows.ui.xaml.docументс. h</dt> </dl> |



 

 




