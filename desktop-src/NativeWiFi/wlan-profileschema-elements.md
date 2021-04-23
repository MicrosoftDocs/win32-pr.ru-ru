---
description: '\_Схема профиля WLAN определяет следующие элементы.'
ms.assetid: 9eb0f446-1202-4770-b09e-250e83524119
title: WLAN_profile элементы схемы
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a94394c32712d8ee8871ada753f342861e1f530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810379"
---
# <a name="wlan_profile-schema-elements"></a><span data-ttu-id="0b88b-103">\_Элементы схемы профиля WLAN</span><span class="sxs-lookup"><span data-stu-id="0b88b-103">WLAN\_profile Schema Elements</span></span>

<span data-ttu-id="0b88b-104">\_Схема профиля WLAN определяет следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="0b88b-104">The WLAN\_profile schema defines the following elements.</span></span> <span data-ttu-id="0b88b-105">Большинство элементов находятся в пространстве имен `https://www.microsoft.com/networking/WLAN/profile/v1` , за исключением [**Фипсмоде (аусенкриптион)**](wlan-profileschema-fipsmode-authencryption-element.md), который находится в пространстве имен `https://www.microsoft.com/networking/WLAN/profile/v2` .</span><span class="sxs-lookup"><span data-stu-id="0b88b-105">Most elements are in the namespace `https://www.microsoft.com/networking/WLAN/profile/v1`, except for [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), which is in the namespace `https://www.microsoft.com/networking/WLAN/profile/v2`.</span></span>

