---
description: Представляет атрибуты и поведение сетевого адаптера. Этот класс включает дополнительные свойства и методы, которые поддерживают управление протоколом TCP/IP, который не зависит от сетевого адаптера.
ms.assetid: 690b46ed-a065-4973-b044-0df4e81e41a1
ms.tgt_platform: multiple
title: Класс Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration
- Win32_NetworkAdapterConfiguration.Caption
- Win32_NetworkAdapterConfiguration.Description
- Win32_NetworkAdapterConfiguration.SettingID
- Win32_NetworkAdapterConfiguration.ArpAlwaysSourceRoute
- Win32_NetworkAdapterConfiguration.ArpUseEtherSNAP
- Win32_NetworkAdapterConfiguration.DatabasePath
- Win32_NetworkAdapterConfiguration.DeadGWDetectEnabled
- Win32_NetworkAdapterConfiguration.DefaultIPGateway
- Win32_NetworkAdapterConfiguration.DefaultTOS
- Win32_NetworkAdapterConfiguration.DefaultTTL
- Win32_NetworkAdapterConfiguration.DHCPEnabled
- Win32_NetworkAdapterConfiguration.DHCPLeaseExpires
- Win32_NetworkAdapterConfiguration.DHCPLeaseObtained
- Win32_NetworkAdapterConfiguration.DHCPServer
- Win32_NetworkAdapterConfiguration.DNSDomain
- Win32_NetworkAdapterConfiguration.DNSDomainSuffixSearchOrder
- Win32_NetworkAdapterConfiguration.DNSEnabledForWINSResolution
- Win32_NetworkAdapterConfiguration.DNSHostName
- Win32_NetworkAdapterConfiguration.DNSServerSearchOrder
- Win32_NetworkAdapterConfiguration.DomainDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.ForwardBufferMemory
- Win32_NetworkAdapterConfiguration.FullDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.GatewayCostMetric
- Win32_NetworkAdapterConfiguration.IGMPLevel
- Win32_NetworkAdapterConfiguration.Index
- Win32_NetworkAdapterConfiguration.InterfaceIndex
- Win32_NetworkAdapterConfiguration.IPAddress
- Win32_NetworkAdapterConfiguration.IPConnectionMetric
- Win32_NetworkAdapterConfiguration.IPEnabled
- Win32_NetworkAdapterConfiguration.IPFilterSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPPortSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPSecPermitIPProtocols
- Win32_NetworkAdapterConfiguration.IPSecPermitTCPPorts
- Win32_NetworkAdapterConfiguration.IPSecPermitUDPPorts
- Win32_NetworkAdapterConfiguration.IPSubnet
- Win32_NetworkAdapterConfiguration.IPUseZeroBroadcast
- Win32_NetworkAdapterConfiguration.IPXAddress
- Win32_NetworkAdapterConfiguration.IPXEnabled
- Win32_NetworkAdapterConfiguration.IPXFrameType
- Win32_NetworkAdapterConfiguration.IPXMediaType
- Win32_NetworkAdapterConfiguration.IPXNetworkNumber
- Win32_NetworkAdapterConfiguration.IPXVirtualNetNumber
- Win32_NetworkAdapterConfiguration.KeepAliveInterval
- Win32_NetworkAdapterConfiguration.KeepAliveTime
- Win32_NetworkAdapterConfiguration.MACAddress
- Win32_NetworkAdapterConfiguration.MTU
- Win32_NetworkAdapterConfiguration.NumForwardPackets
- Win32_NetworkAdapterConfiguration.PMTUBHDetectEnabled
- Win32_NetworkAdapterConfiguration.PMTUDiscoveryEnabled
- Win32_NetworkAdapterConfiguration.ServiceName
- Win32_NetworkAdapterConfiguration.TcpipNetbiosOptions
- Win32_NetworkAdapterConfiguration.TcpMaxConnectRetransmissions
- Win32_NetworkAdapterConfiguration.TcpMaxDataRetransmissions
- Win32_NetworkAdapterConfiguration.TcpNumConnections
- Win32_NetworkAdapterConfiguration.TcpUseRFC1122UrgentPointer
- Win32_NetworkAdapterConfiguration.TcpWindowSize
- Win32_NetworkAdapterConfiguration.WINSEnableLMHostsLookup
- Win32_NetworkAdapterConfiguration.WINSHostLookupFile
- Win32_NetworkAdapterConfiguration.WINSPrimaryServer
- Win32_NetworkAdapterConfiguration.WINSScopeID
- Win32_NetworkAdapterConfiguration.WINSSecondaryServer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e93ae76ae3c4880c7ad041e6e90d39f1b22820d3
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153577"
---
# <a name="win32_networkadapterconfiguration-class"></a><span data-ttu-id="d1657-104">\_Класс Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1657-104">Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d1657-105">Класс **WMI \_ NetworkAdapterConfiguration** [инструментария](../wmisdk/retrieving-a-class.md) Win32 представляет атрибуты и поведение сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="d1657-105">The **Win32\_NetworkAdapterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the attributes and behaviors of a network adapter.</span></span> <span data-ttu-id="d1657-106">Этот класс включает дополнительные свойства и методы, которые поддерживают управление протоколом TCP/IP, который не зависит от сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="d1657-106">This class includes extra properties and methods that support the management of the TCP/IP protocol that are independent from the network adapter.</span></span>

