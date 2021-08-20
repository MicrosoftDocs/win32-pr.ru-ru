---
title: Элемент User
description: Сведения об элементе User. Этот элемент не используется при использовании устаревших методов через API-интерфейсы EAPHost.
ms.assetid: d35fb4ba-5f48-431d-b2bf-738043f5d1ff
keywords:
- Элемент пользователя EAPHost
topic_type:
- apiref
api_name:
- User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0f21b22320029bf1d10a209eae6a3b2192512a541c1e681b71e112d488c87ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086408"
---
# <a name="user-element"></a>Элемент User

Элемент **User** не используется при использовании устаревших методов через API-интерфейсы EAPHost.

``` syntax
<xs:element name="User">
    <xs:complexType>
        <xs:sequence>
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                  | Тип | Описание                                                                     |
|----------------------------------------------------------|------|---------------------------------------------------------------------------------|
| [**Протокола**](baseeapuserpropertiesv1schema-eap-element.md) |      | Захватывает сведения о типе метода и учетных данных, специфичных для метода.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Сервер<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





