---
description: Содержит профиль беспроводной локальной сети.
ms.assetid: bc97cb49-3891-4a4a-aab4-895cd9ce6908
title: Вланпрофиле, элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 227d912128bf3f656fca7aecbaf0fe0640659465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913252"
---
# <a name="wlanprofile-element"></a><span data-ttu-id="f19a1-103">Вланпрофиле, элемент</span><span class="sxs-lookup"><span data-stu-id="f19a1-103">WLANProfile Element</span></span>

<span data-ttu-id="f19a1-104">Элемент **вланпрофиле** содержит профиль беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="f19a1-104">The **WLANProfile** element contains a wireless LAN profile.</span></span> <span data-ttu-id="f19a1-105">Этот элемент является уникальным корневым элементом для профиля беспроводной связи.</span><span class="sxs-lookup"><span data-stu-id="f19a1-105">This element is the unique root element for a wireless profile.</span></span>

<span data-ttu-id="f19a1-106">Целевое пространство имен для элемента Вланпрофиле — `https://www.microsoft.com/networking/WLAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="f19a1-106">The target namespace for the WLANProfile element is `https://www.microsoft.com/networking/WLAN/profile/v1`.</span></span>

``` syntax
<xs:element name="WLANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="SSIDConfig"
                maxOccurs="256"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="SSID"
                            maxOccurs="256"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="hex"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:minLength
                                                    value="1"
                                                 />
                                                <xs:maxLength
                                                    value="32"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="name"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:minLength
                                                    value="1"
                                                 />
                                                <xs:maxLength
                                                    value="32"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="nonBroadcast"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="connectionType">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="IBSS"
                         />
                        <xs:enumeration
                            value="ESS"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="connectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="manual"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="autoSwitch"
                type="boolean"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
            <xs:element name="MSM"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="connectivity"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="phyType"
                                        minOccurs="0"
                                        maxOccurs="4"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="a"
                                                 />
                                                <xs:enumeration
                                                    value="b"
                                                 />
                                                <xs:enumeration
                                                    value="g"
                                                 />
                                                <xs:enumeration
                                                    value="n"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="security"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="authEncryption">
                                        <xs:complexType>
                                            <xs:sequence>
                                                <xs:element name="authentication">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="open"
                                                             />
                                                            <xs:enumeration
                                                                value="shared"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA"
                                                             />
                                                            <xs:enumeration
                                                                value="WPAPSK"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA2"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA2PSK"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="encryption">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="none"
                                                             />
                                                            <xs:enumeration
                                                                value="WEP"
                                                             />
                                                            <xs:enumeration
                                                                value="TKIP"
                                                             />
                                                            <xs:enumeration
                                                                value="AES"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="useOneX"
                                                    type="boolean"
                                                    minOccurs="0"
                                                 />
                                                <xs:any
                                                    processContents="lax"
                                                    minOccurs="0"
                                                    maxOccurs="unbounded"
                                                    namespace="##other"
                                                 />
                                            </xs:sequence>
                                        </xs:complexType>
                                    </xs:element>
                                    <xs:element name="sharedKey"
                                        minOccurs="0"
                                    >
                                        <xs:complexType>
                                            <xs:sequence>
                                                <xs:element name="keyType">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="networkKey"
                                                             />
                                                            <xs:enumeration
                                                                value="passPhrase"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="protected"
                                                    type="boolean"
                                                 />
                                                <xs:element name="keyMaterial"
                                                    type="string"
                                                 />
                                                <xs:any
                                                    processContents="lax"
                                                    minOccurs="0"
                                                    maxOccurs="unbounded"
                                                    namespace="##other"
                                                 />
                                            </xs:sequence>
                                        </xs:complexType>
                                    </xs:element>
                                    <xs:element name="keyIndex"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="0"
                                                 />
                                                <xs:maxInclusive
                                                    value="3"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheMode"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="disabled"
                                                 />
                                                <xs:enumeration
                                                    value="enabled"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheTTL"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="5"
                                                 />
                                                <xs:maxInclusive
                                                    value="1400"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheSize"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="1"
                                                 />
                                                <xs:maxInclusive
                                                    value="255"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="preAuthMode"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="disabled"
                                                 />
                                                <xs:enumeration
                                                    value="enabled"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="preAuthThrottle"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="1"
                                                 />
                                                <xs:maxInclusive
                                                    value="16"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="IHV"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUIHeader">
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="OUI">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:length
                                                    value="3"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="type">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:length
                                                    value="1"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="connectivity"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:any
                                        processContents="lax"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="security"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:any
                                        processContents="lax"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="useMSOneX"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="f19a1-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f19a1-107">Child elements</span></span>



| <span data-ttu-id="f19a1-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="f19a1-108">Element</span></span>                                                                            | <span data-ttu-id="f19a1-109">Тип</span><span class="sxs-lookup"><span data-stu-id="f19a1-109">Type</span></span>                                                              | <span data-ttu-id="f19a1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f19a1-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f19a1-111">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="f19a1-111">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="f19a1-112">Указывает пару для проверки подлинности и шифрования, которая будет использоваться для этого профиля.</span><span class="sxs-lookup"><span data-stu-id="f19a1-112">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="f19a1-113">**идентификаци**</span><span class="sxs-lookup"><span data-stu-id="f19a1-113">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="f19a1-114">Указывает метод проверки подлинности, используемый для подключения к беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="f19a1-114">Specifies the authentication method to be used to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="f19a1-115">**Автопереключение**</span><span class="sxs-lookup"><span data-stu-id="f19a1-115">**autoSwitch**</span></span>](wlan-profileschema-autoswitch-wlanprofile-element.md)            | [<span data-ttu-id="f19a1-116">boolean</span><span class="sxs-lookup"><span data-stu-id="f19a1-116">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="f19a1-117">Определяет режим роуминга для автоматической подключенной сети при наличии более предпочтительной сети в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="f19a1-117">Determines the roaming behavior of an auto-connected network when a more preferred network is in range.</span></span> <span data-ttu-id="f19a1-118">Этот элемент является необязательным и не влияет на сеть, подключенную вручную.</span><span class="sxs-lookup"><span data-stu-id="f19a1-118">This element is optional and has no effect on a manually connected network.</span></span><br/> <span data-ttu-id="f19a1-119">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f19a1-119">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="f19a1-120">**connectionMode**</span><span class="sxs-lookup"><span data-stu-id="f19a1-120">**connectionMode**</span></span>](wlan-profileschema-connectionmode-wlanprofile-element.md)    |                                                                   | <span data-ttu-id="f19a1-121">Указывает, должно ли подключение к беспроводной локальной сети выполняться автоматически (автоматически) или инициировано пользователем ("вручную").</span><span class="sxs-lookup"><span data-stu-id="f19a1-121">Indicates whether connection to the wireless LAN should be automatic ("auto") or initiated ("manual") by user.</span></span> <span data-ttu-id="f19a1-122">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f19a1-122">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="f19a1-123">**connectionType**</span><span class="sxs-lookup"><span data-stu-id="f19a1-123">**connectionType**</span></span>](wlan-profileschema-connectiontype-wlanprofile-element.md)    |                                                                   | <span data-ttu-id="f19a1-124">Указывает, является ли сеть инфраструктурой ("ESS") или ad-hoc ("ИБСС").</span><span class="sxs-lookup"><span data-stu-id="f19a1-124">Indicates whether the network is infrastructure ("ESS") or ad-hoc ("IBSS").</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="f19a1-125">**установлен**</span><span class="sxs-lookup"><span data-stu-id="f19a1-125">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | <span data-ttu-id="f19a1-126">Содержит различные параметры подключения.</span><span class="sxs-lookup"><span data-stu-id="f19a1-126">Contains various connectivity settings.</span></span> <span data-ttu-id="f19a1-127">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f19a1-127">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="f19a1-128">**установлен**</span><span class="sxs-lookup"><span data-stu-id="f19a1-128">**connectivity**</span></span>](wlan-profileschema-connectivity-ihv-element.md)                |                                                                   | <span data-ttu-id="f19a1-129">Содержит параметры подключения, связанные с IHV.</span><span class="sxs-lookup"><span data-stu-id="f19a1-129">Contains IHV-related connectivity settings.</span></span><br/> <span data-ttu-id="f19a1-130">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f19a1-130">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="f19a1-131">**ключ**</span><span class="sxs-lookup"><span data-stu-id="f19a1-131">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="f19a1-132">Задает шифрование данных, используемое для подключения к беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="f19a1-132">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="f19a1-133">**hex**</span><span class="sxs-lookup"><span data-stu-id="f19a1-133">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)                                 |                                                                   | <span data-ttu-id="f19a1-134">Содержит идентификатор SSID беспроводной локальной сети в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="f19a1-134">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="f19a1-135">**АППАРАТ**</span><span class="sxs-lookup"><span data-stu-id="f19a1-135">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)                          |                                                                   | <span data-ttu-id="f19a1-136">Содержит необязательные параметры независимых поставщиков оборудования (IHV).</span><span class="sxs-lookup"><span data-stu-id="f19a1-136">Contains optional independent hardware vendor (IHV) settings.</span></span><br/> <span data-ttu-id="f19a1-137">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f19a1-137">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="f19a1-138">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="f19a1-138">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="f19a1-139">Указывает, какой индекс ключа следует использовать для шифрования беспроводного трафика.</span><span class="sxs-lookup"><span data-stu-id="f19a1-139">Specifies which key index should be used to encrypt wireless traffic.</span></span> <span data-ttu-id="f19a1-140">Используется, только если параметр [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) имеет значение "нетворккэй".</span><span class="sxs-lookup"><span data-stu-id="f19a1-140">This is only used when [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) is set to "networkKey".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="f19a1-141">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="f19a1-141">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="f19a1-142">string</span><span class="sxs-lookup"><span data-stu-id="f19a1-142">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="f19a1-143">Содержит ключ сети или парольную фразу.</span><span class="sxs-lookup"><span data-stu-id="f19a1-143">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="f19a1-144">**keyType**</span><span class="sxs-lookup"><span data-stu-id="f19a1-144">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="f19a1-145">Тип ключа.</span><span class="sxs-lookup"><span data-stu-id="f19a1-145">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="f19a1-146">**MSM**</span><span class="sxs-lookup"><span data-stu-id="f19a1-146">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)                          |                                                                   | <span data-ttu-id="f19a1-147">Содержит различные параметры MSM.</span><span class="sxs-lookup"><span data-stu-id="f19a1-147">Contains various MSM settings.</span></span> <span data-ttu-id="f19a1-148">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f19a1-148">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="f19a1-149">**безымян**</span><span class="sxs-lookup"><span data-stu-id="f19a1-149">**name**</span></span>](wlan-profileschema-name-wlanprofile-element.md)                        | [<span data-ttu-id="f19a1-150">**наметипе**</span><span class="sxs-lookup"><span data-stu-id="f19a1-150">**nameType**</span></span>](wlan-profileschema-nametype-simpletype.md)        | <span data-ttu-id="f19a1-151">Имя профиля WLAN.</span><span class="sxs-lookup"><span data-stu-id="f19a1-151">Name of the WLAN profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="f19a1-152">**безымян**</span><span class="sxs-lookup"><span data-stu-id="f19a1-152">**name**</span></span>](wlan-profileschema-name-ssid-element.md)                               |                                                                   | <span data-ttu-id="f19a1-153">Содержит идентификатор SSID беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="f19a1-153">Contains the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="f19a1-154">**Нешироковещательная рассылка**</span><span class="sxs-lookup"><span data-stu-id="f19a1-154">**nonBroadcast**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md)         | [<span data-ttu-id="f19a1-155">boolean</span><span class="sxs-lookup"><span data-stu-id="f19a1-155">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="f19a1-156">Указывает, будет ли сеть рассылать свое SSID.</span><span class="sxs-lookup"><span data-stu-id="f19a1-156">Indicates whether the network broadcasts its SSID.</span></span><br/> <span data-ttu-id="f19a1-157">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f19a1-157">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="f19a1-158">**КОДОМ**</span><span class="sxs-lookup"><span data-stu-id="f19a1-158">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)                            |                                                                   | <span data-ttu-id="f19a1-159">Содержит 3-байтовый hexBinary, определяющий IHV.</span><span class="sxs-lookup"><span data-stu-id="f19a1-159">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/> <span data-ttu-id="f19a1-160">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f19a1-160">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="f19a1-161">**ауихеадер**</span><span class="sxs-lookup"><span data-stu-id="f19a1-161">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)                      |                                                                   | <span data-ttu-id="f19a1-162">Идентифицирует независимый поставщик оборудования.</span><span class="sxs-lookup"><span data-stu-id="f19a1-162">Identifies the IHV.</span></span><br/> <span data-ttu-id="f19a1-163">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f19a1-163">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="f19a1-164">**фитипе**</span><span class="sxs-lookup"><span data-stu-id="f19a1-164">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | <span data-ttu-id="f19a1-165">Указывает стандарт беспроводной локальной сети 802,11, используемый в беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="f19a1-165">Specifies the 802.11 wireless LAN standard used on the wireless LAN.</span></span> <span data-ttu-id="f19a1-166">Значение n поддерживается только в Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f19a1-166">The value "n" is only supported on Windows Vista with SP1 and later versions of the operating system.</span></span><br/> <span data-ttu-id="f19a1-167">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f19a1-167">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="f19a1-168">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="f19a1-168">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="f19a1-169">Указывает, будет ли использоваться кэширование PMK.</span><span class="sxs-lookup"><span data-stu-id="f19a1-169">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="f19a1-170">Этот элемент допустим только для сетей, определенных WPA2.</span><span class="sxs-lookup"><span data-stu-id="f19a1-170">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="f19a1-171">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f19a1-171">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="f19a1-172">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="f19a1-172">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="f19a1-173">Указывает количество записей в кэше PMK на клиенте.</span><span class="sxs-lookup"><span data-stu-id="f19a1-173">Specifies the number of entries in the PMK cache on the client.</span></span> <span data-ttu-id="f19a1-174">Этот элемент допустим только для сетей, определенных с помощью WPA2, для [**пмккачемоде**](wlan-profileschema-pmkcachemode-security-element.md) задано значение "Enabled".</span><span class="sxs-lookup"><span data-stu-id="f19a1-174">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="f19a1-175">Если **пмккачемоде** включен и этот элемент отсутствует, размер кэша по умолчанию составляет 128 записей.</span><span class="sxs-lookup"><span data-stu-id="f19a1-175">If **PMKCacheMode** is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="f19a1-176">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f19a1-176">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="f19a1-177">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="f19a1-177">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="f19a1-178">Указывает период времени в минутах, в течение которого будет храниться кэш PMK.</span><span class="sxs-lookup"><span data-stu-id="f19a1-178">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="f19a1-179">Этот элемент допустим только для сетей, определенных с помощью WPA2, для [**пмккачемоде**](wlan-profileschema-pmkcachemode-security-element.md) задано значение "Enabled".</span><span class="sxs-lookup"><span data-stu-id="f19a1-179">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span><br/> <span data-ttu-id="f19a1-180">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f19a1-180">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="f19a1-181">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="f19a1-181">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="f19a1-182">Определяет, будет ли клиент использовать предварительную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="f19a1-182">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="f19a1-183">Предварительная проверка подлинности обеспечивает безопасное быстрое перемещение WPA2.</span><span class="sxs-lookup"><span data-stu-id="f19a1-183">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="f19a1-184">Этот элемент допустим только для сетей, определенных с помощью WPA2, для [**пмккачемоде**](wlan-profileschema-pmkcachemode-security-element.md) задано значение "Enabled".</span><span class="sxs-lookup"><span data-stu-id="f19a1-184">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="f19a1-185">Если **пмккачемоде** включен и этот элемент отсутствует, значение по умолчанию — disabled.</span><span class="sxs-lookup"><span data-stu-id="f19a1-185">If **PMKCacheMode** is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="f19a1-186">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f19a1-186">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="f19a1-187">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="f19a1-187">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="f19a1-188">Указывает число попыток при предварительной проверке подлинности на соседних ТД.</span><span class="sxs-lookup"><span data-stu-id="f19a1-188">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="f19a1-189">Этот элемент допустим только для сетей, определенных с помощью WPA2, для [**пмккачемоде**](wlan-profileschema-pmkcachemode-security-element.md) задано значение "Enabled".</span><span class="sxs-lookup"><span data-stu-id="f19a1-189">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="f19a1-190">Если **пмккачемоде** включен и этот элемент отсутствует, число попыток по умолчанию будет равно 3.</span><span class="sxs-lookup"><span data-stu-id="f19a1-190">If **PMKCacheMode** is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="f19a1-191">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f19a1-191">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="f19a1-192">**protected**</span><span class="sxs-lookup"><span data-stu-id="f19a1-192">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="f19a1-193">boolean</span><span class="sxs-lookup"><span data-stu-id="f19a1-193">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="f19a1-194">Указывает, зашифрован ли ключ.</span><span class="sxs-lookup"><span data-stu-id="f19a1-194">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="f19a1-195">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент должен иметь значение **false**.</span><span class="sxs-lookup"><span data-stu-id="f19a1-195">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of **FALSE**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="f19a1-196">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="f19a1-196">**security**</span></span>](wlan-profileschema-security-msm-element.md)                        |                                                                   | <span data-ttu-id="f19a1-197">Содержит различные параметры безопасности.</span><span class="sxs-lookup"><span data-stu-id="f19a1-197">Contains various security settings.</span></span> <span data-ttu-id="f19a1-198">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f19a1-198">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="f19a1-199">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="f19a1-199">**security**</span></span>](wlan-profileschema-security-ihv-element.md)                        |                                                                   | <span data-ttu-id="f19a1-200">Содержит параметры безопасности, зависящие от IHV.</span><span class="sxs-lookup"><span data-stu-id="f19a1-200">Contains IHV-specific security settings.</span></span> <span data-ttu-id="f19a1-201">Параметры безопасности Microsoft и параметры безопасности IHV являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="f19a1-201">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="f19a1-202">Если оба набора параметров безопасности находятся в одном профиле, профиль будет недействительным.</span><span class="sxs-lookup"><span data-stu-id="f19a1-202">If both sets of security settings are present in the same profile, the profile is invalid.</span></span><br/> <span data-ttu-id="f19a1-203">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f19a1-203">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="f19a1-204">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="f19a1-204">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="f19a1-205">Содержит сведения об общем ключе.</span><span class="sxs-lookup"><span data-stu-id="f19a1-205">Contains the shared key information.</span></span> <span data-ttu-id="f19a1-206">Этот элемент необходим только в том случае, если для пары "Проверка подлинности и шифрование" требуются ключи WEP или PSK.</span><span class="sxs-lookup"><span data-stu-id="f19a1-206">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="f19a1-207">**SSID**</span><span class="sxs-lookup"><span data-stu-id="f19a1-207">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)                         |                                                                   | <span data-ttu-id="f19a1-208">Указывает идентификатор SSID беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="f19a1-208">Specifies the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="f19a1-209">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="f19a1-209">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)            |                                                                   | <span data-ttu-id="f19a1-210">Содержит один или несколько идентификаторов SSID, а также другие общие параметры.</span><span class="sxs-lookup"><span data-stu-id="f19a1-210">Contains one or more SSIDs along with other common settings.</span></span> <br/> <span data-ttu-id="f19a1-211">Профиль может иметь несколько элементов [**ссидконфиг**](wlan-profileschema-ssidconfig-wlanprofile-element.md) , и каждый элемент [**ссидконфиг**](wlan-profileschema-ssidconfig-wlanprofile-element.md) может иметь несколько элементов [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f19a1-211">A profile can have multiple [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) elements and each [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element can have multiple [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) elements.</span></span> <span data-ttu-id="f19a1-212">Однако Windows рассматривает только первый элемент [**ссидконфиг**](wlan-profileschema-ssidconfig-wlanprofile-element.md) в элементе [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f19a1-212">However, Windows only ever considers the first [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element in a [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span><br/> <span data-ttu-id="f19a1-213">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** В профиле может присутствовать не более одного элемента [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f19a1-213">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element can appear in a profile.</span></span><br/> |
| [<span data-ttu-id="f19a1-214">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f19a1-214">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md)                          |                                                                   | <span data-ttu-id="f19a1-215">Содержит 1-байтовый **hexBinary** , используемый для различения сетевых карт одним и тем же IHV.</span><span class="sxs-lookup"><span data-stu-id="f19a1-215">Contains a 1 byte **hexBinary** that is used to differentiate NICs by the same IHV.</span></span><br/> <span data-ttu-id="f19a1-216">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f19a1-216">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="f19a1-217">**усемсонекс**</span><span class="sxs-lookup"><span data-stu-id="f19a1-217">**useMSOneX**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)                      | [<span data-ttu-id="f19a1-218">boolean</span><span class="sxs-lookup"><span data-stu-id="f19a1-218">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="f19a1-219">Указывает источник параметров безопасности 802.1 X, используемых компонентом безопасности независимого поставщика оборудования.</span><span class="sxs-lookup"><span data-stu-id="f19a1-219">Specifies the origin of 802.1X security settings used by an IHV security component.</span></span> <span data-ttu-id="f19a1-220">Если [**усемсонекс**](wlan-profileschema-usemsonex-ihv-element.md) имеет значение true, компоненты безопасности IHV используют определенные корпорацией Майкрософт параметры 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="f19a1-220">When [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="f19a1-221">Если **усемсонекс** имеет значение false, компоненты безопасности IHV используют предоставленные поставщиком параметры 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="f19a1-221">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span> <span data-ttu-id="f19a1-222">По умолчанию **усемсонекс** имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="f19a1-222">By default, **useMSOneX** is false.</span></span> <span data-ttu-id="f19a1-223">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f19a1-223">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="f19a1-224">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="f19a1-224">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="f19a1-225">boolean</span><span class="sxs-lookup"><span data-stu-id="f19a1-225">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="f19a1-226">Указывает, используется ли 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="f19a1-226">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="f19a1-227">Этот флаг является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f19a1-227">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="f19a1-228">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f19a1-228">Remarks</span></span>

<span data-ttu-id="f19a1-229">Большинство дочерних элементов элемента Вланпрофиле находятся в `https://www.microsoft.com/networking/WLAN/profile/v1` пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="f19a1-229">Most child elements of the WLANProfile element are in the `https://www.microsoft.com/networking/WLAN/profile/v1` namespace.</span></span> <span data-ttu-id="f19a1-230">Существует два исключения: элемент [**фипсмоде**](wlan-profileschema-fipsmode-authencryption-element.md) находится в `https://www.microsoft.com/networking/WLAN/profile/v2` пространстве имен, а элемент [**OneX**](onexschema-onex-element.md) — в `https://www.microsoft.com/networking/OneX/v1` пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="f19a1-230">There are two exceptions: the [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element is in the `https://www.microsoft.com/networking/WLAN/profile/v2` namespace and the [**OneX**](onexschema-onex-element.md) element is in the `https://www.microsoft.com/networking/OneX/v1` namespace.</span></span>

