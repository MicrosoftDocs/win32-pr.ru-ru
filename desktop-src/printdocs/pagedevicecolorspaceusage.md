---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: c529c731-fcf0-463e-a251-6a05215e4d23
title: пажедевицеколорспацеусаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf26811bc8c008fa06d647b25e48914a6e724d7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999181"
---
# <a name="pagedevicecolorspaceusage"></a>пажедевицеколорспацеусаже

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

В сочетании с параметром Пажедевицеколорспацепрофилеури этот параметр определяет поведение отрисовки для элементов, представленных в цветовом пространстве устройства.

-   [Сведения об элементе](#element-information)
-   [Структурное содержимое](#structural-content)
-   [Содержимое язык XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Сведения об элементе



| Имя | Значение |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Тип элемента <br/>   | Компонент<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Префикс области <br/> | Страница<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Примечания <br/>          | Это относится только к документам XPS и не должен использоваться в произвольных PrintTicket.<br/> Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket. Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части. Эти параметры относятся к формату XPS. <br/> URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса. Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.<br/> |



 

## <a name="structural-content"></a>Структурное содержимое

XML-структура этого элемента:

``` syntax
<psf:Feature name="psk:PageDeviceColorSpaceUsage">
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
<psf:Feature name="psk:PageDeviceColorSpaceUsage">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- If the device determines that the profile specified by the PageDeviceColorSpaceProfileURI parameter can be used as a device color space profile, all elements using the same profile are treated as already being specified in device color space. All other elements MUST use the profile specified for that element.
If the profile cannot be used as a device color space profile, elements using the profile MUST be color managed like any other element using the color profile. -->
  <psf:Option name="psk:MatchToDefault" />
  <!-- If the profile specified by the PageDeviceColorSpaceProfileURI parameter has a number of channels matching the number of primaries of the device, it SHOULD be used instead of the devices internal color management for all elements. Elements using this profile are assumed to be in device color space and will not be color managed further. -->
  <psf:Option name="psk:OverrideDeviceDefault" />
</psf:Feature>
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




