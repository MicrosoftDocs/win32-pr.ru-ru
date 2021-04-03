---
title: Трустедрутка (Сервервалидатионпараметерс), элемент
description: Записывает отпечатки для корневых центров сертификации (CAs), которые являются доверенными для клиента. | Трустедрутка (Сервервалидатионпараметерс), элемент
ms.assetid: f0485dcc-8610-4c5b-b4db-6f2a77057489
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
ms.openlocfilehash: e62b691c5075f1a42f87e558a9a1f0795b90e8bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914303"
---
# <a name="trustedrootca-servervalidationparameters-element"></a>Трустедрутка (Сервервалидатионпараметерс), элемент

Элемент **трустедрутка (сервервалидатионпараметерс)** захватывает отпечатки для корневых центров сертификации (CAS), которые являются доверенными для клиента.

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

Элемент **трустедрутка** определяется сложным типом [**сервервалидатионпараметерс**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

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

[**сервервалидатионпараметерс**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Возможные непосредственные родительские элементы в экземпляре схемы**
</dt> <dt>

[**Сервервалидатион (Еаптипе)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Элементы схемы mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





