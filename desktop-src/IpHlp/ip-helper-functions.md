---
title: Вспомогательные функции IP
description: Следующие функции извлекают и изменяют параметры конфигурации для транспорта TCP/IP на локальном компьютере.
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5f562470-f3e8-4305-a015-3a84cd09a1eb
ms.openlocfilehash: ee16bb0b65545c4abbef387c5b90d42fb9d3c629
ms.sourcegitcommit: ea0069adb72dbfa717e73f3a96c3407a49ec0dab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2021
ms.locfileid: "114394217"
---
# <a name="ip-helper-functions"></a><span data-ttu-id="3b33f-103">Вспомогательные функции IP</span><span class="sxs-lookup"><span data-stu-id="3b33f-103">IP Helper functions</span></span>

<span data-ttu-id="3b33f-104">Следующие функции извлекают и изменяют параметры конфигурации для транспорта TCP/IP на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3b33f-104">The following functions retrieve and modify configuration settings for the TCP/IP transport on the local computer.</span></span> <span data-ttu-id="3b33f-105">Следующий список категорий поможет определить, какая коллекция функций лучше всего подходит для данной задачи.</span><span class="sxs-lookup"><span data-stu-id="3b33f-105">The following categorical listing can help determine which collection of functions is best suited for a given task.</span></span>

-   [<span data-ttu-id="3b33f-106">**жетнетворкконнективитихинт**</span><span class="sxs-lookup"><span data-stu-id="3b33f-106">**GetNetworkConnectivityHint**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhint)
-   [<span data-ttu-id="3b33f-107">**жетнетворкконнективитихинтфоринтерфаце**</span><span class="sxs-lookup"><span data-stu-id="3b33f-107">**GetNetworkConnectivityHintForInterface**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhintforinterface)
-   [<span data-ttu-id="3b33f-108">**нотифинетворкконнективитихинтчанже**</span><span class="sxs-lookup"><span data-stu-id="3b33f-108">**NotifyNetworkConnectivityHintChange**</span></span>](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange)

## <a name="adapter-management"></a><span data-ttu-id="3b33f-109">Управление адаптерами</span><span class="sxs-lookup"><span data-stu-id="3b33f-109">Adapter management</span></span>

