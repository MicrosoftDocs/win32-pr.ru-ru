---
description: Использует общий ключ для проверки подлинности сети. Этот пример профиля использует Wi-Fi безопасность защищенного доступа в личном режиме (WPA-личное).
ms.assetid: f04de28b-a98d-40cd-91c8-e446cf669555
title: Пример профиля WPA-Personal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334076d4b0cf10372ed845265a1fff652f0879b9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395029"
---
# <a name="wpa-personal-profile-sample"></a><span data-ttu-id="d6fac-104">Пример профиля WPA-Personal</span><span class="sxs-lookup"><span data-stu-id="d6fac-104">WPA-Personal Profile Sample</span></span>

<span data-ttu-id="d6fac-105">Этот пример профиля использует общий ключ для проверки подлинности сети.</span><span class="sxs-lookup"><span data-stu-id="d6fac-105">This sample profile uses a pre-shared key for network authentication.</span></span> <span data-ttu-id="d6fac-106">Ключ используется совместно с клиентом и точкой доступа.</span><span class="sxs-lookup"><span data-stu-id="d6fac-106">The key is shared with the client and the access point.</span></span> <span data-ttu-id="d6fac-107">Этот пример профиля настроен для использования защиты Wi-Fi защищенного доступа, работающей в личном режиме (WPA-Personal).</span><span class="sxs-lookup"><span data-stu-id="d6fac-107">This sample profile is configured to use Wi-Fi Protected Access security running in Personal mode (WPA-Personal).</span></span> <span data-ttu-id="d6fac-108">Для шифрования используется протокол TKIP.</span><span class="sxs-lookup"><span data-stu-id="d6fac-108">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="d6fac-109">**Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети:** Изменения реализуются в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети для оптимизации производительности беспроводных сетей.</span><span class="sxs-lookup"><span data-stu-id="d6fac-109">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="d6fac-110">Параметр по умолчанию для [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) , если этот элемент не задан в профиле беспроводной локальной сети, изменился.</span><span class="sxs-lookup"><span data-stu-id="d6fac-110">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="d6fac-111">Значение по умолчанию изменено на "false" в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="d6fac-111">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="d6fac-112">Значение по умолчанию — true в Windows Server 2008 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d6fac-112">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="d6fac-113">Дополнительные сведения см. в описании элемента схемы [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d6fac-113">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="d6fac-114">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Дочерний элемент [**Name**](wlan-profileschema-name-wlanprofile-element.md) элемента [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d6fac-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="d6fac-115">Имя профиля, хранящееся в хранилище профилей, является производным от дочернего элемента [**имени**](wlan-profileschema-name-ssid-element.md) [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d6fac-115">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAPSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAPSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPAPSK</authentication>
                <encryption>TKIP</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

<span data-ttu-id="d6fac-116">Общий ключ пропущен в этом примере профиля.</span><span class="sxs-lookup"><span data-stu-id="d6fac-116">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="d6fac-117">Если вы попытаетесь использовать этот пример профиля для подключения к сети, вам будет предложено ввести общий ключ.</span><span class="sxs-lookup"><span data-stu-id="d6fac-117">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="d6fac-118">Этот запрос можно избежать, добавив дочерний элемент [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) в элемент [**безопасности**](wlan-profileschema-security-msm-element.md) сразу после элемента [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d6fac-118">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="d6fac-119">В следующем фрагменте кода показан элемент [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) , содержащий незашифрованный ключ.</span><span class="sxs-lookup"><span data-stu-id="d6fac-119">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="d6fac-120">`<!-- insert key here -->`Перед использованием этого фрагмента в профиле необходимо заменить комментарий фактическим незашифрованным ключом.</span><span class="sxs-lookup"><span data-stu-id="d6fac-120">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="d6fac-121">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d6fac-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6fac-122">Образцы профиля беспроводной связи</span><span class="sxs-lookup"><span data-stu-id="d6fac-122">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



