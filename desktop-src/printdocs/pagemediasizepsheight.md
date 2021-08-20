---
description: Получение сведений о параметре Пажемедиасизепшеигхт. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 857caf51-ccf6-415c-aab3-1fed50fa7b34
title: пажемедиасизепшеигхт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53af9494fe895c16fd884e06991b3072f320261e6a47d5fd7f2f06e029bff2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868209"
---
# <a name="pagemediasizepsheight"></a>пажемедиасизепшеигхт

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

задает высоту страницы, параллельную направлению ориентации канала (ссылка [PostScript принтера описание формата файла](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).

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
<psf:ParameterDef name="psk:PageMediaSizePSHeight">
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

[PostScript Спецификация формата файла описания принтера](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




