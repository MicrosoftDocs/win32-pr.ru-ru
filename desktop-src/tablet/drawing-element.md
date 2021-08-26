---
description: Содержит содержимое, классифицированное анализатором или пользователем в виде рисунка.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Элемент Drawing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d44eab0f9feec4b80369a365663917ca1aea0f211bba70dd4b99e9161316c662
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936594"
---
# <a name="drawing-element"></a>Элемент Drawing

Содержит содержимое, классифицированное анализатором или пользователем в виде рисунка.

## <a name="definition"></a>Определение

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Родительские элементы

[**Содержимое**](content-element--journal-reader.md)

[**граупноде**](groupnode-element.md)

## <a name="child-elements"></a>Дочерние элементы

[**скалартрансформ**](scalartransform-element.md)

[**канреклассифи**](canreclassify-element.md)

[**инккласс**](inkclass-element.md)

[**инкобжект**](inkobject-element.md)

## <a name="attributes"></a>Атрибуты



| attribute  | Тип                      | Обязательно | Описание                                                                             | Возможные значения           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Слева**   | **xs:integer**            | Обязательно | Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента. | Любое целое число.              |
| **Top**    | **xs:integer**            | Обязательно | Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.  | Любое целое число.              |
| **Width**  | **xs:nonNegativeInteger** | Обязательно | Ширина ограничивающего прямоугольника для элемента.                                          | Любое неотрицательное целое число. |
| **Height** | **xs:nonNegativeInteger** | Обязательно | Высота ограничивающего прямоугольника для элемента.                                         | Любое неотрицательное целое число. |



 

## <a name="element-information"></a>Сведения об элементе



|  Элемент     | Значение                                                     |
|--------------|-------------------------------------------------------------|
| Тип элемента | [**Дравингтипе**](drawingtype-complex-type.md) complexType |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк                  |
| Имя схемы  | Средство чтения журнала                                              |



 

 

 



