---
description: Сведения об элементе Жобпримариковербакксаурце, который указывает источник для пользовательского первичного основного листа для задания.
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: жобпримариковербакксаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ac990caca0f10e03f33eda9971ad967c1c7192ae07a1326675f66880c27857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471686"
---
# <a name="jobprimarycoverbacksource"></a>жобпримариковербакксаурце

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Указывает источник пользовательского первичного листа для задания.

-   [Сведения об элементе](#element-information)
-   [Содержимое структуры](#structure-content)

## <a name="element-information"></a>Сведения об элементе



| Имя | Значение |
|----------------------------|-------------------------------------------|
| Тип элемента <br/>   | параметердеф<br/>                   |
| Префикс области <br/> | Задание<br/>                            |
| Примечания <br/>          | Связано с элементом Жобковербакк<br/> |



 

## <a name="structure-content"></a>Содержимое структуры

XML-структура этого элемента:

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverBackSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer ">1</psf:Value>
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

 

 




