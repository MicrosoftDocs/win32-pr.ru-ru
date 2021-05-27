---
title: Вспомогательные функции IP
description: Следующие функции извлекают и изменяют параметры конфигурации для транспорта TCP/IP на локальном компьютере.
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5f562470-f3e8-4305-a015-3a84cd09a1eb
ms.openlocfilehash: ae19803c25512242b613735a060c7beda8c1df70
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549509"
---
# <a name="ip-helper-functions"></a><span data-ttu-id="94f4e-103">Вспомогательные функции IP</span><span class="sxs-lookup"><span data-stu-id="94f4e-103">IP Helper functions</span></span>

<span data-ttu-id="94f4e-104">Следующие функции извлекают и изменяют параметры конфигурации для транспорта TCP/IP на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="94f4e-104">The following functions retrieve and modify configuration settings for the TCP/IP transport on the local computer.</span></span> <span data-ttu-id="94f4e-105">Следующий список категорий поможет определить, какая коллекция функций лучше всего подходит для данной задачи.</span><span class="sxs-lookup"><span data-stu-id="94f4e-105">The following categorical listing can help determine which collection of functions is best suited for a given task.</span></span>

-   [<span data-ttu-id="94f4e-106">**жетнетворкконнективитихинт**</span><span class="sxs-lookup"><span data-stu-id="94f4e-106">**GetNetworkConnectivityHint**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhint)
-   [<span data-ttu-id="94f4e-107">**жетнетворкконнективитихинтфоринтерфаце**</span><span class="sxs-lookup"><span data-stu-id="94f4e-107">**GetNetworkConnectivityHintForInterface**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhintforinterface)
-   [<span data-ttu-id="94f4e-108">**нотифинетворкконнективитихинтчанже**</span><span class="sxs-lookup"><span data-stu-id="94f4e-108">**NotifyNetworkConnectivityHintChange**</span></span>](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange)

## <a name="adapter-management"></a><span data-ttu-id="94f4e-109">Управление адаптерами</span><span class="sxs-lookup"><span data-stu-id="94f4e-109">Adapter management</span></span>

