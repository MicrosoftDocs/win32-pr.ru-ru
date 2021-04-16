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
ms.openlocfilehash: 5aabc29a7fe5122a7f7571750b97ebccb38158d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710505"
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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**Соединения**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Соединения**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





