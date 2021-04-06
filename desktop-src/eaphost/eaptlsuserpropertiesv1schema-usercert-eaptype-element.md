---
title: Усерцерт (Еаптипе), элемент
description: Ссылается на хэш SHA-1 сертификата, который следует использовать для проверки подлинности.
ms.assetid: 0f0fa37c-dff2-44c6-bd7c-ca54c569fcf1
keywords:
- Элемент Усерцерт EAPHost
topic_type:
- apiref
api_name:
- UserCert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c23840b489bad1e06bdd0c7eb6e0033bfb1961f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803550"
---
# <a name="usercert-eaptype-element"></a>Усерцерт (Еаптипе), элемент

Элемент **усерцерт (еаптипе)** ссылается на хэш SHA-1 сертификата, который следует использовать для проверки подлинности.

``` syntax
<xs:element name="UserCert"
    type="hexBinary"
 />
```

Элемент **усерцерт** определяется элементом [**еаптипе**](eaptlsuserpropertiesv1schema-eaptype-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**еаптипе**](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**еаптипе**](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





