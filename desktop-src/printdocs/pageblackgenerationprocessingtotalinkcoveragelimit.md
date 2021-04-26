---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: пажеблаккженератионпроцессингтоталинкковеражелимит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29918bfe48d1547a3c61b8d79425b36368f6d249
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993881"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a>пажеблаккженератионпроцессингтоталинкковеражелимит

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Указывает максимально допустимую сумму четырех объемов рукописного ввода в любом месте изображения.

-   [Сведения об элементе](#element-information)
-   [Содержимое структуры](#structure-content)

## <a name="element-information"></a>Сведения об элементе



| Имя | Значение |
|----------------------------|------------------------------------------------------------|
| Тип элемента <br/>   | параметердеф<br/>                                    |
| Префикс области <br/> | Страница<br/>                                            |
| Примечания <br/>          | Связано с элементом Пажеблаккженератионпроцессинг<br/> |



 

## <a name="structure-content"></a>Содержимое структуры

XML-структура этого элемента:

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">200</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a>Свойства структуры

В следующей таблице описаны характеристики переменных, определенных в структуре XML.



| Свойство                | xsi:type           | Значение                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | строка<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | строка<br/>  | неопределенный<br/>       |
| MaxValue<br/>     | Целое число<br/> | 400<br/>             |
| MinValue<br/>     | Целое число<br/> | 200<br/>             |
| Несколько<br/>     | целое число<br/> | 1<br/>               |
| Обязательный<br/>    | строка<br/>  | PSK: условный<br/> |
| Единицах UnitType<br/>     | строка<br/>  | percent<br/>         |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




