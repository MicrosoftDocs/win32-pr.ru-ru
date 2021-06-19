---
description: Получение сведений о параметре Пажемедиасизепсвидс. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: a1a684ce-5615-4ff7-a7aa-5c9f786f84ed
title: пажемедиасизепсвидс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe678107d2a183ee0f0bf6ce290dfe230fa8cc2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395649"
---
# <a name="pagemediasizepswidth"></a>пажемедиасизепсвидс

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Задает ширину страницы, перпендикулярной направлению ориентации канала ( [Спецификация формата файла описания PostScript-принтера](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).

-   [Сведения об элементе](#element-information)
-   [Содержимое структуры](#structure-content)

## <a name="element-information"></a>Сведения об элементе



| Имя | Значение |
|----------------------------|-------------------------------------------------------------|
| Тип элемента <br/>   | параметердеф<br/>                                     |
| Префикс области <br/> | Страница<br/>                                             |
| Примечания <br/>          | Ссылка на элемент Пажемедиасизе, параметр Кустомпс<br/> |



 

## <a name="structure-content"></a>Содержимое структуры

XML-структура этого элемента:

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidth">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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



| Свойство                | xsi:type           | Значение                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | строка<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | Целое число<br/> | неопределенный<br/>       |
| MaxValue<br/>     | Целое число<br/> | неопределенный<br/>       |
| MinValue<br/>     | Целое число<br/> | неопределенный<br/>       |
| Обязательный<br/>    | строка<br/>  | PSK: условный<br/> |
| Несколько<br/>     | целое число<br/> | 1<br/>               |
| Единицах UnitType<br/>     | строка<br/>  | мкм<br/>         |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Спецификация формата файла описания PostScript Printer](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




