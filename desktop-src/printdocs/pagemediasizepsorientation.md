---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: пажемедиасизепсориентатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a188c61d3bb3c47286b887406174a3fc41f3c58a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703484"
---
# <a name="pagemediasizepsorientation"></a>пажемедиасизепсориентатион

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Задает ориентацию относительно направления ориентации канала ( [Спецификация формата файла описания PostScript-принтера](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).

-   [Сведения об элементе](#element-information)
-   [Содержимое структуры](#structure-content)

## <a name="element-information"></a>Сведения об элементе



| Имя                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| Тип элемента <br/>   | параметердеф<br/>                                     |
| Префикс области <br/> | Страница<br/>                                             |
| Примечания <br/>          | Ссылка на элемент Пажемедиасизе, параметр Кустомпс<br/> |



 

## <a name="structure-content"></a>Содержимое структуры

XML-структура этого элемента:

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSOrientation">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">3</psf:Value>
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
    <psf:Value xsi:type="xs:string">PageMediaSizeEnum</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Свойства структуры

В следующей таблице описаны характеристики переменных, определенных в структуре XML.



| Свойство                | xsi:type           | Значение                        |
|-------------------------|--------------------|------------------------------|
| DataType<br/>     | строка<br/>  | xs:integer<br/>        |
| DefaultValue<br/> | целое число<br/> | 0<br/>                 |
| MaxValue<br/>     | Целое число<br/> | 3<br/>                 |
| MinValue<br/>     | целое число<br/> | 0<br/>                 |
| Обязательный<br/>    | строка<br/>  | PSK: условный<br/>   |
| Несколько<br/>     | целое число<br/> | 1<br/>                 |
| Единицах UnitType<br/>     | строка<br/>  | пажемедиасизинум<br/> |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Спецификация формата файла описания PostScript Printer](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




