---
description: Глоссарий терминов сетевой монитор, начинающихся с буквы N.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: a9b0e907-45c0-4301-9e83-398dd1c1c39a
title: N (сетевой монитор)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54404640b13bff3b098b9d223e656e8f1905c055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911636"
---
# <a name="n-network-monitor"></a><span data-ttu-id="70dd3-103">N (сетевой монитор)</span><span class="sxs-lookup"><span data-stu-id="70dd3-103">N (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="70dd3-104"><span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**АДАПТЕР**</span><span class="sxs-lookup"><span data-stu-id="70dd3-104"><span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**NDIS**</span></span>
</dt> <dd>

<span data-ttu-id="70dd3-105">См. спецификацию интерфейса сетевого драйвера.</span><span class="sxs-lookup"><span data-stu-id="70dd3-105">See network driver interface specification.</span></span>

</dd> <dt>

<span data-ttu-id="70dd3-106"><span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**Спецификация интерфейса сетевого драйвера (NDIS)**</span><span class="sxs-lookup"><span data-stu-id="70dd3-106"><span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**network driver interface specification (NDIS)**</span></span>
</dt> <dd>

<span data-ttu-id="70dd3-107">Спецификация интерфейса между драйверами устройств и сетью.</span><span class="sxs-lookup"><span data-stu-id="70dd3-107">The specification for the interface between device drivers and a network.</span></span> <span data-ttu-id="70dd3-108">Все транспорты вызывают интерфейс NDIS для доступа к картам сетевых интерфейсов и работы с ними.</span><span class="sxs-lookup"><span data-stu-id="70dd3-108">All transports call the NDIS interface to access and work with network interface cards.</span></span>

</dd> <dt>

<span data-ttu-id="70dd3-109"><span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Агент сетевой монитор**</span><span class="sxs-lookup"><span data-stu-id="70dd3-109"><span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Network Monitor agent**</span></span>
</dt> <dd>

<span data-ttu-id="70dd3-110">Компонент сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="70dd3-110">A Network Monitor component.</span></span> <span data-ttu-id="70dd3-111">Агент позволяет удаленному компьютеру записывать данные из сети.</span><span class="sxs-lookup"><span data-stu-id="70dd3-111">The agent enables a remote computer to capture data from the network.</span></span> <span data-ttu-id="70dd3-112">При удаленной установке сетевой монитор к агенту сетевой монитор и инициирует запись, статистика из записи передается по сети на управляющий компьютер.</span><span class="sxs-lookup"><span data-stu-id="70dd3-112">When a Network Monitor installation connects remotely to the Network Monitor agent and initiates a capture, statistics from the capture are transferred over the network to the managing computer.</span></span> <span data-ttu-id="70dd3-113">Перемещение продолжается с интервалов, указанных при установке соединения.</span><span class="sxs-lookup"><span data-stu-id="70dd3-113">The transfer proceeds at intervals specified when the connection is made.</span></span>

</dd> <dt>

<span data-ttu-id="70dd3-114"><span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**Поставщик сетевых пакетов (НПП)**</span><span class="sxs-lookup"><span data-stu-id="70dd3-114"><span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**network packet provider (NPP)**</span></span>
</dt> <dd>

<span data-ttu-id="70dd3-115">Компонент сетевой монитор, собирающий сетевой трафик в кадрах, а затем передающий кадры эксперту и НПП приложение.</span><span class="sxs-lookup"><span data-stu-id="70dd3-115">The Network Monitor component that collects network traffic in frames, and then passes the frames to an expert, and NPP application.</span></span> <span data-ttu-id="70dd3-116">НПП использует драйвер сетевой монитор системы (Nmnt.sys) для получения кадров, собранных из сети, и предоставляет несколько COM-интерфейсов, которые передают кадры эксперту, монитору и в приложение поставщика сетевых пакетов (НПП), где их можно просматривать и анализировать.</span><span class="sxs-lookup"><span data-stu-id="70dd3-116">An NPP uses the Network Monitor system driver (Nmnt.sys) to get the frames collected from the network, and provides several COM interfaces that pass the frames to an expert, monitor, and network packet provider (NPP) application where they can be displayed and analyzed.</span></span>

</dd> <dt>

<span data-ttu-id="70dd3-117"><span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**нпп**</span><span class="sxs-lookup"><span data-stu-id="70dd3-117"><span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**NPP**</span></span>
</dt> <dd>

<span data-ttu-id="70dd3-118">См. раздел поставщик сетевых пакетов.</span><span class="sxs-lookup"><span data-stu-id="70dd3-118">See network packet provider.</span></span>

</dd> <dt>

<span data-ttu-id="70dd3-119"><span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**Приложение НПП**</span><span class="sxs-lookup"><span data-stu-id="70dd3-119"><span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**NPP application**</span></span>
</dt> <dd>

<span data-ttu-id="70dd3-120">Приложение, которое обходит как средство управления сетевой монитор пользовательского интерфейса, так и монитор, и напрямую подключается к поставщику сетевых пакетов (НПП).</span><span class="sxs-lookup"><span data-stu-id="70dd3-120">An application that bypasses both the Network Monitor UI and Monitor Control Tool, and connects directly to the network packet provider (NPP).</span></span> <span data-ttu-id="70dd3-121">Приложение НПП может подключаться к компоненту НПП с помощью любого из пяти интерфейсов COM НПП.</span><span class="sxs-lookup"><span data-stu-id="70dd3-121">An NPP application can connect to the NPP component with any of the five NPP COM interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="70dd3-122"><span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**НПП Finder**</span><span class="sxs-lookup"><span data-stu-id="70dd3-122"><span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**NPP Finder**</span></span>
</dt> <dd>

<span data-ttu-id="70dd3-123">Компонент сетевой монитор, взаимодействующий с НППС.</span><span class="sxs-lookup"><span data-stu-id="70dd3-123">The Network Monitor component that communicates with NPPs.</span></span>

</dd> </dl>

 

 



