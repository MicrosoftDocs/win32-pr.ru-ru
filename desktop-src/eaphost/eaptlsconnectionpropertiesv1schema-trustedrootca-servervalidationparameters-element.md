---
title: Элемент Трустедрутка (Сервервалидатионпараметерс) — подключение
description: Записывает отпечатки для корневых центров сертификации (CAs), которые являются доверенными для клиента. | Трустедрутка (Сервервалидатионпараметерс), элемент
ms.assetid: 81e3b6ca-6360-42dc-bfd3-298e81e66c1a
keywords:
- Элемент Трустедрутка EAPHost
topic_type:
- apiref
api_name:
- TrustedRootCA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e6f91816ba90300a76545a7a22cea6d037b4e897
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105694366"
---
# <a name="trustedrootca-servervalidationparameters-element-for-connection-properties"></a>Элемент Трустедрутка (Сервервалидатионпараметерс) для свойств соединения

Элемент **трустедрутка (сервервалидатионпараметерс)** захватывает отпечатки для корневых центров сертификации (CAS), которые являются доверенными для клиента.

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

Элемент **трустедрутка** определяется сложным типом [**сервервалидатионпараметерс**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="remarks"></a>Комментарии

Thumb Print — это шестнадцатеричная строка, которая содержит хэш SHA-1 сертификата. Элемент **трустедрутка** является необязательным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



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

 

 





