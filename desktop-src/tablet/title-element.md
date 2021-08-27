---
description: Содержит сведения о названии заметки журнала.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Элемент Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05661be8566cf4136194af4e08d8f9774d3413dc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473140"
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




| attribute | Тип | Обязательно | Описание | Возможные значения | 
|-----------|------|----------|-------------|-----------------|
| <strong>Стиль</strong> | <strong>xs:string</strong> | Обязательно | Задает тип границы, окружающей заголовок примечания. | <ul><li>None</li><li>солидскуаре</li><li>аутлинескуаре</li><li>солидраундрект</li><li>аутлинераундрект</li><li>солидраундректдоттедбаселине</li></ul> | 
| <strong>датестиле</strong> | <strong>xs:string</strong> | Обязательно | Определяет, содержит ли заголовок дату или нет. | <ul><li>None</li><li>Short</li></ul> | 
| <strong>Цвет</strong> | <a href="colortype-simple-type.md"><strong>Колортипе simpleType</strong></a> | Необязательно | Указывает цвет фона. | См. <a href="colortype-simple-type.md"><strong>Колортипе simpleType</strong></a>. | 




 

## <a name="element-information"></a>Сведения об элементе



| Элемент      | Значение                                                   |
|--------------|---------------------------------------------------------|
| Тип элемента | [**Титлетипе**](titletype-complex-type.md) complexType |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк              |
| Имя схемы  | Средство чтения журнала                                          |



 

 

 