<span data-ttu-id="d1657-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d1657-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d1657-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="d1657-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1657-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1657-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C515-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  boolean  ArpAlwaysSourceRoute;
  boolean  ArpUseEtherSNAP;
  string   DatabasePath;
  boolean  DeadGWDetectEnabled;
  string   DefaultIPGateway[];
  uint8    DefaultTOS;
  uint8    DefaultTTL;
  boolean  DHCPEnabled;
  datetime DHCPLeaseExpires;
  datetime DHCPLeaseObtained;
  string   DHCPServer;
  string   DNSDomain;
  string   DNSDomainSuffixSearchOrder[];
  boolean  DNSEnabledForWINSResolution;
  string   DNSHostName;
  string   DNSServerSearchOrder[];
  boolean  DomainDNSRegistrationEnabled;
  uint32   ForwardBufferMemory;
  boolean  FullDNSRegistrationEnabled;
  uint16   GatewayCostMetric[];
  uint8    IGMPLevel;
  uint32   Index;
  uint32   InterfaceIndex;
  string   IPAddress[];
  uint32   IPConnectionMetric;
  boolean  IPEnabled;
  boolean  IPFilterSecurityEnabled;
  boolean  IPPortSecurityEnabled;
  string   IPSecPermitIPProtocols[];
  string   IPSecPermitTCPPorts[];
  string   IPSecPermitUDPPorts[];
  string   IPSubnet[];
  boolean  IPUseZeroBroadcast;
  string   IPXAddress;
  boolean  IPXEnabled;
  uint32   IPXFrameType[];
  uint32   IPXMediaType;
  string   IPXNetworkNumber[];
  string   IPXVirtualNetNumber;
  uint32   KeepAliveInterval;
  uint32   KeepAliveTime;
  string   MACAddress;
  uint32   MTU;
  uint32   NumForwardPackets;
  boolean  PMTUBHDetectEnabled;
  boolean  PMTUDiscoveryEnabled;
  string   ServiceName;
  uint32   TcpipNetbiosOptions;
  uint32   TcpMaxConnectRetransmissions;
  uint32   TcpMaxDataRetransmissions;
  uint32   TcpNumConnections;
  boolean  TcpUseRFC1122UrgentPointer;
  uint16   TcpWindowSize;
  boolean  WINSEnableLMHostsLookup;
  string   WINSHostLookupFile;
  string   WINSPrimaryServer;
  string   WINSScopeID;
  string   WINSSecondaryServer;
};
```

## <a name="members"></a><span data-ttu-id="d1657-110">Члены</span><span class="sxs-lookup"><span data-stu-id="d1657-110">Members</span></span>

<span data-ttu-id="d1657-111">Класс **Win32 \_ NetworkAdapterConfiguration** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d1657-111">The **Win32\_NetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="d1657-112">Методы</span><span class="sxs-lookup"><span data-stu-id="d1657-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d1657-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1657-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d1657-114">Методы</span><span class="sxs-lookup"><span data-stu-id="d1657-114">Methods</span></span>

<span data-ttu-id="d1657-115">Класс **Win32 \_ NetworkAdapterConfiguration** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d1657-115">The **Win32\_NetworkAdapterConfiguration** class has these methods.</span></span>



| <span data-ttu-id="d1657-116">Метод</span><span class="sxs-lookup"><span data-stu-id="d1657-116">Method</span></span>                                                                                                                       | <span data-ttu-id="d1657-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d1657-117">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1657-118">**дисаблеипсек**</span><span class="sxs-lookup"><span data-stu-id="d1657-118">**DisableIPSec**</span></span>](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="d1657-119">Отключает протокол IPsec на этом сетевом адаптере с поддержкой TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d1657-119">Disables IPsec on this TCP/IP-enabled network adapter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="d1657-120">**EnableDHCP**</span><span class="sxs-lookup"><span data-stu-id="d1657-120">**EnableDHCP**</span></span>](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="d1657-121">Включает протокол DHCP для службы с этим сетевым адаптером.</span><span class="sxs-lookup"><span data-stu-id="d1657-121">Enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span><br/>                                              |
| [<span data-ttu-id="d1657-122">**енабледнс**</span><span class="sxs-lookup"><span data-stu-id="d1657-122">**EnableDNS**</span></span>](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | <span data-ttu-id="d1657-123">Включает службу доменных имен (DNS) для службы на этом сетевом адаптере, привязанном к TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d1657-123">Enables the Domain Name System (DNS) for service on this TCP/IP-bound network adapter.</span></span><br/>                                                     |
| [<span data-ttu-id="d1657-124">**енаблеипфилтерсек**</span><span class="sxs-lookup"><span data-stu-id="d1657-124">**EnableIPFilterSec**</span></span>](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="d1657-125">Включает протокол IPsec глобально для всех сетевых адаптеров, привязанных к IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="d1657-125">Enables IPsec globally across all IP-bound network adapters.</span></span><br/>                                                                               |
| [<span data-ttu-id="d1657-126">**енаблеипсек**</span><span class="sxs-lookup"><span data-stu-id="d1657-126">**EnableIPSec**</span></span>](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="d1657-127">Включает протокол IPsec для этого конкретного сетевого адаптера с поддержкой TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d1657-127">Enables IPsec on this specific TCP/IP-enabled network adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="d1657-128">**EnableStatic**</span><span class="sxs-lookup"><span data-stu-id="d1657-128">**EnableStatic**</span></span>](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="d1657-129">Включает статическую адресацию TCP/IP для целевого сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="d1657-129">Enables static TCP/IP addressing for the target network adapter.</span></span><br/>                                                                           |
| [<span data-ttu-id="d1657-130">**Свойство enablewins**</span><span class="sxs-lookup"><span data-stu-id="d1657-130">**EnableWINS**</span></span>](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="d1657-131">Включение параметров WINS, относящихся к TCP/IP, но независимо от сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="d1657-131">Enables WINS settings specific to TCP/IP, but independent of the network adapter.</span></span><br/>                                                          |
| [<span data-ttu-id="d1657-132">**ReleaseDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="d1657-132">**ReleaseDHCPLease**</span></span>](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="d1657-133">Освобождает IP-адрес, привязанный к определенному сетевому адаптеру с поддержкой DHCP.</span><span class="sxs-lookup"><span data-stu-id="d1657-133">Releases the IP address bound to a specific DHCP-enabled network adapter.</span></span><br/>                                                                  |
| [<span data-ttu-id="d1657-134">**ReleaseDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="d1657-134">**ReleaseDHCPLeaseAll**</span></span>](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | <span data-ttu-id="d1657-135">Освобождает IP-адреса, привязанные ко всем сетевым адаптерам с поддержкой DHCP.</span><span class="sxs-lookup"><span data-stu-id="d1657-135">Releases the IP addresses bound to all DHCP-enabled network adapters.</span></span><br/>                                                                      |
| [<span data-ttu-id="d1657-136">**RenewDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="d1657-136">**RenewDHCPLease**</span></span>](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | <span data-ttu-id="d1657-137">Обновляет IP-адрес на конкретных сетевых адаптерах с поддержкой DHCP.</span><span class="sxs-lookup"><span data-stu-id="d1657-137">Renews the IP address on specific DHCP-enabled network adapters.</span></span><br/>                                                                           |
| [<span data-ttu-id="d1657-138">**RenewDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="d1657-138">**RenewDHCPLeaseAll**</span></span>](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="d1657-139">Обновляет IP-адреса на всех сетевых адаптерах с поддержкой DHCP.</span><span class="sxs-lookup"><span data-stu-id="d1657-139">Renews the IP addresses on all DHCP-enabled network adapters.</span></span><br/>                                                                              |
| [<span data-ttu-id="d1657-140">**сетарпалвайссаурцерауте**</span><span class="sxs-lookup"><span data-stu-id="d1657-140">**SetArpAlwaysSourceRoute**</span></span>](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="d1657-141">Задает передачу запросов ARP по протоколу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d1657-141">Sets the transmission of ARP queries by the TCP/IP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="d1657-142">**сетарпусисерснап**</span><span class="sxs-lookup"><span data-stu-id="d1657-142">**SetArpUseEtherSNAP**</span></span>](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | <span data-ttu-id="d1657-143">Позволяет использовать пакеты Ethernet для кодирования привязки 802,3.</span><span class="sxs-lookup"><span data-stu-id="d1657-143">Enables Ethernet packets to use 802.3 SNAP encoding.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d1657-144">**сетдатабасепас**</span><span class="sxs-lookup"><span data-stu-id="d1657-144">**SetDatabasePath**</span></span>](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="d1657-145">Задает путь к стандартным файлам базы данных Интернета (узлы, файлы LMHOSTS, сети и ПРОТОКОЛы).</span><span class="sxs-lookup"><span data-stu-id="d1657-145">Sets the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span><br/>                                           |
| [<span data-ttu-id="d1657-146">**сетдеадгвдетект**</span><span class="sxs-lookup"><span data-stu-id="d1657-146">**SetDeadGWDetect**</span></span>](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="d1657-147">Включает обнаружение неработающих шлюзов.</span><span class="sxs-lookup"><span data-stu-id="d1657-147">Enables dead gateway detection.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="d1657-148">**сетдефаулттос**</span><span class="sxs-lookup"><span data-stu-id="d1657-148">**SetDefaultTOS**</span></span>](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="d1657-149">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="d1657-149">Obsolete.</span></span> <span data-ttu-id="d1657-150">Этот метод задает значение типа службы (TOS) по умолчанию в заголовке исходящих пакетов IP.</span><span class="sxs-lookup"><span data-stu-id="d1657-150">This method sets the default Type of Service (TOS) value in the header of outgoing IP packets.</span></span><br/>                                   |
| [<span data-ttu-id="d1657-151">**сетдефаултттл**</span><span class="sxs-lookup"><span data-stu-id="d1657-151">**SetDefaultTTL**</span></span>](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="d1657-152">Задает значение срока жизни (TTL) по умолчанию в заголовке исходящих пакетов IP.</span><span class="sxs-lookup"><span data-stu-id="d1657-152">Sets the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span><br/>                                                            |
| [<span data-ttu-id="d1657-153">**SetDNSDomain**</span><span class="sxs-lookup"><span data-stu-id="d1657-153">**SetDNSDomain**</span></span>](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="d1657-154">Задает домен DNS.</span><span class="sxs-lookup"><span data-stu-id="d1657-154">Sets the DNS domain.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="d1657-155">**сетднссерверсеарчордер**</span><span class="sxs-lookup"><span data-stu-id="d1657-155">**SetDNSServerSearchOrder**</span></span>](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="d1657-156">Задает порядок поиска сервера в виде массива элементов.</span><span class="sxs-lookup"><span data-stu-id="d1657-156">Sets the server search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="d1657-157">**сетднссуффикссеарчордер**</span><span class="sxs-lookup"><span data-stu-id="d1657-157">**SetDNSSuffixSearchOrder**</span></span>](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="d1657-158">Задает порядок поиска суффиксов в виде массива элементов.</span><span class="sxs-lookup"><span data-stu-id="d1657-158">Sets the suffix search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="d1657-159">**сетдинамикднсрегистратион**</span><span class="sxs-lookup"><span data-stu-id="d1657-159">**SetDynamicDNSRegistration**</span></span>](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | <span data-ttu-id="d1657-160">Указывает динамическую регистрацию DNS IP-адресов для этого адаптера, привязанного к IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="d1657-160">Indicates dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span><br/>                                                              |
| [<span data-ttu-id="d1657-161">**сетфорвардбуффермемори**</span><span class="sxs-lookup"><span data-stu-id="d1657-161">**SetForwardBufferMemory**</span></span>](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | <span data-ttu-id="d1657-162">Указывает, сколько IP-адресов памяти выделяется для хранения данных пакетов в очереди пакетов маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="d1657-162">Specifies how much memory IP allocates to store packet data in the router packet queue.</span></span><br/>                                                    |
| [<span data-ttu-id="d1657-163">**сетгатевайс**</span><span class="sxs-lookup"><span data-stu-id="d1657-163">**SetGateways**</span></span>](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="d1657-164">Указывает список шлюзов для пакетов маршрутизации, предназначенных для другой подсети, к которой подключен этот адаптер.</span><span class="sxs-lookup"><span data-stu-id="d1657-164">Specifies a list of gateways for routing packets destined for a different subnet than the one this adapter is connected to.</span></span><br/>                |
| [<span data-ttu-id="d1657-165">**сетигмплевел**</span><span class="sxs-lookup"><span data-stu-id="d1657-165">**SetIGMPLevel**</span></span>](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="d1657-166">Задает степень, с которой система поддерживает многоадресную рассылку IP-адресов и участвует в протоколе управления группами Интернета.</span><span class="sxs-lookup"><span data-stu-id="d1657-166">Sets the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span><br/>                   |
| [<span data-ttu-id="d1657-167">**сетипконнектионметрик**</span><span class="sxs-lookup"><span data-stu-id="d1657-167">**SetIPConnectionMetric**</span></span>](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="d1657-168">Задает метрику маршрутизации, связанную с этим адаптером, привязанным к IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="d1657-168">Sets the routing metric associated with this IP-bound adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="d1657-169">**сетипусезероброадкаст**</span><span class="sxs-lookup"><span data-stu-id="d1657-169">**SetIPUseZeroBroadcast**</span></span>](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="d1657-170">Задает использование IP-адресов без широковещательной рассылки.</span><span class="sxs-lookup"><span data-stu-id="d1657-170">Sets IP zero broadcast usage.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="d1657-171">**сетипксфраметипенетворкпаирс**</span><span class="sxs-lookup"><span data-stu-id="d1657-171">**SetIPXFrameTypeNetworkPairs**</span></span>](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | <span data-ttu-id="d1657-172">Задает пары номеров или кадров сетевого протокола IPX для этого сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="d1657-172">Sets Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span><br/>                                            |
| [<span data-ttu-id="d1657-173">**сетипксвиртуалнетворкнумбер**</span><span class="sxs-lookup"><span data-stu-id="d1657-173">**SetIPXVirtualNetworkNumber**</span></span>](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | <span data-ttu-id="d1657-174">Задает номер виртуальной сети сетевого обмена пакетами (IPX) на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="d1657-174">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span><br/>                                       |
| [<span data-ttu-id="d1657-175">**сеткипаливеинтервал**</span><span class="sxs-lookup"><span data-stu-id="d1657-175">**SetKeepAliveInterval**</span></span>](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="d1657-176">Задает интервал между повторными передачами проверки активности до получения ответа.</span><span class="sxs-lookup"><span data-stu-id="d1657-176">Sets the interval separating Keep Alive Retransmissions until a response is received.</span></span><br/>                                                      |
| [<span data-ttu-id="d1657-177">**сеткипаливетиме**</span><span class="sxs-lookup"><span data-stu-id="d1657-177">**SetKeepAliveTime**</span></span>](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="d1657-178">Задает частоту, с которой TCP пытается проверить, что неактивное подключение по-прежнему доступно, отправив пакет проверки активности.</span><span class="sxs-lookup"><span data-stu-id="d1657-178">Sets how often TCP attempts to verify that an idle connection is still available by sending a Keep Alive packet.</span></span><br/>                           |
| [<span data-ttu-id="d1657-179">**сетмту**</span><span class="sxs-lookup"><span data-stu-id="d1657-179">**SetMTU**</span></span>](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | <span data-ttu-id="d1657-180">Задает для сетевого интерфейса максимальное значение по умолчанию (MTU).</span><span class="sxs-lookup"><span data-stu-id="d1657-180">Sets the default Maximum Transmission Unit (MTU) for a network interface.</span></span><br/> <span data-ttu-id="d1657-181">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d1657-181">This method is not supported.</span></span><br/>                         |
| [<span data-ttu-id="d1657-182">**сетнумфорвардпаккетс**</span><span class="sxs-lookup"><span data-stu-id="d1657-182">**SetNumForwardPackets**</span></span>](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="d1657-183">Задает число заголовков IP-пакетов, выделенных для очереди пакетов маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="d1657-183">Sets the number of IP packet headers allocated for the router packet queue.</span></span><br/>                                                                |
| [<span data-ttu-id="d1657-184">**сетпмтубхдетект**</span><span class="sxs-lookup"><span data-stu-id="d1657-184">**SetPMTUBHDetect**</span></span>](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="d1657-185">Включает обнаружение маршрутизаторов-черных дыр.</span><span class="sxs-lookup"><span data-stu-id="d1657-185">Enables detection of Black Hole routers.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="d1657-186">**сетпмтудисковери**</span><span class="sxs-lookup"><span data-stu-id="d1657-186">**SetPMTUDiscovery**</span></span>](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="d1657-187">Включает обнаружение максимального блока передачи (MTU).</span><span class="sxs-lookup"><span data-stu-id="d1657-187">Enables Maximum Transmission Unit (MTU) discovery.</span></span><br/>                                                                                         |
| [<span data-ttu-id="d1657-188">**сетткпипнетбиос**</span><span class="sxs-lookup"><span data-stu-id="d1657-188">**SetTcpipNetbios**</span></span>](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="d1657-189">Задает используемую по умолчанию операцию NetBIOS через TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d1657-189">Sets the default operation of NetBIOS over TCP/IP.</span></span><br/>                                                                                         |
| [<span data-ttu-id="d1657-190">**сетткпмаксконнектретрансмиссионс**</span><span class="sxs-lookup"><span data-stu-id="d1657-190">**SetTcpMaxConnectRetransmissions**</span></span>](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | <span data-ttu-id="d1657-191">Задает число попыток, по истечении которых TCP будет повторно передавать запрос на подключение, прежде чем прервать выполнение.</span><span class="sxs-lookup"><span data-stu-id="d1657-191">Sets the number of attempts TCP will retransmit a connect request before aborting.</span></span><br/>                                                         |
| [<span data-ttu-id="d1657-192">**сетткпмаксдатаретрансмиссионс**</span><span class="sxs-lookup"><span data-stu-id="d1657-192">**SetTcpMaxDataRetransmissions**</span></span>](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | <span data-ttu-id="d1657-193">Задает число повторных попыток передачи отдельного сегмента данных, передаваемых TCP, перед прерыванием соединения.</span><span class="sxs-lookup"><span data-stu-id="d1657-193">Sets the number of times TCP will retransmit an individual data segment before aborting the connection.</span></span><br/>                                    |
| [<span data-ttu-id="d1657-194">**сетткпнумконнектионс**</span><span class="sxs-lookup"><span data-stu-id="d1657-194">**SetTcpNumConnections**</span></span>](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="d1657-195">Задает максимальное число подключений, которые TCP может открыть одновременно.</span><span class="sxs-lookup"><span data-stu-id="d1657-195">Sets the maximum number of connections that TCP may have open simultaneously.</span></span><br/>                                                              |
| [<span data-ttu-id="d1657-196">**SetTcpUseRFC1122UrgentPointer**</span><span class="sxs-lookup"><span data-stu-id="d1657-196">**SetTcpUseRFC1122UrgentPointer**</span></span>](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | <span data-ttu-id="d1657-197">Указывает, использует ли TCP спецификацию RFC 1122 для срочных данных или режим, используемый в производных системах проектирования программного обеспечения (BSD).</span><span class="sxs-lookup"><span data-stu-id="d1657-197">Specifies whether TCP uses the RFC 1122 specification for urgent data, or the mode used by Berkeley Software Design (BSD) derived systems.</span></span><br/> |
| [<span data-ttu-id="d1657-198">**сетткпвиндовсизе**</span><span class="sxs-lookup"><span data-stu-id="d1657-198">**SetTcpWindowSize**</span></span>](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="d1657-199">Задает максимальный размер окна приема TCP, предлагаемый системой.</span><span class="sxs-lookup"><span data-stu-id="d1657-199">Sets the maximum TCP Receive Window size offered by the system.</span></span><br/>                                                                            |
| [<span data-ttu-id="d1657-200">**сетвинссервер**</span><span class="sxs-lookup"><span data-stu-id="d1657-200">**SetWINSServer**</span></span>](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="d1657-201">Задает основной и дополнительный серверы Windows Internet Служба именования (WINS) в этом сетевом адаптере, привязанном к TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d1657-201">Sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="d1657-202">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1657-202">Properties</span></span>

<span data-ttu-id="d1657-203">Класс **Win32 \_ NetworkAdapterConfiguration** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d1657-203">The **Win32\_NetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1657-204">**арпалвайссаурцерауте**</span><span class="sxs-lookup"><span data-stu-id="d1657-204">**ArpAlwaysSourceRoute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-205">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-207">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| арпалвайссаурцерауте")</span><span class="sxs-lookup"><span data-stu-id="d1657-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpAlwaysSourceRoute")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-208">Если **значение — true**, протокол TCP/IP передает запросы ARP с включенной маршрутизацией источника в сетях Token Ring.</span><span class="sxs-lookup"><span data-stu-id="d1657-208">If **TRUE**, TCP/IP transmits Address Resolution Protocol (ARP) queries with source routing enabled on Token Ring networks.</span></span> <span data-ttu-id="d1657-209">По умолчанию (FALSE), ARP сначала выполняет запросы без исходной маршрутизации, а затем попытается включить исходную маршрутизацию, если ответ не получен.</span><span class="sxs-lookup"><span data-stu-id="d1657-209">By default (FALSE), ARP first queries without source routing, and then retries with source routing enabled if no reply is received.</span></span> <span data-ttu-id="d1657-210">Маршрутизация источников позволяет выполнять маршрутизацию сетевых пакетов между различными типами сетей.</span><span class="sxs-lookup"><span data-stu-id="d1657-210">Source routing allows the routing of network packets across different types of networks.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-211">**арпусисерснап**</span><span class="sxs-lookup"><span data-stu-id="d1657-211">**ArpUseEtherSNAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-212">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-214">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| арпусисерснап")</span><span class="sxs-lookup"><span data-stu-id="d1657-214">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpUseEtherSNAP")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-215">Если **true**, пакеты Ethernet следуют кодировке протокола IEEE 802,3 Sub-Network Access (привязать).</span><span class="sxs-lookup"><span data-stu-id="d1657-215">If **TRUE**, Ethernet packets follow the IEEE 802.3 Sub-Network Access Protocol (SNAP) encoding.</span></span> <span data-ttu-id="d1657-216">Установка для этого параметра значения 1 заставляет TCP/IP передавать пакеты Ethernet с помощью кодировки привязки 802,3.</span><span class="sxs-lookup"><span data-stu-id="d1657-216">Setting this parameter to 1 forces TCP/IP to transmit Ethernet packets by using 802.3 SNAP encoding.</span></span> <span data-ttu-id="d1657-217">По умолчанию (FALSE) стек передает пакеты в формате Ethernet DIX.</span><span class="sxs-lookup"><span data-stu-id="d1657-217">By default (FALSE), the stack transmits packets in DIX Ethernet format.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-218">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d1657-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-221">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d1657-221">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d1657-222">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="d1657-222">Short textual description of the current object.</span></span>

<span data-ttu-id="d1657-223">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d1657-223">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1657-224">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="d1657-224">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-227">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| DatabasePath")</span><span class="sxs-lookup"><span data-stu-id="d1657-227">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DatabasePath")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-228">Допустимый путь к файлам Windows для стандартных файлов базы данных Интернета (узлы, файлы LMHOSTS, сети и ПРОТОКОЛы).</span><span class="sxs-lookup"><span data-stu-id="d1657-228">Valid Windows file path to standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span> <span data-ttu-id="d1657-229">Путь к файлу используется интерфейсом сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="d1657-229">The file path is used by the Windows Sockets interface.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-230">**деадгвдетектенаблед**</span><span class="sxs-lookup"><span data-stu-id="d1657-230">**DeadGWDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-231">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-233">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| енабледеадгвдетект")</span><span class="sxs-lookup"><span data-stu-id="d1657-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDeadGWDetect")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-234">Если **значение равно true**, происходит обнаружение недоставленных шлюзов.</span><span class="sxs-lookup"><span data-stu-id="d1657-234">If **TRUE**, dead gateway detection occurs.</span></span> <span data-ttu-id="d1657-235">Если эта функция включена, протокол TCP запрашивает переключение IP-адреса на резервный шлюз, если он несколько раз пересылает сегмент, не получая ответа.</span><span class="sxs-lookup"><span data-stu-id="d1657-235">With this feature enabled, Transmission Control Protocol (TCP) asks Internet Protocol (IP) to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-236">**DefaultIPGateway**</span><span class="sxs-lookup"><span data-stu-id="d1657-236">**DefaultIPGateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-237">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d1657-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1657-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-239">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| DefaultGateway")</span><span class="sxs-lookup"><span data-stu-id="d1657-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|DefaultGateway")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-240">Массив IP-адресов шлюзов по умолчанию, которые использует компьютерная система.</span><span class="sxs-lookup"><span data-stu-id="d1657-240">Array of IP addresses of default gateways that the computer system uses.</span></span>

<span data-ttu-id="d1657-241">Пример: "192.168.12.1 192.168.46.1"</span><span class="sxs-lookup"><span data-stu-id="d1657-241">Example: "192.168.12.1 192.168.46.1"</span></span>

</dd> <dt>

<span data-ttu-id="d1657-242">**дефаулттос**</span><span class="sxs-lookup"><span data-stu-id="d1657-242">**DefaultTOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-243">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d1657-243">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-245">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| дефаулттос")</span><span class="sxs-lookup"><span data-stu-id="d1657-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTOS")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-246">Значение типа службы (TOS) по умолчанию, заданное в заголовке исходящих пакетов IP.</span><span class="sxs-lookup"><span data-stu-id="d1657-246">Default Type Of Service (TOS) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="d1657-247">Для запроса комментариев (RFC) 791 определяются значения.</span><span class="sxs-lookup"><span data-stu-id="d1657-247">Request for Comments (RFC) 791 defines the values.</span></span> <span data-ttu-id="d1657-248">Значение по умолчанию: 0 (ноль), допустимый диапазон: 0-255.</span><span class="sxs-lookup"><span data-stu-id="d1657-248">Default: 0 (zero), Valid Range: 0 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-249">**DefaultTTL**</span><span class="sxs-lookup"><span data-stu-id="d1657-249">**DefaultTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-250">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d1657-250">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-252">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| DefaultTTL")</span><span class="sxs-lookup"><span data-stu-id="d1657-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTTL")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-253">Значение срока жизни (TTL) по умолчанию, заданное в заголовке исходящих пакетов IP.</span><span class="sxs-lookup"><span data-stu-id="d1657-253">Default Time To Live (TTL) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="d1657-254">TTL указывает число маршрутизаторов, через которые может пройти IP-пакет, чтобы достичь его назначения, прежде чем будет удалено.</span><span class="sxs-lookup"><span data-stu-id="d1657-254">The TTL specifies the number of routers an IP packet can pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="d1657-255">Каждый маршрутизатор уменьшается на единицу TTL по мере прохождения пакета и отбрасывает пакеты, если TTL равен 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="d1657-255">Each router decrements by one the TTL count of a packet as it passes through and discards the packets—if the TTL is 0 (zero).</span></span> <span data-ttu-id="d1657-256">Значение по умолчанию: 32, допустимый диапазон: 1-255.</span><span class="sxs-lookup"><span data-stu-id="d1657-256">Default: 32, Valid Range: 1 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-257">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d1657-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1657-260">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="d1657-260">Textual description of the current object.</span></span>

<span data-ttu-id="d1657-261">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d1657-261">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1657-262">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="d1657-262">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-263">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-263">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-265">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP")</span><span class="sxs-lookup"><span data-stu-id="d1657-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|EnableDHCP")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-266">Если **значение — true**, сервер DHCP автоматически назначает IP-адрес компьютерной системе при установлении сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="d1657-266">If **TRUE**, the dynamic host configuration protocol (DHCP) server automatically assigns an IP address to the computer system when establishing a network connection.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-267">**дхкплеасикспирес**</span><span class="sxs-lookup"><span data-stu-id="d1657-267">**DHCPLeaseExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-268">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1657-268">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-270">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| леасетерминатестиме")</span><span class="sxs-lookup"><span data-stu-id="d1657-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseTerminatesTime")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-271">Дата и время истечения срока действия IP-адреса, назначенного компьютеру сервером протокола динамической настройки узлов (DHCP).</span><span class="sxs-lookup"><span data-stu-id="d1657-271">Expiration date and time for a leased IP address that was assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="d1657-272">Пример: 20521201000230,000000000</span><span class="sxs-lookup"><span data-stu-id="d1657-272">Example: 20521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="d1657-273">**дхкплеасеобтаинед**</span><span class="sxs-lookup"><span data-stu-id="d1657-273">**DHCPLeaseObtained**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-274">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1657-274">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-276">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| леасеобтаинедтиме")</span><span class="sxs-lookup"><span data-stu-id="d1657-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseObtainedTime")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-277">Дата и время получения аренды IP-адреса, назначенного компьютеру сервером DHCP.</span><span class="sxs-lookup"><span data-stu-id="d1657-277">Date and time the lease was obtained for the IP address assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="d1657-278">Пример: 19521201000230,000000000</span><span class="sxs-lookup"><span data-stu-id="d1657-278">Example: 19521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="d1657-279">**DHCPServer**</span><span class="sxs-lookup"><span data-stu-id="d1657-279">**DHCPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-280">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-282">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| DhcpServer")</span><span class="sxs-lookup"><span data-stu-id="d1657-282">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|DhcpServer")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-283">IP-адрес DHCP-сервера.</span><span class="sxs-lookup"><span data-stu-id="d1657-283">IP address of the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="d1657-284">Пример: "10.55.34.2"</span><span class="sxs-lookup"><span data-stu-id="d1657-284">Example: "10.55.34.2"</span></span>

</dd> <dt>

<span data-ttu-id="d1657-285">**DNSDomain**</span><span class="sxs-lookup"><span data-stu-id="d1657-285">**DNSDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-288">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| domain")</span><span class="sxs-lookup"><span data-stu-id="d1657-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-289">Название организации, за которой следует точка и расширение, указывающее тип организации, например "microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="d1657-289">Organization name followed by a period and an extension that indicates the type of organization, such as "microsoft.com".</span></span> <span data-ttu-id="d1657-290">Имя может быть любым сочетанием букв от A до Z, цифрами от 0 до 9 и дефисом (-), а также символа точки (.), используемого в качестве разделителя.</span><span class="sxs-lookup"><span data-stu-id="d1657-290">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span>

<span data-ttu-id="d1657-291">Пример: "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="d1657-291">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="d1657-292">**днсдомаинсуффикссеарчордер**</span><span class="sxs-lookup"><span data-stu-id="d1657-292">**DNSDomainSuffixSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-293">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d1657-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1657-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-295">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| сеарчлист")</span><span class="sxs-lookup"><span data-stu-id="d1657-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|SearchList")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-296">Массив DNS-суффиксов доменов, добавляемых к концу имен узлов во время разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="d1657-296">Array of DNS domain suffixes to be appended to the end of host names during name resolution.</span></span> <span data-ttu-id="d1657-297">При попытке разрешить полное доменное имя (FQDN) из имени только для узла система сначала добавит имя локального домена.</span><span class="sxs-lookup"><span data-stu-id="d1657-297">When attempting to resolve a fully qualified domain name (FQDN) from a host-only name, the system will first append the local domain name.</span></span> <span data-ttu-id="d1657-298">Если это не удалось, система будет использовать список суффиксов домена для создания дополнительных полных доменных имен в указанном порядке и запроса DNS-серверов для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="d1657-298">If this is not successful, the system will use the domain suffix list to create additional FQDNs in the order listed and query DNS servers for each.</span></span>

<span data-ttu-id="d1657-299">Пример: "samples.microsoft.com example.microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="d1657-299">Example: "samples.microsoft.com example.microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="d1657-300">**днсенабледфорвинсресолутион**</span><span class="sxs-lookup"><span data-stu-id="d1657-300">**DNSEnabledForWINSResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-301">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-303">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| енабледнс")</span><span class="sxs-lookup"><span data-stu-id="d1657-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDNS")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-304">Если **значение — true**, служба доменных имен (DNS) включает разрешение имен по разрешению Windows Internet служба ИМЕНОВАНИЯ (WINS).</span><span class="sxs-lookup"><span data-stu-id="d1657-304">If **TRUE**, the Domain Name System (DNS) is enabled for name resolution over Windows Internet Naming Service (WINS) resolution.</span></span> <span data-ttu-id="d1657-305">Если имя не удается разрешить с помощью DNS, запрос имени перенаправляется в WINS для разрешения.</span><span class="sxs-lookup"><span data-stu-id="d1657-305">If the name cannot be resolved using DNS, the name request is forwarded to WINS for resolution.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-306">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="d1657-306">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-309">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Параметры \| HostName")</span><span class="sxs-lookup"><span data-stu-id="d1657-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Hostname")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-310">Имя узла, используемое для идентификации локального компьютера для проверки подлинности некоторыми служебными программами.</span><span class="sxs-lookup"><span data-stu-id="d1657-310">Host name used to identify the local computer for authentication by some utilities.</span></span> <span data-ttu-id="d1657-311">Другие служебные программы на основе TCP/IP могут использовать это значение для получения имени локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="d1657-311">Other TCP/IP-based utilities can use this value to acquire the name of the local computer.</span></span> <span data-ttu-id="d1657-312">Имена узлов хранятся на DNS-серверах в таблице, которая сопоставляет имена с IP-адресами, используемыми службой DNS.</span><span class="sxs-lookup"><span data-stu-id="d1657-312">Host names are stored on DNS servers in a table that maps names to IP addresses for use by DNS.</span></span> <span data-ttu-id="d1657-313">Имя может быть любым сочетанием букв от A до Z, цифрами от 0 до 9 и дефисом (-), а также символа точки (.), используемого в качестве разделителя.</span><span class="sxs-lookup"><span data-stu-id="d1657-313">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span> <span data-ttu-id="d1657-314">По умолчанию это имя компьютера сети Microsoft, но администратор сети может назначить другое имя узла, не влияя на имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="d1657-314">By default, this value is the Microsoft networking computer name, but the network administrator can assign another host name without affecting the computer name.</span></span>

<span data-ttu-id="d1657-315">Пример: "корпднс"</span><span class="sxs-lookup"><span data-stu-id="d1657-315">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="d1657-316">**днссерверсеарчордер**</span><span class="sxs-lookup"><span data-stu-id="d1657-316">**DNSServerSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-317">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d1657-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1657-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-319">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| nameserver")</span><span class="sxs-lookup"><span data-stu-id="d1657-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NameServer")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-320">Массив IP-адресов сервера, используемых для запросов DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="d1657-320">Array of server IP addresses to be used in querying for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-321">**домаинднсрегистратионенаблед**</span><span class="sxs-lookup"><span data-stu-id="d1657-321">**DomainDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-322">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1657-324">Если задано **значение true**, IP-адреса для этого подключения регистрируются в DNS под доменным именем этого подключения, а не регистрируются в полном DNS-имени компьютера.</span><span class="sxs-lookup"><span data-stu-id="d1657-324">If **TRUE**, the IP addresses for this connection are registered in DNS under the domain name of this connection in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="d1657-325">Доменное имя этого соединения задается с помощью метода [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() или назначается DSCP.</span><span class="sxs-lookup"><span data-stu-id="d1657-325">The domain name of this connection is either set using the [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() method or assigned by DSCP.</span></span> <span data-ttu-id="d1657-326">Зарегистрированное имя — это имя узла компьютера с добавленным доменным именем.</span><span class="sxs-lookup"><span data-stu-id="d1657-326">The registered name is the host name of the computer with the domain name appended.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-327">**Параметра**</span><span class="sxs-lookup"><span data-stu-id="d1657-327">**ForwardBufferMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-328">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1657-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-330">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="d1657-330">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-331">Память, выделенная протоколом IP для хранения данных пакетов в очереди пакетов маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="d1657-331">Memory allocated by IP to store packet data in the router packet queue.</span></span> <span data-ttu-id="d1657-332">Когда это пространство буфера заполнено, маршрутизатор начинает удалять пакеты в случайном порядке из очереди.</span><span class="sxs-lookup"><span data-stu-id="d1657-332">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span> <span data-ttu-id="d1657-333">Буферы данных очереди пакетов имеют длину 256 байт, поэтому значение этого параметра должно быть кратно 256.</span><span class="sxs-lookup"><span data-stu-id="d1657-333">Packet queue data buffers are 256 bytes in length, so the value of this parameter should be a multiple of 256.</span></span> <span data-ttu-id="d1657-334">Несколько буферов объединяются в цепочку для больших пакетов.</span><span class="sxs-lookup"><span data-stu-id="d1657-334">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="d1657-335">Заголовок IP-адреса для пакета хранится отдельно.</span><span class="sxs-lookup"><span data-stu-id="d1657-335">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="d1657-336">Этот параметр игнорируется, и никакие буферы не выделяются, если IP-маршрутизатор не включен.</span><span class="sxs-lookup"><span data-stu-id="d1657-336">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="d1657-337">Размер буфера может варьироваться от MTU сети до значения меньше 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="d1657-337">The buffer size can range from the network MTU to a value smaller than 0xFFFFFFFF.</span></span> <span data-ttu-id="d1657-338">Значение по умолчанию: 74240 (50 1480-байтовых пакетов, округленное до кратного 256).</span><span class="sxs-lookup"><span data-stu-id="d1657-338">Default: 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> <dt>

<span data-ttu-id="d1657-339">**фуллднсрегистратионенаблед**</span><span class="sxs-lookup"><span data-stu-id="d1657-339">**FullDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-340">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1657-342">Если задано **значение true**, IP-адреса для этого подключения регистрируются в DNS под полным DNS-именем компьютера.</span><span class="sxs-lookup"><span data-stu-id="d1657-342">If **TRUE**, the IP addresses for this connection are registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="d1657-343">Полное DNS-имя компьютера отображается на вкладке **Сетевая идентификация** в окне Системное приложение панели управления.</span><span class="sxs-lookup"><span data-stu-id="d1657-343">The full DNS name of the computer is displayed on the **Network Identification** tab in the System application in Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-344">**гатевайкостметрик**</span><span class="sxs-lookup"><span data-stu-id="d1657-344">**GatewayCostMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-345">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d1657-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d1657-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1657-347">Массив значений метрик целочисленной стоимости (от 1 до 9999), которые будут использоваться для вычисления самых быстрых, наиболее надежных или наименее ресурсоемких маршрутов.</span><span class="sxs-lookup"><span data-stu-id="d1657-347">Array of integer cost metric values (ranging from 1 to 9999) to be used in calculating the fastest, most reliable, or least resource-intensive routes.</span></span> <span data-ttu-id="d1657-348">Этот аргумент имеет корреспонденцию "один к одному" со свойством **дефаултипгатевай** .</span><span class="sxs-lookup"><span data-stu-id="d1657-348">This argument has a one-to-one correspondence with the **DefaultIPGateway** property.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-349">**игмплевел**</span><span class="sxs-lookup"><span data-stu-id="d1657-349">**IGMPLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-350">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d1657-350">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-352">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| игмплевел")</span><span class="sxs-lookup"><span data-stu-id="d1657-352">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IGMPLevel")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-353">Область, в которой система поддерживает многоадресную рассылку IP-адресов и участвует в протоколе IGMP.</span><span class="sxs-lookup"><span data-stu-id="d1657-353">Extent to which the system supports IP multicast and participates in the Internet Group Management Protocol (IGMP).</span></span> <span data-ttu-id="d1657-354">На уровне 0 (нуль) система не обеспечивает поддержку многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="d1657-354">At level 0 (zero), the system provides no multicast support.</span></span> <span data-ttu-id="d1657-355">На уровне 1 система может только передавать пакеты IP-адресов многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="d1657-355">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="d1657-356">На уровне 2 система может отправлять пакеты многоадресной рассылки IP-адресов и полностью участвовать в протоколе IGMP для получения пакетов многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="d1657-356">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="d1657-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Без многоадресной рассылки** (0)</span><span class="sxs-lookup"><span data-stu-id="d1657-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="d1657-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**Многоадресная рассылка IP** (1)</span><span class="sxs-lookup"><span data-stu-id="d1657-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="d1657-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP-& многоадресная рассылка IGMP** (2)</span><span class="sxs-lookup"><span data-stu-id="d1657-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP & IGMP multicast** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d1657-360">Многоадресная рассылка IP и IGMP (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d1657-360">IP and IGMP Multicast (default)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1657-361">**Index**</span><span class="sxs-lookup"><span data-stu-id="d1657-361">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-362">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1657-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-364">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| класс Win32Registry системы \\ \\ \\ \\ управления CurrentControlSet \\ \\ \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="d1657-364">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-365">Номер индекса конфигурации сетевого адаптера Windows.</span><span class="sxs-lookup"><span data-stu-id="d1657-365">Index number of the Windows network adapter configuration.</span></span> <span data-ttu-id="d1657-366">Номер индекса используется, если доступно более одной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d1657-366">The index number is used when there is more than one configuration available.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-367">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="d1657-367">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-368">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1657-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1657-370">Значение индекса, уникально идентифицирующего локальный сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d1657-370">Index value that uniquely identifies a local network interface.</span></span> <span data-ttu-id="d1657-371">Значение этого свойства совпадает со значением свойства **InterfaceIndex** в экземпляре [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) , представляющем сетевой интерфейс в таблице маршрутов.</span><span class="sxs-lookup"><span data-stu-id="d1657-371">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-372">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="d1657-372">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-373">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d1657-373">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1657-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-375">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ tcpip \| IPAddress")</span><span class="sxs-lookup"><span data-stu-id="d1657-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip\|IPAddress")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-376">Массив всех IP-адресов, связанных с текущим сетевым адаптером.</span><span class="sxs-lookup"><span data-stu-id="d1657-376">Array of all of the IP addresses associated with the current network adapter.</span></span> <span data-ttu-id="d1657-377">Это свойство может содержать адреса IPv6 или IPv4.</span><span class="sxs-lookup"><span data-stu-id="d1657-377">This property can contain either IPv6 addresses or IPv4 addresses.</span></span> <span data-ttu-id="d1657-378">Дополнительные сведения см. [в разделе Поддержка IPv6 и IPv4 в WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="d1657-378">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="d1657-379">Пример IPv6-адреса: "2010:836B: 4179:: 836B: 4179"</span><span class="sxs-lookup"><span data-stu-id="d1657-379">Example IPv6 address: "2010:836B:4179::836B:4179"</span></span>

</dd> <dt>

<span data-ttu-id="d1657-380">**ипконнектионметрик**</span><span class="sxs-lookup"><span data-stu-id="d1657-380">**IPConnectionMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-381">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1657-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1657-383">Стоимость использования настроенных маршрутов для адаптера с IP-адресом и является взвешенным значением для этих маршрутов в таблице IP-маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="d1657-383">Cost of using the configured routes for the IP bound adapter and is the weighted value for those routes in the IP routing table.</span></span> <span data-ttu-id="d1657-384">При наличии нескольких маршрутов к назначению в таблице IP-маршрутизации используется маршрут с наименьшей метрикой.</span><span class="sxs-lookup"><span data-stu-id="d1657-384">If there are multiple routes to a destination in the IP routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="d1657-385">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="d1657-385">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-386">**IPEnabled**</span><span class="sxs-lookup"><span data-stu-id="d1657-386">**IPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-387">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-389">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ tcpip")</span><span class="sxs-lookup"><span data-stu-id="d1657-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-390">Если задано **значение true**, TCP/IP привязан и включен на этом сетевом адаптере.</span><span class="sxs-lookup"><span data-stu-id="d1657-390">If **TRUE**, TCP/IP is bound and enabled on this network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-391">**ипфилтерсекуритенаблед**</span><span class="sxs-lookup"><span data-stu-id="d1657-391">**IPFilterSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-392">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-392">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-394">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ипфилтерсекуритенаблед")</span><span class="sxs-lookup"><span data-stu-id="d1657-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-395">При **значении true** безопасность IP-портов включается глобально для всех сетевых адаптеров, привязанных к IP-адресу, и действуют значения безопасности, связанные с отдельными сетевыми адаптерами.</span><span class="sxs-lookup"><span data-stu-id="d1657-395">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters and the security values associated with individual network adapters are in effect.</span></span> <span data-ttu-id="d1657-396">Это свойство используется в сочетании с **ипсекпермитткппортс**, **ипсекпермитудппортс** и **ипсекпермитиппротоколс**.</span><span class="sxs-lookup"><span data-stu-id="d1657-396">This property is used in conjunction with **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts**, and **IPSecPermitIPProtocols**.</span></span> <span data-ttu-id="d1657-397">Если задано **значение false**, безопасность IP-фильтра отключается для всех сетевых адаптеров и обеспечивает нефильтрованный трафик для трафика всех портов и протоколов.</span><span class="sxs-lookup"><span data-stu-id="d1657-397">If **FALSE**, IP filter security is disabled across all network adapters and allows all port and protocol traffic to flow unfiltered.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-398">**иппортсекуритенаблед**</span><span class="sxs-lookup"><span data-stu-id="d1657-398">**IPPortSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-399">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-399">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-401">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration \| ипфилтерсекуритенаблед")</span><span class="sxs-lookup"><span data-stu-id="d1657-401">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapterConfiguration\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-402">При **значении true** безопасность IP-портов включается глобально для всех сетевых адаптеров, привязанных к IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="d1657-402">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters.</span></span> <span data-ttu-id="d1657-403">Это свойство устарело.</span><span class="sxs-lookup"><span data-stu-id="d1657-403">This property is obsolete.</span></span> <span data-ttu-id="d1657-404">Вместо этого свойства следует использовать **ипфилтерсекуритенаблед**.</span><span class="sxs-lookup"><span data-stu-id="d1657-404">In place of this property, you should use **IPFilterSecurityEnabled**.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-405">**ипсекпермитиппротоколс**</span><span class="sxs-lookup"><span data-stu-id="d1657-405">**IPSecPermitIPProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-406">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d1657-406">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1657-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-408">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| равипалловедпротоколс")</span><span class="sxs-lookup"><span data-stu-id="d1657-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|RawIPAllowedProtocols")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-409">Массив протоколов, разрешенных для запуска по IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="d1657-409">Array of the protocols permitted to run over the IP.</span></span> <span data-ttu-id="d1657-410">Список протоколов определяется с помощью метода [**енаблеипсек**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="d1657-410">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="d1657-411">Список будет либо пустым, либо содержать числовые значения.</span><span class="sxs-lookup"><span data-stu-id="d1657-411">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="d1657-412">Числовое значение 0 (ноль) означает, что разрешение на доступ предоставляется для всех протоколов.</span><span class="sxs-lookup"><span data-stu-id="d1657-412">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="d1657-413">Пустая строка указывает, что не разрешено выполнять никакие протоколы, если **ипфилтерсекуритенаблед** имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="d1657-413">An empty string indicates that no protocols are permitted to run when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-414">**ипсекпермитткппортс**</span><span class="sxs-lookup"><span data-stu-id="d1657-414">**IPSecPermitTCPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-415">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d1657-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1657-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-417">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ткпалловедпортс")</span><span class="sxs-lookup"><span data-stu-id="d1657-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TCPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-418">Массив портов, которым будет предоставлено разрешение на доступ к TCP.</span><span class="sxs-lookup"><span data-stu-id="d1657-418">Array of the ports that will be granted access permission for TCP.</span></span> <span data-ttu-id="d1657-419">Список протоколов определяется с помощью метода [**енаблеипсек**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="d1657-419">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="d1657-420">Список будет либо пустым, либо содержать числовые значения.</span><span class="sxs-lookup"><span data-stu-id="d1657-420">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="d1657-421">Числовое значение 0 (ноль) означает, что разрешение на доступ предоставляется для всех портов.</span><span class="sxs-lookup"><span data-stu-id="d1657-421">A numeric value of 0 (zero)indicates access permission is granted for all ports.</span></span> <span data-ttu-id="d1657-422">Пустая строка указывает, что нет портов, которым предоставляется разрешение на доступ, если **ипфилтерсекуритенаблед** имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="d1657-422">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-423">**ипсекпермитудппортс**</span><span class="sxs-lookup"><span data-stu-id="d1657-423">**IPSecPermitUDPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-424">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d1657-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1657-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-426">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| удпалловедпортс")</span><span class="sxs-lookup"><span data-stu-id="d1657-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UDPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-427">Массив портов, которым будет предоставлено разрешение на доступ по протоколу UDP.</span><span class="sxs-lookup"><span data-stu-id="d1657-427">Array of the ports that will be granted User Datagram Protocol (UDP) access permission.</span></span> <span data-ttu-id="d1657-428">Список протоколов определяется с помощью метода [**енаблеипсек**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="d1657-428">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="d1657-429">Список будет либо пустым, либо содержать числовые значения.</span><span class="sxs-lookup"><span data-stu-id="d1657-429">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="d1657-430">Числовое значение 0 (ноль) означает, что разрешение на доступ предоставляется для всех портов.</span><span class="sxs-lookup"><span data-stu-id="d1657-430">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="d1657-431">Пустая строка указывает, что нет портов, которым предоставляется разрешение на доступ, если **ипфилтерсекуритенаблед** имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="d1657-431">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-432">**IPSubnet**</span><span class="sxs-lookup"><span data-stu-id="d1657-432">**IPSubnet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-433">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d1657-433">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1657-434">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-435">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ службы \| Parameters \| Маска подсети")</span><span class="sxs-lookup"><span data-stu-id="d1657-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|SubnetMask")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-436">Массив всех масок подсети, связанных с текущим сетевым адаптером.</span><span class="sxs-lookup"><span data-stu-id="d1657-436">Array of all of the subnet masks associated with the current network adapter.</span></span>

<span data-ttu-id="d1657-437">Пример: 255.255.0.0</span><span class="sxs-lookup"><span data-stu-id="d1657-437">Example: "255.255.0.0"</span></span>

</dd> <dt>

<span data-ttu-id="d1657-438">**ипусезероброадкаст**</span><span class="sxs-lookup"><span data-stu-id="d1657-438">**IPUseZeroBroadcast**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-439">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-441">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| усезероброадкаст")</span><span class="sxs-lookup"><span data-stu-id="d1657-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UseZeroBroadcast")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-442">Если задано **значение true**, IP-нули — широковещательные (0.0.0.0), а в системе используются широковещательные рассылки (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="d1657-442">If **TRUE**, IP zeros-broadcasts are used (0.0.0.0), and the system uses ones-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="d1657-443">В компьютерных системах обычно используются такие широковещательные рассылки, но на основе реализаций BSD используются нулевые широковещательные рассылки.</span><span class="sxs-lookup"><span data-stu-id="d1657-443">Computer systems generally use ones-broadcasts, but those derived from BSD implementations use zeros-broadcasts.</span></span> <span data-ttu-id="d1657-444">Системы, которые не используют те же широковещательные пакеты, не будут взаимодействовать в одной сети.</span><span class="sxs-lookup"><span data-stu-id="d1657-444">Systems that do not use that same broadcasts will not interoperate on the same network.</span></span> <span data-ttu-id="d1657-445">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="d1657-445">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-446">**ипксаддресс**</span><span class="sxs-lookup"><span data-stu-id="d1657-446">**IPXAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-447">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-448">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-449">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Sockets версии 2 \| [**жетсоккопт**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ Address")</span><span class="sxs-lookup"><span data-stu-id="d1657-449">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Sockets Version 2\|[**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt)\|IPX\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-450">Технология IPX не поддерживается, и это свойство не содержит полезных данных.</span><span class="sxs-lookup"><span data-stu-id="d1657-450">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-451">**ипксенаблед**</span><span class="sxs-lookup"><span data-stu-id="d1657-451">**IPXEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-452">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-452">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-453">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-454">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d1657-454">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-455">Технология IPX не поддерживается, и это свойство не содержит полезных данных.</span><span class="sxs-lookup"><span data-stu-id="d1657-455">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-456">**ипксфраметипе**</span><span class="sxs-lookup"><span data-stu-id="d1657-456">**IPXFrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-457">Тип данных: массив **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1657-457">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="d1657-458">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-459">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ нвлнкипкс \\ \\ Parameters \| пкттипе")</span><span class="sxs-lookup"><span data-stu-id="d1657-459">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|PktType")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-460">Технология IPX не поддерживается, и это свойство не содержит полезных данных.</span><span class="sxs-lookup"><span data-stu-id="d1657-460">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="d1657-461">**Ethernet II** (0)</span><span class="sxs-lookup"><span data-stu-id="d1657-461">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="d1657-462">**Ethernet 802,3** (1)</span><span class="sxs-lookup"><span data-stu-id="d1657-462">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="d1657-463">**Ethernet 802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="d1657-463">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="d1657-464">**Оснастка Ethernet** (3)</span><span class="sxs-lookup"><span data-stu-id="d1657-464">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="d1657-465">**Авто** (255)</span><span class="sxs-lookup"><span data-stu-id="d1657-465">**AUTO** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1657-466">**ипксмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="d1657-466">**IPXMediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-467">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1657-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-468">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-469">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ нвлнкипкс \\ \\ Parameters \| mediaType")</span><span class="sxs-lookup"><span data-stu-id="d1657-469">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-470">Технология IPX не поддерживается, и это свойство не содержит полезных данных.</span><span class="sxs-lookup"><span data-stu-id="d1657-470">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="d1657-471">**Ethernet** (1)</span><span class="sxs-lookup"><span data-stu-id="d1657-471">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="d1657-472">**Token Ring** (2)</span><span class="sxs-lookup"><span data-stu-id="d1657-472">**Token ring** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="d1657-473">**FDDI** (3)</span><span class="sxs-lookup"><span data-stu-id="d1657-473">**FDDI** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="d1657-474">**АркНет** (8)</span><span class="sxs-lookup"><span data-stu-id="d1657-474">**ARCNET** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1657-475">**ипкснетворкнумбер**</span><span class="sxs-lookup"><span data-stu-id="d1657-475">**IPXNetworkNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-476">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d1657-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1657-477">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-478">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ нвлнкипкс \\ \\ Parameters \| нетворкнумбер")</span><span class="sxs-lookup"><span data-stu-id="d1657-478">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|NetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-479">Технология IPX не поддерживается, и это свойство не содержит полезных данных.</span><span class="sxs-lookup"><span data-stu-id="d1657-479">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-480">**ипксвиртуалнетнумбер**</span><span class="sxs-lookup"><span data-stu-id="d1657-480">**IPXVirtualNetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-481">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-482">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-483">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ нвлнкипкс \\ \\ Parameters \| виртуалнетворкнумбер")</span><span class="sxs-lookup"><span data-stu-id="d1657-483">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|VirtualNetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-484">Технология IPX не поддерживается, и это свойство не содержит полезных данных.</span><span class="sxs-lookup"><span data-stu-id="d1657-484">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-485">**KeepAliveInterval**</span><span class="sxs-lookup"><span data-stu-id="d1657-485">**KeepAliveInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-486">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1657-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-487">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-488">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| keepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("миллисекунды")</span><span class="sxs-lookup"><span data-stu-id="d1657-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-489">Интервал между повторными передачами проверки активности проверяется до получения ответа.</span><span class="sxs-lookup"><span data-stu-id="d1657-489">Interval separating Keep Alive Retransmissions until a response is received.</span></span> <span data-ttu-id="d1657-490">После получения ответа задержка до следующей передачи активности продолжает управляться значением **KeepAliveTime**.</span><span class="sxs-lookup"><span data-stu-id="d1657-490">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of **KeepAliveTime**.</span></span> <span data-ttu-id="d1657-491">Соединение будет прервано после того, как число повторных передач, указанных в **TcpMaxDataRetransmissions** , не ответило.</span><span class="sxs-lookup"><span data-stu-id="d1657-491">The connection will be aborted after the number of retransmissions specified by **TcpMaxDataRetransmissions** have gone unanswered.</span></span> <span data-ttu-id="d1657-492">Значение по умолчанию: 1000, допустимый диапазон: 1 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="d1657-492">Default: 1000, Valid Range: 1 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-493">**KeepAliveTime**</span><span class="sxs-lookup"><span data-stu-id="d1657-493">**KeepAliveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-494">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1657-494">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-495">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-496">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| keepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("миллисекунды")</span><span class="sxs-lookup"><span data-stu-id="d1657-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-497">Свойство **KeepAliveTime** показывает, как часто TCP пытается проверить, что неактивное соединение остается неизменным, отправив пакет проверки активности.</span><span class="sxs-lookup"><span data-stu-id="d1657-497">The **KeepAliveTime** property indicates how often the TCP attempts to verify that an idle connection is still intact by sending a Keep Alive Packet.</span></span> <span data-ttu-id="d1657-498">Доступная удаленная система будет подтверждать передачу проверки активности.</span><span class="sxs-lookup"><span data-stu-id="d1657-498">A remote system that is reachable will acknowledge the keep alive transmission.</span></span> <span data-ttu-id="d1657-499">Пакеты проверки активности не отправляются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d1657-499">Keep Alive packets are not sent by default.</span></span> <span data-ttu-id="d1657-500">Эта функция может быть включена в подключении приложения.</span><span class="sxs-lookup"><span data-stu-id="d1657-500">This feature may be enabled in a connection by an application.</span></span> <span data-ttu-id="d1657-501">По умолчанию: 7 200 000 (два часа).</span><span class="sxs-lookup"><span data-stu-id="d1657-501">Default: 7,200,000 (two hours).</span></span>

</dd> <dt>

<span data-ttu-id="d1657-502">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="d1657-502">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-503">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-504">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-505">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| входные и выходные функции устройства Win32API \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="d1657-505">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-506">MAC-адрес сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="d1657-506">Media Access Control (MAC) address of the network adapter.</span></span> <span data-ttu-id="d1657-507">Изготовитель назначает MAC-адрес для уникальной идентификации сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="d1657-507">A MAC address is assigned by the manufacturer to uniquely identify the network adapter.</span></span>

<span data-ttu-id="d1657-508">Пример: "00:80: C7:8F: 6C: 96"</span><span class="sxs-lookup"><span data-stu-id="d1657-508">Example: "00:80:C7:8F:6C:96"</span></span>

</dd> <dt>

<span data-ttu-id="d1657-509">**Максимальный передаваемый блок данных**</span><span class="sxs-lookup"><span data-stu-id="d1657-509">**MTU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-510">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1657-510">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-511">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-512">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="d1657-512">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-513">Переопределяет максимальное значение по умолчанию (MTU) для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d1657-513">Overrides the default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="d1657-514">MTU — это максимальный размер пакета (включая транспортный заголовок), который транспорт будет передавать через базовую сеть.</span><span class="sxs-lookup"><span data-stu-id="d1657-514">The MTU is the maximum packet size (including the transport header) that the transport will transmit over the underlying network.</span></span> <span data-ttu-id="d1657-515">Датаграмма IP может охватывать несколько пакетов.</span><span class="sxs-lookup"><span data-stu-id="d1657-515">The IP datagram can span multiple packets.</span></span> <span data-ttu-id="d1657-516">Диапазон этого значения охватывает минимальный размер пакета (68) до MTU, поддерживаемый базовой сетью.</span><span class="sxs-lookup"><span data-stu-id="d1657-516">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-517">**нумфорвардпаккетс**</span><span class="sxs-lookup"><span data-stu-id="d1657-517">**NumForwardPackets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-518">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1657-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-519">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-520">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| нумфорвардпаккетс")</span><span class="sxs-lookup"><span data-stu-id="d1657-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NumForwardPackets")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-521">Число заголовков IP-пакетов, выделенных для очереди пакетов маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="d1657-521">Number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="d1657-522">Если все заголовки используются, маршрутизатор начнет отбрасывать пакеты из очереди в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="d1657-522">When all headers are in use, the router will begin to discard packets from the queue at random.</span></span> <span data-ttu-id="d1657-523">Это значение должно быть не меньше значения параметра **ForwardBufferMemory** , деленного на максимальный размер данных IP-адреса сетей, подключенных к маршрутизатору.</span><span class="sxs-lookup"><span data-stu-id="d1657-523">This value should be at least as large as the **ForwardBufferMemory** value divided by the maximum IP data size of the networks connected to the router.</span></span> <span data-ttu-id="d1657-524">Оно должно быть не больше значения параметра **ForwardBufferMemory** , деленного на 256, поскольку для каждого пакета используются по крайней мере 256 байт памяти буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="d1657-524">It should be no larger than the **ForwardBufferMemory** value divided by 256, since at least 256 bytes of forward buffer memory are used for each packet.</span></span> <span data-ttu-id="d1657-525">Оптимальное число пересылаемых пакетов для заданного значения **ForwardBufferMemory** зависит от типа трафика в сети.</span><span class="sxs-lookup"><span data-stu-id="d1657-525">The optimal number of forward packets for a given **ForwardBufferMemory** size depends on the type of traffic on the network.</span></span> <span data-ttu-id="d1657-526">Эти два значения будут находиться в другом месте.</span><span class="sxs-lookup"><span data-stu-id="d1657-526">It will be somewhere between these two values.</span></span> <span data-ttu-id="d1657-527">Если маршрутизатор не включен, этот параметр пропускается и заголовки не выделяются.</span><span class="sxs-lookup"><span data-stu-id="d1657-527">If the router is not enabled, this parameter is ignored and no headers are allocated.</span></span> <span data-ttu-id="d1657-528">Значение по умолчанию: 50, допустимый диапазон: 1 — 0xFFFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="d1657-528">Default: 50, Valid Range: 1 - 0xFFFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-529">**пмтубхдетектенаблед**</span><span class="sxs-lookup"><span data-stu-id="d1657-529">**PMTUBHDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-530">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-530">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-531">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-532">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| енаблепмтубхдетект")</span><span class="sxs-lookup"><span data-stu-id="d1657-532">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUBHDetect")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-533">Если **значение — true**, обнаружение маршрутизаторов-черных дыр происходит, когда TCP обнаруживает путь к максимальной единице передачи.</span><span class="sxs-lookup"><span data-stu-id="d1657-533">If **TRUE**, detection of black hole routers occurs while TCP discovers the path of the Maximum Transmission Unit.</span></span> <span data-ttu-id="d1657-534">Маршрутизатор с черными отверстиями не возвращает сообщения с недостижимыми адресами ICMP, когда требуется фрагментировать IP-датаграмму с установленным битом «не фрагментировать».</span><span class="sxs-lookup"><span data-stu-id="d1657-534">A black hole router does not return ICMP Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="d1657-535">Протокол TCP зависит от получения этих сообщений для выполнения обнаружения MTU пути.</span><span class="sxs-lookup"><span data-stu-id="d1657-535">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span> <span data-ttu-id="d1657-536">Если эта функция включена, протокол TCP попытается отправить сегменты без установленного бита дефрагментации, если несколько повторных передач сегмента попадают в неподтвержденные.</span><span class="sxs-lookup"><span data-stu-id="d1657-536">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="d1657-537">Если сегмент подтвержден как результат, размер MSS будет уменьшен, а в будущих пакетах соединения будет установлен бит не фрагмента.</span><span class="sxs-lookup"><span data-stu-id="d1657-537">If the segment is acknowledged as a result, the MSS will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="d1657-538">Включение обнаружения "Черная дыра" увеличивает максимальное число повторных передач, выполненных для данного сегмента.</span><span class="sxs-lookup"><span data-stu-id="d1657-538">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span> <span data-ttu-id="d1657-539">Значение этого свойства по умолчанию равно **false**.</span><span class="sxs-lookup"><span data-stu-id="d1657-539">The default value of this property is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-540">**пмтудисковеренаблед**</span><span class="sxs-lookup"><span data-stu-id="d1657-540">**PMTUDiscoveryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-541">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-542">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-543">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| енаблепмтудисковери")</span><span class="sxs-lookup"><span data-stu-id="d1657-543">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUDiscovery")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-544">Если задано **значение true**, то по пути к удаленному узлу обнаруживается максимальный путь передаваемых данных (MTU).</span><span class="sxs-lookup"><span data-stu-id="d1657-544">If **TRUE**, the Maximum Transmission Unit (MTU) path is discovered over the path to a remote host.</span></span> <span data-ttu-id="d1657-545">При обнаружении пути MTU и ограничении сегментов TCP этим размером TCP может исключить фрагментацию маршрутизаторов по пути, соединяющего сети с разными MTU.</span><span class="sxs-lookup"><span data-stu-id="d1657-545">By discovering the MTU path and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="d1657-546">Фрагментация негативно влияет на пропускную способность TCP и перегрузку сети.</span><span class="sxs-lookup"><span data-stu-id="d1657-546">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="d1657-547">Если задать для этого параметра **значение false** , то для всех подключений, которые не являются компьютерами в локальной подсети, будет использоваться значение MTU в 576 байт.</span><span class="sxs-lookup"><span data-stu-id="d1657-547">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet.</span></span> <span data-ttu-id="d1657-548">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="d1657-548">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-549">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="d1657-549">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-550">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-551">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-552">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ нетворккардс \| ServiceName")</span><span class="sxs-lookup"><span data-stu-id="d1657-552">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-553">Имя службы сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="d1657-553">Service name of the network adapter.</span></span> <span data-ttu-id="d1657-554">Обычно это имя короче полного названия продукта.</span><span class="sxs-lookup"><span data-stu-id="d1657-554">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="d1657-555">Пример: "Елнкии"</span><span class="sxs-lookup"><span data-stu-id="d1657-555">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="d1657-556">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="d1657-556">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-557">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-558">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-559">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="d1657-559">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d1657-560">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="d1657-560">Identifier by which the current object is known.</span></span>

<span data-ttu-id="d1657-561">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d1657-561">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1657-562">**ткпипнетбиосоптионс**</span><span class="sxs-lookup"><span data-stu-id="d1657-562">**TcpipNetbiosOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-563">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1657-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-564">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1657-565">Битовая карта возможных параметров, связанных с NetBIOS через TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d1657-565">Bitmap of the possible settings related to NetBIOS over TCP/IP.</span></span> <span data-ttu-id="d1657-566">Значения определяются в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="d1657-566">Values are identified in the following list.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="d1657-567">**Енабленетбиосвиадхкп** (0)</span><span class="sxs-lookup"><span data-stu-id="d1657-567">**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="d1657-568">**EnableNetbios** (1)</span><span class="sxs-lookup"><span data-stu-id="d1657-568">**EnableNetbios** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="d1657-569">**Дисабленетбиос** (2)</span><span class="sxs-lookup"><span data-stu-id="d1657-569">**DisableNetbios** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1657-570">**ткпмаксконнектретрансмиссионс**</span><span class="sxs-lookup"><span data-stu-id="d1657-570">**TcpMaxConnectRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-571">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1657-571">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-572">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-573">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ткпмаксконнектретрансмиссионс")</span><span class="sxs-lookup"><span data-stu-id="d1657-573">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxConnectRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-574">Число попыток TCP повторно передать запрос на подключение перед завершением соединения.</span><span class="sxs-lookup"><span data-stu-id="d1657-574">Number of times TCP attempts to retransmit a Connect Request before terminating the connection.</span></span> <span data-ttu-id="d1657-575">Начальное время ожидания повторной передачи — 3 секунды.</span><span class="sxs-lookup"><span data-stu-id="d1657-575">The initial retransmission timeout is 3 seconds.</span></span> <span data-ttu-id="d1657-576">Время ожидания повторной передачи удваивается для каждой попытки.</span><span class="sxs-lookup"><span data-stu-id="d1657-576">The retransmission timeout doubles for each attempt.</span></span> <span data-ttu-id="d1657-577">Значение по умолчанию: 3, допустимый диапазон: 0 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="d1657-577">Default: 3, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-578">**TcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="d1657-578">**TcpMaxDataRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-579">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1657-579">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-580">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-581">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpMaxDataRetransmissions")</span><span class="sxs-lookup"><span data-stu-id="d1657-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxDataRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-582">Число раз, когда TCP пересылает отдельный сегмент данных (не сегмент соединения) перед завершением соединения.</span><span class="sxs-lookup"><span data-stu-id="d1657-582">Number of times TCP retransmits an individual data segment (nonconnect segment) before terminating the connection.</span></span> <span data-ttu-id="d1657-583">Время ожидания повторной передачи удваивается при каждой последующей повторной передаче соединения.</span><span class="sxs-lookup"><span data-stu-id="d1657-583">The retransmission timeout doubles with each successive retransmission on a connection.</span></span> <span data-ttu-id="d1657-584">Значение по умолчанию: 5, допустимый диапазон: 0 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="d1657-584">Default: 5, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-585">**ткпнумконнектионс**</span><span class="sxs-lookup"><span data-stu-id="d1657-585">**TcpNumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-586">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1657-586">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-587">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-587">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-588">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ткпнумконнектионс")</span><span class="sxs-lookup"><span data-stu-id="d1657-588">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpNumConnections")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-589">Максимальное число подключений, которые TCP может открыть одновременно.</span><span class="sxs-lookup"><span data-stu-id="d1657-589">Maximum number of connections that TCP can have open simultaneously.</span></span> <span data-ttu-id="d1657-590">Значение по умолчанию: 0xFFFFFE, допустимый диапазон: 0 — 0xFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="d1657-590">Default: 0xFFFFFE, Valid Range: 0 - 0xFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-591">**TcpUseRFC1122UrgentPointer**</span><span class="sxs-lookup"><span data-stu-id="d1657-591">**TcpUseRFC1122UrgentPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-592">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-592">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-593">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-593">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-594">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpUseRFC1122UrgentPointer")</span><span class="sxs-lookup"><span data-stu-id="d1657-594">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpUseRFC1122UrgentPointer")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-595">Если **значение — true**, TCP использует спецификацию RFC 1122 для срочных данных.</span><span class="sxs-lookup"><span data-stu-id="d1657-595">If **TRUE**, TCP uses the RFC 1122 specification for urgent data.</span></span> <span data-ttu-id="d1657-596">Если **значение равно false** (по умолчанию), TCP использует режим, используемый в производных системах проектирования программного обеспечения (BSD).</span><span class="sxs-lookup"><span data-stu-id="d1657-596">If **FALSE** (default), TCP uses the mode used by Berkeley Software Design (BSD) derived systems.</span></span> <span data-ttu-id="d1657-597">Два механизма по-разному обрабатывают срочный указатель и не взаимодействуют.</span><span class="sxs-lookup"><span data-stu-id="d1657-597">The two mechanisms interpret the urgent pointer differently and are not interoperable.</span></span> <span data-ttu-id="d1657-598">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="d1657-598">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-599">**TcpWindowSize**</span><span class="sxs-lookup"><span data-stu-id="d1657-599">**TcpWindowSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-600">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1657-600">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-601">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-602">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="d1657-602">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-603">Максимальный размер окна приема TCP, предлагаемый системой.</span><span class="sxs-lookup"><span data-stu-id="d1657-603">Maximum TCP Receive Window size offered by the system.</span></span> <span data-ttu-id="d1657-604">В окне приема указывается число байтов, которое отправитель может передать без получения подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d1657-604">The Receive Window specifies the number of bytes a sender may transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="d1657-605">Как правило, больший объем получаемых окон повысит производительность по сравнению с сетями с высокой задержкой и высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="d1657-605">In general, larger receiving windows will improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="d1657-606">Для повышения эффективности принимающее окно должно быть кратно максимальному размеру сегмента (MSS) TCP.</span><span class="sxs-lookup"><span data-stu-id="d1657-606">For efficiency, the receiving window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span> <span data-ttu-id="d1657-607">По умолчанию: в четыре раза больше, чем максимальный размер данных TCP, или даже кратный объему данных TCP, округленный до ближайшего числа, кратного 8192.</span><span class="sxs-lookup"><span data-stu-id="d1657-607">Default: Four times the maximum TCP data size or an even multiple of TCP data size rounded up to the nearest multiple of 8192.</span></span> <span data-ttu-id="d1657-608">Сети Ethernet по умолчанию имеют значение 8760.</span><span class="sxs-lookup"><span data-stu-id="d1657-608">Ethernet networks default to 8760.</span></span> <span data-ttu-id="d1657-609">Допустимый диапазон: 0-65535.</span><span class="sxs-lookup"><span data-stu-id="d1657-609">Valid range: 0 - 65535.</span></span>

> [!Note]  
> <span data-ttu-id="d1657-610">Windows Vista: это свойство обращается к `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` записи реестра, которая не используется в текущей реализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d1657-610">Windows Vista: This property accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

</dd> <dt>

<span data-ttu-id="d1657-611">**винсенаблелмхостслукуп**</span><span class="sxs-lookup"><span data-stu-id="d1657-611">**WINSEnableLMHostsLookup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-612">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1657-612">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-613">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-613">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-614">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| енаблелмхостс")</span><span class="sxs-lookup"><span data-stu-id="d1657-614">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableLMHOSTS")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-615">Если **значение — true**, используются локальные файлы поиска.</span><span class="sxs-lookup"><span data-stu-id="d1657-615">If **TRUE**, local lookup files are used.</span></span> <span data-ttu-id="d1657-616">Файлы подстановок будут содержать карту IP-адресов для имен узлов.</span><span class="sxs-lookup"><span data-stu-id="d1657-616">Lookup files will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="d1657-617">Если они существуют в локальной системе, они будут находиться в драйверах% SystemRoot% \\ system32 \\ \\ и т. д.</span><span class="sxs-lookup"><span data-stu-id="d1657-617">If they exist on the local system, they will be found in %SystemRoot%\\system32\\drivers\\etc.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-618">**виншостлукупфиле**</span><span class="sxs-lookup"><span data-stu-id="d1657-618">**WINSHostLookupFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-619">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-620">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-621">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| системные сведения о функциях \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ драйверы \\ \\ и т. д. \\ \\ )</span><span class="sxs-lookup"><span data-stu-id="d1657-621">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)\|\\\\drivers\\\\etc\\\\lmhosts")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-622">Путь к файлу поиска WINS в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="d1657-622">Path to a WINS lookup file on the local system.</span></span> <span data-ttu-id="d1657-623">Этот файл будет содержать карту IP-адресов для имен узлов.</span><span class="sxs-lookup"><span data-stu-id="d1657-623">This file will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="d1657-624">Если файл, указанный в этом свойстве, найден, он будет скопирован в папку% SystemRoot% \\ system32 с \\ драйверами \\ и в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="d1657-624">If the file specified in this property is found, it will be copied to the %SystemRoot%\\system32\\drivers\\etc folder of the local system.</span></span> <span data-ttu-id="d1657-625">Действует, только если свойство **винсенаблелмхостслукуп** имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="d1657-625">Valid only if the **WINSEnableLMHostsLookup** property is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-626">**винспримарисервер**</span><span class="sxs-lookup"><span data-stu-id="d1657-626">**WINSPrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-627">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-627">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-628">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-629">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| входные и выходные функции устройства Win32API \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="d1657-629">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-630">IP-адрес основного WINS-сервера.</span><span class="sxs-lookup"><span data-stu-id="d1657-630">IP address for the primary WINS server.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-631">**винсскопеид**</span><span class="sxs-lookup"><span data-stu-id="d1657-631">**WINSScopeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-632">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-632">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-633">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-634">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Параметры \| ScopeId")</span><span class="sxs-lookup"><span data-stu-id="d1657-634">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ScopeID")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-635">Значение, добавляемое к концу NetBIOS-имени, которое изолирует группу компьютерных систем, взаимодействующих друг с другом.</span><span class="sxs-lookup"><span data-stu-id="d1657-635">Value appended to the end of the NetBIOS name that isolates a group of computer systems communicating with only each other.</span></span> <span data-ttu-id="d1657-636">Он используется для всех транзакций NetBIOS через TCP/IP-связь с этой компьютерной системой.</span><span class="sxs-lookup"><span data-stu-id="d1657-636">It is used for all NetBIOS transactions over TCP/IP communications from that computer system.</span></span> <span data-ttu-id="d1657-637">Компьютеры, настроенные с идентичными идентификаторами областей, могут взаимодействовать с этим компьютером.</span><span class="sxs-lookup"><span data-stu-id="d1657-637">Computers configured with identical scope identifiers are able to communicate with this computer.</span></span> <span data-ttu-id="d1657-638">Клиенты TCP/IP с разными идентификаторами областей пропускают пакеты с компьютеров с этим идентификатором области.</span><span class="sxs-lookup"><span data-stu-id="d1657-638">TCP/IP clients with different scope identifiers disregard packets from computers with this scope identifier.</span></span> <span data-ttu-id="d1657-639">Действует, только если метод [**свойство enablewins**](enablewins-method-in-class-win32-networkadapterconfiguration.md) успешно выполняется.</span><span class="sxs-lookup"><span data-stu-id="d1657-639">Valid only when the [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) method executes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="d1657-640">**винссекондарисервер**</span><span class="sxs-lookup"><span data-stu-id="d1657-640">**WINSSecondaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1657-641">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1657-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1657-642">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1657-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1657-643">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| входные и выходные функции устройства Win32API \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="d1657-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="d1657-644">IP-адрес дополнительного WINS-сервера.</span><span class="sxs-lookup"><span data-stu-id="d1657-644">IP address for the secondary WINS server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1657-645">Remarks</span><span class="sxs-lookup"><span data-stu-id="d1657-645">Remarks</span></span>

<span data-ttu-id="d1657-646">Класс **Win32 \_ NetworkAdapterConfiguration** является производным от [**\_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d1657-646">The **Win32\_NetworkAdapterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d1657-647">Примеры</span><span class="sxs-lookup"><span data-stu-id="d1657-647">Examples</span></span>

<span data-ttu-id="d1657-648">Пример кода VBScript для надстройки [инструментария WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) в коллекции TechNet использует класс **Win32 \_ NetworkAdapterConfiguration** для получения сведений о конфигурации сети с нескольких удаленных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="d1657-648">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_NetworkAdapterConfiguration** class to retrieve network configuration information from a number of remote computers.</span></span>

<span data-ttu-id="d1657-649">Пример " [Get-компутеринфо-запрос компьютера с локального/удаленного компьютера" (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell в коллекции TechNet использует несколько вызовов оборудования и программного обеспечения, включая **Win32 \_ NetworkAdapterConfiguration**, для вывода сведений о локальной или удаленной системе.</span><span class="sxs-lookup"><span data-stu-id="d1657-649">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapterConfiguration**, to display information about a local or remote system.</span></span>

<span data-ttu-id="d1657-650">Следующий код PowerShell извлекает параметры конфигурации для адаптера Microsoft ИСТАП.</span><span class="sxs-lookup"><span data-stu-id="d1657-650">The following PowerShell code retrieves the configuration settings for the Microsoft ISTAP Adapter.</span></span>


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



<span data-ttu-id="d1657-651">В следующем \# примере C извлекается описание и номер индекса всех экземпляров конфигурации сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="d1657-651">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="d1657-652">Обратите внимание, что в этом \# образце C используется пространство имен [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , которое обычно масштабируется более эффективно, чем классы WMI пространства имен [System. Management](/dotnet/api/system.management) .</span><span class="sxs-lookup"><span data-stu-id="d1657-652">Note that this C\# sample uses the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace, which generally scales more efficiently than the [System.Management](/dotnet/api/system.management) namespace WMI classes.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
{
   CimSession session = CimSession.Create("localHost");
   IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapterConfiguration");

   foreach (CimInstance cimObj in queryInstance)
   {
      Console.WriteLine(cimObj.CimInstanceProperties["Index"].ToString());
      Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
      Console.WriteLine();
   }

Console.ReadLine();
}
```



