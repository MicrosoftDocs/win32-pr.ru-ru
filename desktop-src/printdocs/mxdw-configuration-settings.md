---
description: Средство записи документов XPS (Майкрософт) (МКСДВ) позволяет пользователям создавать файлы документов XPS путем печати из любого приложения Windows.
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: Параметры конфигурации МКСДВ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4026a99baa33ec50bc3ad129ef6610a428f83ab
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105684810"
---
# <a name="mxdw-configuration-settings"></a>Параметры конфигурации МКСДВ

Средство записи документов XPS (Майкрософт) (МКСДВ) позволяет пользователям создавать файлы документов XPS путем печати из любого приложения Windows. Разработчики приложений могут управлять следующими параметрами вывода МКСДВ с помощью частей PrintTicket и PrintCapabilities [схемы печати](./printschema.md).

## <a name="jobinterleaving"></a>жобинтерлеавинг

Параметр Жобинтерлеавинг управляет порядком расположения содержимого для документов XPS. Дополнительные сведения о переработе заданий см. в [спецификации XML Paper](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf). МКСДВ поддерживает следующие два параметра для этого параметра:

-   **Отключено** . Этот параметр отключает вывод, чтобы все данные для каждого элемента содержимого в документе были непрерывными, что повышает эффективность произвольного доступа. Этот вариант лучше подходит для просмотра документа XPS.
-   **On** — этот параметр включает вывод, чтобы данные для каждого элемента содержимого были разбиты и переупорядочены для более эффективной последовательной обработки. Этот вариант лучше подходит для скачивания и печати через Интернет.

В следующем примере приведен пример XML-кода PrintCapabilities, который включает параметр Жобинтерлеавинг.


```XML
<psf:Feature name="ns0000:JobInterleaving">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Interleaving</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:OFF" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">Off - Best for viewing</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:ON" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">On - Best for the web/printing</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



XML PrintTicket аналогичен, за исключением того, что он указывает конкретный параметр. Дополнительные сведения см. в [схеме печати](./printschema.md) .

Поскольку Жобинтерлеавинг не является одним из [общедоступных ключевых слов схемы печати](./print-schema-public-keywords.md), необходимо включить объявление пространства имен (в данном случае "ns0000") в теге **PrintCapabilities** (или **PrintTicket**) в начале документа PrintCapabilities (или PrintTicket), как показано в следующем примере:


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a>жобимажетипе

Жобимажетипе управляет форматом вывода внедренных растровых форматов. МКСДВ поддерживает следующие четыре параметра для этого параметра:

-   **Жпегхигх** . Этот параметр указывает изображение JPEG с высоким уровнем сжатия. Этот параметр дает минимальный размер файла, но самое низкое качество изображения.
-   **Жпегмед** . Этот параметр указывает изображение JPEG с средним уровнем сжатия. Этот параметр обеспечивает оптимальный баланс размера файла и качества изображения.
-   **Жпеглов** . Этот параметр указывает изображение JPEG с низким уровнем сжатия. Этот параметр приводит к наименьшему сокращению размера файла и высокого качества изображения.
-   **PNG** — этот параметр задает формат изображения PNG с уплотнением без потерь. Этот параметр позволяет получить максимальный размер файла и наибольшее качество изображения.

Ниже показан XML-код PrintCapabilities параметра Жобимажетипе:


```XML
<psf:Feature name="ns0000:JobImageType">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Images</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:JPEGHigh" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Maximum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGMed" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
        <psf:Value xsi:type="xsd:string">JPG - Medium compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGLow" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Minimum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:PNG" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">PNG - Lossless compression</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



XML PrintTicket аналогичен, за исключением того, что он указывает конкретный параметр. Дополнительные сведения см. в [схеме печати](./printschema.md) .

Поскольку Жобимажетипе не является одним из [общедоступных ключевых слов схемы печати](./print-schema-public-keywords.md), необходимо включить объявление пространства имен (в данном случае "ns0000") в теге **PrintCapabilities** (или **PrintTicket**) в начале документа PrintCapabilities (или PrintTicket), как показано в следующем примере:


```XML
<psf:PrintTicket 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[Схема печати](./printschema.md)
</dt> <dt>

[Спецификация XPS и загрузка лицензий](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
