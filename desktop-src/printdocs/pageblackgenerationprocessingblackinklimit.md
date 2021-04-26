---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: пажеблаккженератионпроцессингблаккинклимит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3052d8cec8fd46c2f7607e6366aa6868cccbdbda
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996191"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a>пажеблаккженератионпроцессингблаккинклимит

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Содержимое приложения с меткой указанного именованного цвета должно отображаться во всех цветоделении.

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
<psf:ParameterDef name="psk:PageBlackGenerationProcessingBlackInkLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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
| MaxValue<br/>     | Целое число<br/> | 100<br/>             |
| MinValue<br/>     | целое число<br/> | 0<br/>               |
| Несколько<br/>     | целое число<br/> | 1<br/>               |
| Обязательный<br/>    | строка<br/>  | PSK: условный<br/> |
| Единицах UnitType<br/>     | строка<br/>  | percent<br/>         |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




