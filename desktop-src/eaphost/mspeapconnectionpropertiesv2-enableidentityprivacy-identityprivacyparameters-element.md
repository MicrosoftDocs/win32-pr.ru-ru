---
title: Енаблеидентитиприваци (Идентитиприваципараметерс), элемент
description: Указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение. | Енаблеидентитиприваци (Идентитиприваципараметерс), элемент
ms.assetid: 7751e5fa-895e-47f7-99d9-aa7ef2451eb1
keywords:
- Элемент Енаблеидентитиприваци EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a96b49fe462f4ef8cedad550d1a6c87d680939
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353772"
---
# <a name="enableidentityprivacy-identityprivacyparameters-element"></a>Енаблеидентитиприваци (Идентитиприваципараметерс), элемент

Элемент **енаблеидентитиприваци (идентитиприваципараметерс)** указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение.

``` syntax
<xs:element name="EnableIdentityPrivacy"
    type="xs:Boolean"
    minOccurs="0"
 />
```

Элемент **енаблеидентитиприваци** определяется параметром [идентитиприваципараметерс](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .

## <a name="remarks"></a>Комментарии

Элемент **енаблеидентитиприваци** является необязательным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[идентитиприваципараметерс](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
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

 

 





