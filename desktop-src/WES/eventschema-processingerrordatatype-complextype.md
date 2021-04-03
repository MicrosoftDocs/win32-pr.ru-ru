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
ms.openlocfilehash: ffcc9d2beed4050a8eed34925f30e52f67d129b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136898"
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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





