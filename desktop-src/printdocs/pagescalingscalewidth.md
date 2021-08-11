---
description: Получение сведений о параметре Пажескалингскалевидс. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: пажескалингскалевидс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c461b8e66b38605af749546a66b31016362140365e7998dca9960e9ad61d201
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234349"
---
# <a name="pagescalingscalewidth"></a>пажескалингскалевидс

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Задает коэффициент масштабирования в направлении Имажеаблесизевидс для пользовательского масштабирования.

-   [Сведения об элементе](#element-information)
-   [Содержимое структуры](#structure-content)

## <a name="element-information"></a>Сведения об элементе



| name | Значение |
|----------------------------|---------------------------------------------------------|
| Тип элемента <br/>   | параметердеф<br/>                                 |
| Префикс области <br/> | Страница<br/>                                         |
| Примечания <br/>          | Ссылка на элемент Пажескалинг, Пользовательский параметр<br/> |



 

## <a name="structure-content"></a>Содержимое структуры

XML-структура этого элемента:

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleWidth">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
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
| DataType<br/>     | Строка<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | Целочисленный тип<br/> | неопределенный<br/>       |
| MaxValue<br/>     | Целочисленный тип<br/> | неопределенный<br/>       |
| MinValue<br/>     | Целое число<br/> | 1<br/>               |
| Обязательный<br/>    | Строка<br/>  | PSK: условный<br/> |
| Несколько<br/>     | Целое число<br/> | 1<br/>               |
| Единицах UnitType<br/>     | Строка<br/>  | мкм<br/>         |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




