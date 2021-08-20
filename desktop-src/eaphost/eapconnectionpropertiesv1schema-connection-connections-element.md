---
title: Элемент соединения (Connections)
description: Определяет каждый параметр конфигурации и связывает его с именем. Элемент Connection является необязательным.
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- Элемент соединения EAPHost
topic_type:
- apiref
api_name:
- Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6948675f7910c46cb2b5db4285ce0df795fa057f275ce29b7f4c664b14c4ce1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498374"
---
# <a name="connection-connections-element"></a>Элемент соединения (Connections)

Элемент **Connection (Connections)** определяет каждый параметр конфигурации и связывает его с именем. Элемент **Connection** является необязательным.

``` syntax
<xs:element name="Connection">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="string"
             />
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Элемент **Connection** определяется элементом [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                 | Тип   | Описание                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [**Протокола**](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | Определяет элемент конфигурации EAP.<br/>                                                                    |
| [**Название**](eapconnectionpropertiesv1schema-name-connection-element.md) | строка | Захватывает имя определяемого соединения, помогая идентифицировать несколько соединений. <br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**Соединение**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Соединение**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





