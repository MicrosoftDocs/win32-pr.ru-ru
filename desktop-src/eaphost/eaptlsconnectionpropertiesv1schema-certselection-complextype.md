---
title: Сложный тип Цертселектион
description: Сведения о сложном типе Цертселектион. Этот тип определяет, как пользователь выбирает сертификат.
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- Цертселектион сложный тип EAPHost
topic_type:
- apiref
api_name:
- CertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba22df8dca61696f214e495542319168183dd2bf
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339260"
---
# <a name="certselection-complex-type"></a>Сложный тип Цертселектион

Сложный тип **цертселектион** определяет, как пользователь выбирает сертификат.

``` syntax
<xs:complexType name="CertSelection">
    <xs:sequence>
        <xs:element name="SimpleCertSelection"
            type="boolean"
            minOccurs="0"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                     | Тип    | Описание                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**симплецертселектион**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | Логическое | По умолчанию имеет значение TRUE. Если [**симплецертселектион**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) имеет значение true, EAP-TLS выполняет простой поиск сертификатов без раскрывающихся списков для выбора сертификатов. Если **симплецертселектион** имеет значение false, EAP-TLS показывает пользователю подходящий сертификат для выбора.<br/> |



## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Сложные типы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





