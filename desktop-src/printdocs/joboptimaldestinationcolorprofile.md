---
description: Сведения об элементе Жобоптималдестинатионколорпрофиле, который указывает оптимальный цветовой профиль, заданный текущей конфигурацией устройства.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: жобоптималдестинатионколорпрофиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2a63f63993f6a9cf8de8ba0a332407bb645099d98e6d92669c18368bd7629a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099672"
---
# <a name="joboptimaldestinationcolorprofile"></a>жобоптималдестинатионколорпрофиле

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Задает оптимальный цветовой профиль, заданный текущей конфигурацией устройства.

-   [Сведения об элементе](#element-information)
-   [Структурное содержимое](#structural-content)
-   [Содержимое язык XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Сведения об элементе



| Имя | Значение |
|----------------------------|---------------------|
| Тип элемента <br/>   | Свойство<br/> |
| Префикс области <br/> | Задание<br/>      |
| Примечания <br/>          | Нет<br/>     |



 

## <a name="structural-content"></a>Структурное содержимое

XML-структура этого элемента:

``` syntax
<psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_ProfileValue_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_ProfileDataValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_PathValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a>Переменные структуры

В следующей таблице описаны характеристики переменных, определенных в структуре XML.



| Имя                            | Тип данных         | Единица измерения           | Поддерживаемые значения          | Сводка                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| \_профилевалуе\_<br/>     | строка<br/> | Недоступно<br/> | RGB, ICC, CMYK<br/> | Задает цветовой профиль.<br/>        |
| \_пасвалуе\_<br/>        | строка<br/> | Недоступно<br/> | Недоступно<br/>            | Указывает путь к профилю файла.<br/> |
| \_профиледатавалуе\_<br/> | строка<br/> | Недоступно<br/> | Недоступно<br/>            | Содержит содержимое данных профиля.<br/>      |



 

## <a name="extensible-markup-language-xml-content"></a>Содержимое язык XML (XML)

Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен. Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:

``` syntax
 <psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




