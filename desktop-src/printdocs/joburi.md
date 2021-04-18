---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: жобури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb06148438b0fd6715370c56ff9efe54d512219
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693925"
---
# <a name="joburi"></a>жобури

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Задает универсальный код ресурса (URI) для документа.

-   [Сведения об элементе](#element-information)
-   [Структурное содержимое](#structural-content)
-   [Содержимое язык XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Сведения об элементе



| Имя                       |                     |
|----------------------------|---------------------|
| Тип элемента <br/>   | Свойство<br/> |
| Префикс области <br/> | Задание<br/>      |
| Примечания <br/>          | Нет<br/>     |



 

## <a name="structural-content"></a>Структурное содержимое

XML-структура этого элемента выглядит следующим образом:

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a>Переменные структуры

В следующей таблице описаны характеристики переменных, определенных в структуре XML.



| Имя                       | Тип данных         | Unit | Поддерживаемые значения | Сводка |
|----------------------------|-------------------|------|------------------|---------|
| \_жобуривалуе\_<br/> | строка<br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a>Содержимое язык XML (XML)

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




