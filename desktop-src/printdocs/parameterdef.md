---
description: Сведения об элементе Параметердеф, который определяет допустимые характеристики входных параметров. Значение вводится с помощью элемента Параметеринит.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: параметердеф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a657350c11f56dca032df6aff6b530f304aaa3a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883693"
---
# <a name="parameterdef"></a>параметердеф

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Элемент Параметердеф определяет допустимые характеристики входных параметров. Значение вводится с помощью элемента Параметеринит.

## <a name="element-tag"></a>Тег элемента

&lt;параметердеф&gt;

## <a name="xml-attributes"></a>XML-атрибуты

В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.



| Атрибут XML   | Сведения                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Определяет уникальное имя для параметра в контексте текущего документа. Дублирующиеся атрибуты имени Параметердеф отображают недопустимый документ PrintCapabilities.<br/> |



 

Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .

## <a name="element-information"></a>Сведения об элементе

В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.




| Категория | Сведения | 
|----------|---------|
| Родительские элементы<br /> | PrintCapabilities <br /> | 
| Дочерние элементы<br /> | Property (один или больше)<br /> Следующие стандартные элементы свойств должны отображаться как содержимое элемента Параметердеф. <br /><ul><li>DataType <br /></li><li>DefaultValue <br /></li><li>Обязательный <br /></li><li>MaxLength или MaxValue<br /></li><li>MinLength или MinValue<br /></li><li>Несколько <br /></li><li>Единицах UnitType <br /></li></ul> | 
| Этот элемент<br /> | Символьные данные не допускаются.<br /> Дублирование дочерних одноуровневых элементов не разрешено.<br /> | 




 

\*Требуется, если DataType имеет тип Integer или Decimal. Необязательный аргумент, если DataType является строковым.

## <a name="configuration-dependencies"></a>Зависимости конфигурации

Параметердеф и его содержимое с любым уровнем вложенности может не иметь зависимостей конфигурации.

## <a name="example"></a>Пример

В следующем примере задаются все обязательные элементы свойств для этого параметра. В примере в [параметеринит](parameterinit.md) показано, как инициализировать этот параметр.

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">594106</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Optional</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