<span data-ttu-id="d1657-653">В следующем \# примере C извлекается описание и номер индекса всех экземпляров конфигурации сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="d1657-653">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="d1657-654">Обратите внимание, что \# в этом примере на языке C используется исходное пространство имен [System. Management](/dotnet/api/system.management) , которое было заменено [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d1657-654">Note that this C\# sample uses the original [System.Management](/dotnet/api/system.management) namespace, which has been superceded by [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).</span></span>


```CSharp
using System.Management;
...
static void oldSchoolQueryInstanceFunc()
{

   ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapterConfiguration");
   ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);

   ManagementObjectCollection queryCollection = searcher.Get();
   foreach (ManagementObject m in queryCollection)
   {
      Console.WriteLine("Index : {0}", m["Index"]);
      Console.WriteLine("Description : {0}", m["Description"]);
      Console.WriteLine();
   }
   Console.ReadLine();
}
```



<span data-ttu-id="d1657-655">В следующем примере извлекаются сведения из класса **Win32 \_ NetworkAdapterConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="d1657-655">The following example retrieves information from the **Win32\_NetworkAdapterConfiguration** class.</span></span>


```VB
on error resume next


PrintAll_NICAdapter_information()

'PrintOnlyEnabled_NICAdapter_information()


Function PrintAll_NICAdapter_information()


    strComputer = "."

    Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")


    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration",,48)


    i = 0

    For Each objItem in colItems

        i = i + 1

        Wscript.Echo "-----------------------------------"

        Wscript.Echo "Win32_NetworkAdapterConfiguration instance: " & i

        Wscript.Echo "-----------------------------------"

        

        strDefaultIPGateway = GetMultiString_FromArray(objitem.DefaultIPGateway, ", ")

        Wscript.Echo "MACAddress                  : " & vbtab & objItem.MACAddress
        Wscript.Echo "Description                 : " & vbtab & objItem.Description
        Wscript.Echo "DHCPEnabled                 : " & vbtab & objItem.DHCPEnabled

        strIPAddress=GetMultiString_FromArray(objitem.IPAddress, ", ")

        Wscript.Echo "IPAddress                   : " & vbtab & strIPAddress

        strIPSubnet = GetMultiString_FromArray(objitem.IPSubnet, ", ")

        Wscript.Echo "IPSubnet                    : " & vbtab & strIPSubnet
        Wscript.Echo "IPConnectionMetric          : " & vbtab & objItem.IPConnectionMetric
        Wscript.Echo "DHCPLeaseExpires            : " & vbtab & objItem.DHCPLeaseExpires
        Wscript.Echo "DHCPLeaseObtained           : " & vbtab & objItem.DHCPLeaseObtained
        Wscript.Echo "DHCPServer                  : " & vbtab & objItem.DHCPServer
        Wscript.Echo "DNSDomain                   : " & vbtab & objItem.DNSDomain
        Wscript.Echo "IPEnabled                   : " & vbtab & objItem.IPEnabled
        Wscript.Echo "DefaultIPGateway            : " & vbtab & strDefaultIPGateway
        Wscript.Echo "GatewayCostMetric           : " & vbtab & strGatewayCostMetric
        Wscript.Echo "IPFilterSecurityEnabled     : " & vbtab & objItem.IPFilterSecurityEnabled
        Wscript.Echo "IPPortSecurityEnabled       : " & vbtab & objItem.IPPortSecurityEnabled

        strDNSDomainSuffixSearchOrder = GetMultiString_FromArray(objitem.DNSDomainSuffixSearchOrder, ", ")

        Wscript.Echo "DNSDomainSuffixSearchOrder  : " & vbtab & strDNSDomainSuffixSearchOrder
        Wscript.Echo "DNSEnabledForWINSResolution : " & vbtab & objItem.DNSEnabledForWINSResolution
        Wscript.Echo "DNSHostName                 : " & vbtab & objItem.DNSHostName

        

        strDNSServerSearchOrder = GetMultiString_FromArray(objitem.DNSServerSearchOrder, ", ")

        Wscript.Echo "DNSServerSearchOrder        : " & vbtab & strDNSServerSearchOrder
        Wscript.Echo "DomainDNSRegistrationEnabled: " & vbtab & objItem.DomainDNSRegistrationEnabled
        Wscript.Echo "ForwardBufferMemory         : " & vbtab & objItem.ForwardBufferMemory
        Wscript.Echo "FullDNSRegistrationEnabled  : " & vbtab & objItem.FullDNSRegistrationEnabled

        strGatewayCostMetric = GetMultiString_FromArray(objitem.GatewayCostMetric, ", ")

        Wscript.Echo "IGMPLevel                   : " & vbtab & objItem.IGMPLevel
        Wscript.Echo "Index                       : " & vbtab & objItem.Index

        strIPSecPermitIPProtocols = GetMultiString_FromArray(objitem.IPSecPermitIPProtocols, ", ")

        Wscript.Echo "IPSecPermitIPProtocols      : " & vbtab & strIPSecPermitIPProtocols


        strIPSecPermitTCPPorts =GetMultiString_FromArray(objitem.IPSecPermitTCPPorts, ", ")

        Wscript.Echo "IPSecPermitTCPPorts         : " & vbtab & strIPSecPermitTCPPorts


        strIPSecPermitUDPPorts = GetMultiString_FromArray(objitem.IPSecPermitUDPPorts, ", ")

        Wscript.Echo "IPSecPermitUDPPorts         : " & vbtab & strIPSecPermitUDPPorts


        Wscript.Echo "IPUseZeroBroadcast          : " & vbtab & objItem.IPUseZeroBroadcast
        Wscript.Echo "IPXAddress                  : " & vbtab & objItem.IPXAddress
        Wscript.Echo "IPXEnabled                  : " & vbtab & objItem.IPXEnabled

        strIPXFrameType=GetMultiString_FromArray(objitem.IPXFrameType, ", ")

        Wscript.Echo "IPXFrameType                : " & vbtab & strIPXFrameType


        strIPXNetworkNumber=GetMultiString_FromArray(objitem.IPXNetworkNumber, ", ")

        Wscript.Echo "IPXNetworkNumber            : " & vbtab & strIPXNetworkNumber
        Wscript.Echo "IPXVirtualNetNumber         : " & vbtab & objItem.IPXVirtualNetNumber
        Wscript.Echo "KeepAliveInterval           : " & vbtab & objItem.KeepAliveInterval

        Wscript.Echo "KeepAliveTime               : " & vbtab & objItem.KeepAliveTime
        Wscript.Echo "MTU                         : " & vbtab & objItem.MTU
        Wscript.Echo "NumForwardPackets           : " & vbtab & objItem.NumForwardPackets
        Wscript.Echo "PMTUBHDetectEnabled         : " & vbtab & objItem.PMTUBHDetectEnabled
        Wscript.Echo "PMTUDiscoveryEnabled        : " & vbtab & objItem.PMTUDiscoveryEnabled
        Wscript.Echo "ServiceName                 : " & vbtab & objItem.ServiceName
        Wscript.Echo "SettingID                   : " & vbtab & objItem.SettingID
        Wscript.Echo "TcpipNetbiosOptions         : " & vbtab & objItem.TcpipNetbiosOptions
        Wscript.Echo "TcpMaxConnectRetransmissions: " & vbtab & objItem.TcpMaxConnectRetransmissions
        Wscript.Echo "TcpMaxDataRetransmissions   : " & vbtab & objItem.TcpMaxDataRetransmissions
        Wscript.Echo "TcpNumConnections           : " & vbtab & objItem.TcpNumConnections
        Wscript.Echo "TcpUseRFC1122UrgentPointer  : " & vbtab & objItem.TcpUseRFC1122UrgentPointer
        Wscript.Echo "TcpWindowSize               : " & vbtab & objItem.TcpWindowSize
        Wscript.Echo "WINSEnableLMHostsLookup     : " & vbtab & objItem.WINSEnableLMHostsLookup
        Wscript.Echo "WINSHostLookupFile          : " & vbtab & objItem.WINSHostLookupFile
        Wscript.Echo "WINSPrimaryServer           : " & vbtab & objItem.WINSPrimaryServer
        Wscript.Echo "WINSScopeID                 : " & vbtab & objItem.WINSScopeID
        Wscript.Echo "WINSSecondaryServer         : " & vbtab & objItem.WINSSecondaryServer
        Wscript.Echo "ArpAlwaysSourceRoute        : " & vbtab & objItem.ArpAlwaysSourceRoute
        Wscript.Echo "ArpUseEtherSNAP             : " & vbtab & objItem.ArpUseEtherSNAP
        Wscript.Echo "DatabasePath                : " & vbtab & objItem.DatabasePath
        Wscript.Echo "DeadGWDetectEnabled         : " & vbtab & objItem.DeadGWDetectEnabled

        Wscript.Echo "DefaultTOS                  : " & vbtab & objItem.DefaultTOS
        Wscript.Echo "DefaultTTL                  : " & vbtab & objItem.DefaultTTL

        

    Next

End Function ' Function PrintAll_NICAdapter_information()


' Script to get comprehensive nic info

sub appendCollection(msg, colctn, nm)

    i=0
    for each t in colctn
        msg = msg & "nic." & nm & "["&i&"]: " & t & vbCRLF
        i = i + 1
    next
end sub


Function PrintOnlyEnabled_NICAdapter_information()

    strComputer = "."

    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colNicConfigs = objWMIService.ExecQuery ("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled = True")


    for each nic in colNicConfigs

        msg = "nic.ArpAlwaysSourceRoute: " & nic.ArpAlwaysSourceRoute & vbCRLF _
        & "nic.ArpUseEtherSNAP: " & nic.ArpUseEtherSNAP & vbCRLF _
        & "nic.Caption: " & nic.Caption & vbCRLF _
        & "nic.DatabasePath: " & nic.DatabasePath & vbCRLF _
        & "nic.DeadGWDetectEnabled: " & nic.DeadGWDetectEnabled & vbCRLF _
        & "nic.DefaultTOS: " & nic.DefaultTOS & vbCRLF _
        & "nic.DefaultTTL: " & nic.DefaultTTL & vbCRLF _
        & "nic.Description: " & nic.Description & vbCRLF _
        & "nic.DHCPEnabled: " & nic.DHCPEnabled & vbCRLF _
        & "nic.DHCPLeaseExpires: " & nic.DHCPLeaseExpires & vbCRLF _
        & "nic.DHCPLeaseObtained: " & nic.DHCPLeaseObtained & vbCRLF _
        & "nic.DHCPServer: " & nic.DHCPServer & vbCRLF _
        & "nic.DNSDomain: " & nic.DNSDomain & vbCRLF _
        & "nic.DNSEnabledForWINSResolution: " & nic.DNSEnabledForWINSResolution & vbCRLF _
        & "nic.DNSHostName: " & nic.DNSHostName & vbCRLF _
        & "nic.DomainDNSRegistrationEnabled: " & nic.DomainDNSRegistrationEnabled & vbCRLF _
        & "nic.DNSDomainSuffixSearchOrder: " & nic.DNSDomainSuffixSearchOrder & vbCRLF _
        & "nic.ForwardBufferMemory: " & nic.ForwardBufferMemory & vbCRLF _
        & "nic.FullDNSRegistrationEnabled: " & nic.FullDNSRegistrationEnabled & vbCRLF _
        & "nic.IGMPLevel: " & nic.IGMPLevel & vbCRLF _
        & "nic.Index: " & nic.Index & vbCRLF _
        & "nic.IPConnectionMetric: " & nic.IPConnectionMetric & vbCRLF _
        & "nic.IPEnabled: " & nic.IPEnabled & vbCRLF _
        & "nic.IPFilterSecurityEnabled: " & nic.IPFilterSecurityEnabled & vbCRLF _
        & "nic.IPPortSecurityEnabled: " & nic.IPPortSecurityEnabled & vbCRLF _
        & "nic.IPUseZeroBroadcast: " & nic.IPUseZeroBroadcast & vbCRLF _
        & "nic.IPXAddress: " & nic.IPXAddress & vbCRLF _
        & "nic.IPXEnabled: " & nic.IPXEnabled & vbCRLF _
        & "nic.IPXFrameType: " & nic.IPXFrameType & vbCRLF _
        & "nic.IPXMediaType: " & nic.IPXMediaType & vbCRLF _
        & "nic.IPXNetworkNumber: " & nic.IPXNetworkNumber & vbCRLF _
        & "nic.IPXVirtualNetNumber: " & nic.IPXVirtualNetNumber & vbCRLF _
        & "nic.KeepAliveInterval: " & nic.KeepAliveInterval & vbCRLF _
        & "nic.KeepAliveTime: " & nic.KeepAliveTime & vbCRLF _
        & "nic.MACAddress: " & nic.MACAddress & vbCRLF _
        & "nic.MTU: " & nic.MTU & vbCRLF _
        & "nic.NumForwardPackets: " & nic.NumForwardPackets & vbCRLF _
        & "nic.PMTUBHDetectEnabled: " & nic.PMTUBHDetectEnabled & vbCRLF _
        & "nic.PMTUDiscoveryEnabled: " & nic.PMTUDiscoveryEnabled & vbCRLF _
        & "nic.ServiceName: " & nic.ServiceName & vbCRLF _
        & "nic.SettingID: " & nic.SettingID & vbCRLF _
        & "nic.TcpipNetbiosOptions: " & nic.TcpipNetbiosOptions & vbCRLF _
        & "nic.TcpMaxConnectRetransmissions: " & nic.TcpMaxConnectRetransmissions & vbCRLF _
        & "nic.TcpMaxDataRetransmissions: " & nic.TcpMaxDataRetransmissions & vbCRLF _
        & "nic.TcpNumConnections: " & nic.TcpNumConnections & vbCRLF _
        & "nic.TcpUseRFC1122UrgentPointer: " & nic.TcpUseRFC1122UrgentPointer & vbCRLF _
        & "nic.TcpWindowSize: " & nic.TcpWindowSize & vbCRLF _
        & "nic.WINSEnableLMHostsLookup: " & nic.WINSEnableLMHostsLookup & vbCRLF _
        & "nic.WINSHostLookupFile: " & nic.WINSHostLookupFile & vbCRLF _
        & "nic.WINSPrimaryServer: " & nic.WINSPrimaryServer & vbCRLF _
        & "nic.WINSScopeID: " & nic.WINSScopeID & vbCRLF _
        & "nic.WINSSecondaryServer: " & nic.WINSSecondaryServer & vbCRLF _
        '& "nic.InterfaceIndex: " & "|"&nic.InterfaceIndex & vbCRLF _


        appendCollection msg, nic.DefaultIPGateway, "DefaultIPGateway"
        appendCollection msg, nic.DNSServerSearchOrder, "DNSServerSearchOrder"
        appendCollection msg, nic.GatewayCostMetric, "GatewayCostMetric"
        appendCollection msg, nic.IPAddress, "IPAddress"
        appendCollection msg, nic.IPSecPermitIPProtocols, "IPSecPermitIPProtocols"
        appendCollection msg, nic.IPSecPermitTCPPorts, "IPSecPermitTCPPorts"
        appendCollection msg, nic.IPSecPermitUDPPorts, "IPSecPermitUDPPorts"
        appendCollection msg, nic.IPSubnet, "IPSubnet"


        WScript.Echo msg

    next


    'Vista only code???

    'Set colAdapters = objWMIService.Execquery ("SELECT * FROM Win32_NetworkAdapter WHERE NetEnabled = True")

    'For Each nic in colAdapters

    ' msg = "nic.DeviceId: " & nic.DeviceId & vbCRLF _

    ' & "nic.Name: " & nic.Name & vbCRLF _

    '

    'Next

End Function 'Function PrintOnlyEnabled_NICAdapter_information()

Function GetMultiString_FromArray( ArrayString, Seprator)

    If IsNull ( ArrayString ) Then

        StrMultiArray = ArrayString

    else

        StrMultiArray = Join( ArrayString, Seprator )

   end if

   GetMultiString_FromArray = StrMultiArray

End Function
```



