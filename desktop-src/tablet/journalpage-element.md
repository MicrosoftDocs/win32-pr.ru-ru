---
description: Содержит сведения об отдельной странице в заметке журнала.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Жаурналпаже, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7223818de8200f2ff7748edd7eb472f49e92e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911392"
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

[**Содержани**](content-element--journal-reader.md)

## <a name="attributes"></a>Атрибуты



| attribute      | Тип                      | Обязательно | Описание                                                                        | Возможные значения                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Число**     | **xs:nonNegativeInteger** | Обязательно | Порядковый номер страницы в документе журнала, начиная с единицы (1). | Любое неотрицательное целое число.                                |
| **Width**      | **xs:nonNegativeInteger** | Обязательно | Ширина страницы.                                                             | Любое неотрицательное целое число.                                |
| **Height**     | **xs:nonNegativeInteger** | Обязательно | Высота страницы.                                                            | Любое неотрицательное целое число.                                |
| **LineHeight** | **xs:nonNegativeInteger** | Необязательно | Высота линии, используемой на странице.                                           | Любое неотрицательное целое число.                                |
| **LanguageId** | **xs:nonNegativeInteger** | Необязательно | Идентификатор языка, используемый для страницы.                                                 | Неотрицательное целое число, представляющее допустимый идентификатор языка. |



 

## <a name="element-information"></a>Сведения об элементе



|              |                                                                     |
|--------------|---------------------------------------------------------------------|
| Тип элемента | [**Жаурналпажетипе**](journalpagetype-complex-type.md) complexType |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк                          |
| Имя схемы  | Средство чтения журнала                                                      |



 

 

 



