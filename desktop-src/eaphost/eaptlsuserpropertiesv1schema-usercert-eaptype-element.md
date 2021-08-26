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
ms.openlocfilehash: ef25a43bf13b1cfb1e4b03f78f5772567b3bfb92f1c31bb810da7882a4d3e1c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067234"
---
# <a name="usercert-eaptype-element"></a>Усерцерт (Еаптипе), элемент

Элемент **усерцерт (еаптипе)** ссылается на хэш SHA-1 сертификата, который следует использовать для проверки подлинности.

``` syntax
<xs:element name="UserCert"
    type="hexBinary"
 />
```

Элемент **усерцерт** определяется элементом [**еаптипе**](eaptlsuserpropertiesv1schema-eaptype-element.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

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

 

 





