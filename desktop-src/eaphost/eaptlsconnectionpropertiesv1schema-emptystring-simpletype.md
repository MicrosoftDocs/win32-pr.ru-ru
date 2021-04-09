---
title: Простой тип emptyString
description: Сведения о простом типе emptyString, который не используется. См. раздел требования и просмотрите дополнительные доступные ресурсы.
ms.assetid: e561b8d5-8683-41a1-bd72-73b1a767b6cf
keywords:
- emptyString простой тип EAPHost
topic_type:
- apiref
api_name:
- emptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 756c8976c8b989cf77be921491770fcff9ea62d5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070643"
---
# <a name="emptystring-simple-type"></a>Простой тип emptyString

Простой тип **emptyString** не используется.

``` syntax
<xs:simpleType name="emptyString">
    <xs:restriction
        base="string"
    >
        <xs:maxLength
            value="0"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|-------------------------------------|------------------------------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Простые типы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-simple-types.md)
</dt> </dl>

 

 





