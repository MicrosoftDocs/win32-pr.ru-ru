---
description: Сведения об элементе ParameterRef, который определяет ссылку на элемент Параметеринит и о том, как он работает с Скоредпроперти.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1030dcaa40e0fe0d5ccd8c3963cee8a2bda57b9b849e1fa7c0547f025b5f8955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947824"
---
# <a name="parameterref"></a>ParameterRef

Этот раздел не является актуальным. Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Элемент ParameterRef определяет ссылку на элемент Параметеринит. Элемент Скоредпроперти, содержащий элемент ParameterRef, не имеет явно заданного элемента value. Вместо этого элемент Скоредпроперти получает свое значение из элемента Параметеринит, на который ссылается элемент ParameterRef.

## <a name="element-tag"></a>Тег элемента

<ParameterRef>

## <a name="xml-attributes"></a>XML-атрибуты

В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.



| Атрибут XML   | Сведения                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Содержит атрибут Name элемента Параметердеф, на который имеется ссылка в контексте текущего документа.<br/> |



 

Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .

## <a name="element-information"></a>Сведения об элементе

В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.



| Категория                   | Сведения                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Родительские элементы<br/> | скоредпроперти <br/>                                                                        |
| Дочерние элементы<br/>  | Нет разрешенных.<br/>                                                                        |
| Этот элемент<br/>    | Символьные данные не допускаются.<br/> Дублирование дочерних одноуровневых элементов не разрешено.<br/> |



 

## <a name="configuration-dependencies"></a>Зависимости конфигурации

Элементы ParameterRef не могут иметь зависимости конфигурации.

## <a name="example"></a>Пример

В следующем примере показано, как использовать элементы ParameterRef, чтобы пользователи могли вводить пользовательские параметры размера носителя.

``` syntax
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
  <psf:Property name="psk:DisplayName">
    <psf:Value xsi:type="xs:string">Fabrikam User Custom</psf:Value>
  </psf:Property>
</psf:Option>
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




