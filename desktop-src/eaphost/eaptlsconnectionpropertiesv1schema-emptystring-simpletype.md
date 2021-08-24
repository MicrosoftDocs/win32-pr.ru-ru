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
ms.openlocfilehash: 4f210fadeb0097ffd7a11d80dd47b252dbbfdc614950af0ac07d612b44edd0aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948214"
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

## <a name="requirements"></a>Requirements (Требования)



| Роль | Минимальная поддерживаемая версия ОС |
|-------------------------------------|------------------------------------------------------|
| Клиент<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Сервер<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Простые типы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-simple-types.md)
</dt> </dl>

 

 