## <a name="requirements"></a><span data-ttu-id="d1657-656">Требования</span><span class="sxs-lookup"><span data-stu-id="d1657-656">Requirements</span></span>



| <span data-ttu-id="d1657-657">Требование</span><span class="sxs-lookup"><span data-stu-id="d1657-657">Requirement</span></span> | <span data-ttu-id="d1657-658">Значение</span><span class="sxs-lookup"><span data-stu-id="d1657-658">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1657-659">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1657-659">Minimum supported client</span></span><br/> | <span data-ttu-id="d1657-660">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1657-660">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1657-661">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1657-661">Minimum supported server</span></span><br/> | <span data-ttu-id="d1657-662">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1657-662">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1657-663">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d1657-663">Namespace</span></span><br/>                | <span data-ttu-id="d1657-664">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d1657-664">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1657-665">MOF</span><span class="sxs-lookup"><span data-stu-id="d1657-665">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1657-666"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1657-666"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1657-667">DLL</span><span class="sxs-lookup"><span data-stu-id="d1657-667">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1657-668"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1657-668"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1657-669">См. также</span><span class="sxs-lookup"><span data-stu-id="d1657-669">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1657-670">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="d1657-670">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="d1657-671">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="d1657-671">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d1657-672">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="d1657-672">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="d1657-673">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="d1657-673">WMI Tasks: Accounts and Domains</span></span>](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[<span data-ttu-id="d1657-674">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="d1657-674">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
