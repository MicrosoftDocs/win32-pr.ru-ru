---
title: Симплецертселектион (Цертселектион), элемент
description: Сведения об элементе Симплецертселектион (Цертселектион). Этот элемент определяет, как пользователь выбирает сертификат.
ms.assetid: 28454877-fd07-4b47-9544-f2b4e91c6651
keywords:
- Элемент Симплецертселектион EAPHost
topic_type:
- apiref
api_name:
- SimpleCertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30af9872f7583232e91b037c5b8961e18c7ce863
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070633"
---
# <a name="simplecertselection-certselection-element"></a>Симплецертселектион (Цертселектион), элемент

Элемент **симплецертселектион (цертселектион)** определяет, как пользователь выбирает сертификат.

``` syntax
<xs:element name="SimpleCertSelection"
    type="boolean"
 />
```

Элемент **симплецертселектион** определяется сложным типом [**цертселектион**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) .

## <a name="remarks"></a>Комментарии

По умолчанию **симплецертселектион** имеет значение true. Если **симплецертселектион** имеет значение true, EAP-TLS выполняет простой поиск сертификатов без раскрывающихся списков для выбора сертификатов. Если **симплецертселектион** имеет значение false, EAP-TLS показывает пользователю подходящий сертификат для выбора.

## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|----------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**цертселектион**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**CertificateStore (Кредентиалссаурцепараметерс)**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Элементы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





