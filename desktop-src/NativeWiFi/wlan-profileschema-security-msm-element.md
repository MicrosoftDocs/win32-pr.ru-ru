---
description: Содержит различные параметры безопасности.
ms.assetid: 1d912fb1-8fb4-4761-8991-5a50ffb0399e
title: Элемент Security (MSM) (LAN_policy) (WLAN)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f6ea42a83d39c328db88e992555e5d593cc778b6
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2021
ms.locfileid: "105689538"
---
# <a name="security-msm-element-lan_policy-for-wlan"></a><span data-ttu-id="98d12-103">Элемент Security (MSM) (LAN_policy) для WLAN</span><span class="sxs-lookup"><span data-stu-id="98d12-103">Security (MSM) Element (LAN_policy) for WLAN</span></span>

<span data-ttu-id="98d12-104">Элемент Security (MSM) содержит различные параметры безопасности.</span><span class="sxs-lookup"><span data-stu-id="98d12-104">The security (MSM) element contains various security settings.</span></span>

``` syntax
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
```

<span data-ttu-id="98d12-105">Элемент определяется элементом [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="98d12-105">The element is defined by the [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="98d12-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="98d12-106">Child elements</span></span>



| <span data-ttu-id="98d12-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="98d12-107">Element</span></span>                                                                            | <span data-ttu-id="98d12-108">Тип</span><span class="sxs-lookup"><span data-stu-id="98d12-108">Type</span></span>                                                              | <span data-ttu-id="98d12-109">Описание</span><span class="sxs-lookup"><span data-stu-id="98d12-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98d12-110">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="98d12-110">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="98d12-111">Указывает пару для проверки подлинности и шифрования, которая будет использоваться для этого профиля.</span><span class="sxs-lookup"><span data-stu-id="98d12-111">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="98d12-112">**идентификаци**</span><span class="sxs-lookup"><span data-stu-id="98d12-112">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="98d12-113">Указывает пару для проверки подлинности и шифрования, которая будет использоваться для этого профиля.</span><span class="sxs-lookup"><span data-stu-id="98d12-113">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="98d12-114">**ключ**</span><span class="sxs-lookup"><span data-stu-id="98d12-114">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="98d12-115">Задает шифрование данных, используемое для подключения к беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="98d12-115">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="98d12-116">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="98d12-116">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="98d12-117">Указывает, какой индекс ключа должен использоваться для шифрования беспроводного трафика.</span><span class="sxs-lookup"><span data-stu-id="98d12-117">Specifies which key index must be used to encrypt wireless traffic.</span></span> <span data-ttu-id="98d12-118">Используется, только если параметр keyType имеет значение Нетворккэй.</span><span class="sxs-lookup"><span data-stu-id="98d12-118">This is only used when keyType is set to networkKey.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="98d12-119">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="98d12-119">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="98d12-120">string</span><span class="sxs-lookup"><span data-stu-id="98d12-120">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="98d12-121">Содержит ключ сети или парольную фразу.</span><span class="sxs-lookup"><span data-stu-id="98d12-121">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="98d12-122">**keyType**</span><span class="sxs-lookup"><span data-stu-id="98d12-122">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="98d12-123">Тип ключа.</span><span class="sxs-lookup"><span data-stu-id="98d12-123">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="98d12-124">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="98d12-124">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="98d12-125">Указывает, будет ли использоваться кэширование PMK.</span><span class="sxs-lookup"><span data-stu-id="98d12-125">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="98d12-126">Этот элемент допустим только для сетей, определенных WPA2.</span><span class="sxs-lookup"><span data-stu-id="98d12-126">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="98d12-127">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="98d12-127">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="98d12-128">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="98d12-128">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="98d12-129">Указывает количество записей в кэше ОМК на клиенте.</span><span class="sxs-lookup"><span data-stu-id="98d12-129">Specifies the number of entries in the OMK cache on the client.</span></span> <span data-ttu-id="98d12-130">Этот элемент допустим только для сетей, определенных WPA2, в режиме Пмккаче задано значение Enabled.</span><span class="sxs-lookup"><span data-stu-id="98d12-130">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="98d12-131">Если включен режим Пмккаче и этот элемент отсутствует, по умолчанию размер кэша составляет 128 записей.</span><span class="sxs-lookup"><span data-stu-id="98d12-131">If PMKCache mode is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="98d12-132">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="98d12-132">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                   |
| [<span data-ttu-id="98d12-133">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="98d12-133">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="98d12-134">Указывает период времени в минутах, в течение которого будет храниться кэш PMK.</span><span class="sxs-lookup"><span data-stu-id="98d12-134">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="98d12-135">Этот элемент допустим только для сетей, определенных WPA2, в режиме Пмккаче задано значение Enabled.</span><span class="sxs-lookup"><span data-stu-id="98d12-135">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span><br/> <span data-ttu-id="98d12-136">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="98d12-136">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="98d12-137">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="98d12-137">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="98d12-138">Определяет, будет ли клиент использовать предварительную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="98d12-138">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="98d12-139">Предварительная проверка подлинности обеспечивает безопасное быстрое перемещение WPA2.</span><span class="sxs-lookup"><span data-stu-id="98d12-139">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="98d12-140">Этот элемент допустим только для сетей, определенных WPA2, в режиме Пмккаче задано значение Enabled.</span><span class="sxs-lookup"><span data-stu-id="98d12-140">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="98d12-141">Если включен режим Пмккаче и этот элемент отсутствует, значение по умолчанию — disabled.</span><span class="sxs-lookup"><span data-stu-id="98d12-141">If PMKCache mode is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="98d12-142">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="98d12-142">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="98d12-143">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="98d12-143">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="98d12-144">Указывает число попыток при предварительной проверке подлинности на соседних ТД.</span><span class="sxs-lookup"><span data-stu-id="98d12-144">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="98d12-145">Этот элемент допустим только для сетей, определенных WPA2, в режиме Пмккаче задано значение Enabled.</span><span class="sxs-lookup"><span data-stu-id="98d12-145">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="98d12-146">Если включен режим Пмккаче и этот элемент отсутствует, число попыток по умолчанию будет равно 3.</span><span class="sxs-lookup"><span data-stu-id="98d12-146">If PMKCache mode is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="98d12-147">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="98d12-147">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="98d12-148">**protected**</span><span class="sxs-lookup"><span data-stu-id="98d12-148">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="98d12-149">boolean</span><span class="sxs-lookup"><span data-stu-id="98d12-149">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="98d12-150">Указывает, зашифрован ли ключ.</span><span class="sxs-lookup"><span data-stu-id="98d12-150">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="98d12-151">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент должен иметь значение **false**.</span><span class="sxs-lookup"><span data-stu-id="98d12-151">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of **FALSE**.</span></span><br/>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="98d12-152">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="98d12-152">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="98d12-153">Содержит сведения об общем ключе.</span><span class="sxs-lookup"><span data-stu-id="98d12-153">Contains the shared key information.</span></span> <span data-ttu-id="98d12-154">Этот элемент необходим только в том случае, если для пары "Проверка подлинности и шифрование" требуются ключи WEP или PSK.</span><span class="sxs-lookup"><span data-stu-id="98d12-154">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="98d12-155">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="98d12-155">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="98d12-156">boolean</span><span class="sxs-lookup"><span data-stu-id="98d12-156">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="98d12-157">Указывает, используется ли 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="98d12-157">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="98d12-158">Этот флаг является необязательным.</span><span class="sxs-lookup"><span data-stu-id="98d12-158">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="98d12-159">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98d12-159">Remarks</span></span>

<span data-ttu-id="98d12-160">Элемент [**фипсмоде**](wlan-profileschema-fipsmode-authencryption-element.md) может быть вставлен как дочерний элемент элемента [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="98d12-160">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="98d12-161">Элемент [**OneX**](onexschema-onex-element.md) может быть вставлен как дочерний элемент элемента **Security (MSM)** .</span><span class="sxs-lookup"><span data-stu-id="98d12-161">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the **security (MSM)** element.</span></span>

## <a name="examples"></a><span data-ttu-id="98d12-162">Примеры</span><span class="sxs-lookup"><span data-stu-id="98d12-162">Examples</span></span>

<span data-ttu-id="98d12-163">Чтобы просмотреть образцы профилей, в которых используется элемент **Security** , см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="98d12-163">To view sample profiles that use the **security** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98d12-164">Требования</span><span class="sxs-lookup"><span data-stu-id="98d12-164">Requirements</span></span>



| <span data-ttu-id="98d12-165">Требование</span><span class="sxs-lookup"><span data-stu-id="98d12-165">Requirement</span></span> | <span data-ttu-id="98d12-166">Значение</span><span class="sxs-lookup"><span data-stu-id="98d12-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="98d12-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98d12-167">Minimum supported client</span></span><br/> | <span data-ttu-id="98d12-168">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="98d12-168">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="98d12-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98d12-169">Minimum supported server</span></span><br/> | <span data-ttu-id="98d12-170">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98d12-170">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="98d12-171">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="98d12-171">Redistributable</span></span><br/>          | <span data-ttu-id="98d12-172">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="98d12-172">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="98d12-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98d12-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98d12-174">Образцы профиля беспроводной связи</span><span class="sxs-lookup"><span data-stu-id="98d12-174">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="98d12-175">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="98d12-175">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="98d12-176">**MSM**</span><span class="sxs-lookup"><span data-stu-id="98d12-176">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="98d12-177">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="98d12-177">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="98d12-178">**MSM (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="98d12-178">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 
