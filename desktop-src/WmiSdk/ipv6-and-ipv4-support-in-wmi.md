---
description: Поставщик IP-маршрута WMI и классы сетевых классов предоставляют данные для адресов IPv4. Начиная с Windows Vista, Инструментарий WMI также обеспечивает ограниченную поддержку возможностей сети IPv6.
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: Поддержка IPv6 и IPv4 в WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107872b2a65ffe02f34245a39e0a803d2ac53a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683896"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a><span data-ttu-id="f62f1-104">Поддержка IPv6 и IPv4 в WMI</span><span class="sxs-lookup"><span data-stu-id="f62f1-104">IPv6 and IPv4 Support in WMI</span></span>

<span data-ttu-id="f62f1-105">[Поставщик IP-маршрута](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI и классы сетевых классов предоставляют данные для адресов IPv4.</span><span class="sxs-lookup"><span data-stu-id="f62f1-105">WMI [IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) and network classes supply data for IPv4 addresses.</span></span> <span data-ttu-id="f62f1-106">Начиная с Windows Vista, Инструментарий WMI также обеспечивает ограниченную поддержку возможностей сети IPv6.</span><span class="sxs-lookup"><span data-stu-id="f62f1-106">Starting with Windows Vista, WMI also provides limited support for IPv6 network capabilities.</span></span>

## <a name="wmi-ip-data"></a><span data-ttu-id="f62f1-107">Данные IP-адреса WMI</span><span class="sxs-lookup"><span data-stu-id="f62f1-107">WMI IP Data</span></span>

<span data-ttu-id="f62f1-108">Следующие классы предоставляют только данные IPv4:</span><span class="sxs-lookup"><span data-stu-id="f62f1-108">The following classes supply only IPv4 data:</span></span>

-   [<span data-ttu-id="f62f1-109">**\_IP4RouteTable Win32**</span><span class="sxs-lookup"><span data-stu-id="f62f1-109">**Win32\_IP4RouteTable**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [<span data-ttu-id="f62f1-110">**\_IP4PersistedRouteTable Win32**</span><span class="sxs-lookup"><span data-stu-id="f62f1-110">**Win32\_IP4PersistedRouteTable**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [<span data-ttu-id="f62f1-111">**\_IP4RouteTableEvent Win32**</span><span class="sxs-lookup"><span data-stu-id="f62f1-111">**Win32\_IP4RouteTableEvent**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [<span data-ttu-id="f62f1-112">**\_Активерауте Win32**</span><span class="sxs-lookup"><span data-stu-id="f62f1-112">**Win32\_ActiveRoute**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [<span data-ttu-id="f62f1-113">**\_Сетевого адаптера Win32**</span><span class="sxs-lookup"><span data-stu-id="f62f1-113">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)

<span data-ttu-id="f62f1-114">Следующие классы предоставляют данные для IPv4 и IPv6.</span><span class="sxs-lookup"><span data-stu-id="f62f1-114">The following classes supply data for both IPv4 and IPv6.</span></span>

-   [<span data-ttu-id="f62f1-115">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="f62f1-115">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    <span data-ttu-id="f62f1-116">Свойство **ипаддесс** содержит IPv6-адрес компьютера в сети IPv6.</span><span class="sxs-lookup"><span data-stu-id="f62f1-116">The **IpAddess** property contains the IPv6 address of the computer in an IPv6 network.</span></span>

-   [<span data-ttu-id="f62f1-117">**\_Пингстатус Win32**</span><span class="sxs-lookup"><span data-stu-id="f62f1-117">**Win32\_PingStatus**</span></span>](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    <span data-ttu-id="f62f1-118">[**Win32 \_ Пингстатус**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) может возвращать данные для адресов IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="f62f1-118">[**Win32\_PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) can return data for either IPv4 or IPv6 addresses.</span></span>

## <a name="ipv4-and-ipv6-connections-to-wmi"></a><span data-ttu-id="f62f1-119">Подключения IPv4 и IPv6 к WMI</span><span class="sxs-lookup"><span data-stu-id="f62f1-119">IPv4 and IPv6 Connections to WMI</span></span>

<span data-ttu-id="f62f1-120">При подключении к пространству имен WMI на удаленном компьютере на целевом компьютере должно быть работает то же программное обеспечение, что и для подключающегося компьютера.</span><span class="sxs-lookup"><span data-stu-id="f62f1-120">When connecting to a WMI namespace on a remote computer, the target computer must be running the same IP software as the connecting computer.</span></span> <span data-ttu-id="f62f1-121">Например, компьютер с протоколом IPv4 не может подключиться к компьютеру с протоколом IPv6, даже если попытка подключения выполняется с помощью имени компьютера в вызове [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md)или с помощью `winmgmts` подключения моникера.</span><span class="sxs-lookup"><span data-stu-id="f62f1-121">For example, a computer running IPv4 cannot connect to a computer running IPv6, even if the connection is attempted by using a computer name in the call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), or by using the `winmgmts` moniker connection.</span></span> <span data-ttu-id="f62f1-122">Обратная связь также имеет значение true: компьютер, на котором работает только протокол IPv6, не может подключиться к компьютеру, на котором выполняется только протокол IPv4.</span><span class="sxs-lookup"><span data-stu-id="f62f1-122">The reverse is also true: a computer running only IPv6 cannot connect to a computer running only IPv4.</span></span>

<span data-ttu-id="f62f1-123">Если конечный компьютер работает как с IPv4, так и с IPv6, то подключение можно выполнить с компьютера, на котором работает программное обеспечение с любым IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="f62f1-123">If the target computer is running both IPv4 and IPv6, then a connection can be made from a computer running either IP software.</span></span> <span data-ttu-id="f62f1-124">Имя компьютера или IP-адрес в формате IPv4 или IPv6 можно указать в соединении с пространством имен WMI.</span><span class="sxs-lookup"><span data-stu-id="f62f1-124">A computer name or an IP address in either IPv4 or IPv6 format can be supplied in the connection to a WMI namespace.</span></span>

<span data-ttu-id="f62f1-125">Компьютер, на котором запущены протоколы IPv4 и IPv6 и подключается к целевому компьютеру только по протоколу IPv4 или только к IPv6, должен предоставить IP-адрес в соответствующем формате для IP-адреса целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="f62f1-125">A computer that runs both IPv4 and IPv6 and connects to a target computer running only IPv4 or only IPv6 must supply an IP address in the appropriate format for the target computer IP software.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f62f1-126">См. также</span><span class="sxs-lookup"><span data-stu-id="f62f1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f62f1-127">Сведения об инструментарии WMI</span><span class="sxs-lookup"><span data-stu-id="f62f1-127">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
