---
description: Из-за базовых различий в архитектуре операционной системы Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2) поддерживают только подмножество элементов, описанных в \_ справочнике по схеме профиля WLAN и справочным материалам схемы OneX.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Совместимость профиля беспроводной связи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e0eebfa627fb99d50490907108a2ddc7360202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545679"
---
# <a name="wireless-profile-compatibility"></a><span data-ttu-id="bca19-103">Совместимость профиля беспроводной связи</span><span class="sxs-lookup"><span data-stu-id="bca19-103">Wireless Profile Compatibility</span></span>

<span data-ttu-id="bca19-104">Из-за базовых различий в архитектуре операционной системы Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2) поддерживают только подмножество элементов, описанных в справочнике по [ \_ схеме профиля WLAN](wlan-profileschema-schema.md) и справочным материалам [схемы OneX](onexschema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="bca19-104">Because of underlying architectural differences in the operating system, Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2) support only a subset of the elements described in the [WLAN\_profile Schema](wlan-profileschema-schema.md) and [OneX Schema](onexschema-schema.md) reference material.</span></span>

<span data-ttu-id="bca19-105">Все профили, которые соответствуют требованиям Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2), также можно использовать в Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="bca19-105">All profiles that conform to Windows XP with SP3 and Wireless LAN API for Windows XP with SP2 requirements can also be used on Windows Vista and Windows Server 2008.</span></span>

## <a name="wlan_profile-support"></a><span data-ttu-id="bca19-106">\_Поддержка профиля WLAN</span><span class="sxs-lookup"><span data-stu-id="bca19-106">WLAN\_profile Support</span></span>

<span data-ttu-id="bca19-107">Следующие \_ элементы профиля WLAN не поддерживаются в Windows XP с пакетом обновления 3 (SP3) или API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):</span><span class="sxs-lookup"><span data-stu-id="bca19-107">The following WLAN\_profile elements are not supported in Windows XP with SP3 or Wireless LAN API for Windows XP with SP2:</span></span>

-   <span data-ttu-id="bca19-108">подключение (IHV)</span><span class="sxs-lookup"><span data-stu-id="bca19-108">connectivity (IHV)</span></span>
-   <span data-ttu-id="bca19-109">IHV (Вланпрофиле)</span><span class="sxs-lookup"><span data-stu-id="bca19-109">IHV (WLANProfile)</span></span>
-   <span data-ttu-id="bca19-110">OUI (Ауихеадер)</span><span class="sxs-lookup"><span data-stu-id="bca19-110">OUI (OUIHeader)</span></span>
-   <span data-ttu-id="bca19-111">Фитипе (подключение)</span><span class="sxs-lookup"><span data-stu-id="bca19-111">phyType (connectivity)</span></span>
-   <span data-ttu-id="bca19-112">Пмккачемоде (безопасность)</span><span class="sxs-lookup"><span data-stu-id="bca19-112">PMKCacheMode (security)</span></span>
-   <span data-ttu-id="bca19-113">Пмккачесизе (безопасность)</span><span class="sxs-lookup"><span data-stu-id="bca19-113">PMKCacheSize (security)</span></span>
-   <span data-ttu-id="bca19-114">Пмккачеттл (безопасность)</span><span class="sxs-lookup"><span data-stu-id="bca19-114">PMKCacheTTL (security)</span></span>
-   <span data-ttu-id="bca19-115">Преаусмоде (безопасность)</span><span class="sxs-lookup"><span data-stu-id="bca19-115">preAuthMode (security)</span></span>
-   <span data-ttu-id="bca19-116">Преауссроттле (безопасность)</span><span class="sxs-lookup"><span data-stu-id="bca19-116">preAuthThrottle (security)</span></span>
-   <span data-ttu-id="bca19-117">безопасность (IHV)</span><span class="sxs-lookup"><span data-stu-id="bca19-117">security (IHV)</span></span>
-   <span data-ttu-id="bca19-118">тип (Ауихеадер)</span><span class="sxs-lookup"><span data-stu-id="bca19-118">type (OUIHeader)</span></span>
-   <span data-ttu-id="bca19-119">Усемсонекс (IHV)</span><span class="sxs-lookup"><span data-stu-id="bca19-119">useMSOneX (IHV)</span></span>

<span data-ttu-id="bca19-120">В следующей таблице показаны \_ элементы профиля WLAN с ограниченными значениями для Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="bca19-120">The following table shows WLAN\_profile elements with constrained values for Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:</span></span>



| <span data-ttu-id="bca19-121">Элемент</span><span class="sxs-lookup"><span data-stu-id="bca19-121">Element</span></span>                                                                               | <span data-ttu-id="bca19-122">Ограничение</span><span class="sxs-lookup"><span data-stu-id="bca19-122">Constraint</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bca19-123">**имя (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="bca19-123">**name (WLANProfile)**</span></span>](wlan-profileschema-name-wlanprofile-element.md)             | <span data-ttu-id="bca19-124">Элемент name игнорируется при сохранении профиля в хранилище профилей.</span><span class="sxs-lookup"><span data-stu-id="bca19-124">The name element is ignored when the profile is saved in the profile store.</span></span> <span data-ttu-id="bca19-125">Имя профиля извлекается автоматически из идентификатора SSID сети.</span><span class="sxs-lookup"><span data-stu-id="bca19-125">The name of the profile is derived automatically from the SSID of the network.</span></span> <span data-ttu-id="bca19-126">Для сетевых профилей инфраструктуры имя профиля — это идентификатор SSID сети.</span><span class="sxs-lookup"><span data-stu-id="bca19-126">For infrastructure network profiles, the name of the profile is the SSID of the network.</span></span> <span data-ttu-id="bca19-127">Для сетевых профилей ad hoc имя профиля — это идентификатор SSID нерегламентированной сети, за которым следует `-adhoc` .</span><span class="sxs-lookup"><span data-stu-id="bca19-127">For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by `-adhoc`.</span></span> |
| [<span data-ttu-id="bca19-128">**защищено (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="bca19-128">**protected (sharedKey)**</span></span>](wlan-profileschema-protected-sharedkey-element.md)       | <span data-ttu-id="bca19-129">Должно иметь значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="bca19-129">Must have a value of FALSE.</span></span>                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="bca19-130">**Ссидконфиг (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="bca19-130">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md) | <span data-ttu-id="bca19-131">Ограничено одним дочерним элементом [**SSID (ссидконфиг)**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bca19-131">Restricted to one child [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a><span data-ttu-id="bca19-132">Поддержка OneX</span><span class="sxs-lookup"><span data-stu-id="bca19-132">OneX Support</span></span>

<span data-ttu-id="bca19-133">Только элемент [**еапконфиг**](onexschema-eapconfig-onex-element.md) поддерживается в Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="bca19-133">Only the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is supported on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span> <span data-ttu-id="bca19-134">Другие элементы OneX, если они есть в профиле, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="bca19-134">Other OneX elements, if present in a profile, will be ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bca19-135">См. также</span><span class="sxs-lookup"><span data-stu-id="bca19-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bca19-136">Сведения о встроенном API Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="bca19-136">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="bca19-137">Встроенная поддержка интерфейса API WiFi в Windows XP</span><span class="sxs-lookup"><span data-stu-id="bca19-137">Native Wifi API Support on Windows XP</span></span>](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



