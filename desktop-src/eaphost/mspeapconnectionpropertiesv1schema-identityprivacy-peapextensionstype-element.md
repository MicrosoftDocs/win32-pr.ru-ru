---
title: Элемент Идентитиприваци (Пеапекстенсионстипе) (v1)
description: Элемент Идентитиприваци (Пеапекстенсионстипе) указывает, отправляется ли в схеме mspeapconnectionpropertiesv1 истинное удостоверение пользователя.
ms.assetid: 1ae5b6e8-b1f8-45a7-ad22-fdb57cc756a2
keywords:
- элемент EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7195ce43fb3f1a1f1710fe7aee3f5f74e18f3786
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989219"
---
# <a name="identityprivacy-peapextensionstype-element"></a>Идентитиприваци (Пеапекстенсионстипе), элемент

Элемент **идентитиприваци (пеапекстенсионстипе)** указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение.

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:IdentityPrivacy"
 />
```

Элемент определяется элементом [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .

## <a name="remarks"></a>Remarks

Элемент **идентитиприваци** является необязательным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**пеапекстенсионс**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Элементы схемы mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[**Идентитиприваци (Пеапекстенсионстипе)**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)
</dt> </dl>

 

 





