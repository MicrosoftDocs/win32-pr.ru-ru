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
# <a name="hotspot2-wlanprofile-element"></a><span data-ttu-id="e2dc4-103">Hotspot2 (Вланпрофиле), элемент</span><span class="sxs-lookup"><span data-stu-id="e2dc4-103">Hotspot2 (WLANProfile) element</span></span>

<span data-ttu-id="e2dc4-104">Расширяет схему профиля WLAN v1 для поддержки сетей Hotspot 2,0.</span><span class="sxs-lookup"><span data-stu-id="e2dc4-104">Extends the WLAN Profile Schema v1 to support Hotspot 2.0 networks.</span></span> <span data-ttu-id="e2dc4-105">Hotspot 2,0 обеспечивает автоматическое подключение к общедоступным службам Wi-Fi, используя существующие учетные данные и членство в сетях поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="e2dc4-105">Hotspot 2.0 enables automatic connection to public Wi-Fi services using existing credentials and membership in service provider networks.</span></span> <span data-ttu-id="e2dc4-106">Поставщики услуг указывают, как соединения устанавливаются с помощью новых элементов схемы, чтобы описать используемые сети и способ проверки подлинности в них.</span><span class="sxs-lookup"><span data-stu-id="e2dc4-106">Service providers specify how connections are made using the new schema elements to describe which networks to use, and how to authenticate to them.</span></span>

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

<span data-ttu-id="e2dc4-107">Элемент определяется элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e2dc4-107">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e2dc4-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e2dc4-108">Child elements</span></span>

| <span data-ttu-id="e2dc4-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="e2dc4-109">Element</span></span> | <span data-ttu-id="e2dc4-110">Тип</span><span class="sxs-lookup"><span data-stu-id="e2dc4-110">Type</span></span> | <span data-ttu-id="e2dc4-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e2dc4-111">Description</span></span> |
|-|-|-|
| [<span data-ttu-id="e2dc4-112">**Имя_домена**</span><span class="sxs-lookup"><span data-stu-id="e2dc4-112">**DomainName**</span></span>](wlan-profileschema-hotspot2-domainname-element.md) | | <span data-ttu-id="e2dc4-113">Доменное имя поставщика домашней сети устройства, идентифицирующее оператора сети.</span><span class="sxs-lookup"><span data-stu-id="e2dc4-113">The domain name for the device's Home Network Provider, identifying the operator of the network.</span></span> |
| [<span data-ttu-id="e2dc4-114">**наиреалм**</span><span class="sxs-lookup"><span data-stu-id="e2dc4-114">**NAIRealm**</span></span>](wlan-profileschema-hotspot2-nairealm-element.md) | | <span data-ttu-id="e2dc4-115">Список идентификаторов области идентификаторов доступа к сети (наи).</span><span class="sxs-lookup"><span data-stu-id="e2dc4-115">A list of Network Access Identifier (NAI) Realm identifiers.</span></span> <span data-ttu-id="e2dc4-116">Записи в этом списке обычно имеют форму user@domain .</span><span class="sxs-lookup"><span data-stu-id="e2dc4-116">Entries in this list are usually of the form user@domain.</span></span> |
| [<span data-ttu-id="e2dc4-117">**Network3GPP**</span><span class="sxs-lookup"><span data-stu-id="e2dc4-117">**Network3GPP**</span></span>](wlan-profileschema-hotspot2-network3gpp-element.md) | | <span data-ttu-id="e2dc4-118">Список общедоступных идентификаторов мобильной сети (ПЛМН).</span><span class="sxs-lookup"><span data-stu-id="e2dc4-118">A list of Public Land Mobile Network (PLMN) IDs.</span></span> |
| [<span data-ttu-id="e2dc4-119">**роамингконсортиум**</span><span class="sxs-lookup"><span data-stu-id="e2dc4-119">**RoamingConsortium**</span></span>](wlan-profileschema-hotspot2-roamingconsortium-element.md) | | <span data-ttu-id="e2dc4-120">Список уникальных идентификаторов (OUI), назначенных IEEE.</span><span class="sxs-lookup"><span data-stu-id="e2dc4-120">A list of Organizationally Unique Identifiers (OUI) assigned by IEEE.</span></span>  |

## <a name="examples"></a><span data-ttu-id="e2dc4-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="e2dc4-121">Examples</span></span>

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
