---
title: Идентификатор типа безопасности (Чаннелпублишингтипе), элемент
description: Определяет, следует ли включать идентификатор безопасности (SID) участника с каждым событием, записанным в канал.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- Журнал событий элемента идентификатор типа безопасности
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41653a1fbda3400b74ca5302deb8075ae891e69f22ca0f0e88b6ec4dbb58dfc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589155"
---
# <a name="sidtype-channelpublishingtype-element"></a>Идентификатор типа безопасности (Чаннелпублишингтипе), элемент

Определяет, следует ли включать идентификатор безопасности (SID) участника с каждым событием, записанным в канал.

``` syntax
<xs:element name="sidType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="None"
             />
            <xs:enumeration
                value="Publishing"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Элемент **идентификатор типа безопасности** определяется сложным типом [**чаннелпублишингтипе**](eventmanifestschema-channelpublishingtype-complextype.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**Публикация (Чаннелтипе)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





