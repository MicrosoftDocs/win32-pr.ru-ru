---
title: Элемент EventID (Системпропертиестипе)
description: Идентификатор, используемый поставщиком для идентификации события.
ms.assetid: 2d5ac44b-4157-4b87-bd8f-e992e85dd0b1
keywords:
- Журнал событий элемента EventID
topic_type:
- apiref
api_name:
- EventID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac1b2edd671f06d88c8c51b49c16f759fd05e087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489489"
---
# <a name="eventid-systempropertiestype-element"></a>Элемент EventID (Системпропертиестипе)

Идентификатор, используемый поставщиком для идентификации события.

``` syntax
<xs:element name="EventID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedInt"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

Элемент **EventID** определяется сложным типом [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**Система (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





