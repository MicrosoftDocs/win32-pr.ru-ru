---
title: Элемент username (TLS)
description: Сведения об элементе username. Этот элемент захватывает имя пользователя, которое будет отправлено в ответе EAP-Identity.
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
keywords:
- Элемент username, EAPHost
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
ms.openlocfilehash: 2975b425bc760979b33d83182d94469532944e46
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105700933"
---
# <a name="username-element-tls"></a>Элемент username (TLS)

Элемент **username** захватывает имя пользователя, которое будет отправлено в ответе EAP-Identity.

Если элемент **username** отсутствует, то EAP-TLS использует имя в сертификате, на который ссылается элемент [**усерцерт**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|-------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





