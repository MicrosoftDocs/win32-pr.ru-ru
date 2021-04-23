---
title: служба SNMP;
description: Реализация протокола SNMP в Microsoft Windows используется для настройки удаленных устройств, наблюдения за производительностью сети, аудита использования сети и обнаружения сбоев сети или неправильного доступа. Важно! API Microsoft Windows SNMP поддерживает только версии протокола до SNMPv2C. Она не поддерживает никакие более поздние версии протокола.
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP-ПРОТОКОЛ SNMP
- SNMP, страница начальной страницы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71df55c79244c0f74ef685271834adc01ca7e981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070501"
---
# <a name="snmp-service"></a><span data-ttu-id="6db7d-106">служба SNMP;</span><span class="sxs-lookup"><span data-stu-id="6db7d-106">SNMP Service</span></span>

<span data-ttu-id="6db7d-107">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="6db7d-107">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6db7d-108">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="6db7d-108">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6db7d-109">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="6db7d-109">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

## <a name="purpose"></a><span data-ttu-id="6db7d-110">Назначение</span><span class="sxs-lookup"><span data-stu-id="6db7d-110">Purpose</span></span>

<span data-ttu-id="6db7d-111">Реализация протокола SNMP в Microsoft Windows используется для настройки удаленных устройств, наблюдения за производительностью сети, аудита использования сети и обнаружения сбоев сети или неправильного доступа.</span><span class="sxs-lookup"><span data-stu-id="6db7d-111">The Microsoft Windows implementation of the Simple Network Management Protocol (SNMP) is used to configure remote devices, monitor network performance, audit network usage, and detect network faults or inappropriate access.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6db7d-112">API Microsoft Windows SNMP поддерживает только версии протокола до SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="6db7d-112">The Microsoft Windows SNMP API only supports protocol versions up to SNMPv2C.</span></span> <span data-ttu-id="6db7d-113">Она не поддерживает никакие более поздние версии протокола.</span><span class="sxs-lookup"><span data-stu-id="6db7d-113">It does not support any later versions of the protocol.</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="6db7d-114">Где применимо</span><span class="sxs-lookup"><span data-stu-id="6db7d-114">Where applicable</span></span>

<span data-ttu-id="6db7d-115">Протокол SNMP использует распределенную архитектуру, состоящую из приложений управления и агентов.</span><span class="sxs-lookup"><span data-stu-id="6db7d-115">SNMP uses a distributed architecture consisting of management applications and agent applications.</span></span> <span data-ttu-id="6db7d-116">Служба SNMP реализует агент SNMP.</span><span class="sxs-lookup"><span data-stu-id="6db7d-116">The SNMP service implements an SNMP agent.</span></span> <span data-ttu-id="6db7d-117">Чтобы использовать сведения, предоставляемые службой SNMP, необходимо наличие хотя бы одного узла, на котором выполняется приложение управления SNMP.</span><span class="sxs-lookup"><span data-stu-id="6db7d-117">To use the information the SNMP service provides, you must have at least one host that is running an SNMP management application.</span></span> <span data-ttu-id="6db7d-118">Можно использовать стороннее программное обеспечение управления SNMP или разработать собственное программное приложение для управления SNMP.</span><span class="sxs-lookup"><span data-stu-id="6db7d-118">You can use third-party SNMP management software, or you can develop your own SNMP management software application.</span></span> <span data-ttu-id="6db7d-119">Для этой цели доступны следующие API:</span><span class="sxs-lookup"><span data-stu-id="6db7d-119">The following APIs are available for this purpose:</span></span>

-   <span data-ttu-id="6db7d-120">API управления SNMP — набор функций, которые можно использовать для быстрой разработки основных систем управления SNMP.</span><span class="sxs-lookup"><span data-stu-id="6db7d-120">SNMP Management API, a set of functions that can be used to quickly develop basic SNMP management systems</span></span>
-   <span data-ttu-id="6db7d-121">WinSNMP API, версия 2,0, набор функций для кодирования, декодирования, отправки и получения сообщений SNMP</span><span class="sxs-lookup"><span data-stu-id="6db7d-121">WinSNMP API, version 2.0, a set of functions for encoding, decoding, sending, and receiving SNMP messages</span></span>

