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
ms.openlocfilehash: 25582be51d3206c17076c702bb159f13b012d5964a10cc4ebd7908459447fcc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801124"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**ланполици**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**ланполици**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