-   [<span data-ttu-id="94f4e-110">**жетадаптериндекс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-110">**GetAdapterIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadapterindex)
-   [<span data-ttu-id="94f4e-111">**жетадаптерсаддрессес**</span><span class="sxs-lookup"><span data-stu-id="94f4e-111">**GetAdaptersAddresses**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)
-   [<span data-ttu-id="94f4e-112">**жетадаптерсинфо**</span><span class="sxs-lookup"><span data-stu-id="94f4e-112">**GetAdaptersInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)
-   [<span data-ttu-id="94f4e-113">**жетперадаптеринфо**</span><span class="sxs-lookup"><span data-stu-id="94f4e-113">**GetPerAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)
-   [<span data-ttu-id="94f4e-114">**жетунидиректионаладаптеринфо**</span><span class="sxs-lookup"><span data-stu-id="94f4e-114">**GetUniDirectionalAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

## <a name="address-resolution-protocol-arp-management"></a><span data-ttu-id="94f4e-115">Управление протоколом разрешения адресов (ARP)</span><span class="sxs-lookup"><span data-stu-id="94f4e-115">Address Resolution Protocol (ARP) management</span></span>

-   [<span data-ttu-id="94f4e-116">**креатеипнетентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-116">**CreateIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipnetentry)
-   [<span data-ttu-id="94f4e-117">**креатепроксярпентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-117">**CreateProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createproxyarpentry)
-   [<span data-ttu-id="94f4e-118">**делетеипнетентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-118">**DeleteIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipnetentry)
-   [<span data-ttu-id="94f4e-119">**делетепроксярпентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-119">**DeleteProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)
-   [<span data-ttu-id="94f4e-120">**флушипнеттабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-120">**FlushIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-flushipnettable)
-   [<span data-ttu-id="94f4e-121">**жетипнеттабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-121">**GetIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipnettable)
-   [<span data-ttu-id="94f4e-122">**сендарп**</span><span class="sxs-lookup"><span data-stu-id="94f4e-122">**SendARP**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-sendarp)
-   [<span data-ttu-id="94f4e-123">**сетипнетентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-123">**SetIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipnetentry)

## <a name="interface-conversion"></a><span data-ttu-id="94f4e-124">Преобразование интерфейса</span><span class="sxs-lookup"><span data-stu-id="94f4e-124">Interface conversion</span></span>

-   [<span data-ttu-id="94f4e-125">**конвертинтерфацеалиастолуид**</span><span class="sxs-lookup"><span data-stu-id="94f4e-125">**ConvertInterfaceAliasToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [<span data-ttu-id="94f4e-126">**конвертинтерфацегуидтолуид**</span><span class="sxs-lookup"><span data-stu-id="94f4e-126">**ConvertInterfaceGuidToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [<span data-ttu-id="94f4e-127">**конвертинтерфацеиндекстолуид**</span><span class="sxs-lookup"><span data-stu-id="94f4e-127">**ConvertInterfaceIndexToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [<span data-ttu-id="94f4e-128">**конвертинтерфацелуидтоалиас**</span><span class="sxs-lookup"><span data-stu-id="94f4e-128">**ConvertInterfaceLuidToAlias**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoalias)
-   [<span data-ttu-id="94f4e-129">**конвертинтерфацелуидтогуид**</span><span class="sxs-lookup"><span data-stu-id="94f4e-129">**ConvertInterfaceLuidToGuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [<span data-ttu-id="94f4e-130">**конвертинтерфацелуидтоиндекс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-130">**ConvertInterfaceLuidToIndex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [<span data-ttu-id="94f4e-131">**конвертинтерфацелуидтонамеа**</span><span class="sxs-lookup"><span data-stu-id="94f4e-131">**ConvertInterfaceLuidToNameA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [<span data-ttu-id="94f4e-132">**конвертинтерфацелуидтонамев**</span><span class="sxs-lookup"><span data-stu-id="94f4e-132">**ConvertInterfaceLuidToNameW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [<span data-ttu-id="94f4e-133">**конвертинтерфаценаметолуида**</span><span class="sxs-lookup"><span data-stu-id="94f4e-133">**ConvertInterfaceNameToLuidA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [<span data-ttu-id="94f4e-134">**конвертинтерфаценаметолуидв**</span><span class="sxs-lookup"><span data-stu-id="94f4e-134">**ConvertInterfaceNameToLuidW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [<span data-ttu-id="94f4e-135">**Если \_ индекстонаме**</span><span class="sxs-lookup"><span data-stu-id="94f4e-135">**if\_indextoname**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_indextoname)
-   [<span data-ttu-id="94f4e-136">**Если \_ наметоиндекс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-136">**if\_nametoindex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_nametoindex)

## <a name="interface-management"></a><span data-ttu-id="94f4e-137">Управление интерфейсом</span><span class="sxs-lookup"><span data-stu-id="94f4e-137">Interface management</span></span>

-   [<span data-ttu-id="94f4e-138">**жетфриендлифиндекс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-138">**GetFriendlyIfIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)
-   [<span data-ttu-id="94f4e-139">**жетифентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-139">**GetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getifentry)
-   [<span data-ttu-id="94f4e-140">**GetIfEntry2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-140">**GetIfEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2)
-   [<span data-ttu-id="94f4e-141">**GetIfEntry2Ex**</span><span class="sxs-lookup"><span data-stu-id="94f4e-141">**GetIfEntry2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2ex)
-   [<span data-ttu-id="94f4e-142">**жетифстакктабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-142">**GetIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifstacktable)
-   [<span data-ttu-id="94f4e-143">**жетифтабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-143">**GetIfTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getiftable)
-   [<span data-ttu-id="94f4e-144">**GetIfTable2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-144">**GetIfTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2)
-   [<span data-ttu-id="94f4e-145">**GetIfTable2Ex**</span><span class="sxs-lookup"><span data-stu-id="94f4e-145">**GetIfTable2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2ex)
-   [<span data-ttu-id="94f4e-146">**жетинтерфацеинфо**</span><span class="sxs-lookup"><span data-stu-id="94f4e-146">**GetInterfaceInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)
-   [<span data-ttu-id="94f4e-147">**жетинвертедифстакктабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-147">**GetInvertedIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [<span data-ttu-id="94f4e-148">**жетипинтерфацеентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-148">**GetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [<span data-ttu-id="94f4e-149">**жетипинтерфацетабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-149">**GetIpInterfaceTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [<span data-ttu-id="94f4e-150">**жетнумберофинтерфацес**</span><span class="sxs-lookup"><span data-stu-id="94f4e-150">**GetNumberOfInterfaces**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)
-   [<span data-ttu-id="94f4e-151">**инитиализеипинтерфацеентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-151">**InitializeIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [<span data-ttu-id="94f4e-152">**сетифентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-152">**SetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setifentry)
-   [<span data-ttu-id="94f4e-153">**сетипинтерфацеентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-153">**SetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipinterfaceentry)

## <a name="internet-protocol-ip-and-internet-control-message-protocol-icmp"></a><span data-ttu-id="94f4e-154">Протокол Интернета (IP) и Протокол управляющих сообщений Интернета (ICMP)</span><span class="sxs-lookup"><span data-stu-id="94f4e-154">Internet Protocol (IP) and Internet Control Message Protocol (ICMP)</span></span>

-   [<span data-ttu-id="94f4e-155">**жетикмпстатистикс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-155">**GetIcmpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-geticmpstatistics)
-   [<span data-ttu-id="94f4e-156">**жетипстатистикс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-156">**GetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipstatistics)
-   [<span data-ttu-id="94f4e-157">**Icmp6CreateFile**</span><span class="sxs-lookup"><span data-stu-id="94f4e-157">**Icmp6CreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6createfile)
-   [<span data-ttu-id="94f4e-158">**Icmp6ParseReplies**</span><span class="sxs-lookup"><span data-stu-id="94f4e-158">**Icmp6ParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6parsereplies)
-   [<span data-ttu-id="94f4e-159">**Icmp6SendEcho2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-159">**Icmp6SendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6sendecho2)
-   [<span data-ttu-id="94f4e-160">**икмпклосехандле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-160">**IcmpCloseHandle**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpclosehandle)
-   [<span data-ttu-id="94f4e-161">**икмпкреатефиле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-161">**IcmpCreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpcreatefile)
-   [<span data-ttu-id="94f4e-162">**икмппарсереплиес**</span><span class="sxs-lookup"><span data-stu-id="94f4e-162">**IcmpParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpparsereplies)
-   [<span data-ttu-id="94f4e-163">**икмпсендечо**</span><span class="sxs-lookup"><span data-stu-id="94f4e-163">**IcmpSendEcho**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho)
-   [<span data-ttu-id="94f4e-164">**IcmpSendEcho2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-164">**IcmpSendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2)
-   [<span data-ttu-id="94f4e-165">**IcmpSendEcho2Ex**</span><span class="sxs-lookup"><span data-stu-id="94f4e-165">**IcmpSendEcho2Ex**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)
-   [<span data-ttu-id="94f4e-166">**сетипттл**</span><span class="sxs-lookup"><span data-stu-id="94f4e-166">**SetIpTTL**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipttl)

## <a name="ip-address-management"></a><span data-ttu-id="94f4e-167">Управление IP-адресами</span><span class="sxs-lookup"><span data-stu-id="94f4e-167">IP address management</span></span>

-   [<span data-ttu-id="94f4e-168">**аддипаддресс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-168">**AddIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-addipaddress)
-   [<span data-ttu-id="94f4e-169">**креатеаникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-169">**CreateAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [<span data-ttu-id="94f4e-170">**креатеуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-170">**CreateUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [<span data-ttu-id="94f4e-171">**делетеипаддресс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-171">**DeleteIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipaddress)
-   [<span data-ttu-id="94f4e-172">**делетеаникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-172">**DeleteAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [<span data-ttu-id="94f4e-173">**делетеуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-173">**DeleteUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [<span data-ttu-id="94f4e-174">**жетаникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-174">**GetAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [<span data-ttu-id="94f4e-175">**жетаникастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-175">**GetAnycastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [<span data-ttu-id="94f4e-176">**жетипаддртабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-176">**GetIpAddrTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipaddrtable)
-   [<span data-ttu-id="94f4e-177">**жетмултикастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-177">**GetMulticastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [<span data-ttu-id="94f4e-178">**жетмултикастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-178">**GetMulticastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [<span data-ttu-id="94f4e-179">**жетуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-179">**GetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [<span data-ttu-id="94f4e-180">**жетуникастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-180">**GetUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [<span data-ttu-id="94f4e-181">**инитиализеуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-181">**InitializeUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [<span data-ttu-id="94f4e-182">**ипрелеасеаддресс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-182">**IpReleaseAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)
-   [<span data-ttu-id="94f4e-183">**ипреневаддресс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-183">**IpRenewAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-iprenewaddress)
-   [<span data-ttu-id="94f4e-184">**нотифистаблеуникастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-184">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [<span data-ttu-id="94f4e-185">**сетуникастипаддрессентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-185">**SetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setunicastipaddressentry)

## <a name="ip-address-string-conversion"></a><span data-ttu-id="94f4e-186">Преобразование строки IP-адреса</span><span class="sxs-lookup"><span data-stu-id="94f4e-186">IP address string conversion</span></span>

-   [<span data-ttu-id="94f4e-187">**RtlIpv4AddressToString**</span><span class="sxs-lookup"><span data-stu-id="94f4e-187">**RtlIpv4AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [<span data-ttu-id="94f4e-188">**RtlIpv4AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="94f4e-188">**RtlIpv4AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [<span data-ttu-id="94f4e-189">**RtlIpv4StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="94f4e-189">**RtlIpv4StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [<span data-ttu-id="94f4e-190">**RtlIpv4StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="94f4e-190">**RtlIpv4StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [<span data-ttu-id="94f4e-191">**RtlIpv6AddressToString**</span><span class="sxs-lookup"><span data-stu-id="94f4e-191">**RtlIpv6AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [<span data-ttu-id="94f4e-192">**RtlIpv6AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="94f4e-192">**RtlIpv6AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [<span data-ttu-id="94f4e-193">**RtlIpv6StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="94f4e-193">**RtlIpv6StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [<span data-ttu-id="94f4e-194">**RtlIpv6StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="94f4e-194">**RtlIpv6StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

## <a name="ip-neighbor-address-management"></a><span data-ttu-id="94f4e-195">Управление адресами соседей IP</span><span class="sxs-lookup"><span data-stu-id="94f4e-195">IP neighbor address management</span></span>

-   [<span data-ttu-id="94f4e-196">**CreateIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-196">**CreateIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipnetentry2)
-   [<span data-ttu-id="94f4e-197">**DeleteIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-197">**DeleteIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [<span data-ttu-id="94f4e-198">**FlushIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-198">**FlushIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushipnettable2)
-   [<span data-ttu-id="94f4e-199">**GetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-199">**GetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnetentry2)
-   [<span data-ttu-id="94f4e-200">**GetIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-200">**GetIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnettable2)
-   [<span data-ttu-id="94f4e-201">**ResolveIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-201">**ResolveIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [<span data-ttu-id="94f4e-202">**ресолвенеигхбор**</span><span class="sxs-lookup"><span data-stu-id="94f4e-202">**ResolveNeighbor**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [<span data-ttu-id="94f4e-203">**SetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-203">**SetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipnetentry2)

## <a name="ip-path-management"></a><span data-ttu-id="94f4e-204">Управление IP-путями</span><span class="sxs-lookup"><span data-stu-id="94f4e-204">IP path management</span></span>

-   [<span data-ttu-id="94f4e-205">**флушиппастабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-205">**FlushIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushippathtable)
-   [<span data-ttu-id="94f4e-206">**жетиппасентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-206">**GetIpPathEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathentry)
-   [<span data-ttu-id="94f4e-207">**жетиппастабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-207">**GetIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathtable)

## <a name="ip-route-management"></a><span data-ttu-id="94f4e-208">Управление IP-маршрутами</span><span class="sxs-lookup"><span data-stu-id="94f4e-208">IP route management</span></span>

-   [<span data-ttu-id="94f4e-209">**креатеипфорвардентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-209">**CreateIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipforwardentry)
-   [<span data-ttu-id="94f4e-210">**CreateIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-210">**CreateIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [<span data-ttu-id="94f4e-211">**делетеипфорвардентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-211">**DeleteIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)
-   [<span data-ttu-id="94f4e-212">**DeleteIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-212">**DeleteIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [<span data-ttu-id="94f4e-213">**енаблераутер**</span><span class="sxs-lookup"><span data-stu-id="94f4e-213">**EnableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-enablerouter)
-   [<span data-ttu-id="94f4e-214">**жетбестинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="94f4e-214">**GetBestInterface**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterface)
-   [<span data-ttu-id="94f4e-215">**жетбестинтерфацеекс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-215">**GetBestInterfaceEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterfaceex)
-   [<span data-ttu-id="94f4e-216">**жетбестрауте**</span><span class="sxs-lookup"><span data-stu-id="94f4e-216">**GetBestRoute**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestroute)
-   [<span data-ttu-id="94f4e-217">**GetBestRoute2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-217">**GetBestRoute2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getbestroute2)
-   [<span data-ttu-id="94f4e-218">**GetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-218">**GetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [<span data-ttu-id="94f4e-219">**жетипфорвардтабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-219">**GetIpForwardTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipforwardtable)
-   [<span data-ttu-id="94f4e-220">**GetIpForwardTable2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-220">**GetIpForwardTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [<span data-ttu-id="94f4e-221">**жетрттандхопкаунт**</span><span class="sxs-lookup"><span data-stu-id="94f4e-221">**GetRTTAndHopCount**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getrttandhopcount)
-   [<span data-ttu-id="94f4e-222">**инитиализеипфорвардентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-222">**InitializeIpForwardEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [<span data-ttu-id="94f4e-223">**сетипфорвардентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-223">**SetIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipforwardentry)
-   [<span data-ttu-id="94f4e-224">**SetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-224">**SetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [<span data-ttu-id="94f4e-225">**сетипстатистикс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-225">**SetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatistics)
-   [<span data-ttu-id="94f4e-226">**сетипстатистиксекс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-226">**SetIpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)
-   [<span data-ttu-id="94f4e-227">**уненаблераутер**</span><span class="sxs-lookup"><span data-stu-id="94f4e-227">**UnenableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-unenablerouter)

## <a name="ip-table-memory-management"></a><span data-ttu-id="94f4e-228">Управление памятью таблицы IP</span><span class="sxs-lookup"><span data-stu-id="94f4e-228">IP table memory management</span></span>

-   [<span data-ttu-id="94f4e-229">**фримибтабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-229">**FreeMibTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-freemibtable)

## <a name="ip-utility"></a><span data-ttu-id="94f4e-230">Служебная программа IP</span><span class="sxs-lookup"><span data-stu-id="94f4e-230">IP utility</span></span>

-   [<span data-ttu-id="94f4e-231">**ConvertIpv4MaskToLength**</span><span class="sxs-lookup"><span data-stu-id="94f4e-231">**ConvertIpv4MaskToLength**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [<span data-ttu-id="94f4e-232">**ConvertLengthToIpv4Mask**</span><span class="sxs-lookup"><span data-stu-id="94f4e-232">**ConvertLengthToIpv4Mask**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [<span data-ttu-id="94f4e-233">**креатесортедаддресспаирс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-233">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [<span data-ttu-id="94f4e-234">**парсенетворкстринг**</span><span class="sxs-lookup"><span data-stu-id="94f4e-234">**ParseNetworkString**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

## <a name="network-configuration"></a><span data-ttu-id="94f4e-235">Сетевая конфигурация</span><span class="sxs-lookup"><span data-stu-id="94f4e-235">Network configuration</span></span>

-   [<span data-ttu-id="94f4e-236">**жетнетворкпарамс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-236">**GetNetworkParams**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnetworkparams)

## <a name="notification"></a><span data-ttu-id="94f4e-237">Уведомление</span><span class="sxs-lookup"><span data-stu-id="94f4e-237">Notification</span></span>

-   [<span data-ttu-id="94f4e-238">**CancelMibChangeNotify2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-238">**CancelMibChangeNotify2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [<span data-ttu-id="94f4e-239">**нотифяддрчанже**</span><span class="sxs-lookup"><span data-stu-id="94f4e-239">**NotifyAddrChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyaddrchange)
-   [<span data-ttu-id="94f4e-240">**нотифипинтерфацечанже**</span><span class="sxs-lookup"><span data-stu-id="94f4e-240">**NotifyIpInterfaceChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [<span data-ttu-id="94f4e-241">**нотифираутечанже**</span><span class="sxs-lookup"><span data-stu-id="94f4e-241">**NotifyRouteChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyroutechange)
-   [<span data-ttu-id="94f4e-242">**NotifyRouteChange2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-242">**NotifyRouteChange2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [<span data-ttu-id="94f4e-243">**нотифюникастипаддрессчанже**</span><span class="sxs-lookup"><span data-stu-id="94f4e-243">**NotifyUnicastIpAddressChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

## <a name="packet-timestamping"></a><span data-ttu-id="94f4e-244">Метки времени пакетов</span><span class="sxs-lookup"><span data-stu-id="94f4e-244">Packet timestamping</span></span>

-   [<span data-ttu-id="94f4e-245">**каптуреинтерфацехардварекросстиместамп**</span><span class="sxs-lookup"><span data-stu-id="94f4e-245">**CaptureInterfaceHardwareCrossTimestamp**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp)
-   [<span data-ttu-id="94f4e-246">**жетинтерфацеактиветиместампкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="94f4e-246">**GetInterfaceActiveTimestampCapabilities**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities)
-   [<span data-ttu-id="94f4e-247">**жетинтерфацесуппортедтиместампкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="94f4e-247">**GetInterfaceSupportedTimestampCapabilities**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities)
-   [<span data-ttu-id="94f4e-248">**регистеринтерфацетиместампконфигчанже**</span><span class="sxs-lookup"><span data-stu-id="94f4e-248">**RegisterInterfaceTimestampConfigChange**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange)
-   [<span data-ttu-id="94f4e-249">**унрегистеринтерфацетиместампконфигчанже**</span><span class="sxs-lookup"><span data-stu-id="94f4e-249">**UnregisterInterfaceTimestampConfigChange**</span></span>](/windows/win32/api/iphlpapi/unregisterinterfacetimestampconfigchange)

## <a name="persistent-port-reservation"></a><span data-ttu-id="94f4e-250">Постоянное резервирование портов</span><span class="sxs-lookup"><span data-stu-id="94f4e-250">Persistent port reservation</span></span>

-   [<span data-ttu-id="94f4e-251">**креатеперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="94f4e-251">**CreatePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [<span data-ttu-id="94f4e-252">**креатеперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="94f4e-252">**CreatePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [<span data-ttu-id="94f4e-253">**делетеперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="94f4e-253">**DeletePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [<span data-ttu-id="94f4e-254">**делетеперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="94f4e-254">**DeletePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [<span data-ttu-id="94f4e-255">**лукупперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="94f4e-255">**LookupPersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [<span data-ttu-id="94f4e-256">**лукупперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="94f4e-256">**LookupPersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="security-health"></a><span data-ttu-id="94f4e-257">Работоспособность системы безопасности</span><span class="sxs-lookup"><span data-stu-id="94f4e-257">Security health</span></span>

-   <span data-ttu-id="94f4e-258">[**канцелсекуритихеалсчанженотифи**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="94f4e-258">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span></span>
-   <span data-ttu-id="94f4e-259">[**нотифисекуритихеалсчанже**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="94f4e-259">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span></span>

<span data-ttu-id="94f4e-260">Эти функции определяются только в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="94f4e-260">These functions are defined only on Windows Server 2003.</span></span>

> [!Note]  
> <span data-ttu-id="94f4e-261">Эти функции недоступны в Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="94f4e-261">These functions are not available on Windows Vista, nor on Windows Server 2008.</span></span>

## <a name="teredo-ipv6-client-management"></a><span data-ttu-id="94f4e-262">Управление клиентом Teredo IPv6</span><span class="sxs-lookup"><span data-stu-id="94f4e-262">Teredo IPv6 client management</span></span>

-   [<span data-ttu-id="94f4e-263">**жеттередопорт**</span><span class="sxs-lookup"><span data-stu-id="94f4e-263">**GetTeredoPort**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="94f4e-264">**нотифитередопортчанже**</span><span class="sxs-lookup"><span data-stu-id="94f4e-264">**NotifyTeredoPortChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="94f4e-265">**нотифистаблеуникастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-265">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

## <a name="transmission-control-protocol-tcp-and-user-datagram-protocol-udp"></a><span data-ttu-id="94f4e-266">Протокол TCP и протокол UDP.</span><span class="sxs-lookup"><span data-stu-id="94f4e-266">Transmission Control Protocol (TCP) and User Datagram Protocol (UDP)</span></span>

-   [<span data-ttu-id="94f4e-267">**жетекстендедткптабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-267">**GetExtendedTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedtcptable)
-   [<span data-ttu-id="94f4e-268">**жетекстендедудптабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-268">**GetExtendedUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedudptable)
-   [<span data-ttu-id="94f4e-269">**GetOwnerModuleFromTcp6Entry**</span><span class="sxs-lookup"><span data-stu-id="94f4e-269">**GetOwnerModuleFromTcp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [<span data-ttu-id="94f4e-270">**жетовнермодулефромткпентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-270">**GetOwnerModuleFromTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [<span data-ttu-id="94f4e-271">**GetOwnerModuleFromUdp6Entry**</span><span class="sxs-lookup"><span data-stu-id="94f4e-271">**GetOwnerModuleFromUdp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)
-   [<span data-ttu-id="94f4e-272">**жетовнермодулефромудпентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-272">**GetOwnerModuleFromUdpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [<span data-ttu-id="94f4e-273">**GetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="94f4e-273">**GetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [<span data-ttu-id="94f4e-274">**жетперткпконнектионестатс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-274">**GetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [<span data-ttu-id="94f4e-275">**жетткпстатистикс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-275">**GetTcpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)
-   [<span data-ttu-id="94f4e-276">**жетткпстатистиксекс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-276">**GetTcpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex)
-   [<span data-ttu-id="94f4e-277">**GetTcpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-277">**GetTcpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex2)
-   [<span data-ttu-id="94f4e-278">**GetTcp6Table**</span><span class="sxs-lookup"><span data-stu-id="94f4e-278">**GetTcp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [<span data-ttu-id="94f4e-279">**GetTcp6Table2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-279">**GetTcp6Table2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [<span data-ttu-id="94f4e-280">**жетткптабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-280">**GetTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable)
-   [<span data-ttu-id="94f4e-281">**GetTcpTable2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-281">**GetTcpTable2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [<span data-ttu-id="94f4e-282">**SetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="94f4e-282">**SetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [<span data-ttu-id="94f4e-283">**сетперткпконнектионестатс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-283">**SetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)
-   [<span data-ttu-id="94f4e-284">**сетткпентри**</span><span class="sxs-lookup"><span data-stu-id="94f4e-284">**SetTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-settcpentry)
-   [<span data-ttu-id="94f4e-285">**GetUdp6Table**</span><span class="sxs-lookup"><span data-stu-id="94f4e-285">**GetUdp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudp6table)
-   [<span data-ttu-id="94f4e-286">**жетудпстатистикс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-286">**GetUdpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatistics)
-   [<span data-ttu-id="94f4e-287">**жетудпстатистиксекс**</span><span class="sxs-lookup"><span data-stu-id="94f4e-287">**GetUdpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex)
-   [<span data-ttu-id="94f4e-288">**GetUdpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="94f4e-288">**GetUdpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex2)
-   [<span data-ttu-id="94f4e-289">**жетудптабле**</span><span class="sxs-lookup"><span data-stu-id="94f4e-289">**GetUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudptable)

## <a name="deprecated-apis"></a><span data-ttu-id="94f4e-290">Устаревшие интерфейсы API</span><span class="sxs-lookup"><span data-stu-id="94f4e-290">Deprecated APIs</span></span>

> [!Note]  
> <span data-ttu-id="94f4e-291">Эти функции являются устаревшими и не поддерживаются корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="94f4e-291">These functions are deprecated, and are not supported by Microsoft.</span></span>

-   [<span data-ttu-id="94f4e-292">**аллокатеанджетткпекстаблефромстакк**</span><span class="sxs-lookup"><span data-stu-id="94f4e-292">**AllocateAndGetTcpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgettcpextablefromstack)
-   [<span data-ttu-id="94f4e-293">**аллокатеанджетудпекстаблефромстакк**</span><span class="sxs-lookup"><span data-stu-id="94f4e-293">**AllocateAndGetUdpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgetudpextablefromstack)
