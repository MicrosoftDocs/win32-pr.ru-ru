---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: пажеватермаркоригинвидс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78cf29952258a7c6c3489d40291ba8cd4b756c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996071"
---
# <a name="pagewatermarkoriginwidth"></a>пажеватермаркоригинвидс

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Задает источник водяного знака относительно источника Пажеимажеаблесизе.

-   [Сведения об элементе](#element-information)
-   [Содержимое структуры](#structure-content)

## <a name="element-information"></a>Сведения об элементе



| Имя | Значение |
|----------------------------|--------------------------------------------|
| Тип элемента <br/>   | параметердеф<br/>                    |
| Префикс области <br/> | Страница<br/>                            |
| Примечания <br/>          | Связано с элементом Пажеватермарк<br/> |



 

## <a name="structure-content"></a>Содержимое структуры

XML-структура этого элемента:

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Свойства структуры

В следующей таблице описаны характеристики переменных, определенных в структуре XML.



| Свойство                | xsi:type           | Значение                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| DataType<br/>     | строка<br/>  | xs:integer<br/>                                                  |
| DefaultValue<br/> | Целое число<br/> | неопределенный<br/>                                                   |
| MaxValue<br/>     | Целое число<br/> | Меньше или равно Пажеимажеаблесизе-ExtentWidth значение<br/> |
| MinValue<br/>     | целое число<br/> | 0<br/>                                                           |
| Несколько<br/>     | целое число<br/> | 1<br/>                                                           |
| Обязательный<br/>    | строка<br/>  | PSK: условный<br/>                                             |
| Единицах UnitType<br/>     | строка<br/>  | мкм<br/>                                                     |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




