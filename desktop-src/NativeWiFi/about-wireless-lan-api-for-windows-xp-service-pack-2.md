---
description: Подмножество встроенных функций интерфейса API WiFi поддерживается в Windows XP с пакетом обновления 2 (SP2) и Windows XP с пакетом обновления 3 (SP3).
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Встроенная поддержка интерфейса API WiFi в Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cd422c6589b37f516b9d45d072489c9d5e00b82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346012"
---
# <a name="native-wifi-api-support-on-windows-xp"></a><span data-ttu-id="d4344-103">Встроенная поддержка интерфейса API WiFi в Windows XP</span><span class="sxs-lookup"><span data-stu-id="d4344-103">Native Wifi API Support on Windows XP</span></span>

<span data-ttu-id="d4344-104">Подмножество встроенных функций интерфейса API WiFi поддерживается в Windows XP с пакетом обновления 2 (SP2) и Windows XP с пакетом обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="d4344-104">A subset of the Native Wifi API functionality is supported on Windows XP with Service Pack 2 (SP2) and Windows XP with Service Pack 3 (SP3).</span></span> <span data-ttu-id="d4344-105">Эта функция включена в Windows XP с пакетом обновления 3 (SP3) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d4344-105">This functionality is included in Windows XP with SP3 by default.</span></span> <span data-ttu-id="d4344-106">В Windows XP с пакетом обновления 2 (SP2) эту функцию можно добавить, применив исправление, которое называется API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="d4344-106">In Windows XP with SP2, this functionality can be added by applying a hotfix, which is known as Wireless LAN API for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="d4344-107">Дополнительные сведения или о загрузке исправления см. в разделе "разработчики не могут создавать беспроводные клиентские программы, управляющие профилями и подключениями по беспроводной сети с помощью службы настройки беспроводных подключений в Microsoft Windows XP с пакетом обновления 2 (SP2) в центре знаний справки и поддержки по адресу [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .</span><span class="sxs-lookup"><span data-stu-id="d4344-107">For more information or to download the hotfix, see "Developers cannot create wireless client programs that manage wireless profiles and connections over the Wireless Zero Configuration service in Microsoft Windows XP Service Pack 2 (SP2)" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997).</span></span>

<span data-ttu-id="d4344-108">Из-за базовых архитектурных различий в Windows XP встроенный API Wi-Fi на имеет некоторые ограничения.</span><span class="sxs-lookup"><span data-stu-id="d4344-108">Because of underlying architectural differences in Windows XP, the Native Wifi API on has some limitations.</span></span> <span data-ttu-id="d4344-109">Ниже приведен список ограничений.</span><span class="sxs-lookup"><span data-stu-id="d4344-109">Here is a list of limitations:</span></span>

-   <span data-ttu-id="d4344-110">С профилем можно связать не более одного SSID.</span><span class="sxs-lookup"><span data-stu-id="d4344-110">At most one SSID can be associated with a profile.</span></span>
-   <span data-ttu-id="d4344-111">Сети инфраструктуры всегда отображаются перед сетями ad hoc в списке профилей.</span><span class="sxs-lookup"><span data-stu-id="d4344-111">Infrastructure networks always appear before ad hoc networks in the profile list.</span></span>
-   <span data-ttu-id="d4344-112">Имена профилей являются производными от SSID и не могут быть заданы пользователем произвольной строкой.</span><span class="sxs-lookup"><span data-stu-id="d4344-112">Profile names are derived from the SSID, and cannot be set by the user to an arbitrary string.</span></span>
-   <span data-ttu-id="d4344-113">Типы PHY не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d4344-113">PHY types are not supported.</span></span>
-   <span data-ttu-id="d4344-114">Кэширование парных главных ключей (PMK) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d4344-114">Pairwise master key (PMK) caching is not supported.</span></span>
-   <span data-ttu-id="d4344-115">Функции расширяемости независимых поставщиков оборудования (IHV) не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d4344-115">Independent hardware vendor (IHV) extensibility functions are not supported.</span></span>
-   <span data-ttu-id="d4344-116">Разрешения профиля не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d4344-116">Profile permissions are not supported.</span></span>
-   <span data-ttu-id="d4344-117">\_ \_ Доступны только подключение к ACM по беспроводной сети \_ \_ и уведомления \_ о \_ разъединении ACM для уведомлений WLAN \_ .</span><span class="sxs-lookup"><span data-stu-id="d4344-117">Only the wlan\_notification\_acm\_connection\_complete and the wlan\_notification\_acm\_disconnected notifications are available.</span></span>
-   <span data-ttu-id="d4344-118">Глобальные параметры конфигурации 802.1 X и EAPOL не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d4344-118">Global 802.1X and EAPOL configuration settings are not supported.</span></span>

