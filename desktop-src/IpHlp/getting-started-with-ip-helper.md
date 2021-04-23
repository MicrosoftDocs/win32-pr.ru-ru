---
description: Ниже приведено пошаговое руководство по началу работы с использованием программного интерфейса (API) вспомогательного приложения IP. Он предназначен для понимания основных вспомогательных функций и структур данных IP и их совместной работы.
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: начало работы с вспомогательным модулем IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 566ed4503c9bbafaee846aebf30c31993f7ce7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913687"
---
# <a name="getting-started-with-ip-helper"></a><span data-ttu-id="cfdcb-104">начало работы с вспомогательным модулем IP</span><span class="sxs-lookup"><span data-stu-id="cfdcb-104">Getting Started with IP Helper</span></span>

<span data-ttu-id="cfdcb-105">Ниже приведено пошаговое руководство по началу работы с использованием программного интерфейса (API) вспомогательного приложения IP.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-105">The following is a step-by-step guide to getting started programming using the IP Helper application programming interface (API).</span></span> <span data-ttu-id="cfdcb-106">Он предназначен для понимания основных вспомогательных функций и структур данных IP и их совместной работы.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-106">It is designed to provide an understanding of basic IP Helper functions and data structures, and how they work together.</span></span>

<span data-ttu-id="cfdcb-107">Приложение, используемое для иллюстрации, — это очень простое вспомогательное приложение IP.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-107">The application that is used for illustration is a very basic IP Helper application.</span></span> <span data-ttu-id="cfdcb-108">В образцы, входящие в состав пакета средств разработки программного обеспечения (SDK) для Microsoft Windows, включены более сложные примеры кода.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-108">More advanced code examples are included in the samples included with the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="cfdcb-109">Первый шаг аналогичен большинству вспомогательных приложений IP.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-109">The first step is the same for most IP Helper applications.</span></span>

-   [<span data-ttu-id="cfdcb-110">Создание базового вспомогательного приложения IP-адресов</span><span class="sxs-lookup"><span data-stu-id="cfdcb-110">Creating a Basic IP Helper Application</span></span>](creating-a-basic-ip-helper-application.md)

<span data-ttu-id="cfdcb-111">В следующих разделах описаны оставшиеся шаги по созданию базового вспомогательного приложения IP.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-111">The following sections describe the remaining steps for creating this basic IP Helper application.</span></span>

