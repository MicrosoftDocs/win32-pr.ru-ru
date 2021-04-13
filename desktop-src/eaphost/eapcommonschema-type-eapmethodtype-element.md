---
title: Элемент Type (Еапмесодтипе)
description: Сведения об элементе Type (Еапмесодтипе), который ссылается на тип метода EAP. См. раздел требования и просмотрите дополнительные доступные ресурсы.
ms.assetid: 7911e97c-9436-4d60-8497-bee45cdb8db4
keywords:
- Элемент Type EAPHost
topic_type:
- apiref
api_name:
- Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d45defd098f560d4deb8698e0fd569492668e0b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413736"
---
# <a name="type-eapmethodtype-element"></a>Элемент Type (Еапмесодтипе)

Элемент **Type (еапмесодтипе)** ссылается на тип метода EAP.

Тип — это уникальный номер, выданный IANA.

``` syntax
<xs:element name="Type"
    type="unsignedByte"
 />
```

Элемент **Type** определяется сложным типом [**еапмесодтипе**](eapcommonschema-eapmethodtype-complextype.md) .

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**еапмесодтипе**](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема еапкоммон](eapcommonschema-schema.md)
</dt> </dl>

 

 