<span data-ttu-id="d4344-119">Следующие функции поддерживаются Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):</span><span class="sxs-lookup"><span data-stu-id="d4344-119">The following functions are supported by Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:</span></span>

-   [<span data-ttu-id="d4344-120">**\_ \_ обратный вызов уведомления WLAN**</span><span class="sxs-lookup"><span data-stu-id="d4344-120">**WLAN\_NOTIFICATION\_CALLBACK**</span></span>](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [<span data-ttu-id="d4344-121">**вланаллокатемемори**</span><span class="sxs-lookup"><span data-stu-id="d4344-121">**WlanAllocateMemory**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [<span data-ttu-id="d4344-122">**вланклосехандле**</span><span class="sxs-lookup"><span data-stu-id="d4344-122">**WlanCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [<span data-ttu-id="d4344-123">**вланконнект**</span><span class="sxs-lookup"><span data-stu-id="d4344-123">**WlanConnect**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [<span data-ttu-id="d4344-124">**вланделетепрофиле**</span><span class="sxs-lookup"><span data-stu-id="d4344-124">**WlanDeleteProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [<span data-ttu-id="d4344-125">**вландисконнект**</span><span class="sxs-lookup"><span data-stu-id="d4344-125">**WlanDisconnect**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [<span data-ttu-id="d4344-126">**вланенуминтерфацес**</span><span class="sxs-lookup"><span data-stu-id="d4344-126">**WlanEnumInterfaces**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [<span data-ttu-id="d4344-127">**вланфримемори**</span><span class="sxs-lookup"><span data-stu-id="d4344-127">**WlanFreeMemory**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [<span data-ttu-id="d4344-128">**вланжетаваилабленетворклист**</span><span class="sxs-lookup"><span data-stu-id="d4344-128">**WlanGetAvailableNetworkList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [<span data-ttu-id="d4344-129">**вланжетпрофиле**</span><span class="sxs-lookup"><span data-stu-id="d4344-129">**WlanGetProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [<span data-ttu-id="d4344-130">**вланжетпрофилелист**</span><span class="sxs-lookup"><span data-stu-id="d4344-130">**WlanGetProfileList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [<span data-ttu-id="d4344-131">**вланопенхандле**</span><span class="sxs-lookup"><span data-stu-id="d4344-131">**WlanOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [<span data-ttu-id="d4344-132">**вланкуеринтерфаце**</span><span class="sxs-lookup"><span data-stu-id="d4344-132">**WlanQueryInterface**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [<span data-ttu-id="d4344-133">**вланреасонкодетостринг**</span><span class="sxs-lookup"><span data-stu-id="d4344-133">**WlanReasonCodeToString**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [<span data-ttu-id="d4344-134">**вланрегистернотификатион**</span><span class="sxs-lookup"><span data-stu-id="d4344-134">**WlanRegisterNotification**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [<span data-ttu-id="d4344-135">**вланскан**</span><span class="sxs-lookup"><span data-stu-id="d4344-135">**WlanScan**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [<span data-ttu-id="d4344-136">**влансетинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="d4344-136">**WlanSetInterface**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [<span data-ttu-id="d4344-137">**влансетпрофиле**</span><span class="sxs-lookup"><span data-stu-id="d4344-137">**WlanSetProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [<span data-ttu-id="d4344-138">**влансетпрофилиапксмлусердата**</span><span class="sxs-lookup"><span data-stu-id="d4344-138">**WlanSetProfileEapXmlUserData**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [<span data-ttu-id="d4344-139">**влансетпрофилелист**</span><span class="sxs-lookup"><span data-stu-id="d4344-139">**WlanSetProfileList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [<span data-ttu-id="d4344-140">**влансетпрофилепоситион**</span><span class="sxs-lookup"><span data-stu-id="d4344-140">**WlanSetProfilePosition**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a><span data-ttu-id="d4344-141">См. также</span><span class="sxs-lookup"><span data-stu-id="d4344-141">Related topics</span></span>

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[<span data-ttu-id="d4344-142">О встроенных WiFi</span><span class="sxs-lookup"><span data-stu-id="d4344-142">About Native Wifi</span></span>](about-native-wifi.md)
</dt> </dl>

 

 
