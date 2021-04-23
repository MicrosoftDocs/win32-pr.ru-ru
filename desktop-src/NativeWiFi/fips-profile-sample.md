---
description: Используется для подключения к сети, которая требует параметров безопасности, соответствующих Федеральному стандарту обработки информации (FIPS) 140-2 Standard.
ms.assetid: 169df4a3-e8b9-4f05-874f-a7eef6658d01
title: Пример профиля FIPS
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6d24f82a815c752a662af5f093dd9a7c34de33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156682"
---
# <a name="fips-profile-sample"></a><span data-ttu-id="8929a-103">Пример профиля FIPS</span><span class="sxs-lookup"><span data-stu-id="8929a-103">FIPS Profile Sample</span></span>

<span data-ttu-id="8929a-104">Пример профиля FIPS можно использовать для подключения к сети, которая требует параметров безопасности, соответствующих Федеральному стандарту обработки информации (FIPS) 140-2 Standard.</span><span class="sxs-lookup"><span data-stu-id="8929a-104">The FIPS profile sample can be used to connect to a network that requires security settings that comply with Federal Information Processing Standards (FIPS) 140-2 standard.</span></span> <span data-ttu-id="8929a-105">Дополнительные сведения о FIPS см. в разделе [**фипсмоде**](wlan-profileschema-fipsmode-authencryption-element.md).</span><span class="sxs-lookup"><span data-stu-id="8929a-105">For more information about FIPS, see [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md).</span></span>

<span data-ttu-id="8929a-106">**Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети:** Изменения реализуются в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети для оптимизации производительности беспроводных сетей.</span><span class="sxs-lookup"><span data-stu-id="8929a-106">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="8929a-107">Параметр по умолчанию для [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) , если этот элемент не задан в профиле беспроводной локальной сети, изменился.</span><span class="sxs-lookup"><span data-stu-id="8929a-107">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="8929a-108">Значение по умолчанию изменено на "false" в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="8929a-108">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="8929a-109">Значение по умолчанию — true в Windows Server 2008 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8929a-109">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="8929a-110">Дополнительные сведения см. в описании элемента схемы [**автопереключения**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8929a-110">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="8929a-111">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Дочерний элемент [**Name**](wlan-profileschema-name-wlanprofile-element.md) элемента [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8929a-111">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="8929a-112">Имя профиля, хранящееся в хранилище профилей, является производным от дочернего элемента [**имени**](wlan-profileschema-name-ssid-element.md) [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8929a-112">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span> <span data-ttu-id="8929a-113">Элемент [**фипсмоде**](wlan-profileschema-fipsmode-authencryption-element.md) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8929a-113">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element is not supported.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>FIPS_TEST</name>
    <SSIDConfig>
        <SSID>
            <hex>464950535F54455354</hex>
            <name>FIPS_TEST</name>
        </SSID>
        <nonBroadcast>false</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2</authentication>
                <encryption>AES</encryption>
                <useOneX>true</useOneX>
                <FIPSMode xmlns="https://www.microsoft.com/networking/WLAN/profile/v2">true</FIPSMode>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig">
                    <EapMethod>
                        <Type xmlns="https://www.microsoft.com/provisioning/EapCommon">25</Type>
                        <VendorId xmlns="https://www.microsoft.com/provisioning/EapCommon">0</VendorId>
                        <VendorType xmlns="https://www.microsoft.com/provisioning/EapCommon">0</VendorType>
                        <AuthorId xmlns="https://www.microsoft.com/provisioning/EapCommon">0</AuthorId>
                    </EapMethod>
                    <ConfigBlob></ConfigBlob>
                    </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="8929a-114">См. также</span><span class="sxs-lookup"><span data-stu-id="8929a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8929a-115">Образцы профиля беспроводной связи</span><span class="sxs-lookup"><span data-stu-id="8929a-115">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



