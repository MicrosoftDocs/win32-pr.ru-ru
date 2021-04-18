---
description: Содержит различные параметры модуля для конкретных носителей (MSM).
ms.assetid: 31f98af8-a577-4f6a-9a0a-b182b5a89cc3
title: Элемент MSM (Вланпрофиле)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: b2e1ffdc5ad27524d3d2fc5b37b3a060a90c7575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684020"
---
# <a name="msm-wlanprofile-element"></a><span data-ttu-id="376f3-103">Элемент MSM (Вланпрофиле)</span><span class="sxs-lookup"><span data-stu-id="376f3-103">MSM (WLANProfile) Element</span></span>

<span data-ttu-id="376f3-104">Элемент MSM (Вланпрофиле) содержит различные параметры модуля для конкретных носителей (MSM).</span><span class="sxs-lookup"><span data-stu-id="376f3-104">The MSM (WLANProfile) element contains various media-specific module (MSM) settings.</span></span>

``` syntax
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
```

<span data-ttu-id="376f3-105">Элемент определяется элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="376f3-105">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="376f3-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="376f3-106">Child elements</span></span>



| <span data-ttu-id="376f3-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="376f3-107">Element</span></span>                                                                            | <span data-ttu-id="376f3-108">Тип</span><span class="sxs-lookup"><span data-stu-id="376f3-108">Type</span></span>                                                              | <span data-ttu-id="376f3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="376f3-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="376f3-110">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="376f3-110">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="376f3-111">Указывает пару для проверки подлинности и шифрования, которая будет использоваться для этого профиля.</span><span class="sxs-lookup"><span data-stu-id="376f3-111">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="376f3-112">**идентификаци**</span><span class="sxs-lookup"><span data-stu-id="376f3-112">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="376f3-113">Указывает пару для проверки подлинности и шифрования, которая будет использоваться для этого профиля.</span><span class="sxs-lookup"><span data-stu-id="376f3-113">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="376f3-114">**установлен**</span><span class="sxs-lookup"><span data-stu-id="376f3-114">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | <span data-ttu-id="376f3-115">Содержит различные параметры подключения.</span><span class="sxs-lookup"><span data-stu-id="376f3-115">Contains various connectivity settings.</span></span> <span data-ttu-id="376f3-116">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="376f3-116">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="376f3-117">**ключ**</span><span class="sxs-lookup"><span data-stu-id="376f3-117">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="376f3-118">Задает шифрование данных, используемое для подключения к беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="376f3-118">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="376f3-119">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="376f3-119">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="376f3-120">Указывает, какой индекс ключа должен использоваться для шифрования беспроводного трафика.</span><span class="sxs-lookup"><span data-stu-id="376f3-120">Specifies which key index must be used to encrypt wireless traffic.</span></span> <span data-ttu-id="376f3-121">Используется, только если параметр keyType имеет значение Нетворккэй.</span><span class="sxs-lookup"><span data-stu-id="376f3-121">This is only used when keyType is set to networkKey.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="376f3-122">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="376f3-122">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="376f3-123">string</span><span class="sxs-lookup"><span data-stu-id="376f3-123">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="376f3-124">Содержит ключ сети или парольную фразу.</span><span class="sxs-lookup"><span data-stu-id="376f3-124">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="376f3-125">**keyType**</span><span class="sxs-lookup"><span data-stu-id="376f3-125">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="376f3-126">Тип ключа.</span><span class="sxs-lookup"><span data-stu-id="376f3-126">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="376f3-127">**фитипе**</span><span class="sxs-lookup"><span data-stu-id="376f3-127">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | <span data-ttu-id="376f3-128">Указывает стандарт беспроводной локальной сети 802,11, используемый в беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="376f3-128">Specifies the 802.11 wireless LAN standard used on the wireless LAN.</span></span> <span data-ttu-id="376f3-129">Значение n поддерживается только в Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="376f3-129">The value "n" is only supported on Windows Vista with SP1 and later versions of the operating system.</span></span><br/> <span data-ttu-id="376f3-130">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="376f3-130">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="376f3-131">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="376f3-131">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="376f3-132">Указывает, будет ли использоваться кэширование PMK.</span><span class="sxs-lookup"><span data-stu-id="376f3-132">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="376f3-133">Этот элемент допустим только для сетей, определенных WPA2.</span><span class="sxs-lookup"><span data-stu-id="376f3-133">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="376f3-134">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="376f3-134">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="376f3-135">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="376f3-135">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="376f3-136">Указывает количество записей в кэше ОМК на клиенте.</span><span class="sxs-lookup"><span data-stu-id="376f3-136">Specifies the number of entries in the OMK cache on the client.</span></span> <span data-ttu-id="376f3-137">Этот элемент допустим только для сетей, определенных WPA2, в режиме Пмккаче задано значение Enabled.</span><span class="sxs-lookup"><span data-stu-id="376f3-137">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="376f3-138">Если включен режим Пмккаче и этот элемент отсутствует, по умолчанию размер кэша составляет 128 записей.</span><span class="sxs-lookup"><span data-stu-id="376f3-138">If PMKCache mode is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="376f3-139">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="376f3-139">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                   |
| [<span data-ttu-id="376f3-140">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="376f3-140">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="376f3-141">Указывает период времени в минутах, в течение которого будет храниться кэш PMK.</span><span class="sxs-lookup"><span data-stu-id="376f3-141">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="376f3-142">Этот элемент допустим только для сетей, определенных WPA2, в режиме Пмккаче задано значение Enabled.</span><span class="sxs-lookup"><span data-stu-id="376f3-142">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span><br/> <span data-ttu-id="376f3-143">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="376f3-143">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="376f3-144">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="376f3-144">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="376f3-145">Определяет, будет ли клиент использовать предварительную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="376f3-145">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="376f3-146">Предварительная проверка подлинности обеспечивает безопасное быстрое перемещение WPA2.</span><span class="sxs-lookup"><span data-stu-id="376f3-146">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="376f3-147">Этот элемент допустим только для сетей, определенных WPA2, в режиме Пмккаче задано значение Enabled.</span><span class="sxs-lookup"><span data-stu-id="376f3-147">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="376f3-148">Если включен режим Пмккаче и этот элемент отсутствует, значение по умолчанию — disabled.</span><span class="sxs-lookup"><span data-stu-id="376f3-148">If PMKCache mode is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="376f3-149">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="376f3-149">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="376f3-150">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="376f3-150">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="376f3-151">Указывает число попыток при предварительной проверке подлинности на соседних ТД.</span><span class="sxs-lookup"><span data-stu-id="376f3-151">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="376f3-152">Этот элемент допустим только для сетей, определенных WPA2, в режиме Пмккаче задано значение Enabled.</span><span class="sxs-lookup"><span data-stu-id="376f3-152">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="376f3-153">Если включен режим Пмккаче и этот элемент отсутствует, число попыток по умолчанию будет равно 3.</span><span class="sxs-lookup"><span data-stu-id="376f3-153">If PMKCache mode is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="376f3-154">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="376f3-154">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="376f3-155">**protected**</span><span class="sxs-lookup"><span data-stu-id="376f3-155">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="376f3-156">boolean</span><span class="sxs-lookup"><span data-stu-id="376f3-156">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="376f3-157">Указывает, зашифрован ли ключ.</span><span class="sxs-lookup"><span data-stu-id="376f3-157">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="376f3-158">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент должен иметь значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="376f3-158">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of FALSE.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="376f3-159">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="376f3-159">**security**</span></span>](wlan-profileschema-security-msm-element.md)                        |                                                                   | <span data-ttu-id="376f3-160">Содержит различные параметры безопасности.</span><span class="sxs-lookup"><span data-stu-id="376f3-160">Contains various security settings.</span></span> <span data-ttu-id="376f3-161">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="376f3-161">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="376f3-162">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="376f3-162">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="376f3-163">Содержит сведения об общем ключе.</span><span class="sxs-lookup"><span data-stu-id="376f3-163">Contains the shared key information.</span></span> <span data-ttu-id="376f3-164">Этот элемент необходим только в том случае, если для пары "Проверка подлинности и шифрование" требуются ключи WEP или PSK.</span><span class="sxs-lookup"><span data-stu-id="376f3-164">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="376f3-165">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="376f3-165">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="376f3-166">boolean</span><span class="sxs-lookup"><span data-stu-id="376f3-166">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="376f3-167">Указывает, используется ли 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="376f3-167">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="376f3-168">Этот флаг является необязательным.</span><span class="sxs-lookup"><span data-stu-id="376f3-168">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="376f3-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="376f3-169">Remarks</span></span>

