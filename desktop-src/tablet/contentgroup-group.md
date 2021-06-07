---
description: Определяет группу, содержащую набор сгруппированных содержимого в заметке журнала.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Группа Контентграуп
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e4291da1912c43674871c06fb803e1936f7178
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432616"
---
# <a name="contentgroup-group"></a>Группа Контентграуп

Определяет группу, содержащую набор сгруппированных содержимого в заметке журнала.

## <a name="definition"></a>Определение

``` syntax
<xs:group name="ContentGroup" >
  <xs:choice>
    <xs:element name="GroupNode" type="GroupNodeType" />
    <xs:element name="Paragraph" type="ParagraphType" />
    <xs:element name="InkWord" type="InkWordType" />
    <xs:element name="Drawing" type="DrawingType" />
    <xs:element name="Text" type="TextType" />
    <xs:element name="Image" type="ImageType" />
    <xs:element name="Flag" type="FlagType" />
    <xs:element name="Reflow" type="ReflowType" />
  </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Дочерние элементы

[**граупноде**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**инкворд**](inkword-element.md)

[**Рисование**](drawing-element.md)

[**Полнотекстовым**](text-element.md)

[**Изображение**](docimage-element.md)

[**Flag**](flag-element.md)

## <a name="attributes"></a>Атрибуты



| attribute  | Тип                      | Обязательно | Описание                                                                                        | поссиблевалуес                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Слева**   | **xs:integer**            | Обязательно | Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.<br/> | Любое целое число.<br/>              |
| **Top**    | **xs:integer**            | Обязательно | Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.<br/>  | Любое целое число.<br/>              |
| **Width**  | **xs:nonNegativeInteger** | Обязательно | Ширина ограничивающего прямоугольника для элемента.<br/>                                          | Любое неотрицательное целое число.<br/> |
| **Height** | **xs:nonNegativeInteger** | Обязательно | Высота ограничивающего прямоугольника для элемента.<br/>                                         | Любое неотрицательное целое число.<br/> |



 

## <a name="type-information"></a>Сведения о типе



|  Элемент     | Значение                                                     |
|-------------|--------------------------------------------|
| Пространство имен   | urn: schemas-microsoft-com: TabletPC: ричинк |
| Имя схемы | Средство чтения журнала                             |



 

 

 




