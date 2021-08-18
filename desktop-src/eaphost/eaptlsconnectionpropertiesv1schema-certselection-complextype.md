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
ms.openlocfilehash: 375ea26fddf07f8d775617c0a2167ed02aa8160de8cc5dde49a92f37f57a335e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984134"
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



## <a name="requirements"></a>Requirements (Требования)



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Сервер<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Сложные типы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