-   [<span data-ttu-id="3b33f-110">**жетадаптериндекс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-110">**GetAdapterIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadapterindex)
-   [<span data-ttu-id="3b33f-111">**жетадаптерсаддрессес**</span><span class="sxs-lookup"><span data-stu-id="3b33f-111">**GetAdaptersAddresses**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)
-   [<span data-ttu-id="3b33f-112">**жетадаптерсинфо**</span><span class="sxs-lookup"><span data-stu-id="3b33f-112">**GetAdaptersInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)
-   [<span data-ttu-id="3b33f-113">**жетперадаптеринфо**</span><span class="sxs-lookup"><span data-stu-id="3b33f-113">**GetPerAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)
-   [<span data-ttu-id="3b33f-114">**жетунидиректионаладаптеринфо**</span><span class="sxs-lookup"><span data-stu-id="3b33f-114">**GetUniDirectionalAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

## <a name="address-resolution-protocol-arp-management"></a><span data-ttu-id="3b33f-115">Управление протоколом разрешения адресов (ARP)</span><span class="sxs-lookup"><span data-stu-id="3b33f-115">Address Resolution Protocol (ARP) management</span></span>

-   [<span data-ttu-id="3b33f-116">**креатеипнетентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-116">**CreateIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipnetentry)
-   [<span data-ttu-id="3b33f-117">**креатепроксярпентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-117">**CreateProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createproxyarpentry)
-   [<span data-ttu-id="3b33f-118">**делетеипнетентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-118">**DeleteIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipnetentry)
-   [<span data-ttu-id="3b33f-119">**делетепроксярпентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-119">**DeleteProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)
-   [<span data-ttu-id="3b33f-120">**флушипнеттабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-120">**FlushIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-flushipnettable)
-   [<span data-ttu-id="3b33f-121">**жетипнеттабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-121">**GetIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipnettable)
-   [<span data-ttu-id="3b33f-122">**сендарп**</span><span class="sxs-lookup"><span data-stu-id="3b33f-122">**SendARP**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-sendarp)
-   [<span data-ttu-id="3b33f-123">**сетипнетентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-123">**SetIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipnetentry)

## <a name="interface-conversion"></a><span data-ttu-id="3b33f-124">Преобразование интерфейса</span><span class="sxs-lookup"><span data-stu-id="3b33f-124">Interface conversion</span></span>

-   [<span data-ttu-id="3b33f-125">**конвертинтерфацеалиастолуид**</span><span class="sxs-lookup"><span data-stu-id="3b33f-125">**ConvertInterfaceAliasToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [<span data-ttu-id="3b33f-126">**конвертинтерфацегуидтолуид**</span><span class="sxs-lookup"><span data-stu-id="3b33f-126">**ConvertInterfaceGuidToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [<span data-ttu-id="3b33f-127">**конвертинтерфацеиндекстолуид**</span><span class="sxs-lookup"><span data-stu-id="3b33f-127">**ConvertInterfaceIndexToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [<span data-ttu-id="3b33f-128">**конвертинтерфацелуидтоалиас**</span><span class="sxs-lookup"><span data-stu-id="3b33f-128">**ConvertInterfaceLuidToAlias**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoalias)
-   [<span data-ttu-id="3b33f-129">**конвертинтерфацелуидтогуид**</span><span class="sxs-lookup"><span data-stu-id="3b33f-129">**ConvertInterfaceLuidToGuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [<span data-ttu-id="3b33f-130">**конвертинтерфацелуидтоиндекс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-130">**ConvertInterfaceLuidToIndex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [<span data-ttu-id="3b33f-131">**конвертинтерфацелуидтонамеа**</span><span class="sxs-lookup"><span data-stu-id="3b33f-131">**ConvertInterfaceLuidToNameA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [<span data-ttu-id="3b33f-132">**конвертинтерфацелуидтонамев**</span><span class="sxs-lookup"><span data-stu-id="3b33f-132">**ConvertInterfaceLuidToNameW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [<span data-ttu-id="3b33f-133">**конвертинтерфаценаметолуида**</span><span class="sxs-lookup"><span data-stu-id="3b33f-133">**ConvertInterfaceNameToLuidA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [<span data-ttu-id="3b33f-134">**конвертинтерфаценаметолуидв**</span><span class="sxs-lookup"><span data-stu-id="3b33f-134">**ConvertInterfaceNameToLuidW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [<span data-ttu-id="3b33f-135">**Если \_ индекстонаме**</span><span class="sxs-lookup"><span data-stu-id="3b33f-135">**if\_indextoname**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_indextoname)
-   [<span data-ttu-id="3b33f-136">**Если \_ наметоиндекс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-136">**if\_nametoindex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_nametoindex)

## <a name="interface-management"></a><span data-ttu-id="3b33f-137">Управление интерфейсом</span><span class="sxs-lookup"><span data-stu-id="3b33f-137">Interface management</span></span>

-   [<span data-ttu-id="3b33f-138">**фриинтерфацеднссеттингс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-138">**FreeInterfaceDnsSettings**</span></span>](/windows/win32/api/netioapi/nf-netioapi-freeinterfacednssettings)
-   [<span data-ttu-id="3b33f-139">**жетфриендлифиндекс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-139">**GetFriendlyIfIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)
-   [<span data-ttu-id="3b33f-140">**жетифентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-140">**GetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getifentry)
-   [<span data-ttu-id="3b33f-141">**GetIfEntry2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-141">**GetIfEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2)
-   [<span data-ttu-id="3b33f-142">**GetIfEntry2Ex**</span><span class="sxs-lookup"><span data-stu-id="3b33f-142">**GetIfEntry2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2ex)
-   [<span data-ttu-id="3b33f-143">**жетифстакктабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-143">**GetIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifstacktable)
-   [<span data-ttu-id="3b33f-144">**жетифтабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-144">**GetIfTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getiftable)
-   [<span data-ttu-id="3b33f-145">**GetIfTable2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-145">**GetIfTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2)
-   [<span data-ttu-id="3b33f-146">**GetIfTable2Ex**</span><span class="sxs-lookup"><span data-stu-id="3b33f-146">**GetIfTable2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2ex)
-   [<span data-ttu-id="3b33f-147">**жетинтерфацеднссеттингс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-147">**GetInterfaceDnsSettings**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getinterfacednssettings)
-   [<span data-ttu-id="3b33f-148">**жетинтерфацеинфо**</span><span class="sxs-lookup"><span data-stu-id="3b33f-148">**GetInterfaceInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)
-   [<span data-ttu-id="3b33f-149">**жетинвертедифстакктабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-149">**GetInvertedIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [<span data-ttu-id="3b33f-150">**жетипинтерфацеентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-150">**GetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [<span data-ttu-id="3b33f-151">**жетипинтерфацетабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-151">**GetIpInterfaceTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [<span data-ttu-id="3b33f-152">**жетнумберофинтерфацес**</span><span class="sxs-lookup"><span data-stu-id="3b33f-152">**GetNumberOfInterfaces**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)
-   [<span data-ttu-id="3b33f-153">**инитиализеипинтерфацеентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-153">**InitializeIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [<span data-ttu-id="3b33f-154">**сетифентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-154">**SetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setifentry)
-   [<span data-ttu-id="3b33f-155">**сетинтерфацеднссеттингс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-155">**SetInterfaceDnsSettings**</span></span>](/windows/win32/api/netioapi/nf-netioapi-setinterfacednssettings)
-   [<span data-ttu-id="3b33f-156">**сетипинтерфацеентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-156">**SetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipinterfaceentry)

## <a name="internet-protocol-ip-and-internet-control-message-protocol-icmp"></a><span data-ttu-id="3b33f-157">Протокол Интернета (IP) и Протокол управляющих сообщений Интернета (ICMP)</span><span class="sxs-lookup"><span data-stu-id="3b33f-157">Internet Protocol (IP) and Internet Control Message Protocol (ICMP)</span></span>

-   [<span data-ttu-id="3b33f-158">**жетикмпстатистикс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-158">**GetIcmpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-geticmpstatistics)
-   [<span data-ttu-id="3b33f-159">**жетипстатистикс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-159">**GetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipstatistics)
-   [<span data-ttu-id="3b33f-160">**Icmp6CreateFile**</span><span class="sxs-lookup"><span data-stu-id="3b33f-160">**Icmp6CreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6createfile)
-   [<span data-ttu-id="3b33f-161">**Icmp6ParseReplies**</span><span class="sxs-lookup"><span data-stu-id="3b33f-161">**Icmp6ParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6parsereplies)
-   [<span data-ttu-id="3b33f-162">**Icmp6SendEcho2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-162">**Icmp6SendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6sendecho2)
-   [<span data-ttu-id="3b33f-163">**икмпклосехандле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-163">**IcmpCloseHandle**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpclosehandle)
-   [<span data-ttu-id="3b33f-164">**икмпкреатефиле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-164">**IcmpCreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpcreatefile)
-   [<span data-ttu-id="3b33f-165">**икмппарсереплиес**</span><span class="sxs-lookup"><span data-stu-id="3b33f-165">**IcmpParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpparsereplies)
-   [<span data-ttu-id="3b33f-166">**икмпсендечо**</span><span class="sxs-lookup"><span data-stu-id="3b33f-166">**IcmpSendEcho**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho)
-   [<span data-ttu-id="3b33f-167">**IcmpSendEcho2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-167">**IcmpSendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2)
-   [<span data-ttu-id="3b33f-168">**IcmpSendEcho2Ex**</span><span class="sxs-lookup"><span data-stu-id="3b33f-168">**IcmpSendEcho2Ex**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)
-   [<span data-ttu-id="3b33f-169">**сетипттл**</span><span class="sxs-lookup"><span data-stu-id="3b33f-169">**SetIpTTL**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipttl)

## <a name="ip-address-management"></a><span data-ttu-id="3b33f-170">Управление IP-адресами</span><span class="sxs-lookup"><span data-stu-id="3b33f-170">IP address management</span></span>

-   [<span data-ttu-id="3b33f-171">**аддипаддресс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-171">**AddIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-addipaddress)
-   [<span data-ttu-id="3b33f-172">**креатеаникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-172">**CreateAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [<span data-ttu-id="3b33f-173">**креатеуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-173">**CreateUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [<span data-ttu-id="3b33f-174">**делетеипаддресс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-174">**DeleteIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipaddress)
-   [<span data-ttu-id="3b33f-175">**делетеаникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-175">**DeleteAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [<span data-ttu-id="3b33f-176">**делетеуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-176">**DeleteUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [<span data-ttu-id="3b33f-177">**жетаникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-177">**GetAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [<span data-ttu-id="3b33f-178">**жетаникастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-178">**GetAnycastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [<span data-ttu-id="3b33f-179">**жетипаддртабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-179">**GetIpAddrTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipaddrtable)
-   [<span data-ttu-id="3b33f-180">**жетмултикастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-180">**GetMulticastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [<span data-ttu-id="3b33f-181">**жетмултикастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-181">**GetMulticastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [<span data-ttu-id="3b33f-182">**жетуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-182">**GetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [<span data-ttu-id="3b33f-183">**жетуникастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-183">**GetUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [<span data-ttu-id="3b33f-184">**инитиализеуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-184">**InitializeUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [<span data-ttu-id="3b33f-185">**ипрелеасеаддресс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-185">**IpReleaseAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)
-   [<span data-ttu-id="3b33f-186">**ипреневаддресс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-186">**IpRenewAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-iprenewaddress)
-   [<span data-ttu-id="3b33f-187">**нотифистаблеуникастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-187">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [<span data-ttu-id="3b33f-188">**сетуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-188">**SetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setunicastipaddressentry)

## <a name="ip-address-string-conversion"></a><span data-ttu-id="3b33f-189">Преобразование строки IP-адреса</span><span class="sxs-lookup"><span data-stu-id="3b33f-189">IP address string conversion</span></span>

-   [<span data-ttu-id="3b33f-190">**RtlIpv4AddressToString**</span><span class="sxs-lookup"><span data-stu-id="3b33f-190">**RtlIpv4AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [<span data-ttu-id="3b33f-191">**RtlIpv4AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="3b33f-191">**RtlIpv4AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [<span data-ttu-id="3b33f-192">**RtlIpv4StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="3b33f-192">**RtlIpv4StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [<span data-ttu-id="3b33f-193">**RtlIpv4StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="3b33f-193">**RtlIpv4StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [<span data-ttu-id="3b33f-194">**RtlIpv6AddressToString**</span><span class="sxs-lookup"><span data-stu-id="3b33f-194">**RtlIpv6AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [<span data-ttu-id="3b33f-195">**RtlIpv6AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="3b33f-195">**RtlIpv6AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [<span data-ttu-id="3b33f-196">**RtlIpv6StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="3b33f-196">**RtlIpv6StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [<span data-ttu-id="3b33f-197">**RtlIpv6StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="3b33f-197">**RtlIpv6StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

## <a name="ip-neighbor-address-management"></a><span data-ttu-id="3b33f-198">Управление адресами соседей IP</span><span class="sxs-lookup"><span data-stu-id="3b33f-198">IP neighbor address management</span></span>

-   [<span data-ttu-id="3b33f-199">**CreateIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-199">**CreateIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipnetentry2)
-   [<span data-ttu-id="3b33f-200">**DeleteIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-200">**DeleteIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [<span data-ttu-id="3b33f-201">**FlushIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-201">**FlushIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushipnettable2)
-   [<span data-ttu-id="3b33f-202">**GetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-202">**GetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnetentry2)
-   [<span data-ttu-id="3b33f-203">**GetIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-203">**GetIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnettable2)
-   [<span data-ttu-id="3b33f-204">**ResolveIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-204">**ResolveIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [<span data-ttu-id="3b33f-205">**ресолвенеигхбор**</span><span class="sxs-lookup"><span data-stu-id="3b33f-205">**ResolveNeighbor**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [<span data-ttu-id="3b33f-206">**SetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-206">**SetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipnetentry2)

## <a name="ip-path-management"></a><span data-ttu-id="3b33f-207">Управление IP-путями</span><span class="sxs-lookup"><span data-stu-id="3b33f-207">IP path management</span></span>

-   [<span data-ttu-id="3b33f-208">**флушиппастабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-208">**FlushIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushippathtable)
-   [<span data-ttu-id="3b33f-209">**жетиппасентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-209">**GetIpPathEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathentry)
-   [<span data-ttu-id="3b33f-210">**жетиппастабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-210">**GetIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathtable)

## <a name="ip-route-management"></a><span data-ttu-id="3b33f-211">Управление IP-маршрутами</span><span class="sxs-lookup"><span data-stu-id="3b33f-211">IP route management</span></span>

-   [<span data-ttu-id="3b33f-212">**креатеипфорвардентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-212">**CreateIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipforwardentry)
-   [<span data-ttu-id="3b33f-213">**CreateIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-213">**CreateIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [<span data-ttu-id="3b33f-214">**делетеипфорвардентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-214">**DeleteIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)
-   [<span data-ttu-id="3b33f-215">**DeleteIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-215">**DeleteIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [<span data-ttu-id="3b33f-216">**енаблераутер**</span><span class="sxs-lookup"><span data-stu-id="3b33f-216">**EnableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-enablerouter)
-   [<span data-ttu-id="3b33f-217">**жетбестинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="3b33f-217">**GetBestInterface**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterface)
-   [<span data-ttu-id="3b33f-218">**жетбестинтерфацеекс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-218">**GetBestInterfaceEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterfaceex)
-   [<span data-ttu-id="3b33f-219">**жетбестрауте**</span><span class="sxs-lookup"><span data-stu-id="3b33f-219">**GetBestRoute**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestroute)
-   [<span data-ttu-id="3b33f-220">**GetBestRoute2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-220">**GetBestRoute2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getbestroute2)
-   [<span data-ttu-id="3b33f-221">**GetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-221">**GetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [<span data-ttu-id="3b33f-222">**жетипфорвардтабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-222">**GetIpForwardTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipforwardtable)
-   [<span data-ttu-id="3b33f-223">**GetIpForwardTable2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-223">**GetIpForwardTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [<span data-ttu-id="3b33f-224">**жетрттандхопкаунт**</span><span class="sxs-lookup"><span data-stu-id="3b33f-224">**GetRTTAndHopCount**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getrttandhopcount)
-   [<span data-ttu-id="3b33f-225">**инитиализеипфорвардентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-225">**InitializeIpForwardEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [<span data-ttu-id="3b33f-226">**сетипфорвардентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-226">**SetIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipforwardentry)
-   [<span data-ttu-id="3b33f-227">**SetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-227">**SetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [<span data-ttu-id="3b33f-228">**сетипстатистикс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-228">**SetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatistics)
-   [<span data-ttu-id="3b33f-229">**сетипстатистиксекс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-229">**SetIpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)
-   [<span data-ttu-id="3b33f-230">**уненаблераутер**</span><span class="sxs-lookup"><span data-stu-id="3b33f-230">**UnenableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-unenablerouter)

## <a name="ip-table-memory-management"></a><span data-ttu-id="3b33f-231">Управление памятью таблицы IP</span><span class="sxs-lookup"><span data-stu-id="3b33f-231">IP table memory management</span></span>

-   [<span data-ttu-id="3b33f-232">**фримибтабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-232">**FreeMibTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-freemibtable)

## <a name="ip-utility"></a><span data-ttu-id="3b33f-233">Служебная программа IP</span><span class="sxs-lookup"><span data-stu-id="3b33f-233">IP utility</span></span>

-   [<span data-ttu-id="3b33f-234">**ConvertIpv4MaskToLength**</span><span class="sxs-lookup"><span data-stu-id="3b33f-234">**ConvertIpv4MaskToLength**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [<span data-ttu-id="3b33f-235">**ConvertLengthToIpv4Mask**</span><span class="sxs-lookup"><span data-stu-id="3b33f-235">**ConvertLengthToIpv4Mask**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [<span data-ttu-id="3b33f-236">**креатесортедаддресспаирс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-236">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [<span data-ttu-id="3b33f-237">**парсенетворкстринг**</span><span class="sxs-lookup"><span data-stu-id="3b33f-237">**ParseNetworkString**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

## <a name="network-configuration"></a><span data-ttu-id="3b33f-238">Сетевая конфигурация</span><span class="sxs-lookup"><span data-stu-id="3b33f-238">Network configuration</span></span>

-   [<span data-ttu-id="3b33f-239">**жетнетворкпарамс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-239">**GetNetworkParams**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnetworkparams)

## <a name="notification"></a><span data-ttu-id="3b33f-240">Уведомление</span><span class="sxs-lookup"><span data-stu-id="3b33f-240">Notification</span></span>

-   [<span data-ttu-id="3b33f-241">**CancelMibChangeNotify2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-241">**CancelMibChangeNotify2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [<span data-ttu-id="3b33f-242">**нотифяддрчанже**</span><span class="sxs-lookup"><span data-stu-id="3b33f-242">**NotifyAddrChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyaddrchange)
-   [<span data-ttu-id="3b33f-243">**нотифипинтерфацечанже**</span><span class="sxs-lookup"><span data-stu-id="3b33f-243">**NotifyIpInterfaceChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [<span data-ttu-id="3b33f-244">**нотифираутечанже**</span><span class="sxs-lookup"><span data-stu-id="3b33f-244">**NotifyRouteChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyroutechange)
-   [<span data-ttu-id="3b33f-245">**NotifyRouteChange2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-245">**NotifyRouteChange2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [<span data-ttu-id="3b33f-246">**нотифюникастипаддрессчанже**</span><span class="sxs-lookup"><span data-stu-id="3b33f-246">**NotifyUnicastIpAddressChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

## <a name="packet-timestamping"></a><span data-ttu-id="3b33f-247">Метки времени пакетов</span><span class="sxs-lookup"><span data-stu-id="3b33f-247">Packet timestamping</span></span>

-   [<span data-ttu-id="3b33f-248">**каптуреинтерфацехардварекросстиместамп**</span><span class="sxs-lookup"><span data-stu-id="3b33f-248">**CaptureInterfaceHardwareCrossTimestamp**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp)
-   [<span data-ttu-id="3b33f-249">**жетинтерфацеактиветиместампкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="3b33f-249">**GetInterfaceActiveTimestampCapabilities**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities)
-   [<span data-ttu-id="3b33f-250">**жетинтерфацесуппортедтиместампкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="3b33f-250">**GetInterfaceSupportedTimestampCapabilities**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities)
-   [<span data-ttu-id="3b33f-251">**регистеринтерфацетиместампконфигчанже**</span><span class="sxs-lookup"><span data-stu-id="3b33f-251">**RegisterInterfaceTimestampConfigChange**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange)
-   [<span data-ttu-id="3b33f-252">**унрегистеринтерфацетиместампконфигчанже**</span><span class="sxs-lookup"><span data-stu-id="3b33f-252">**UnregisterInterfaceTimestampConfigChange**</span></span>](/windows/win32/api/iphlpapi/unregisterinterfacetimestampconfigchange)

## <a name="persistent-port-reservation"></a><span data-ttu-id="3b33f-253">Постоянное резервирование портов</span><span class="sxs-lookup"><span data-stu-id="3b33f-253">Persistent port reservation</span></span>

-   [<span data-ttu-id="3b33f-254">**креатеперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="3b33f-254">**CreatePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [<span data-ttu-id="3b33f-255">**креатеперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="3b33f-255">**CreatePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [<span data-ttu-id="3b33f-256">**делетеперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="3b33f-256">**DeletePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [<span data-ttu-id="3b33f-257">**делетеперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="3b33f-257">**DeletePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [<span data-ttu-id="3b33f-258">**лукупперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="3b33f-258">**LookupPersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [<span data-ttu-id="3b33f-259">**лукупперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="3b33f-259">**LookupPersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="security-health"></a><span data-ttu-id="3b33f-260">Работоспособность системы безопасности</span><span class="sxs-lookup"><span data-stu-id="3b33f-260">Security health</span></span>

-   <span data-ttu-id="3b33f-261">[**канцелсекуритихеалсчанженотифи**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b33f-261">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span></span>
-   <span data-ttu-id="3b33f-262">[**нотифисекуритихеалсчанже**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b33f-262">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span></span>

<span data-ttu-id="3b33f-263">эти функции определяются только на Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3b33f-263">These functions are defined only on Windows Server 2003.</span></span>

> [!Note]  
> <span data-ttu-id="3b33f-264">эти функции недоступны в Windows Vista и на Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3b33f-264">These functions are not available on Windows Vista, nor on Windows Server 2008.</span></span>

## <a name="teredo-ipv6-client-management"></a><span data-ttu-id="3b33f-265">Управление клиентом Teredo IPv6</span><span class="sxs-lookup"><span data-stu-id="3b33f-265">Teredo IPv6 client management</span></span>

-   [<span data-ttu-id="3b33f-266">**жеттередопорт**</span><span class="sxs-lookup"><span data-stu-id="3b33f-266">**GetTeredoPort**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="3b33f-267">**нотифитередопортчанже**</span><span class="sxs-lookup"><span data-stu-id="3b33f-267">**NotifyTeredoPortChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="3b33f-268">**нотифистаблеуникастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-268">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

## <a name="transmission-control-protocol-tcp-and-user-datagram-protocol-udp"></a><span data-ttu-id="3b33f-269">Протокол TCP и протокол UDP.</span><span class="sxs-lookup"><span data-stu-id="3b33f-269">Transmission Control Protocol (TCP) and User Datagram Protocol (UDP)</span></span>

-   [<span data-ttu-id="3b33f-270">**жетекстендедткптабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-270">**GetExtendedTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedtcptable)
-   [<span data-ttu-id="3b33f-271">**жетекстендедудптабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-271">**GetExtendedUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedudptable)
-   [<span data-ttu-id="3b33f-272">**GetOwnerModuleFromTcp6Entry**</span><span class="sxs-lookup"><span data-stu-id="3b33f-272">**GetOwnerModuleFromTcp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [<span data-ttu-id="3b33f-273">**жетовнермодулефромткпентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-273">**GetOwnerModuleFromTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [<span data-ttu-id="3b33f-274">**GetOwnerModuleFromUdp6Entry**</span><span class="sxs-lookup"><span data-stu-id="3b33f-274">**GetOwnerModuleFromUdp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)
-   [<span data-ttu-id="3b33f-275">**жетовнермодулефромудпентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-275">**GetOwnerModuleFromUdpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [<span data-ttu-id="3b33f-276">**GetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="3b33f-276">**GetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [<span data-ttu-id="3b33f-277">**жетперткпконнектионестатс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-277">**GetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [<span data-ttu-id="3b33f-278">**жетткпстатистикс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-278">**GetTcpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)
-   [<span data-ttu-id="3b33f-279">**жетткпстатистиксекс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-279">**GetTcpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex)
-   [<span data-ttu-id="3b33f-280">**GetTcpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-280">**GetTcpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex2)
-   [<span data-ttu-id="3b33f-281">**GetTcp6Table**</span><span class="sxs-lookup"><span data-stu-id="3b33f-281">**GetTcp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [<span data-ttu-id="3b33f-282">**GetTcp6Table2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-282">**GetTcp6Table2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [<span data-ttu-id="3b33f-283">**жетткптабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-283">**GetTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable)
-   [<span data-ttu-id="3b33f-284">**GetTcpTable2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-284">**GetTcpTable2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [<span data-ttu-id="3b33f-285">**SetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="3b33f-285">**SetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [<span data-ttu-id="3b33f-286">**сетперткпконнектионестатс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-286">**SetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)
-   [<span data-ttu-id="3b33f-287">**сетткпентри**</span><span class="sxs-lookup"><span data-stu-id="3b33f-287">**SetTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-settcpentry)
-   [<span data-ttu-id="3b33f-288">**GetUdp6Table**</span><span class="sxs-lookup"><span data-stu-id="3b33f-288">**GetUdp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudp6table)
-   [<span data-ttu-id="3b33f-289">**жетудпстатистикс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-289">**GetUdpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatistics)
-   [<span data-ttu-id="3b33f-290">**жетудпстатистиксекс**</span><span class="sxs-lookup"><span data-stu-id="3b33f-290">**GetUdpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex)
-   [<span data-ttu-id="3b33f-291">**GetUdpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="3b33f-291">**GetUdpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex2)
-   [<span data-ttu-id="3b33f-292">**жетудптабле**</span><span class="sxs-lookup"><span data-stu-id="3b33f-292">**GetUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudptable)

## <a name="deprecated-apis"></a><span data-ttu-id="3b33f-293">Устаревшие интерфейсы API</span><span class="sxs-lookup"><span data-stu-id="3b33f-293">Deprecated APIs</span></span>

> [!Note]  
> <span data-ttu-id="3b33f-294">Эти функции являются устаревшими и не поддерживаются корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3b33f-294">These functions are deprecated, and are not supported by Microsoft.</span></span>

-   [<span data-ttu-id="3b33f-295">**аллокатеанджетткпекстаблефромстакк**</span><span class="sxs-lookup"><span data-stu-id="3b33f-295">**AllocateAndGetTcpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgettcpextablefromstack)
-   [<span data-ttu-id="3b33f-296">**аллокатеанджетудпекстаблефромстакк**</span><span class="sxs-lookup"><span data-stu-id="3b33f-296">**AllocateAndGetUdpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgetudpextablefromstack)
