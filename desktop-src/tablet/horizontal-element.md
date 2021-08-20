---
description: Содержит сведения о форматировании горизонтальных линий, используемых для бланков в заметке журнала.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Горизонтальный элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b66e8557d73570ce1a0b7eb7217c02435c51a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482690"
---
# <a name="horizontal-element"></a>Горизонтальный элемент

Содержит сведения о форматировании горизонтальных линий, используемых для бланков в заметке журнала.

## <a name="definition"></a>Определение

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Родительские элементы

[**линелайаут**](linelayout-element.md)

## <a name="child-elements"></a>Дочерние элементы

Отсутствует.

## <a name="attributes"></a>Атрибуты




| attribute | Тип | Обязательно | Описание | Возможные значения | 
|-----------|------|----------|-------------|-----------------|
| <strong>Стиль</strong> | <a href="linelayoutstyletype-simple-type.md"><strong>Линелайаутстилетипе</strong></a> simpleType | Обязательно | Указывает тип рисуемой линии. | <ul><li>None</li><li>Сплошная</li><li>Штрих</li><li>Точки</li><li>DashDot</li><li>DashDotDot</li><li>Тип Double</li></ul> | 
| <strong>Цвет</strong> | <a href="colortype-simple-type.md"><strong>Колортипе</strong></a> simpleType | Необязательно | Цвет элемента. | Шестнадцатеричное значение RGB. Соответствует следующему регулярному выражению: # [0-9a-zA-Z] {6} . Например, #4a79B5.<br /> | 
| <strong>спаЦингбефоре</strong> | <strong>xs:nonNegativeInteger</strong> | Необязательно | Отступ перед элементом. | Любое неотрицательное целое число. | 
| <strong>спаЦингбетвин</strong> | <strong>xs:nonNegativeInteger</strong> | Необязательно | Интервал между этим элементом и окружающими его элементами. | Любое неотрицательное целое число. | 




 

## <a name="element-information"></a>Сведения об элементе



|  Элемент     | Значение                                                     |
|--------------|-------------------------------------------------------------------|
| Тип элемента | [**Хоризонталтипе complexType**](horizontaltype-complex-type.md) |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк                        |
| Имя схемы  | Средство чтения журнала                                                    |



 

 

 




