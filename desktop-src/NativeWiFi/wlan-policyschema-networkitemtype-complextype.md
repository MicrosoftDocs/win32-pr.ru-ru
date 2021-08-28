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
ms.openlocfilehash: 9c5a08eafebc81a1ff9f18c3d4c2cc9df9c096ac0fef9c10ff1caf1142a1ecf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800194"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 