<span data-ttu-id="376f3-170">Элемент [**фипсмоде**](wlan-profileschema-fipsmode-authencryption-element.md) может быть вставлен как дочерний элемент элемента [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="376f3-170">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="376f3-171">Элемент [**OneX**](onexschema-onex-element.md) может быть вставлен как дочерний элемент элемента [**Security (MSM)**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="376f3-171">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the [**security (MSM)**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="376f3-172">Примеры</span><span class="sxs-lookup"><span data-stu-id="376f3-172">Examples</span></span>

<span data-ttu-id="376f3-173">Чтобы просмотреть образцы профилей, в которых используется элемент **MSM** , см. раздел [образцы профиля беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="376f3-173">To view sample profiles that use the **MSM** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="376f3-174">Требования</span><span class="sxs-lookup"><span data-stu-id="376f3-174">Requirements</span></span>



| <span data-ttu-id="376f3-175">Требование</span><span class="sxs-lookup"><span data-stu-id="376f3-175">Requirement</span></span> | <span data-ttu-id="376f3-176">Значение</span><span class="sxs-lookup"><span data-stu-id="376f3-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="376f3-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="376f3-177">Minimum supported client</span></span><br/> | <span data-ttu-id="376f3-178">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="376f3-178">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="376f3-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="376f3-179">Minimum supported server</span></span><br/> | <span data-ttu-id="376f3-180">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="376f3-180">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="376f3-181">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="376f3-181">Redistributable</span></span><br/>          | <span data-ttu-id="376f3-182">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="376f3-182">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="376f3-183">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="376f3-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="376f3-184">Образцы профиля беспроводной связи</span><span class="sxs-lookup"><span data-stu-id="376f3-184">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="376f3-185">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="376f3-185">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="376f3-186">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="376f3-186">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="376f3-187">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="376f3-187">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="376f3-188">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="376f3-188">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
