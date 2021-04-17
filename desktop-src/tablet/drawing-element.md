---
description: Содержит содержимое, классифицированное анализатором или пользователем в виде рисунка.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Элемент Drawing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe516a4ba33e6e597b17ce8365d792f19468c3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693764"
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



|              |                                                             |
|--------------|-------------------------------------------------------------|
| Тип элемента | [**Дравингтипе**](drawingtype-complex-type.md) complexType |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк                  |
| Имя схемы  | Средство чтения журнала                                              |



 

 

 