<span data-ttu-id="6db7d-122">Кроме того, API агента расширения SNMP определяет интерфейс между службой SNMP и библиотеками DLL агента расширения SNMP сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="6db7d-122">Additionally, the SNMP Extension Agent API defines the interface between the SNMP service and third-party SNMP extension agent DLLs.</span></span> <span data-ttu-id="6db7d-123">Функции API служебной программы SNMP можно использовать для упрощения обработки сообщений SNMP.</span><span class="sxs-lookup"><span data-stu-id="6db7d-123">The SNMP Utility API functions can be used to simplify the processing of SNMP messages.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6db7d-124">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="6db7d-124">Developer audience</span></span>

<span data-ttu-id="6db7d-125">API-интерфейсы, перечисленные в предыдущем разделе, предназначены для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="6db7d-125">The APIs listed in the preceding section are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="6db7d-126">Знание протоколов SNMP и SNMPv2C, а также опыта работы с сетевыми и сетевыми принципами управления, являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="6db7d-126">Familiarity with SNMP and SNMPv2C, as well as a working knowledge of networking and network management concepts, are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6db7d-127">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="6db7d-127">Run-time requirements</span></span>

<span data-ttu-id="6db7d-128">Дополнительные сведения об операционной системе, необходимой для использования определенной функции, см. в разделе "требования" на странице справки по этой функции.</span><span class="sxs-lookup"><span data-stu-id="6db7d-128">For more information about the operating system required to use a particular function, see the Requirements section of the reference page for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6db7d-129">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="6db7d-129">In this section</span></span>



| <span data-ttu-id="6db7d-130">Раздел</span><span class="sxs-lookup"><span data-stu-id="6db7d-130">Topic</span></span>                                                                                                | <span data-ttu-id="6db7d-131">Описание</span><span class="sxs-lookup"><span data-stu-id="6db7d-131">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6db7d-132">Новые в SNMP</span><span class="sxs-lookup"><span data-stu-id="6db7d-132">New in SNMP</span></span>](new-in-snmp.md)<br/>                                                            | <span data-ttu-id="6db7d-133">Сведения об обновлениях протокола SNMP.</span><span class="sxs-lookup"><span data-stu-id="6db7d-133">Information on updates to SNMP.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="6db7d-134">Протокол SNMP</span><span class="sxs-lookup"><span data-stu-id="6db7d-134">Simple Network Management Protocol (SNMP)</span></span>](simple-network-management-protocol-snmp-.md)<br/> | <span data-ttu-id="6db7d-135">Сведения и Справочник по API для SNMP, включая API управления SNMP, API агента расширения SNMP и служебную программу SNMP API.</span><span class="sxs-lookup"><span data-stu-id="6db7d-135">Information and API reference for SNMP, including the SNMP Management API, SNMP Extension Agent API, and SNMP Utility API functions.</span></span><br/> |
| [<span data-ttu-id="6db7d-136">WinSNMP API</span><span class="sxs-lookup"><span data-stu-id="6db7d-136">WinSNMP API</span></span>](snmp-reference.md)<br/>                                                         | <span data-ttu-id="6db7d-137">Информация и Справочник по API для интерфейса прикладного программирования Microsoft Windows SNMP (WinSNMP API).</span><span class="sxs-lookup"><span data-stu-id="6db7d-137">Information and API reference for the Microsoft Windows SNMP Application Programming Interface (WinSNMP API).</span></span> <br/>                       |



 

## <a name="related-topics"></a><span data-ttu-id="6db7d-138">См. также</span><span class="sxs-lookup"><span data-stu-id="6db7d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6db7d-139">Протокол DHCP</span><span class="sxs-lookup"><span data-stu-id="6db7d-139">Dynamic Host Configuration Protocol (DHCP)</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[<span data-ttu-id="6db7d-140">Управление сетью</span><span class="sxs-lookup"><span data-stu-id="6db7d-140">Network Management</span></span>](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[<span data-ttu-id="6db7d-141">Служба маршрутизации и удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="6db7d-141">Routing and Remote Access Service</span></span>](/windows/desktop/RRAS/portal)
</dt> </dl>

 

