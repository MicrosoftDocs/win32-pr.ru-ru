---
title: Сложный тип Процессинжеррордататипе
description: Определяет ошибку, которая произошла во время отображения данных события для события.
ms.assetid: fd1cc78c-1da5-43c5-8c4b-8abe7e1dc1e1
keywords:
- Журнал событий сложных типов Процессинжеррордататипе
topic_type:
- apiref
api_name:
- ProcessingErrorDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ee34e566bafa72812303fcb1f41b664a45aa77772e6ee818b9cb79bc94cbb51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904533"
---
# <a name="processingerrordatatype-complex-type"></a>Сложный тип Процессинжеррордататипе

Определяет ошибку, которая произошла во время отображения данных события для события. Это может произойти, если данные события не соответствуют определению шаблона данных события в манифесте.

``` syntax
<xs:complexType name="ProcessingErrorDataType">
    <xs:sequence>
        <xs:element name="ErrorCode"
            type="unsignedInt"
         />
        <xs:element name="DataItemName"
            type="string"
         />
        <xs:element name="EventPayload"
            type="hexBinary"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                          | Тип        | Описание                                                                          |
|----------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------|
| [**DataItemName**](eventschema-dataitemname-processingerrordatatype-element.md) | строка      | Имя элемента данных события, вызвавшего ошибку.<br/>                    |
| [**Код ошибки**](eventschema-errorcode-processingerrordatatype-element.md)       | unsignedInt | Код ошибки ошибки, произошедшей при отображении данных события.<br/> |
| [**евентпайлоад**](eventschema-eventpayload-processingerrordatatype-element.md) | hexBinary   | Двоичный BLOB-объект, содержащий все данные события.<br/>                        |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





