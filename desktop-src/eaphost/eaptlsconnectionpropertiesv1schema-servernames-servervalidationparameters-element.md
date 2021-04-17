---
title: Элемент ServerName (Сервервалидатионпараметерс) (TLS)
description: Сведения об элементе ServerName (Сервервалидатионпараметерс). Этот элемент представляет список имен серверов, разделенных точкой с запятой. | Элемент ServerName (Сервервалидатионпараметерс) (TLS)
ms.assetid: c6cfcc67-4e6a-4bf0-87d9-37cc1d504598
keywords:
- ServerName, элемент EAPHost
topic_type:
- apiref
api_name:
- ServerNames
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef94bc650432c4fb87abf00a93841d0d4d42e965
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694062"
---
# <a name="servernames-servervalidationparameters-element-tls"></a>Элемент ServerName (Сервервалидатионпараметерс) (TLS)

Элемент **ServerName (сервервалидатионпараметерс)** представляет список имен серверов, разделенных точкой с запятой.

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

Элемент **ServerName** определяется сложным типом [**сервервалидатионпараметерс**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="remarks"></a>Комментарии

Каждое имя сервера отделяется точкой с запятой и может быть представлено регулярными выражениями. Элемент **ServerName** является необязательным.

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**сервервалидатионпараметерс**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Возможные непосредственные родительские элементы в экземпляре схемы**
</dt> <dt>

[**Сервервалидатион (Еаптипе)**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Элементы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





