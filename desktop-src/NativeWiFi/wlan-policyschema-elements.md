---
description: Профиль политики беспроводной локальной сети Wi-Fi (WLAN) состоит из следующих элементов схемы.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: WLAN_policy элементы схемы
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8346aab6aba209933b20790cf3747d5c0944f972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541042"
---
# <a name="wlan_policy-schema-elements"></a><span data-ttu-id="fae1b-103">\_Элементы схемы политики WLAN</span><span class="sxs-lookup"><span data-stu-id="fae1b-103">WLAN\_policy Schema Elements</span></span>

<span data-ttu-id="fae1b-104">Профиль политики беспроводной локальной сети Wi-Fi (WLAN) состоит из следующих элементов схемы.</span><span class="sxs-lookup"><span data-stu-id="fae1b-104">A Native Wifi wireless LAN (WLAN) policy profile is composed of the following schema elements.</span></span> <span data-ttu-id="fae1b-105">Все именованные элементы находятся в пространстве имен `https://www.microsoft.com/networking/WLAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="fae1b-105">All of the named elements are in the namespace `https://www.microsoft.com/networking/WLAN/policy/v1`.</span></span>

<span data-ttu-id="fae1b-106">В следующем списке показаны определенные элементы в порядке, в котором элементы отображаются в профиле.</span><span class="sxs-lookup"><span data-stu-id="fae1b-106">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="fae1b-107">Упорядочение элементов выполняется принудительно.</span><span class="sxs-lookup"><span data-stu-id="fae1b-107">The ordering of elements is enforced.</span></span> <span data-ttu-id="fae1b-108">Не все элементы находятся в каждом профиле, поскольку некоторые элементы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="fae1b-108">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="fae1b-109">В этом списке не отображаются все возможные элементы, которые могут отображаться в профиле, так как элементы можно добавлять в **xs: любые** точки вставки.</span><span class="sxs-lookup"><span data-stu-id="fae1b-109">This list does not show all possible elements that can appear in a profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="fae1b-110">**вланполици**</span><span class="sxs-lookup"><span data-stu-id="fae1b-110">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
    -   [<span data-ttu-id="fae1b-111">**имя (Вланполици)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-111">**name (WLANPolicy)**</span></span>](wlan-policyschema-name-wlanpolicy-element.md)
    -   [<span data-ttu-id="fae1b-112">**Описание (Вланполици)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-112">**description (WLANPolicy)**</span></span>](wlan-policyschema-description-wlanpolicy-element.md)
    -   [<span data-ttu-id="fae1b-113">**Глобалфлагс (Вланполици)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-113">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [<span data-ttu-id="fae1b-114">**Енаблеаутоконфиг (Глобалфлагс)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-114">**enableAutoConfig (globalFlags)**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [<span data-ttu-id="fae1b-115">**Шовдениеднетворк (Глобалфлагс)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-115">**showDeniedNetwork (globalFlags)**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [<span data-ttu-id="fae1b-116">**Алловеверйонетокреатеаллусерпрофилес (Глобалфлагс)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-116">**allowEveryoneToCreateAllUserProfiles (globalFlags)**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [<span data-ttu-id="fae1b-117">**Нетворкфилтер (Вланполици)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-117">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [<span data-ttu-id="fae1b-118">**Разрешенных (Нетворкфилтер)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-118">**allowList (networkFilter)**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [<span data-ttu-id="fae1b-119">**сеть (разрешенных)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-119">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
                -   [<span data-ttu-id="fae1b-120">**networkName (Нетворкитемтипе)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-120">**networkName (networkItemType)**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [<span data-ttu-id="fae1b-121">**Нетворктипе (Нетворкитемтипе)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-121">**networkType (networkItemType)**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [<span data-ttu-id="fae1b-122">**Списка блокировки (Нетворкфилтер)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-122">**blockList (networkFilter)**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [<span data-ttu-id="fae1b-123">**сеть (списка блокировки)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-123">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
                -   [<span data-ttu-id="fae1b-124">**networkName (Нетворкитемтипе)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-124">**networkName (networkItemType)**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [<span data-ttu-id="fae1b-125">**Нетворктипе (Нетворкитемтипе)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-125">**networkType (networkItemType)**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [<span data-ttu-id="fae1b-126">**Деняллибсс (Нетворкфилтер)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-126">**denyAllIBSS (networkFilter)**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [<span data-ttu-id="fae1b-127">**Деняллесс (Нетворкфилтер)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-127">**denyAllESS (networkFilter)**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [<span data-ttu-id="fae1b-128">**Профилелист (Вланполици)**</span><span class="sxs-lookup"><span data-stu-id="fae1b-128">**profileList (WLANPolicy)**</span></span>](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



