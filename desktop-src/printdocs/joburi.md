---
description: Сведения об элементе Жобури, который указывает универсальный код ресурса (URI) для документа.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: жобури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c6ad4eadf3698c1ff3b0d6ae4cb45ce95defa8de3cad2a2a744b0eb7ef36fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461034"
---
# <a name="joburi"></a>жобури

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Задает универсальный код ресурса (URI) для документа.

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

XML-структура этого элемента выглядит следующим образом:

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a>Переменные структуры

В следующей таблице описаны характеристики переменных, определенных в структуре XML.



| Имя                       | Тип данных         | Единица измерения | Поддерживаемые значения | Сводка |
|----------------------------|-------------------|------|------------------|---------|
| \_жобуривалуе\_<br/> | строка<br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a>Содержимое язык XML (XML)

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




