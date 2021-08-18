---
description: Проверьте элемент Пажедестинатионколорпрофиле, настраиваемый пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: пажедестинатионколорпрофиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7287267339abdb078a515b7a8310d19314a25dd36b5fad11b466146ae2ea17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098878"
---
# <a name="pagedestinationcolorprofile"></a>пажедестинатионколорпрофиле

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Определяет характеристики цветового профиля назначения. Описывает, будет ли приложение или драйвер выбирать используемый цветовой профиль назначения.

-   [Сведения об элементе](#element-information)
-   [Структурное содержимое](#structural-content)
-   [Содержимое язык XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Сведения об элементе



| Имя | Значение |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Тип элемента <br/>   | Компонент<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Префикс области <br/> | Страница<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Примечания <br/>          | Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket. Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части. Эти параметры относятся к формату XPS. <br/> URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса. Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.<br/> |



 

## <a name="structural-content"></a>Структурное содержимое

XML-структура этого элемента:

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
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



| Имя                               | Тип данных         | Единица измерения                  | Поддерживаемые значения                                                                                                                                                                      | Итоги                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | строка<br/> | characters<br/> | Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Если пространство имен не указано, предполагается использование пространства имен по умолчанию.<br/> | Имя параметра.<br/>                                           |
| \_идентитйоптионвалуе\_<br/> | строка<br/> | Недоступно<br/>        | True, False.<br/>                                                                                                                                                               | Определяет параметр, который при выборе этого параметра отключит эту функцию.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Содержимое язык XML (XML)

Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен. Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
  <!-- Application specifies the destination profile to be used. -->
  <psf:Option name="psk:Application">
    <!-- Destination profile used to perform color management. -->
    <psf:ScoredProperty name="psk:DestinationColorProfileURI">
      <psf:ParameterRef name="psk:PageDestinationColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DestinationColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageDestinationColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Driver selects the destination profile that best matches its current configuration. -->
  <psf:Option name="psk:DriverConfiguration" />
</psf:Feature>
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




