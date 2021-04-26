---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: жобкопиесаллдокументс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8e606095462dc3a2eee1391121bf663de3655c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998371"
---
# <a name="jobcopiesalldocuments"></a>жобкопиесаллдокументс

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Указывает количество копий задания.

-   [Сведения об элементе](#element-information)
-   [Содержимое структуры](#structure-content)

## <a name="element-information"></a>Сведения об элементе



| Имя | Значение |
|----------------------------|-------------------------|
| Тип элемента <br/>   | параметердеф<br/> |
| Префикс области <br/> | Задание<br/>          |
| Примечания <br/>          | Нет<br/>         |



 

## <a name="structure-content"></a>Содержимое структуры

XML-структура этого элемента:

``` syntax
<psf:ParameterDef name="psk:JobCopiesAllDocuments">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Свойства структуры

В следующей таблице описаны характеристики переменных, определенных в структуре XML.



| Свойство                | xsi:type           | Значение                        |
|-------------------------|--------------------|------------------------------|
| DataType<br/>     | строка<br/>  | xs:integer<br/>        |
| DefaultValue<br/> | целое число<br/> | 1<br/>                 |
| MaxValue<br/>     | Целое число<br/> | неопределенный<br/>         |
| MinValue<br/>     | целое число<br/> | 1<br/>                 |
| Обязательный<br/>    | строка<br/>  | PSK: безусловное<br/> |
| Несколько<br/>     | целое число<br/> | 1<br/>                 |
| Единицах UnitType<br/>     | строка<br/>  | Копи<br/>            |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




