---
description: Сведения об элементе Пажеимажеаблесизе, настраиваемом пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: пажеимажеаблесизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 924c89f304c75863246f266e2c64818ee7ab21c173009a096d32c3d1ac6e178b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948273"
---
# <a name="pageimageablesize"></a>пажеимажеаблесизе

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Описывает полотно с изображением для макета и отрисовки. Это будет сообщено на основе Пажемедиасизе и Пажеориентатион.

На следующих диаграммах показаны переменные использования Пажеимажеаблесизе, основанные на Пажеориентатион.

![Диаграмма, на которой показаны измерения страниц](images/local-1641910626-image.png)

-   [Сведения об элементе](#element-information)
-   [Структурное содержимое](#structural-content)
-   [Содержимое язык XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Сведения об элементе

| Имя                 | Значение         |
|----------------------|---------------|
| Тип элемента<br/>    | Свойство<br/> |
| Префикс области <br/> | Страница<br/>     |
| Примечания <br/>          | Нет<br/>     |

## <a name="structural-content"></a>Структурное содержимое

XML-структура этого элемента:

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_ImageableSizeWidthValue_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_ImageableSizeHeightValue_</psf:Value>
  </psf:Property>
  <!--Specifies the imageable area within the logical page.  -->
  <psf:Property name="psk:ImageableArea">
    <psf:Property name="psk:OriginWidth">
      <psf:Value xsi:type="xs:integer">_OriginWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_OriginHeightValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_ExtentWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_ExtentHeightValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a>Переменные структуры

В следующей таблице описаны характеристики переменных, определенных в структуре XML.



| Имя                                    | Тип данных          | Единица измерения               | Поддерживаемые значения                       | Сводка                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| \_имажеаблесизевидсвалуе\_<br/>  | Целое число<br/> | мкм<br/> | Больше 0.<br/>             | Задает горизонтальное измерение размера носителя приложения относительно Пажеориентатион.<br/>               |
| \_имажеаблесизехеигхтвалуе\_<br/> | Целое число<br/> | мкм<br/> | Больше 0.<br/>             | Задает вертикальное измерение размера носителя приложения относительно Пажеориентатион.<br/>                 |
| \_оригинвидсвалуе\_<br/>         | Целое число<br/> | мкм<br/> | Больше или равно 0.<br/> | Указывает горизонтальный источник области изображения относительно размера носителя приложения.<br/>                   |
| \_оригинхеигхтвалуе\_<br/>        | Целое число<br/> | мкм<br/> | Больше или равно 0.<br/> | Задает вертикальный источник области изображения относительно размера носителя приложения.<br/>                     |
| \_екстентвидсвалуе\_<br/>         | Целое число<br/> | мкм<br/> | Больше 0.<br/>             | Указывает расстояние по горизонтали между началом и ограничивающим пределом размера носителя приложения.<br/>      |
| \_екстенсеигхтвалуе\_<br/>        | Целое число<br/> | мкм<br/> | Больше 0.<br/>             | Задает расстояние по вертикали между источником и ограничивающим пределом размера носителя приложения Canvas.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Содержимое язык XML (XML)

Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен. Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
    <psf:Property name="psk:ImageableArea">
      <psf:Property name="psk:OriginWidth">
        <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
      </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
  
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




