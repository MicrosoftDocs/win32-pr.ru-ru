---
title: Дифферентусернаме (Еаптипе), элемент
description: Сведения об элементе Дифферентусернаме (Еаптипе). Этот элемент определяет, какое имя пользователя использует EAP-TLS.
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- Элемент Дифферентусернаме EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 505e23c74d4c1c8c74a50906809d0acc9ce06c42
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105700931"
---
# <a name="differentusername-eaptype-element"></a>Дифферентусернаме (Еаптипе), элемент

Элемент **дифферентусернаме (еаптипе)** определяет, какое имя пользователя использует EAP-TLS.

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

Элемент **дифферентусернаме** определяется элементом [**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Комментарии

Если элемент **дифферентусернаме** имеет значение true, то EAP-TLS должен использовать имя пользователя, отличное от имени, которое отображается в сертификате. Если элемент **дифферентусернаме** имеет значение false, то EAP-TLS использует имя пользователя, которое отображается в сертификате.

Элемент **дифферентусернаме** является необязательным.

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Элементы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





