---
description: Новые возможности системной поддержки Wi-Fi
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: Новые возможности системной поддержки Wi-Fi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126627f4cf6431fbac2bf4d1f6ec58561bfd8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683087"
---
# <a name="whats-new-in-native-wifi"></a><span data-ttu-id="f0ac1-103">Новые возможности системной поддержки Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="f0ac1-103">What's New in Native Wifi</span></span>

## <a name="windows-10-version-2004"></a><span data-ttu-id="f0ac1-104">Windows 10, версия 2004</span><span class="sxs-lookup"><span data-stu-id="f0ac1-104">Windows 10, version 2004</span></span>

<span data-ttu-id="f0ac1-105">См. статью о [подготовке профиля Wi-Fi через веб-сайт](prov-wifi-profile-via-website.md).</span><span class="sxs-lookup"><span data-stu-id="f0ac1-105">See [Provision a Wi-Fi profile via a website](prov-wifi-profile-via-website.md).</span></span>

## <a name="windows-10"></a><span data-ttu-id="f0ac1-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f0ac1-106">Windows 10</span></span>

<span data-ttu-id="f0ac1-107">В [ \_ схему профиля WLAN](wlan-profileschema-schema.md)добавлена поддержка Hotspot 2,0.</span><span class="sxs-lookup"><span data-stu-id="f0ac1-107">Support for Hotspot 2.0 has been added to the [WLAN\_profile schema](wlan-profileschema-schema.md).</span></span> <span data-ttu-id="f0ac1-108">Hotspot 2,0 обеспечивает автоматическое подключение к общедоступным службам Wi-Fi, используя существующие учетные данные и членство в сетях поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="f0ac1-108">Hotspot 2.0 enables automatic connection to public Wi-Fi services using existing credentials and membership in service provider networks.</span></span> <span data-ttu-id="f0ac1-109">Поставщики услуг указывают, как соединения устанавливаются с помощью новых элементов схемы, чтобы описать используемые сети и способ проверки подлинности в них.</span><span class="sxs-lookup"><span data-stu-id="f0ac1-109">Service providers specify how connections are made using the new schema elements to describe which networks to use, and how to authenticate to them.</span></span> <span data-ttu-id="f0ac1-110">Дополнительные сведения см. в документации по элементу [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f0ac1-110">See the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element documentation for details.</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="f0ac1-111">Windows 8 и Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0ac1-111">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="f0ac1-112">В собственные интерфейсы API Wi-Fi в Windows 8 и Windows Server 2012 были добавлены следующие функции.</span><span class="sxs-lookup"><span data-stu-id="f0ac1-112">The following features have been added to the Native Wifi APIs on Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="f0ac1-113">Wi-Fi Direct, основанный на разработке Wi-Fiной технической спецификации v 1.1 с помощью Wi-Fi Alliance (см. Описание [опубликованных спецификаций Wi-Fi Alliance](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="f0ac1-113">A Wi-Fi Direct feature based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="f0ac1-114">Целью Wi-Fiной технической спецификации является предоставление решения для Wi-Fi подключения устройства к устройству без необходимости использовать беспроводную точку доступа (беспроводный ТД) для настройки подключения или использования существующего механизма нерегламентированных Wi-Fi (ИБСС).</span><span class="sxs-lookup"><span data-stu-id="f0ac1-114">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism.</span></span>

<span data-ttu-id="f0ac1-115">Следующие функции поддерживают функцию прямого Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="f0ac1-115">The following functions support the Wi-Fi Direct feature.</span></span>

-   [<span data-ttu-id="f0ac1-116">**\_ \_ \_ обратный вызов для завершения открытого сеанса \_ WFD**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-116">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [<span data-ttu-id="f0ac1-117">**вфдканцелопенсессион**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-117">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [<span data-ttu-id="f0ac1-118">**вфдклосехандле**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-118">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [<span data-ttu-id="f0ac1-119">**вфдклосесессион**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-119">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [<span data-ttu-id="f0ac1-120">**вфдопенхандле**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-120">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [<span data-ttu-id="f0ac1-121">**вфдопенлегацисессион**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-121">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [<span data-ttu-id="f0ac1-122">**вфдстартопенсессион**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-122">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [<span data-ttu-id="f0ac1-123">**вфдупдатедевицевисибилити**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-123">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="f0ac1-124">Windows 7 и Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f0ac1-124">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="f0ac1-125">В собственные интерфейсы API Wi-Fi в Windows 7 и Windows Server 2008 R2 были добавлены следующие функции.</span><span class="sxs-lookup"><span data-stu-id="f0ac1-125">The following features have been added to the Native Wifi APIs on Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="f0ac1-126">Беспроводная размещенная сеть позволяет одному физическому беспроводному адаптеру подключаться в качестве клиента к точке доступа к оборудованию (AP), в то же время действуя как программный AP, что позволяет другим устройствам, поддерживающим беспроводное подключение, подключаться к нему.</span><span class="sxs-lookup"><span data-stu-id="f0ac1-126">The wireless Hosted Network allows a single physical wireless adapter to connect as a client to a hardware access point (AP), while at the same time acting as a software AP allowing other wireless-capable devices to connect to it.</span></span>

<span data-ttu-id="f0ac1-127">Следующие функции поддерживают функцию беспроводной размещенной сети.</span><span class="sxs-lookup"><span data-stu-id="f0ac1-127">The following functions support the wireless Hosted Network feature.</span></span>

-   [<span data-ttu-id="f0ac1-128">**вланхостеднетворкфорцестарт**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-128">**WlanHostedNetworkForceStart**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [<span data-ttu-id="f0ac1-129">**вланхостеднетворкфорцестоп**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-129">**WlanHostedNetworkForceStop**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [<span data-ttu-id="f0ac1-130">**вланхостеднетворкинитсеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-130">**WlanHostedNetworkInitSettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [<span data-ttu-id="f0ac1-131">**вланхостеднетворккуерипроперти**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-131">**WlanHostedNetworkQueryProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [<span data-ttu-id="f0ac1-132">**вланхостеднетворккуерисекондарикэй**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-132">**WlanHostedNetworkQuerySecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [<span data-ttu-id="f0ac1-133">**вланхостеднетворккуеристатус**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-133">**WlanHostedNetworkQueryStatus**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [<span data-ttu-id="f0ac1-134">**вланхостеднетворкрефрешсекуритисеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-134">**WlanHostedNetworkRefreshSecuritySettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [<span data-ttu-id="f0ac1-135">**вланхостеднетворксетпроперти**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-135">**WlanHostedNetworkSetProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [<span data-ttu-id="f0ac1-136">**вланхостеднетворксетсекондарикэй**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-136">**WlanHostedNetworkSetSecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [<span data-ttu-id="f0ac1-137">**вланхостеднетворкстартусинг**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-137">**WlanHostedNetworkStartUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [<span data-ttu-id="f0ac1-138">**вланхостеднетворкстопусинг**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-138">**WlanHostedNetworkStopUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [<span data-ttu-id="f0ac1-139">**вланрегистервиртуалстатионнотификатион**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-139">**WlanRegisterVirtualStationNotification**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

<span data-ttu-id="f0ac1-140">Следующие новые структуры работают с беспроводной размещенной сетью.</span><span class="sxs-lookup"><span data-stu-id="f0ac1-140">The following new structures that work with wireless Hosted Network.</span></span>

-   [<span data-ttu-id="f0ac1-141">**\_ \_ \_ Параметры сетевого подключения \_ , размещенного в беспроводной сети**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-141">**WLAN\_HOSTED\_NETWORK\_CONNECTION\_SETTINGS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [<span data-ttu-id="f0ac1-142">**\_ \_ \_ \_ изменение состояния однорангового узла данных в \_ сети WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-142">**WLAN\_HOSTED\_NETWORK\_DATA\_PEER\_STATE\_CHANGE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [<span data-ttu-id="f0ac1-143">**\_ \_ \_ состояние одноранговой сети в размещенной WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-143">**WLAN\_HOSTED\_NETWORK\_PEER\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [<span data-ttu-id="f0ac1-144">**\_ \_ состояние радио для сети, РАЗМЕЩЕНной WLAN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-144">**WLAN\_HOSTED\_NETWORK\_RADIO\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [<span data-ttu-id="f0ac1-145">**\_ \_ \_ Параметры безопасности сети, РАЗМЕЩЕНной в WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-145">**WLAN\_HOSTED\_NETWORK\_SECURITY\_SETTINGS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [<span data-ttu-id="f0ac1-146">**\_ \_ \_ изменение состояния РАЗМЕЩЕНной сети WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-146">**WLAN\_HOSTED\_NETWORK\_STATE\_CHANGE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [<span data-ttu-id="f0ac1-147">**\_состояние размещенной \_ сети WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-147">**WLAN\_HOSTED\_NETWORK\_STATUS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

<span data-ttu-id="f0ac1-148">Ниже перечислены новые перечисления, которые работают с беспроводной размещенной сетью.</span><span class="sxs-lookup"><span data-stu-id="f0ac1-148">The following new enumerations that work with wireless Hosted Network.</span></span>

-   [<span data-ttu-id="f0ac1-149">**\_ \_ \_ код уведомления РАЗМЕЩЕНной сети WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-149">**WLAN\_HOSTED\_NETWORK\_NOTIFICATION\_CODE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [<span data-ttu-id="f0ac1-150">**\_ \_ код операции размещенной сети WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-150">**WLAN\_HOSTED\_NETWORK\_OPCODE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [<span data-ttu-id="f0ac1-151">**\_ \_ \_ \_ состояние проверки подлинности однорангового узла беспроводной сети \_**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-151">**WLAN\_HOSTED\_NETWORK\_PEER\_AUTH\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [<span data-ttu-id="f0ac1-152">**\_Причина размещения \_ сети \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-152">**WLAN\_HOSTED\_NETWORK\_REASON**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [<span data-ttu-id="f0ac1-153">**состояние сети, в которой \_ размещена беспроводная \_ сеть \_**</span><span class="sxs-lookup"><span data-stu-id="f0ac1-153">**WLAN\_HOSTED\_NETWORK\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a><span data-ttu-id="f0ac1-154">См. также</span><span class="sxs-lookup"><span data-stu-id="f0ac1-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0ac1-155">Сведения о беспроводной размещенной сети</span><span class="sxs-lookup"><span data-stu-id="f0ac1-155">About the Wireless Hosted Network</span></span>](about-the-wireless-hosted-network.md)
</dt> <dt>

[<span data-ttu-id="f0ac1-156">Использование беспроводной размещенной сети и общего доступа к подключению к Интернету</span><span class="sxs-lookup"><span data-stu-id="f0ac1-156">Using Wireless Hosted Network and Internet Connection Sharing</span></span>](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



