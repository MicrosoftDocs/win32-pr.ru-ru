---
title: Анонимаусусернаме (Идентитиприваципараметерс), элемент
description: Содержит анонимное удостоверение, используемое вместо истинной идентификации пользователя. Он отправляется во время первого этапа проверки подлинности PEAP, когда удостоверение отправляется в виде обычного текста.
ms.assetid: 74a33a75-cf21-4346-a984-f2f8564c3b57
keywords:
- Элемент Анонимаусусернаме EAPHost
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
ms.openlocfilehash: 6bbc973160a8865e246a6cec87ce02ced136d786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415820"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a>Анонимаусусернаме (Идентитиприваципараметерс), элемент

Элемент **анонимаусусернаме (идентитиприваципараметерс)** содержит анонимное удостоверение, используемое вместо истинной идентификации пользователя. Он отправляется во время первого этапа проверки подлинности PEAP, когда **удостоверение** отправляется в виде обычного текста.

Использование анонимных удостоверений определяется элементом [**енаблеидентитиприваци**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

Элемент **анонимаусусернаме** определяется параметром [идентитиприваципараметерс](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .

## <a name="remarks"></a>Комментарии

Элемент **анонимаусусернаме** является необязательным.

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

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Элементы схемы mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





