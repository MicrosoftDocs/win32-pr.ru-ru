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
ms.openlocfilehash: 6b85537ec209f39da87e74db6881abdf60e488b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414904"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**Публикация (Чаннелтипе)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





