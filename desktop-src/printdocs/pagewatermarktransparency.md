---
description: Получение сведений о параметре Пажеватермарктранспаренци. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: пажеватермарктранспаренци
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ba405c3cd4a269edc4585ad8cba4c81f2c05e9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394789"
---
# <a name="pagewatermarktransparency"></a>пажеватермарктранспаренци

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Задает прозрачность для водяного знака. Полностью непрозрачное значение должно быть равно 0.

-   [Сведения об элементе](#element-information)
-   [Содержимое структуры](#structure-content)

## <a name="element-information"></a>Сведения об элементе



| Имя | Значение |
|----------------------------|--------------------------------------------|
| Тип элемента <br/>   | параметердеф<br/>                    |
| Префикс области <br/> | Страница<br/>                            |
| Примечания <br/>          | Связано с элементом Пажеватермарк<br/> |



 

## <a name="structure-content"></a>Содержимое структуры

XML-структура этого элемента выглядит следующим образом:

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTransparency">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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
| DefaultValue<br/> | целое число<br/> | 0<br/>               |
| MaxValue<br/>     | Целое число<br/> | 100<br/>             |
| MinValue<br/>     | целое число<br/> | 0<br/>               |
| Несколько<br/>     | целое число<br/> | 1<br/>               |
| Обязательный<br/>    | строка<br/>  | PSK: условный<br/> |
| Единицах UnitType<br/>     | строка<br/>  | percent<br/>         |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




