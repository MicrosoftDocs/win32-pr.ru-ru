---
description: Элемент Профилелист (Ланполици) — содержит список профилей, применяемых на уровне домена или компьютера.
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: Профилелист (Ланполици), элемент
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
ms.openlocfilehash: 5d18ebc99f48bf72599afe750863d684b8158608
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090782"
---
# <a name="profilelist-lanpolicy-element"></a>Профилелист (Ланполици), элемент

Элемент Профилелист (Ланполици) содержит список профилей, применяемых на уровне домена или компьютера. Профили должны быть основаны на [ \_ схеме профиля локальной сети](lan-profileschema-schema.md)с корневым элементом [**ланпрофиле**](lan-profileschema-lanprofile-element.md). Профили, основанные на любой другой схеме, будут игнорироваться.

Если [**енаблеаутоконфиг**](lan-policyschema-enableautoconfig-globalflags-element.md) имеет значение false, этот элемент не должен присутствовать в профиле политики локальной сети. Если **енаблеаутоконфиг** имеет значение true, этот элемент является обязательным.

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

Элемент **профилелист** определяется элементом [**ланполици**](lan-policyschema-lanpolicy-element.md) .

## <a name="remarks"></a>Remarks

Этот элемент должен содержать только один сетевой профиль. Если в политике указано более одного профиля, будет применена только первая сеть.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**ланполици**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**ланполици**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




