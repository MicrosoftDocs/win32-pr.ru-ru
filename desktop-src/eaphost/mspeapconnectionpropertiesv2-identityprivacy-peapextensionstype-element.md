---
title: Идентитиприваци (Пеапекстенсионстипе), элемент
description: Элемент Идентитиприваци (Пеапекстенсионстипе) указывает, отправляется ли в схеме mspeapconnectionpropertiesv2 истинное удостоверение пользователя.
ms.assetid: 57b8747e-6919-4243-a379-3a85c4a2023a
keywords:
- Элемент Идентитиприваци EAPHost
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
ms.openlocfilehash: d0a23ce28a1a807bb948c114435463102561570b
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988950"
---
# <a name="the-identityprivacy-peapextensionstype-element"></a>Элемент Идентитиприваци (Пеапекстенсионстипе)

Элемент **идентитиприваци (пеапекстенсионстипе)** указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение.

``` syntax
<xs:element name="IdentityPrivacy"
    type="IdentityPrivacyParameters"
 />
```

Элемент **идентитиприваци** определяется элементом [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .

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

[Схема mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Элементы схемы mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





