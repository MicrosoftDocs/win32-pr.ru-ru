---
description: Ознакомьтесь с элементом Пажересолутион, настраиваемым пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: пажересолутион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760384ff900e7b35e37105fdb19e3635a434aa5a
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394827"
---
# <a name="pageresolution"></a>пажересолутион

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Определяет разрешение печатаемых страниц в виде качественного значения, в виде количественного значения, выраженного в точках на дюйм или оба представления.

-   [Сведения об элементе](#element-information)
-   [Структурное содержимое](#structural-content)
-   [Содержимое язык XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Сведения об элементе



| Имя | Значение |
|----------------------------|--------------------|
| Тип элемента <br/>   | Компонент<br/> |
| Префикс области <br/> | Страница<br/>    |
| Примечания <br/>          | Нет<br/>    |



 

## <a name="structural-content"></a>Структурное содержимое

XML-структура этого элемента:

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_ResolutionXValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_ResolutionYValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">_QualitativeResolutionValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a>Переменные структуры

В следующей таблице описаны характеристики переменных, определенных в структуре XML.



| Имя                                      | Тип данных          | Unit                  | Поддерживаемые значения                                                                                                                                                                      | Итоги                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_OptionName\_<br/>                 | строка<br/>  | characters<br/> | Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Если пространство имен не указано, предполагается использование пространства имен по умолчанию.<br/> | Имя параметра.<br/>                                                                                                                               |
| \_идентитйоптионвалуе\_<br/>        | строка<br/>  | Недоступно<br/>        | True, False.<br/>                                                                                                                                                               | Определяет параметр, который при выборе этого параметра отключит эту функцию.<br/>                                                                                     |
| \_ресолутионксвалуе\_<br/>           | Целое число<br/> | DPI<br/>        | Больше 0.<br/>                                                                                                                                                            | Указывает компонент x разрешения относительно Пажеимажеаблесизе в точках на дюйм (относительно Пажемедиасизе и направления носителя).<br/> |
| \_ресолутионивалуе\_<br/>           | Целое число<br/> | DPI<br/>        | Больше 0.<br/>                                                                                                                                                            | Задает компонент y разрешения, относительно Пажеимажеаблесизе в точках на дюйм (относительно Пажемедиасизе и направления потока медиа).<br/> |
| \_куалитативересолутионвалуе\_<br/> | строка<br/>  | Недоступно<br/>        | По умолчанию, черновик, высокий, нормальный, другой.<br/>                                                                                                                                       | Задает метку качества для разрешения.<br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a>Содержимое язык XML (XML)

Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен. Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!-- The horizontal resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- The vertical resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- Value representing the resolution -->
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">Other</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