<span data-ttu-id="f19a1-231">Элемент [**фипсмоде**](wlan-profileschema-fipsmode-authencryption-element.md) может быть вставлен как дочерний элемент элемента [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f19a1-231">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="f19a1-232">Элемент [**OneX**](onexschema-onex-element.md) может быть вставлен как дочерний элемент элемента [**Security (MSM)**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f19a1-232">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the [**security (MSM)**](wlan-profileschema-security-msm-element.md) element.</span></span>

<span data-ttu-id="f19a1-233">Чтобы просмотреть список дочерних элементов в древовидной структуре, см. раздел [ \_ элементы схемы профиля WLAN](wlan-profileschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="f19a1-233">To view the list of child elements in a tree-like structure, see [WLAN\_profile Schema Elements](wlan-profileschema-elements.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f19a1-234">Примеры</span><span class="sxs-lookup"><span data-stu-id="f19a1-234">Examples</span></span>

<span data-ttu-id="f19a1-235">Чтобы просмотреть образцы профилей, см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="f19a1-235">To view sample profiles, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f19a1-236">Требования</span><span class="sxs-lookup"><span data-stu-id="f19a1-236">Requirements</span></span>



| <span data-ttu-id="f19a1-237">Требование</span><span class="sxs-lookup"><span data-stu-id="f19a1-237">Requirement</span></span> | <span data-ttu-id="f19a1-238">Значение</span><span class="sxs-lookup"><span data-stu-id="f19a1-238">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f19a1-239">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f19a1-239">Minimum supported client</span></span><br/> | <span data-ttu-id="f19a1-240">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f19a1-240">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f19a1-241">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f19a1-241">Minimum supported server</span></span><br/> | <span data-ttu-id="f19a1-242">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f19a1-242">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="f19a1-243">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="f19a1-243">Redistributable</span></span><br/>          | <span data-ttu-id="f19a1-244">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="f19a1-244">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f19a1-245">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f19a1-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f19a1-246">Образцы профиля беспроводной связи</span><span class="sxs-lookup"><span data-stu-id="f19a1-246">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
