---
description: Сведения об элементе Пажетруетипефонтмоде, настраиваемом пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 36b1de5d-8575-42cf-b158-dcf7705ec157
title: пажетруетипефонтмоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22765acba62747c26544739c85d0709250463d130ec09ff6c66ca25e472cf7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112284"
---
# <a name="pagetruetypefontmode"></a>пажетруетипефонтмоде

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Описывает метод обработки шрифтов TrueType для использования.

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
<psf:Feature name="psk:PageTrueTypeFontMode">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Переменные структуры

В следующей таблице описаны характеристики переменных, определенных в структуре XML.



| Имя                               | Тип данных         | Единица измерения                  | Поддерживаемые значения                                                                                                                                                                      | Сводка                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | строка<br/> | characters<br/> | Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Если пространство имен не указано, предполагается использование пространства имен по умолчанию.<br/> | Имя параметра.<br/>                                           |
| \_идентитйоптионвалуе\_<br/> | строка<br/> | Недоступно<br/>        | True, False.<br/>                                                                                                                                                               | Определяет параметр, который при выборе этого параметра отключит эту функцию.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Содержимое язык XML (XML)

Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен. Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:

``` syntax
<psf:Feature name="psk:PageTrueTypeFontMode">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Automatic handling of TrueType font-->
  <psf:Option name="psk:Automatic" />
  <!--TrueType font is downloaded as outline font-->
  <psf:Option name="psk:DownloadAsOutlineFont" />
  <!--TrueType font is downloaded as raster font-->
  <psf:Option name="psk:DownloadAsRasterFont" />
  <!--TrueType font is downloaded as native true type font-->
  <psf:Option name="psk:DownloadAsNativeTrueTypeFont" />
  <!--TrueType font is rendered as a bitmap-->
  <psf:Option name="psk:RenderAsBitmap" />
</psf:Feature>    
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




