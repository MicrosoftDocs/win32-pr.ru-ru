---
title: Кредентиалссаурце (Еаптипе), элемент
description: Сведения об элементе Кредентиалссаурце (Еаптипе). Этот элемент содержит сведения о расположении сертификата EAP-TLS.
ms.assetid: 6ef48e5e-7c71-472f-ab01-0a43a97ecd96
keywords:
- Элемент Кредентиалссаурце EAPHost
topic_type:
- apiref
api_name:
- CredentialsSource
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d68eccf44b7e2c248e366d8e3d8f05f4e7dd4774
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105700935"
---
# <a name="credentialssource-eaptype-element"></a>Кредентиалссаурце (Еаптипе), элемент

Элемент **кредентиалссаурце (еаптипе)** содержит сведения о расположении сертификата EAP-TLS.

``` syntax
<xs:element name="CredentialsSource"
    type="CredentialsSourceParameters"
 />
```

Элемент **кредентиалссаурце** определяется элементом [**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Комментарии

Элемент **CredentialSource** является необязательным.

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

 

 