<span data-ttu-id="0b88b-106">В следующем списке показаны определенные элементы в порядке, в котором элементы отображаются в профиле.</span><span class="sxs-lookup"><span data-stu-id="0b88b-106">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="0b88b-107">Упорядочение элементов выполняется принудительно.</span><span class="sxs-lookup"><span data-stu-id="0b88b-107">The ordering of elements is enforced.</span></span> <span data-ttu-id="0b88b-108">Не все элементы находятся в каждом профиле, поскольку некоторые элементы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="0b88b-108">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="0b88b-109">В этом списке не отображаются все возможные элементы, которые могут отображаться в профиле беспроводной связи, так как элементы можно добавлять в **xs: любые** точки вставки.</span><span class="sxs-lookup"><span data-stu-id="0b88b-109">This list does not show all possible elements that can appear in a wireless profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="0b88b-110">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="0b88b-110">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
    -   [<span data-ttu-id="0b88b-111">**имя (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-111">**name (WLANProfile)**</span></span>](wlan-profileschema-name-wlanprofile-element.md)
    -   [<span data-ttu-id="0b88b-112">**Ссидконфиг (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-112">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [<span data-ttu-id="0b88b-113">**SSID (Ссидконфиг)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-113">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [<span data-ttu-id="0b88b-114">**Hex (SSID)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-114">**hex (SSID)**</span></span>](wlan-profileschema-hex-ssid-element.md)
            -   [<span data-ttu-id="0b88b-115">**имя (SSID)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-115">**name (SSID)**</span></span>](wlan-profileschema-name-ssid-element.md)
        -   [<span data-ttu-id="0b88b-116">**Нешироковещательная (Ссидконфиг)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-116">**nonBroadcast (SSIDConfig)**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [<span data-ttu-id="0b88b-117">**Hotspot2 (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-117">**Hotspot2 (WLANProfile)**</span></span>](wlan-profileschema-hotspot2-element.md)
        -   [<span data-ttu-id="0b88b-118">**Имя_домена (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-118">**DomainName (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-domainname-element.md)
        -   [<span data-ttu-id="0b88b-119">**Наиреалм (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-119">**NAIRealm (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [<span data-ttu-id="0b88b-120">**Network3GPP (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-120">**Network3GPP (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [<span data-ttu-id="0b88b-121">**Роамингконсортиум (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-121">**RoamingConsortium (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [<span data-ttu-id="0b88b-122">**connectionType (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-122">**connectionType (WLANProfile)**</span></span>](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [<span data-ttu-id="0b88b-123">**connectionMode (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-123">**connectionMode (WLANProfile)**</span></span>](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [<span data-ttu-id="0b88b-124">**Автопереключение (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-124">**autoSwitch (WLANProfile)**</span></span>](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [<span data-ttu-id="0b88b-125">**MSM (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-125">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
        -   [<span data-ttu-id="0b88b-126">**подключение (MSM)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-126">**connectivity (MSM)**</span></span>](wlan-profileschema-connectivity-msm-element.md)
            -   [<span data-ttu-id="0b88b-127">**Фитипе (подключение)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-127">**phyType (connectivity)**</span></span>](wlan-profileschema-phytype-connectivity-element.md)
        -   [<span data-ttu-id="0b88b-128">**безопасность (MSM)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-128">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
            -   [<span data-ttu-id="0b88b-129">**Аусенкриптион (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-129">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
                -   [<span data-ttu-id="0b88b-130">**Проверка подлинности (Аусенкриптион)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-130">**authentication (authEncryption)**</span></span>](wlan-profileschema-authentication-authencryption-element.md)
                -   [<span data-ttu-id="0b88b-131">**шифрование (Аусенкриптион)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-131">**encryption (authEncryption)**</span></span>](wlan-profileschema-encryption-authencryption-element.md)
                -   [<span data-ttu-id="0b88b-132">**Усеонекс (Аусенкриптион)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-132">**useOneX (authEncryption)**</span></span>](wlan-profileschema-useonex-authencryption-element.md)
                -   [<span data-ttu-id="0b88b-133">**Фипсмоде (Аусенкриптион)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-133">**FIPSMode (authEncryption)**</span></span>](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [<span data-ttu-id="0b88b-134">**sharedKey (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-134">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
                -   [<span data-ttu-id="0b88b-135">**keyType (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-135">**keyType (sharedKey)**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)
                -   [<span data-ttu-id="0b88b-136">**защищено (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-136">**protected (sharedKey)**</span></span>](wlan-profileschema-protected-sharedkey-element.md)
                -   [<span data-ttu-id="0b88b-137">**Кэйматериал (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-137">**keyMaterial (sharedKey)**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)
            -   [<span data-ttu-id="0b88b-138">**Кэйиндекс (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-138">**keyIndex (security)**</span></span>](wlan-profileschema-keyindex-security-element.md)
            -   [<span data-ttu-id="0b88b-139">**Пмккачемоде (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-139">**PMKCacheMode (security)**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)
            -   [<span data-ttu-id="0b88b-140">**Пмккачеттл (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-140">**PMKCacheTTL (security)**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)
            -   [<span data-ttu-id="0b88b-141">**Пмккачесизе (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-141">**PMKCacheSize (security)**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)
            -   [<span data-ttu-id="0b88b-142">**Преаусмоде (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-142">**preAuthMode (security)**</span></span>](wlan-profileschema-preauthmode-security-element.md)
            -   [<span data-ttu-id="0b88b-143">**Преауссроттле (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-143">**preAuthThrottle (security)**</span></span>](wlan-profileschema-preauththrottle-security-element.md)
    -   [<span data-ttu-id="0b88b-144">**IHV (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-144">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
        -   [<span data-ttu-id="0b88b-145">**Ауихеадер (IHV)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-145">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
            -   [<span data-ttu-id="0b88b-146">**OUI (Ауихеадер)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-146">**OUI (OUIHeader)**</span></span>](wlan-profileschema-oui-ouiheader-element.md)
            -   [<span data-ttu-id="0b88b-147">**тип (Ауихеадер)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-147">**type (OUIHeader)**</span></span>](wlan-profileschema-type-ouiheader-element.md)
        -   [<span data-ttu-id="0b88b-148">**подключение (IHV)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-148">**connectivity (IHV)**</span></span>](wlan-profileschema-connectivity-ihv-element.md)
        -   [<span data-ttu-id="0b88b-149">**безопасность (IHV)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-149">**security (IHV)**</span></span>](wlan-profileschema-security-ihv-element.md)
        -   [<span data-ttu-id="0b88b-150">**Усемсонекс (IHV)**</span><span class="sxs-lookup"><span data-stu-id="0b88b-150">**useMSOneX (IHV)**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)

 

 