-   [<span data-ttu-id="cfdcb-112">Получение сведений с помощью Жетнетворкпарамс</span><span class="sxs-lookup"><span data-stu-id="cfdcb-112">Retrieving Information Using GetNetworkParams</span></span>](retrieving-information-using-getnetworkparams.md)
-   [<span data-ttu-id="cfdcb-113">Управление сетевыми адаптерами с помощью Жетадаптерсинфо</span><span class="sxs-lookup"><span data-stu-id="cfdcb-113">Managing Network Adapters Using GetAdaptersInfo</span></span>](managing-network-adapters-using-getadaptersinfo.md)
-   [<span data-ttu-id="cfdcb-114">Управление интерфейсами с помощью Жетинтерфацеинфо</span><span class="sxs-lookup"><span data-stu-id="cfdcb-114">Managing Interfaces Using GetInterfaceInfo</span></span>](managing-interfaces-using-getinterfaceinfo.md)
-   [<span data-ttu-id="cfdcb-115">Управление IP-адресами с помощью Жетипаддртабле</span><span class="sxs-lookup"><span data-stu-id="cfdcb-115">Managing IP Addresses Using GetIpAddrTable</span></span>](managing-ip-addresses-using-getipaddrtable.md)
-   [<span data-ttu-id="cfdcb-116">Управление арендой DHCP с помощью Ипрелеасеаддресс и Ипреневаддресс</span><span class="sxs-lookup"><span data-stu-id="cfdcb-116">Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress</span></span>](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [<span data-ttu-id="cfdcb-117">Управление IP-адресами с помощью Аддипаддресс и Делетеипаддресс</span><span class="sxs-lookup"><span data-stu-id="cfdcb-117">Managing IP Addresses Using AddIPAddress and DeleteIPAddress</span></span>](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [<span data-ttu-id="cfdcb-118">Получение сведений с помощью Жетипстатистикс</span><span class="sxs-lookup"><span data-stu-id="cfdcb-118">Retrieving Information Using GetIpStatistics</span></span>](retrieving-information-using-getipstatistics.md)
-   [<span data-ttu-id="cfdcb-119">Получение сведений с помощью Жетткпстатистикс</span><span class="sxs-lookup"><span data-stu-id="cfdcb-119">Retrieving Information Using GetTcpStatistics</span></span>](retrieving-information-using-gettcpstatistics.md)

<span data-ttu-id="cfdcb-120">Полный исходный код для этого базового вспомогательного примера для IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-120">The complete source code for this basic IP Helper example.</span></span>

-   [<span data-ttu-id="cfdcb-121">Полный исходный код приложения модуля поддержки IP-адресов</span><span class="sxs-lookup"><span data-stu-id="cfdcb-121">Complete IP Helper Application Source Code</span></span>](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a><span data-ttu-id="cfdcb-122">Дополнительные примеры вспомогательных программ для IP</span><span class="sxs-lookup"><span data-stu-id="cfdcb-122">Advanced IP Helper Samples</span></span>

<span data-ttu-id="cfdcb-123">В пакет средств разработки программного обеспечения (SDK) для Microsoft Windows входят несколько дополнительных вспомогательных примеров для IP.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-123">Several more advanced IP Helper samples are included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cfdcb-124">По умолчанию исходный код для примера вспомогательного метода IP устанавливается Windows SDK, выпущенным для Windows 7, в следующем каталоге:</span><span class="sxs-lookup"><span data-stu-id="cfdcb-124">By default, the IP Helper sample source code is installed by the Windows SDK released for Windows 7 in the following directory:</span></span>

<span data-ttu-id="cfdcb-125">*C: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ нетдс \\ ифелп*</span><span class="sxs-lookup"><span data-stu-id="cfdcb-125">*C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\IPHelp*</span></span>

<span data-ttu-id="cfdcb-126">Более сложные примеры, перечисленные ниже, находятся в следующих каталогах:</span><span class="sxs-lookup"><span data-stu-id="cfdcb-126">The more advanced samples listed below are found in the following directories:</span></span>

-   <span data-ttu-id="cfdcb-127">енаблераутер</span><span class="sxs-lookup"><span data-stu-id="cfdcb-127">EnableRouter</span></span>

    <span data-ttu-id="cfdcb-128">Этот каталог содержит пример, демонстрирующий использование вспомогательных функций [**енаблераутер**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) и [**уненаблераутер**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) IP для включения и отключения пересылки IPv4 на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-128">This directory contains a sample that demonstrates how to use the [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) and [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) IP Helper functions to enable and disable IPv4 forwarding on the local computer.</span></span>

-   <span data-ttu-id="cfdcb-129">ипарп</span><span class="sxs-lookup"><span data-stu-id="cfdcb-129">iparp</span></span>

    <span data-ttu-id="cfdcb-130">Этот каталог содержит образец программы, демонстрирующий использование вспомогательных функций IP для отображения и управления записями в таблице ARP IPv4 на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-130">This directory contains a sample program that demonstrates how to use the IP Helper functions to display and manipulate entries in the IPv4 ARP table on the local computer.</span></span>

-   <span data-ttu-id="cfdcb-131">ипчанже</span><span class="sxs-lookup"><span data-stu-id="cfdcb-131">ipchange</span></span>

    <span data-ttu-id="cfdcb-132">Этот каталог содержит образец программы, демонстрирующий использование вспомогательных функций IP для программного изменения IP-адреса определенного сетевого адаптера на компьютере.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-132">This directory contains a sample program that demonstrates how to use IP Helper functions to programmatically change an IP address for a specific network adapter on your machine.</span></span> <span data-ttu-id="cfdcb-133">Эта программа также показывает, как извлечь существующие сведения о конфигурации IP сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-133">This program also demonstrates how to retrieve existing network adapter IP configuration information.</span></span>

-   <span data-ttu-id="cfdcb-134">IPConfig</span><span class="sxs-lookup"><span data-stu-id="cfdcb-134">IPConfig</span></span>

    <span data-ttu-id="cfdcb-135">Этот каталог содержит образец программы, демонстрирующий Программное получение сведений о конфигурации IPv4, аналогичное служебной программе IPCONFIG.EXE.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-135">This directory contains a sample program that demonstrates how to programmatically retrieve IPv4 configuration information similar to the IPCONFIG.EXE utility.</span></span> <span data-ttu-id="cfdcb-136">В нем демонстрируется использование функций [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) и [**жетадаптерсинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) .</span><span class="sxs-lookup"><span data-stu-id="cfdcb-136">It demonstrates how to use the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) and [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) functions.</span></span> <span data-ttu-id="cfdcb-137">Обратите внимание, что функция **жетадаптерсинфо** извлекает только сведения IPv4.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-137">Note that the **GetAdaptersInfo** function only retrieves IPv4 information.</span></span>

-   <span data-ttu-id="cfdcb-138">ипренев</span><span class="sxs-lookup"><span data-stu-id="cfdcb-138">IPRenew</span></span>

    <span data-ttu-id="cfdcb-139">Этот каталог содержит образец программы, демонстрирующий программный выпуск и обновление IPv4-адресов, полученных с помощью DHCP.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-139">This directory contains a sample program that demonstrates how to programmatically release and renew IPv4 addresses obtained through DHCP.</span></span> <span data-ttu-id="cfdcb-140">Эта программа также показывает, как получить сведения о конфигурации сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-140">This program also demonstrates how to retrieve existing network adapter configuration information.</span></span>

-   <span data-ttu-id="cfdcb-141">ипрауте</span><span class="sxs-lookup"><span data-stu-id="cfdcb-141">IPRoute</span></span>

    <span data-ttu-id="cfdcb-142">Этот каталог содержит образец программы, демонстрирующий использование вспомогательных функций IP для работы с таблицей маршрутизации IPv4.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-142">This directory contains a sample program that demonstrates how to use the IP Helper functions to manipulate the IPv4 routing table.</span></span>

-   <span data-ttu-id="cfdcb-143">ипстат</span><span class="sxs-lookup"><span data-stu-id="cfdcb-143">ipstat</span></span>

    <span data-ttu-id="cfdcb-144">Этот каталог содержит образец программы, демонстрирующий использование вспомогательных функций IP для отображения IPv4-подключений для протокола.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-144">This directory contains a sample program that demonstrates how to use the IP Helper functions to show IPv4 connections for a protocol.</span></span> <span data-ttu-id="cfdcb-145">По умолчанию для IP-адресов, ICMP, TCP и UDP отображаются статистические данные.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-145">By default, statistics are shown for IP, ICMP, TCP and UDP.</span></span>

-   <span data-ttu-id="cfdcb-146">нетинфо</span><span class="sxs-lookup"><span data-stu-id="cfdcb-146">Netinfo</span></span>

    <span data-ttu-id="cfdcb-147">Этот каталог содержит образец программы, демонстрирующий использование новых API-интерфейсов вспомогательного интерфейса IP, появившихся в Windows Vista и более поздних версиях для отображения и изменения сведений об адресах и интерфейсе для IPv4 и IPv6.</span><span class="sxs-lookup"><span data-stu-id="cfdcb-147">This directory contains a sample program that demonstrates how to the use the new IP Helper APIs introduced on Windows Vista and later to display/change address and interface information for IPv4 and IPv6.</span></span>

 

 



