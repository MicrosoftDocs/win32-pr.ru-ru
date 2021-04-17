---
description: Используется для подключения к сетям, которые не рассылают свое сетевое имя или SSID.
ms.assetid: 564324ad-6723-4676-ab5c-0b5d2957d201
title: Пример профиля без широковещательной рассылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09bfd9cf9eac724f882a9aa3cf16064f051fdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673661"
---
# <a name="non-broadcast-profile-sample"></a><span data-ttu-id="cce5a-103">Пример профиля без широковещательной рассылки</span><span class="sxs-lookup"><span data-stu-id="cce5a-103">Non-Broadcast Profile Sample</span></span>

<span data-ttu-id="cce5a-104">Образец профиля без вещания можно использовать для подключения к сетям, которые не рассылают имя сети или SSID.</span><span class="sxs-lookup"><span data-stu-id="cce5a-104">The non-broadcast profile sample can be used to connect to networks which do not broadcast their network name or SSID.</span></span>

<span data-ttu-id="cce5a-105">Этот пример профиля настроен для использования защиты Wi-Fi защищенного доступа, работающей в личном режиме (WPA-Personal).</span><span class="sxs-lookup"><span data-stu-id="cce5a-105">This sample profile is configured to use Wi-Fi Protected Access security running in Personal mode (WPA-Personal).</span></span> <span data-ttu-id="cce5a-106">Для шифрования используется протокол TKIP.</span><span class="sxs-lookup"><span data-stu-id="cce5a-106">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span> <span data-ttu-id="cce5a-107">Профили, использующие другие типы безопасности и шифрования, также можно настроить как профили без широковещательной рассылки.</span><span class="sxs-lookup"><span data-stu-id="cce5a-107">Profiles that use other security and cipher types can also be configured as non-broadcast profiles.</span></span>

<span data-ttu-id="cce5a-108">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Дочерний элемент [**Name**](wlan-profileschema-name-wlanprofile-element.md) элемента [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="cce5a-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="cce5a-109">Имя профиля, хранящееся в хранилище профилей, является производным от дочернего элемента [**имени**](wlan-profileschema-name-ssid-element.md) [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cce5a-109">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleNonBroadcast</name>
    <SSIDConfig>
        <SSID>
            <name>SampleNonBroadcast</name>
        </SSID>
        <nonBroadcast>true</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
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

<span data-ttu-id="cce5a-110">Общий ключ пропущен в этом примере профиля.</span><span class="sxs-lookup"><span data-stu-id="cce5a-110">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="cce5a-111">Если вы попытаетесь использовать этот пример профиля для подключения к сети, вам будет предложено ввести общий ключ.</span><span class="sxs-lookup"><span data-stu-id="cce5a-111">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="cce5a-112">Этот запрос можно избежать, добавив дочерний элемент [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) в элемент [**безопасности**](wlan-profileschema-security-msm-element.md) сразу после элемента [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cce5a-112">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="cce5a-113">В следующем фрагменте кода показан элемент [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) , содержащий незашифрованный ключ.</span><span class="sxs-lookup"><span data-stu-id="cce5a-113">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="cce5a-114">`<!-- insert key here -->`Перед использованием этого фрагмента в профиле необходимо заменить комментарий фактическим незашифрованным ключом.</span><span class="sxs-lookup"><span data-stu-id="cce5a-114">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="cce5a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="cce5a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cce5a-116">Образцы профиля беспроводной связи</span><span class="sxs-lookup"><span data-stu-id="cce5a-116">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



