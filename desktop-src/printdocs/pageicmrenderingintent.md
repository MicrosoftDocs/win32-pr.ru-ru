---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: пажеикмрендерингинтент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014213bdd2e11cc2587cef580a0b48fe03172ef0
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104273355"
---
# <a name="pageicmrenderingintent"></a>пажеикмрендерингинтент

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Описывает цель подготовки к просмотру, определенную спецификацией ICC v2. Это значение следует игнорировать, если изображение или графический элемент имеет встроенный профиль, указывающий цель отрисовки.

-   [Сведения об элементе](#element-information)
-   [Структурное содержимое](#structural-content)
-   [Содержимое язык XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Сведения об элементе



| Имя                       |                    |
|----------------------------|--------------------|
| Тип элемента <br/>   | Функция<br/> |
| Префикс области <br/> | Страница<br/>    |
| Примечания <br/>          | Нет <br/>   |



 

## <a name="structural-content"></a>Структурное содержимое

XML-структура этого элемента:

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
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



| Имя                               | Тип данных         | Unit                  | Поддерживаемые значения                                                                                                                                                                      | Сводка                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | строка<br/> | characters<br/> | Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Если пространство имен не указано, предполагается использование пространства имен по умолчанию.<br/> | Имя параметра.<br/>                                           |
| \_идентитйоптионвалуе\_<br/> | строка<br/> | Недоступно<br/>        | True, False.<br/>                                                                                                                                                               | Определяет параметр, который при выборе этого параметра отключит эту функцию.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Содержимое язык XML (XML)

Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен. Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!--Absolute Colorimetric Rendering intent-->
  <psf:Option name="psk:AbsoluteColorimetric" />
  <!--Relative Colorimetric Rendering intent -->
  <psf:Option name="psk:RelativeColorimetric" />
  <!--Photographs Rendering intent -->
  <psf:Option name="psk:Photographs" />
  <!--Business Graphics Rendering intent -->
  <psf:Option name="psk:BusinessGraphics" />
</psf:Feature>
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




