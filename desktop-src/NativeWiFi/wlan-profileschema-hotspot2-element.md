---
description: Расширяет схему профиля WLAN v1 для поддержки сетей Hotspot 2,0.
ms.assetid: DE30DBCB-80B9-43D0-8DE1-56BBA99DBF31
title: Hotspot2 (Вланпрофиле), элемент
ms.topic: reference
ms.date: 10/08/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- Hotspot2
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0e372c1025a74dfb304cacdb0f3a4cf18bcdbabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682822"
---
# <a name="hotspot2-wlanprofile-element"></a>Hotspot2 (Вланпрофиле), элемент

Расширяет схему профиля WLAN v1 для поддержки сетей Hotspot 2,0. Hotspot 2,0 обеспечивает автоматическое подключение к общедоступным службам Wi-Fi, используя существующие учетные данные и членство в сетях поставщиков услуг. Поставщики услуг указывают, как соединения устанавливаются с помощью новых элементов схемы, чтобы описать используемые сети и способ проверки подлинности в них.

``` syntax
<xs:element name="Hotspot2">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="DomainName"
                minOccurs="0"
             />
            <xs:element name="NAIRealm"
                minOccurs="0"
             />
            <xs:element name="Network3GPP"
                minOccurs="0"
             />
            <xs:element name="RoamingConsortium"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Элемент определяется элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Дочерние элементы

| Элемент | Тип | Описание |
|-|-|-|
| [**Имя_домена**](wlan-profileschema-hotspot2-domainname-element.md) | | Доменное имя поставщика домашней сети устройства, идентифицирующее оператора сети. |
| [**наиреалм**](wlan-profileschema-hotspot2-nairealm-element.md) | | Список идентификаторов области идентификаторов доступа к сети (наи). Записи в этом списке обычно имеют форму user@domain . |
| [**Network3GPP**](wlan-profileschema-hotspot2-network3gpp-element.md) | | Список общедоступных идентификаторов мобильной сети (ПЛМН). |
| [**роамингконсортиум**](wlan-profileschema-hotspot2-roamingconsortium-element.md) | | Список уникальных идентификаторов (OUI), назначенных IEEE.  |

## <a name="examples"></a>Примеры

```xml
<Hotspot2>
  <DomainName>contoso.com</DomainName>
  <NAIRealm>
    <name>test1@contoso.com</name>
    <name>test2@contoso.com</name>
  </NAIRealm>
  <Network3GPP>
    <PLMNID>12345</PLMNID>
    <PLMNID>123456</PLMNID>
  </Network3GPP>
  <RoamingConsortium>
    <OUI>00AABB</OUI>
    <OUI>001122</OUI>
  </RoamingConsortium>
</Hotspot2>
```
