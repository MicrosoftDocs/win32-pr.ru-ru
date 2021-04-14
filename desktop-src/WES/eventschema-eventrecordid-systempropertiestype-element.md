---
title: Евентрекордид (Системпропертиестипе), элемент
description: Номер записи, назначенный событию при регистрации.
ms.assetid: d042de4d-e532-432e-bba2-1876a26860a4
keywords:
- Журнал событий элемента Евентрекордид
topic_type:
- apiref
api_name:
- EventRecordID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb937d075bc0ff5fc1cf8bf1335d1274aee4fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414884"
---
# <a name="eventrecordid-systempropertiestype-element"></a>Евентрекордид (Системпропертиестипе), элемент

Номер записи, назначенный событию при регистрации.

``` syntax
<xs:element name="EventRecordID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedLong"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

Элемент **евентрекордид** определяется сложным типом [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





