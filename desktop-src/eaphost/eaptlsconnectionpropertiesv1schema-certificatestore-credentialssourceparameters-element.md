---
title: CertificateStore (Кредентиалссаурцепараметерс), элемент
description: Указывает, что EAP-TLS должен прочитать сертификат из моего хранилища пользователя или проверить подлинность компьютера.
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- Элемент CertificateStore EAPHost
topic_type:
- apiref
api_name:
- CertificateStore
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fb3d2b5c9d50ea8b63c513e4fd9e7297afe236c5ccd16711d9bf4371e76a8d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274296"
---
# <a name="certificatestore-credentialssourceparameters-element"></a>CertificateStore (Кредентиалссаурцепараметерс), элемент

Элемент **CertificateStore (кредентиалссаурцепараметерс)** указывает, что EAP-TLS должен прочитать сертификат из моего хранилища пользователя или проверить подлинность компьютера.

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

Элемент **CertificateStore** определяется сложным типом [**кредентиалссаурцепараметерс**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .

## <a name="remarks"></a>Remarks

Элементы **CertificateStore** и [**смарт-карты**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) не могут одновременно использоваться одновременно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



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

 

 





