---
description: Следующие функции извлекают и изменяют параметры конфигурации для транспорта TCP/IP на локальном компьютере.
ms.assetid: 5f562470-f3e8-4305-a015-3a84cd09a1eb
title: Функции IP Helper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c8bff21f41c04bb5aecf505b251fbbe2f8bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818993"
---
# <a name="ip-helper-functions"></a><span data-ttu-id="78414-103">Вспомогательные функции IP</span><span class="sxs-lookup"><span data-stu-id="78414-103">IP Helper functions</span></span>

<span data-ttu-id="78414-104">Следующие функции извлекают и изменяют параметры конфигурации для транспорта TCP/IP на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="78414-104">The following functions retrieve and modify configuration settings for the TCP/IP transport on the local computer.</span></span> <span data-ttu-id="78414-105">Следующий список категорий поможет определить, какая коллекция функций лучше всего подходит для данной задачи.</span><span class="sxs-lookup"><span data-stu-id="78414-105">The following categorical listing can help determine which collection of functions is best suited for a given task.</span></span>

-   [<span data-ttu-id="78414-106">**жетнетворкконнективитихинт**</span><span class="sxs-lookup"><span data-stu-id="78414-106">**GetNetworkConnectivityHint**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhint)
-   [<span data-ttu-id="78414-107">**жетнетворкконнективитихинтфоринтерфаце**</span><span class="sxs-lookup"><span data-stu-id="78414-107">**GetNetworkConnectivityHintForInterface**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhintforinterface)
-   [<span data-ttu-id="78414-108">**нотифинетворкконнективитихинтчанже**</span><span class="sxs-lookup"><span data-stu-id="78414-108">**NotifyNetworkConnectivityHintChange**</span></span>](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange)

## <a name="adapter-management"></a><span data-ttu-id="78414-109">Управление адаптерами</span><span class="sxs-lookup"><span data-stu-id="78414-109">Adapter management</span></span>

