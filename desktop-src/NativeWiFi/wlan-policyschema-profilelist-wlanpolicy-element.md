---
description: Содержит список профилей, применяемых на уровне домена или компьютера.
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: Профилелист (Вланполици), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c11fbeb41b43faa31b170dcc856bb0823631001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674211"
---
# <a name="profilelist-wlanpolicy-element"></a>Профилелист (Вланполици), элемент

Элемент Профилелист (Вланполици) содержит список профилей, применяемых на уровне домена или компьютера. Этот элемент является необязательным. Если этот элемент имеется, он должен содержать по крайней мере один профиль.

Профили должны основываться на [ \_ схеме профиля WLAN](wlan-profileschema-schema.md)с корневым элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md).

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Элемент **профилелист** определяется элементом [**вланполици**](wlan-policyschema-wlanpolicy-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**вланполици**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**вланполици**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




