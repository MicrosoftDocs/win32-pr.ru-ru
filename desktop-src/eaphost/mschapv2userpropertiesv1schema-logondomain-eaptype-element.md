---
title: LogonDomain (Еаптипе), элемент
description: Сведения об элементе LogonDomain (Еаптипе). Этот элемент определяет домен пользователя или компьютера, для которого выполняется проверка подлинности.
ms.assetid: a93793cd-29ee-47f9-8d91-895844c08bae
keywords:
- Элемент LogonDomain EAPHost
topic_type:
- apiref
api_name:
- LogonDomain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dbbe57bcd29459f6e9807d8f39aedb4faa72a1b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070608"
---
# <a name="logondomain-eaptype-element"></a>LogonDomain (Еаптипе), элемент

Элемент **LogonDomain (еаптипе)** определяет домен пользователя или компьютера, для которого выполняется проверка подлинности.

``` syntax
<xs:element name="LogonDomain
          
        "
    type="string"
 />
```

Элемент **LogonDomain** определяется элементом [**еаптипе**](mschapv2userpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Комментарии

Если элемент **LogonDomain (еаптипе)** отсутствует, используется домен из Winlogon. Этот элемент является необязательным.

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**еаптипе**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**еаптипе**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





