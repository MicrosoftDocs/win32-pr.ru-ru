---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: жобнупаллдокументсконтигуаусли
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e307883a25fc977b9086259789c04f4b3a7cbf
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351995"
---
# <a name="jobnupalldocumentscontiguously"></a>жобнупаллдокументсконтигуаусли

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Описывает вывод нескольких логических страниц на один физический лист. Все документы в задании компилируются последовательно. Жобнупаллдокументсконтигуаусли и Документнуп являются взаимоисключающими. Драйвер определяет обработку ограничений между этими ключевыми словами.

На следующей схеме показан пример с документом 1, содержащим 3 страницы, а также документ 2, содержащий 2 страницы. Каждый документ в задании последовательно расдуплексует. В этом примере показаны направления, представленные в виде параметра Ригхтботтом.

![Диаграмма, показывающая, как размещаются страницы документа на одном листе, основанном на параметре документнуп](images/local-1242234459-jobduplexpics.gif)

-   [Сведения об элементе](#element-information)
-   [Структурное содержимое](#structural-content)
-   [Содержимое язык XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Сведения об элементе



| Имя                       |                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Тип элемента <br/>   | Функция<br/>                                                                                                                             |
| Префикс области <br/> | Задание<br/>                                                                                                                                 |
| Примечания <br/>          | Верхняя, Нижняя, левая и правая относительные относятся к Пажеимажеаблесизе, где Топлефт обозначается исходными значениями высоты и ширины.<br/> |



 

## <a name="structural-content"></a>Структурное содержимое

XML-структура этого элемента:

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_PagesPerSheetValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the ordering direction of the pages.  First direction followed by second direction. -->
  <psf:Feature name="psk:PresentationDirection">
    <psf:Option name="psk:_PresentationDirectionOptionName_" />
  </psf:Feature>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Переменные структуры

В следующей таблице описаны характеристики переменных, определенных в структуре XML.



| Имя                                           | Тип данных          | Unit                     | Поддерживаемые значения                                                                                                                                                                      | Сводка                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| \_OptionName\_<br/>                      | строка<br/>  | characters<br/>    | Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Если пространство имен не указано, предполагается использование пространства имен по умолчанию.<br/> | Имя параметра.<br/>                                                                                                   |
| \_идентитйоптионвалуе\_<br/>             | строка<br/>  | Недоступно<br/>           | True, False.<br/>                                                                                                                                                               | Определяет параметр, который при выборе этого параметра отключит эту функцию.<br/>                                                         |
| \_пажеспершитвалуе\_<br/>              | Целое число<br/> | Логические страницы<br/> | Все целые числа (больше нуля).<br/>                                                                                                                                          | Указывает число логических страниц на физический лист. Поддерживаемым набором может быть любой набор целых чисел, например {1,2,4,6,8,9,16}.<br/> |
| \_пресентатиондиректионоптионнаме\_<br/> | строка<br/>  | characters<br/>    | Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Если пространство имен не указано, предполагается использование пространства имен по умолчанию.<br/> | Имя параметра.<br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a>Содержимое язык XML (XML)

Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен. Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




