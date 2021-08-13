---
description: Содержит сведения об отдельной странице в заметке журнала.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Жаурналпаже, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5062838476e6f67605101157640a490645e454b62d852b69f51dc4bb2215db99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442804"
---
# <a name="journalpage-element"></a>Жаурналпаже, элемент

Содержит сведения об отдельной странице в заметке журнала.

## <a name="definition"></a>Определение

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Родительские элементы

[**жаурналдокумент**](journaldocument-element.md)

## <a name="child-elements"></a>Дочерние элементы

[**Стационарный**](stationery-element.md)

[**доЦимаже**](docimage-element.md)

[**титлеинфо**](titleinfo-element.md)

[**Content**](content-element--journal-reader.md)

## <a name="attributes"></a>Атрибуты



| attribute      | Тип                      | Обязательно | Описание                                                                        | Возможные значения                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Число**     | **xs:nonNegativeInteger** | Обязательно | Порядковый номер страницы в документе журнала, начиная с единицы (1). | Любое неотрицательное целое число.                                |
| **Width**      | **xs:nonNegativeInteger** | Обязательно | Ширина страницы.                                                             | Любое неотрицательное целое число.                                |
| **Height**     | **xs:nonNegativeInteger** | Обязательно | Высота страницы.                                                            | Любое неотрицательное целое число.                                |
| **LineHeight** | **xs:nonNegativeInteger** | Необязательно | Высота линии, используемой на странице.                                           | Любое неотрицательное целое число.                                |
| **LanguageId** | **xs:nonNegativeInteger** | Необязательно | Идентификатор языка, используемый для страницы.                                                 | Неотрицательное целое число, представляющее допустимый идентификатор языка. |



 

## <a name="element-information"></a>Сведения об элементе



|  Элемент     | Значение                                                     |
|--------------|---------------------------------------------------------------------|
| Тип элемента | [**Жаурналпажетипе**](journalpagetype-complex-type.md) complexType |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк                          |
| Имя схемы  | Средство чтения журнала                                                      |



 

 

 