-   [<span data-ttu-id="78414-110">**жетадаптериндекс**</span><span class="sxs-lookup"><span data-stu-id="78414-110">**GetAdapterIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadapterindex)
-   [<span data-ttu-id="78414-111">**жетадаптерсаддрессес**</span><span class="sxs-lookup"><span data-stu-id="78414-111">**GetAdaptersAddresses**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)
-   [<span data-ttu-id="78414-112">**жетадаптерсинфо**</span><span class="sxs-lookup"><span data-stu-id="78414-112">**GetAdaptersInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)
-   [<span data-ttu-id="78414-113">**жетперадаптеринфо**</span><span class="sxs-lookup"><span data-stu-id="78414-113">**GetPerAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)
-   [<span data-ttu-id="78414-114">**жетунидиректионаладаптеринфо**</span><span class="sxs-lookup"><span data-stu-id="78414-114">**GetUniDirectionalAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

## <a name="address-resolution-protocol-arp-management"></a><span data-ttu-id="78414-115">Управление протоколом разрешения адресов (ARP)</span><span class="sxs-lookup"><span data-stu-id="78414-115">Address Resolution Protocol (ARP) management</span></span>

-   [<span data-ttu-id="78414-116">**креатеипнетентри**</span><span class="sxs-lookup"><span data-stu-id="78414-116">**CreateIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipnetentry)
-   [<span data-ttu-id="78414-117">**креатепроксярпентри**</span><span class="sxs-lookup"><span data-stu-id="78414-117">**CreateProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createproxyarpentry)
-   [<span data-ttu-id="78414-118">**делетеипнетентри**</span><span class="sxs-lookup"><span data-stu-id="78414-118">**DeleteIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipnetentry)
-   [<span data-ttu-id="78414-119">**делетепроксярпентри**</span><span class="sxs-lookup"><span data-stu-id="78414-119">**DeleteProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)
-   [<span data-ttu-id="78414-120">**флушипнеттабле**</span><span class="sxs-lookup"><span data-stu-id="78414-120">**FlushIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-flushipnettable)
-   [<span data-ttu-id="78414-121">**жетипнеттабле**</span><span class="sxs-lookup"><span data-stu-id="78414-121">**GetIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipnettable)
-   [<span data-ttu-id="78414-122">**сендарп**</span><span class="sxs-lookup"><span data-stu-id="78414-122">**SendARP**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-sendarp)
-   [<span data-ttu-id="78414-123">**сетипнетентри**</span><span class="sxs-lookup"><span data-stu-id="78414-123">**SetIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipnetentry)

## <a name="interface-conversion"></a><span data-ttu-id="78414-124">Преобразование интерфейса</span><span class="sxs-lookup"><span data-stu-id="78414-124">Interface conversion</span></span>

-   [<span data-ttu-id="78414-125">**конвертинтерфацеалиастолуид**</span><span class="sxs-lookup"><span data-stu-id="78414-125">**ConvertInterfaceAliasToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [<span data-ttu-id="78414-126">**конвертинтерфацегуидтолуид**</span><span class="sxs-lookup"><span data-stu-id="78414-126">**ConvertInterfaceGuidToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [<span data-ttu-id="78414-127">**конвертинтерфацеиндекстолуид**</span><span class="sxs-lookup"><span data-stu-id="78414-127">**ConvertInterfaceIndexToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [<span data-ttu-id="78414-128">**конвертинтерфацелуидтоалиас**</span><span class="sxs-lookup"><span data-stu-id="78414-128">**ConvertInterfaceLuidToAlias**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoalias)
-   [<span data-ttu-id="78414-129">**конвертинтерфацелуидтогуид**</span><span class="sxs-lookup"><span data-stu-id="78414-129">**ConvertInterfaceLuidToGuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [<span data-ttu-id="78414-130">**конвертинтерфацелуидтоиндекс**</span><span class="sxs-lookup"><span data-stu-id="78414-130">**ConvertInterfaceLuidToIndex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [<span data-ttu-id="78414-131">**конвертинтерфацелуидтонамеа**</span><span class="sxs-lookup"><span data-stu-id="78414-131">**ConvertInterfaceLuidToNameA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [<span data-ttu-id="78414-132">**конвертинтерфацелуидтонамев**</span><span class="sxs-lookup"><span data-stu-id="78414-132">**ConvertInterfaceLuidToNameW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [<span data-ttu-id="78414-133">**конвертинтерфаценаметолуида**</span><span class="sxs-lookup"><span data-stu-id="78414-133">**ConvertInterfaceNameToLuidA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [<span data-ttu-id="78414-134">**конвертинтерфаценаметолуидв**</span><span class="sxs-lookup"><span data-stu-id="78414-134">**ConvertInterfaceNameToLuidW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [<span data-ttu-id="78414-135">**Если \_ индекстонаме**</span><span class="sxs-lookup"><span data-stu-id="78414-135">**if\_indextoname**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_indextoname)
-   [<span data-ttu-id="78414-136">**Если \_ наметоиндекс**</span><span class="sxs-lookup"><span data-stu-id="78414-136">**if\_nametoindex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_nametoindex)

## <a name="interface-management"></a><span data-ttu-id="78414-137">Управление интерфейсом</span><span class="sxs-lookup"><span data-stu-id="78414-137">Interface management</span></span>

-   [<span data-ttu-id="78414-138">**жетфриендлифиндекс**</span><span class="sxs-lookup"><span data-stu-id="78414-138">**GetFriendlyIfIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)
-   [<span data-ttu-id="78414-139">**жетифентри**</span><span class="sxs-lookup"><span data-stu-id="78414-139">**GetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getifentry)
-   [<span data-ttu-id="78414-140">**GetIfEntry2**</span><span class="sxs-lookup"><span data-stu-id="78414-140">**GetIfEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2)
-   [<span data-ttu-id="78414-141">**GetIfEntry2Ex**</span><span class="sxs-lookup"><span data-stu-id="78414-141">**GetIfEntry2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2ex)
-   [<span data-ttu-id="78414-142">**жетифстакктабле**</span><span class="sxs-lookup"><span data-stu-id="78414-142">**GetIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifstacktable)
-   [<span data-ttu-id="78414-143">**жетифтабле**</span><span class="sxs-lookup"><span data-stu-id="78414-143">**GetIfTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getiftable)
-   [<span data-ttu-id="78414-144">**GetIfTable2**</span><span class="sxs-lookup"><span data-stu-id="78414-144">**GetIfTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2)
-   [<span data-ttu-id="78414-145">**GetIfTable2Ex**</span><span class="sxs-lookup"><span data-stu-id="78414-145">**GetIfTable2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2ex)
-   [<span data-ttu-id="78414-146">**жетинтерфацеинфо**</span><span class="sxs-lookup"><span data-stu-id="78414-146">**GetInterfaceInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)
-   [<span data-ttu-id="78414-147">**жетинвертедифстакктабле**</span><span class="sxs-lookup"><span data-stu-id="78414-147">**GetInvertedIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [<span data-ttu-id="78414-148">**жетипинтерфацеентри**</span><span class="sxs-lookup"><span data-stu-id="78414-148">**GetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [<span data-ttu-id="78414-149">**жетипинтерфацетабле**</span><span class="sxs-lookup"><span data-stu-id="78414-149">**GetIpInterfaceTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [<span data-ttu-id="78414-150">**жетнумберофинтерфацес**</span><span class="sxs-lookup"><span data-stu-id="78414-150">**GetNumberOfInterfaces**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)
-   [<span data-ttu-id="78414-151">**инитиализеипинтерфацеентри**</span><span class="sxs-lookup"><span data-stu-id="78414-151">**InitializeIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [<span data-ttu-id="78414-152">**сетифентри**</span><span class="sxs-lookup"><span data-stu-id="78414-152">**SetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setifentry)
-   [<span data-ttu-id="78414-153">**сетипинтерфацеентри**</span><span class="sxs-lookup"><span data-stu-id="78414-153">**SetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipinterfaceentry)

## <a name="internet-protocol-ip-and-internet-control-message-protocol-icmp"></a><span data-ttu-id="78414-154">Протокол Интернета (IP) и Протокол управляющих сообщений Интернета (ICMP)</span><span class="sxs-lookup"><span data-stu-id="78414-154">Internet Protocol (IP) and Internet Control Message Protocol (ICMP)</span></span>

-   [<span data-ttu-id="78414-155">**жетикмпстатистикс**</span><span class="sxs-lookup"><span data-stu-id="78414-155">**GetIcmpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-geticmpstatistics)
-   [<span data-ttu-id="78414-156">**жетипстатистикс**</span><span class="sxs-lookup"><span data-stu-id="78414-156">**GetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipstatistics)
-   [<span data-ttu-id="78414-157">**Icmp6CreateFile**</span><span class="sxs-lookup"><span data-stu-id="78414-157">**Icmp6CreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6createfile)
-   [<span data-ttu-id="78414-158">**Icmp6ParseReplies**</span><span class="sxs-lookup"><span data-stu-id="78414-158">**Icmp6ParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6parsereplies)
-   [<span data-ttu-id="78414-159">**Icmp6SendEcho2**</span><span class="sxs-lookup"><span data-stu-id="78414-159">**Icmp6SendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6sendecho2)
-   [<span data-ttu-id="78414-160">**икмпклосехандле**</span><span class="sxs-lookup"><span data-stu-id="78414-160">**IcmpCloseHandle**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpclosehandle)
-   [<span data-ttu-id="78414-161">**икмпкреатефиле**</span><span class="sxs-lookup"><span data-stu-id="78414-161">**IcmpCreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpcreatefile)
-   [<span data-ttu-id="78414-162">**икмппарсереплиес**</span><span class="sxs-lookup"><span data-stu-id="78414-162">**IcmpParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpparsereplies)
-   [<span data-ttu-id="78414-163">**икмпсендечо**</span><span class="sxs-lookup"><span data-stu-id="78414-163">**IcmpSendEcho**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho)
-   [<span data-ttu-id="78414-164">**IcmpSendEcho2**</span><span class="sxs-lookup"><span data-stu-id="78414-164">**IcmpSendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2)
-   [<span data-ttu-id="78414-165">**IcmpSendEcho2Ex**</span><span class="sxs-lookup"><span data-stu-id="78414-165">**IcmpSendEcho2Ex**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)
-   [<span data-ttu-id="78414-166">**сетипттл**</span><span class="sxs-lookup"><span data-stu-id="78414-166">**SetIpTTL**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipttl)

## <a name="ip-address-management"></a><span data-ttu-id="78414-167">Управление IP-адресами</span><span class="sxs-lookup"><span data-stu-id="78414-167">IP address management</span></span>

-   [<span data-ttu-id="78414-168">**аддипаддресс**</span><span class="sxs-lookup"><span data-stu-id="78414-168">**AddIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-addipaddress)
-   [<span data-ttu-id="78414-169">**креатеаникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="78414-169">**CreateAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [<span data-ttu-id="78414-170">**креатеуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="78414-170">**CreateUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [<span data-ttu-id="78414-171">**делетеипаддресс**</span><span class="sxs-lookup"><span data-stu-id="78414-171">**DeleteIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipaddress)
-   [<span data-ttu-id="78414-172">**делетеаникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="78414-172">**DeleteAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [<span data-ttu-id="78414-173">**делетеуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="78414-173">**DeleteUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [<span data-ttu-id="78414-174">**жетаникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="78414-174">**GetAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [<span data-ttu-id="78414-175">**жетаникастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="78414-175">**GetAnycastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [<span data-ttu-id="78414-176">**жетипаддртабле**</span><span class="sxs-lookup"><span data-stu-id="78414-176">**GetIpAddrTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipaddrtable)
-   [<span data-ttu-id="78414-177">**жетмултикастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="78414-177">**GetMulticastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [<span data-ttu-id="78414-178">**жетмултикастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="78414-178">**GetMulticastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [<span data-ttu-id="78414-179">**жетуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="78414-179">**GetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [<span data-ttu-id="78414-180">**жетуникастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="78414-180">**GetUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [<span data-ttu-id="78414-181">**инитиализеуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="78414-181">**InitializeUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [<span data-ttu-id="78414-182">**ипрелеасеаддресс**</span><span class="sxs-lookup"><span data-stu-id="78414-182">**IpReleaseAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)
-   [<span data-ttu-id="78414-183">**ипреневаддресс**</span><span class="sxs-lookup"><span data-stu-id="78414-183">**IpRenewAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-iprenewaddress)
-   [<span data-ttu-id="78414-184">**нотифистаблеуникастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="78414-184">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [<span data-ttu-id="78414-185">**сетуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="78414-185">**SetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setunicastipaddressentry)

## <a name="ip-address-string-conversion"></a><span data-ttu-id="78414-186">Преобразование строки IP-адреса</span><span class="sxs-lookup"><span data-stu-id="78414-186">IP address string conversion</span></span>

-   [<span data-ttu-id="78414-187">**RtlIpv4AddressToString**</span><span class="sxs-lookup"><span data-stu-id="78414-187">**RtlIpv4AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [<span data-ttu-id="78414-188">**RtlIpv4AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="78414-188">**RtlIpv4AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [<span data-ttu-id="78414-189">**RtlIpv4StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="78414-189">**RtlIpv4StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [<span data-ttu-id="78414-190">**RtlIpv4StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="78414-190">**RtlIpv4StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [<span data-ttu-id="78414-191">**RtlIpv6AddressToString**</span><span class="sxs-lookup"><span data-stu-id="78414-191">**RtlIpv6AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [<span data-ttu-id="78414-192">**RtlIpv6AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="78414-192">**RtlIpv6AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [<span data-ttu-id="78414-193">**RtlIpv6StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="78414-193">**RtlIpv6StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [<span data-ttu-id="78414-194">**RtlIpv6StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="78414-194">**RtlIpv6StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

## <a name="ip-neighbor-address-management"></a><span data-ttu-id="78414-195">Управление адресами соседей IP</span><span class="sxs-lookup"><span data-stu-id="78414-195">IP neighbor address management</span></span>

-   [<span data-ttu-id="78414-196">**CreateIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="78414-196">**CreateIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipnetentry2)
-   [<span data-ttu-id="78414-197">**DeleteIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="78414-197">**DeleteIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [<span data-ttu-id="78414-198">**FlushIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="78414-198">**FlushIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushipnettable2)
-   [<span data-ttu-id="78414-199">**GetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="78414-199">**GetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnetentry2)
-   [<span data-ttu-id="78414-200">**GetIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="78414-200">**GetIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnettable2)
-   [<span data-ttu-id="78414-201">**ResolveIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="78414-201">**ResolveIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [<span data-ttu-id="78414-202">**ресолвенеигхбор**</span><span class="sxs-lookup"><span data-stu-id="78414-202">**ResolveNeighbor**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [<span data-ttu-id="78414-203">**SetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="78414-203">**SetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipnetentry2)

## <a name="ip-path-management"></a><span data-ttu-id="78414-204">Управление IP-путями</span><span class="sxs-lookup"><span data-stu-id="78414-204">IP path management</span></span>

-   [<span data-ttu-id="78414-205">**флушиппастабле**</span><span class="sxs-lookup"><span data-stu-id="78414-205">**FlushIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushippathtable)
-   [<span data-ttu-id="78414-206">**жетиппасентри**</span><span class="sxs-lookup"><span data-stu-id="78414-206">**GetIpPathEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathentry)
-   [<span data-ttu-id="78414-207">**жетиппастабле**</span><span class="sxs-lookup"><span data-stu-id="78414-207">**GetIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathtable)

## <a name="ip-route-management"></a><span data-ttu-id="78414-208">Управление IP-маршрутами</span><span class="sxs-lookup"><span data-stu-id="78414-208">IP route management</span></span>

-   [<span data-ttu-id="78414-209">**креатеипфорвардентри**</span><span class="sxs-lookup"><span data-stu-id="78414-209">**CreateIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipforwardentry)
-   [<span data-ttu-id="78414-210">**CreateIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="78414-210">**CreateIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [<span data-ttu-id="78414-211">**делетеипфорвардентри**</span><span class="sxs-lookup"><span data-stu-id="78414-211">**DeleteIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)
-   [<span data-ttu-id="78414-212">**DeleteIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="78414-212">**DeleteIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [<span data-ttu-id="78414-213">**енаблераутер**</span><span class="sxs-lookup"><span data-stu-id="78414-213">**EnableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-enablerouter)
-   [<span data-ttu-id="78414-214">**жетбестинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="78414-214">**GetBestInterface**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterface)
-   [<span data-ttu-id="78414-215">**жетбестинтерфацеекс**</span><span class="sxs-lookup"><span data-stu-id="78414-215">**GetBestInterfaceEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterfaceex)
-   [<span data-ttu-id="78414-216">**жетбестрауте**</span><span class="sxs-lookup"><span data-stu-id="78414-216">**GetBestRoute**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestroute)
-   [<span data-ttu-id="78414-217">**GetBestRoute2**</span><span class="sxs-lookup"><span data-stu-id="78414-217">**GetBestRoute2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getbestroute2)
-   [<span data-ttu-id="78414-218">**GetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="78414-218">**GetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [<span data-ttu-id="78414-219">**жетипфорвардтабле**</span><span class="sxs-lookup"><span data-stu-id="78414-219">**GetIpForwardTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipforwardtable)
-   [<span data-ttu-id="78414-220">**GetIpForwardTable2**</span><span class="sxs-lookup"><span data-stu-id="78414-220">**GetIpForwardTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [<span data-ttu-id="78414-221">**жетрттандхопкаунт**</span><span class="sxs-lookup"><span data-stu-id="78414-221">**GetRTTAndHopCount**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getrttandhopcount)
-   [<span data-ttu-id="78414-222">**инитиализеипфорвардентри**</span><span class="sxs-lookup"><span data-stu-id="78414-222">**InitializeIpForwardEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [<span data-ttu-id="78414-223">**сетипфорвардентри**</span><span class="sxs-lookup"><span data-stu-id="78414-223">**SetIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipforwardentry)
-   [<span data-ttu-id="78414-224">**SetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="78414-224">**SetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [<span data-ttu-id="78414-225">**сетипстатистикс**</span><span class="sxs-lookup"><span data-stu-id="78414-225">**SetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatistics)
-   [<span data-ttu-id="78414-226">**сетипстатистиксекс**</span><span class="sxs-lookup"><span data-stu-id="78414-226">**SetIpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)
-   [<span data-ttu-id="78414-227">**уненаблераутер**</span><span class="sxs-lookup"><span data-stu-id="78414-227">**UnenableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-unenablerouter)

## <a name="ip-table-memory-management"></a><span data-ttu-id="78414-228">Управление памятью таблицы IP</span><span class="sxs-lookup"><span data-stu-id="78414-228">IP table memory management</span></span>

-   [<span data-ttu-id="78414-229">**фримибтабле**</span><span class="sxs-lookup"><span data-stu-id="78414-229">**FreeMibTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-freemibtable)

## <a name="ip-utility"></a><span data-ttu-id="78414-230">Служебная программа IP</span><span class="sxs-lookup"><span data-stu-id="78414-230">IP utility</span></span>

-   [<span data-ttu-id="78414-231">**ConvertIpv4MaskToLength**</span><span class="sxs-lookup"><span data-stu-id="78414-231">**ConvertIpv4MaskToLength**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [<span data-ttu-id="78414-232">**ConvertLengthToIpv4Mask**</span><span class="sxs-lookup"><span data-stu-id="78414-232">**ConvertLengthToIpv4Mask**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [<span data-ttu-id="78414-233">**креатесортедаддресспаирс**</span><span class="sxs-lookup"><span data-stu-id="78414-233">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [<span data-ttu-id="78414-234">**парсенетворкстринг**</span><span class="sxs-lookup"><span data-stu-id="78414-234">**ParseNetworkString**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

## <a name="network-configuration"></a><span data-ttu-id="78414-235">Сетевая конфигурация</span><span class="sxs-lookup"><span data-stu-id="78414-235">Network configuration</span></span>

-   [<span data-ttu-id="78414-236">**жетнетворкпарамс**</span><span class="sxs-lookup"><span data-stu-id="78414-236">**GetNetworkParams**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnetworkparams)

## <a name="notification"></a><span data-ttu-id="78414-237">Уведомление</span><span class="sxs-lookup"><span data-stu-id="78414-237">Notification</span></span>

-   [<span data-ttu-id="78414-238">**CancelMibChangeNotify2**</span><span class="sxs-lookup"><span data-stu-id="78414-238">**CancelMibChangeNotify2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [<span data-ttu-id="78414-239">**нотифяддрчанже**</span><span class="sxs-lookup"><span data-stu-id="78414-239">**NotifyAddrChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyaddrchange)
-   [<span data-ttu-id="78414-240">**нотифипинтерфацечанже**</span><span class="sxs-lookup"><span data-stu-id="78414-240">**NotifyIpInterfaceChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [<span data-ttu-id="78414-241">**нотифираутечанже**</span><span class="sxs-lookup"><span data-stu-id="78414-241">**NotifyRouteChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyroutechange)
-   [<span data-ttu-id="78414-242">**NotifyRouteChange2**</span><span class="sxs-lookup"><span data-stu-id="78414-242">**NotifyRouteChange2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [<span data-ttu-id="78414-243">**нотифюникастипаддрессчанже**</span><span class="sxs-lookup"><span data-stu-id="78414-243">**NotifyUnicastIpAddressChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

## <a name="persistent-port-reservation"></a><span data-ttu-id="78414-244">Постоянное резервирование портов</span><span class="sxs-lookup"><span data-stu-id="78414-244">Persistent port reservation</span></span>

-   [<span data-ttu-id="78414-245">**креатеперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="78414-245">**CreatePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [<span data-ttu-id="78414-246">**креатеперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="78414-246">**CreatePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [<span data-ttu-id="78414-247">**делетеперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="78414-247">**DeletePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [<span data-ttu-id="78414-248">**делетеперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="78414-248">**DeletePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [<span data-ttu-id="78414-249">**лукупперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="78414-249">**LookupPersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [<span data-ttu-id="78414-250">**лукупперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="78414-250">**LookupPersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="security-health"></a><span data-ttu-id="78414-251">Работоспособность системы безопасности</span><span class="sxs-lookup"><span data-stu-id="78414-251">Security health</span></span>

-   <span data-ttu-id="78414-252">[**канцелсекуритихеалсчанженотифи**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78414-252">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span></span>
-   <span data-ttu-id="78414-253">[**нотифисекуритихеалсчанже**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78414-253">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span></span>

<span data-ttu-id="78414-254">Эти функции определяются только в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="78414-254">These functions are defined only on Windows Server 2003.</span></span>

> [!Note]  
> <span data-ttu-id="78414-255">Эти функции недоступны в Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="78414-255">These functions are not available on Windows Vista, nor on Windows Server 2008.</span></span>

## <a name="teredo-ipv6-client-management"></a><span data-ttu-id="78414-256">Управление клиентом Teredo IPv6</span><span class="sxs-lookup"><span data-stu-id="78414-256">Teredo IPv6 client management</span></span>

-   [<span data-ttu-id="78414-257">**жеттередопорт**</span><span class="sxs-lookup"><span data-stu-id="78414-257">**GetTeredoPort**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="78414-258">**нотифитередопортчанже**</span><span class="sxs-lookup"><span data-stu-id="78414-258">**NotifyTeredoPortChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="78414-259">**нотифистаблеуникастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="78414-259">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

## <a name="transmission-control-protocol-tcp-and-user-datagram-protocol-udp"></a><span data-ttu-id="78414-260">Протокол TCP и протокол UDP.</span><span class="sxs-lookup"><span data-stu-id="78414-260">Transmission Control Protocol (TCP) and User Datagram Protocol (UDP)</span></span>

-   [<span data-ttu-id="78414-261">**жетекстендедткптабле**</span><span class="sxs-lookup"><span data-stu-id="78414-261">**GetExtendedTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedtcptable)
-   [<span data-ttu-id="78414-262">**жетекстендедудптабле**</span><span class="sxs-lookup"><span data-stu-id="78414-262">**GetExtendedUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedudptable)
-   [<span data-ttu-id="78414-263">**GetOwnerModuleFromTcp6Entry**</span><span class="sxs-lookup"><span data-stu-id="78414-263">**GetOwnerModuleFromTcp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [<span data-ttu-id="78414-264">**жетовнермодулефромткпентри**</span><span class="sxs-lookup"><span data-stu-id="78414-264">**GetOwnerModuleFromTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [<span data-ttu-id="78414-265">**GetOwnerModuleFromUdp6Entry**</span><span class="sxs-lookup"><span data-stu-id="78414-265">**GetOwnerModuleFromUdp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)
-   [<span data-ttu-id="78414-266">**жетовнермодулефромудпентри**</span><span class="sxs-lookup"><span data-stu-id="78414-266">**GetOwnerModuleFromUdpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [<span data-ttu-id="78414-267">**GetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="78414-267">**GetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [<span data-ttu-id="78414-268">**жетперткпконнектионестатс**</span><span class="sxs-lookup"><span data-stu-id="78414-268">**GetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [<span data-ttu-id="78414-269">**жетткпстатистикс**</span><span class="sxs-lookup"><span data-stu-id="78414-269">**GetTcpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)
-   [<span data-ttu-id="78414-270">**жетткпстатистиксекс**</span><span class="sxs-lookup"><span data-stu-id="78414-270">**GetTcpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex)
-   [<span data-ttu-id="78414-271">**GetTcpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="78414-271">**GetTcpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex2)
-   [<span data-ttu-id="78414-272">**GetTcp6Table**</span><span class="sxs-lookup"><span data-stu-id="78414-272">**GetTcp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [<span data-ttu-id="78414-273">**GetTcp6Table2**</span><span class="sxs-lookup"><span data-stu-id="78414-273">**GetTcp6Table2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [<span data-ttu-id="78414-274">**жетткптабле**</span><span class="sxs-lookup"><span data-stu-id="78414-274">**GetTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable)
-   [<span data-ttu-id="78414-275">**GetTcpTable2**</span><span class="sxs-lookup"><span data-stu-id="78414-275">**GetTcpTable2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [<span data-ttu-id="78414-276">**SetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="78414-276">**SetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [<span data-ttu-id="78414-277">**сетперткпконнектионестатс**</span><span class="sxs-lookup"><span data-stu-id="78414-277">**SetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)
-   [<span data-ttu-id="78414-278">**сетткпентри**</span><span class="sxs-lookup"><span data-stu-id="78414-278">**SetTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-settcpentry)
-   [<span data-ttu-id="78414-279">**GetUdp6Table**</span><span class="sxs-lookup"><span data-stu-id="78414-279">**GetUdp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudp6table)
-   [<span data-ttu-id="78414-280">**жетудпстатистикс**</span><span class="sxs-lookup"><span data-stu-id="78414-280">**GetUdpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatistics)
-   [<span data-ttu-id="78414-281">**жетудпстатистиксекс**</span><span class="sxs-lookup"><span data-stu-id="78414-281">**GetUdpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex)
-   [<span data-ttu-id="78414-282">**GetUdpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="78414-282">**GetUdpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex2)
-   [<span data-ttu-id="78414-283">**жетудптабле**</span><span class="sxs-lookup"><span data-stu-id="78414-283">**GetUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudptable)

## <a name="deprecated-apis"></a><span data-ttu-id="78414-284">Устаревшие интерфейсы API</span><span class="sxs-lookup"><span data-stu-id="78414-284">Deprecated APIs</span></span>

> [!Note]  
> <span data-ttu-id="78414-285">Эти функции являются устаревшими и не поддерживаются корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="78414-285">These functions are deprecated, and are not supported by Microsoft.</span></span>

-   [<span data-ttu-id="78414-286">**аллокатеанджетткпекстаблефромстакк**</span><span class="sxs-lookup"><span data-stu-id="78414-286">**AllocateAndGetTcpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgettcpextablefromstack)
-   [<span data-ttu-id="78414-287">**аллокатеанджетудпекстаблефромстакк**</span><span class="sxs-lookup"><span data-stu-id="78414-287">**AllocateAndGetUdpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgetudpextablefromstack)
