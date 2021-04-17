---
description: Указывает имя и тип беспроводной сети.
ms.assetid: 839afae0-b8e1-489f-8811-19a82c173627
title: Сложный тип Нетворкитемтипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkItemType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5db7c5fc4d9b5227d9cd29c5e2dfc69da6fad139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674216"
---
# <a name="networkitemtype-complex-type"></a>Сложный тип Нетворкитемтипе

Сложный тип Нетворкитемтипе указывает имя и тип беспроводной сети.

``` syntax
<xs:complexType name="networkItemType">
    <xs:sequence>
        <xs:element name="networkName"
            type="networkNameType"
         />
        <xs:element name="networkType"
            type="networkTypeType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                      | Тип                                                                    | Описание                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------|
| [**networkName**](wlan-policyschema-networkname-networkitemtype-element.md) | [**нетворкнаметипе**](wlan-policyschema-networknametype-simpletype.md) | Идентификатор набора служб (SSID) сети. <br/> |
| [**нетворктипе**](wlan-policyschema-networktype-networkitemtype-element.md) | [**нетворктипетипе**](wlan-policyschema-networktypetype-simpletype.md) | Тип сети. <br/>                                 |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




