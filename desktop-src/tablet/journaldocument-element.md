---
description: Элемент верхнего уровня в XML-файле заметки журнала.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Жаурналдокумент, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7820ef68dc87bf42d9580c800e2e165f2f2859a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432176"
---
# <a name="journaldocument-element"></a>Жаурналдокумент, элемент

Элемент верхнего уровня в XML-файле заметки журнала.

## <a name="definition"></a>Определение

``` syntax
<xs:element name="JournalDocument">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="Stationery" type="StationeryType" minOccurs="0" maxOccurs="unbounded" />
    <xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
   </xs:sequence>
   <xs:attribute name="Version" type="xs:string" use="required" fixed="1.0" />
   <xs:attribute name="DefaultPageWidth" type="xs:nonNegativeInteger" use="required" />
   <xs:attribute name="DefaultPageHeight" type="xs:nonNegativeInteger" use="required" />
  </xs:complexType>
</xs:element>/>
```

## <a name="parent-elements"></a>Родительские элементы

Отсутствует.

## <a name="child-elements"></a>Дочерние элементы

[**Stationery**](stationery-element.md)

[**жаурналпаже**](journalpage-element.md)

## <a name="attributes"></a>Атрибуты



| attribute             | Тип                      | Обязательно | Описание                                                      | Возможные значения           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **Версия**           | **xs:string**             | Обязательно | Версия документа журнала, представленного в XML-файле. | 1.0                       |
| **дефаултпажевидс**  | **xs:nonNegativeInteger** | Обязательно | Ширина страницы по умолчанию для документа журнала.          | Любое неотрицательное целое число. |
| **дефаултпажехеигхт** | **xs:nonNegativeInteger** | Обязательно | Высота по умолчанию страницы для документа журнала.         | Любое неотрицательное целое число. |



 

## <a name="element-information"></a>Сведения об элементе



|  Элемент     | Значение                                                     |
|--------------|--------------------------------------------|
| Тип элемента | **жаурналдокумент**                        |
| Пространство имен    | urn: schemas-microsoft-com: TabletPC: ричинк |
| Имя схемы  | Средство чтения журнала                             |



 

 

 



