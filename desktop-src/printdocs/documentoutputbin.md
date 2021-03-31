---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: документаутпутбин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444ca63fee0b76f17909b1aa08e65cd468537dee
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104273359"
---
# <a name="documentoutputbin"></a>документаутпутбин

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Содержит полный список поддерживаемых ячеек для устройства. Разрешает указание выходной ячейки для каждого документа. Ключевые слова Жобаутпутбин, Документаутпутбин и Пажеаутпутбин являются взаимоисключающими только один из них должен быть указан в документе PrintTicket или возможности печати.

-   [Сведения об элементе](#element-information)

-   [Структурное содержимое](#structural-content)

-   [XML-содержимое](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Сведения об элементе



| Имя                       |                     |
|----------------------------|---------------------|
| Тип элемента <br/>   | Функция<br/>  |
| Префикс области <br/> | Документ<br/> |
| Примечания <br/>          | Нет<br/>     |



 

## <a name="structural-content"></a>Структурное содержимое

XML-структура этого элемента:

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Переменные структуры

В следующей таблице описаны характеристики переменных, определенных в структуре XML.



| Имя                                   | Тип данных          | Unit                  | Поддерживаемые значения                                                                                                                                                             | Сводка                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| \_OptionName\_<br/>              | строка<br/>  | characters<br/> | Допустимое полное имя, как определено в https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname . Если пространство имен не указано, предполагается использование пространства имен по умолчанию.<br/> | Имя параметра.<br/>                                                  |
| \_идентитйоптионвалуе\_<br/>     | строка<br/>  | Недоступно<br/>        | True, False.<br/>                                                                                                                                                      | Определяет параметр, который при выборе этого параметра отключит эту функцию.<br/>        |
| \_бинтипевалуе\_<br/>            | строка<br/>  | Недоступно<br/>        | Почтовый ящик, сортировщик, укладчик, финишер, нет.<br/>                                                                                                                         | Указывает общий тип ячейки.<br/>                                   |
| \_медиашиткапаЦитивалуе\_<br/> | Целое число<br/> | свойств<br/>     | Больше 0.<br/>                                                                                                                                                   | Указывает емкость носителя в количестве страниц (полный уровень) ячейки.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Содержимое язык XML (XML)

Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен. Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!--Specifies type of output bin-->
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!--Specifies media capacity for output bin-->
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




