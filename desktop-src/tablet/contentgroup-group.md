---
description: Определяет группу, содержащую набор сгруппированных содержимого в заметке журнала.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Группа Контентграуп
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0085cc52a8fc29d3a51f4d1e1c8f42128b63db9e166a7a1c436dc15bff70a36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009014"
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

[**Флаг**](flag-element.md)

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



 

 

 




