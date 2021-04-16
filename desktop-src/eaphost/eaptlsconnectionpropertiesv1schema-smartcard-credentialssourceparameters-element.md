---
title: Элемент смарт-карты (Кредентиалссаурцепараметерс)
description: Указывает, что EAP-TLS должен считывать сертификат из смарт-карты.
ms.assetid: 0755b0bf-520a-4ae6-a8fc-2f69ae12b066
keywords:
- Элемент смарт-карты EAPHost
topic_type:
- apiref
api_name:
- SmartCard
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14581a06064a242a0f66e763e0b848d7d74bce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710509"
---
# <a name="smartcard-credentialssourceparameters-element"></a>Элемент смарт-карты (Кредентиалссаурцепараметерс)

Элемент Smart Card **(кредентиалссаурцепараметерс)** указывает, что EAP-TLS должен прочитать сертификат из смарт-карты.

``` syntax
<xs:element name="SmartCard"
    type="emptyString"
 />
```

Элемент **смарт-карты** определяется сложным типом [**кредентиалссаурцепараметерс**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .

## <a name="remarks"></a>Комментарии

Элементы [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) и **смарт-карты** не могут одновременно использоваться одновременно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**кредентиалссаурцепараметерс**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Кредентиалссаурце (Еаптипе)**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Элементы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





