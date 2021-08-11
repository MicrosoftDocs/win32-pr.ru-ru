---
description: Сведения об элементе Документпажеранжес, описывающем выходной диапазон документа на страницах.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: документпажеранжес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9a1941b36970628ddcb5c94cad42bd7f520f0b48e00ff5e1263079818757a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235121"
---
# <a name="documentpageranges"></a>документпажеранжес

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Описывает диапазон выходных данных документа на страницах. Значение параметра должно соответствовать следующей структуре:

-   Пажеранжетекст: "*пажеранже*" или "*пажеранже*,*пажеранже*"

-   Пажеранже: "*PageNumber*" или "*PageNumber* - *PageNumber*"

-   PageNumber: от 1 до N, где N — число страниц в документе. Если *PageNumber* > n, то *PageNumber* = n.

Пробелы в строке следует игнорировать.

-   [Сведения об элементе](#element-information)
-   [Структурное содержимое](#structural-content)

## <a name="element-information"></a>Сведения об элементе



| name | Значение |
|----------------------------|-------------------------|
| Тип элемента <br/>   | параметердеф<br/> |
| Префикс области <br/> | Документ<br/>     |
| Примечания <br/>          | Нет<br/>         |



 

## <a name="structural-content"></a>Структурное содержимое

XML-структура этого элемента:

``` syntax
<psf:ParameterDef name="psk:DocumentPageRanges">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Свойства структуры

В следующей таблице описаны характеристики переменных, определенных в структуре XML.



| Свойство                | xsi:type           | Значение                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | строка<br/>  | xs:string<br/>       |
| DefaultValue<br/> | строка<br/>  | неопределенный<br/>       |
| MaxLength<br/>    | Целое число<br/> | неопределенный<br/>       |
| MinLength<br/>    | целое число<br/> | 1<br/>               |
| Обязательный<br/>    | строка<br/>  | PSK: условный<br/> |
| Единицах UnitType<br/>     | строка<br/>  | characters<br/>      |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




