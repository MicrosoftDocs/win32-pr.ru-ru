---
description: Содержит содержимое, классифицированное анализатором или пользователем в виде рисунка.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Элемент Drawing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87c0a3d8879fb5f3146c46c9c88d83a6e658d8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432516"
---
# <a name="drawing-element"></a>Элемент Drawing

Содержит содержимое, классифицированное анализатором или пользователем в виде рисунка.

## <a name="definition"></a>Определение

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Родительские элементы

[**Содержани**](content-element--journal-reader.md)

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



 

 

 



