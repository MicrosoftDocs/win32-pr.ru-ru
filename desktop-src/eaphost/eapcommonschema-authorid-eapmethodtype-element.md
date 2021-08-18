---
title: Аусорид (Еапмесодтипе), элемент
description: Сведения об элементе Аусорид (Еапмесодтипе). Элемент Аусорид (Еапмесодтипе) ссылается на автора метода.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- Элемент Аусорид EAPHost
topic_type:
- apiref
api_name:
- AuthorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f15c5fc981592bb82f9ad52d590f12ac0b1f4b20af3537a511d01dd0a8cc15e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021754"
---
# <a name="authorid-eapmethodtype-element"></a>Аусорид (Еапмесодтипе), элемент

Элемент **аусорид (еапмесодтипе)** ссылается на автора метода.

Аусорид — это уникальный номер, выданный IANA.

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

Элемент **аусорид** определяется сложным типом [**еапмесодтипе**](eapcommonschema-eapmethodtype-complextype.md) .

## <a name="remarks"></a>Remarks

Элементы **аусорид** и [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) не обязательно должны быть одинаковыми для конкретного метода.

## <a name="requirements"></a>Requirements (Требования)



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Сервер<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**еапмесодтипе**](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема еапкоммон](eapcommonschema-schema.md)
</dt> </dl>

 

 





