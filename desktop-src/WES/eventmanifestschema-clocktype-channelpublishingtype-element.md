---
title: Клокктипе (Чаннелпублишингтипе), элемент
description: Разрешение часов, используемое при записи метки времени для каждого события.
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- Журнал событий элемента Клокктипе
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fde3b263c2a190e91fdd2ddde8f05a40e9026486195ca9ae95b5f98cdcf7733d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590035"
---
# <a name="clocktype-channelpublishingtype-element"></a>Клокктипе (Чаннелпублишингтипе), элемент

Разрешение часов, используемое при записи метки времени для каждого события.

``` syntax
<xs:element name="clockType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="SystemTime"
             />
            <xs:enumeration
                value="QPC"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Элемент **клокктипе** определяется сложным типом [**чаннелпублишингтипе**](eventmanifestschema-channelpublishingtype-complextype.md) .

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

 

 





