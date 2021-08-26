---
title: VendorId (Еапмесодтипе), элемент
description: Относится к поставщику, который определил метод, если элемент Type (Еапмесодтипе) имеет значение 254 (Расширенный метод EAP).
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- Элемент VendorId EAPHost
topic_type:
- apiref
api_name:
- VendorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29508121a9724a52df19038b82d97576a924c3c8bab49ac6801c1de51ec71919
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067304"
---
# <a name="vendorid-eapmethodtype-element"></a>VendorId (Еапмесодтипе), элемент

Элемент **VendorID (еапмесодтипе)** ссылается на поставщика, который определил метод, если элемент [**Type (еапмесодтипе)**](eapcommonschema-type-eapmethodtype-element.md) имеет значение 254 (Расширенный метод EAP).

**ИД поставщика** является необязательным. Если используется, то **ИД поставщика** — это уникальный номер, выданный IANA.

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

Элемент **VendorID** определяется сложным типом [**еапмесодтипе**](eapcommonschema-eapmethodtype-complextype.md) .

## <a name="remarks"></a>Remarks

Элементы [**аусорид**](eapcommonschema-authorid-eapmethodtype-element.md) и **VendorID** не обязательно должны быть одинаковыми для конкретного метода.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



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

 

 





