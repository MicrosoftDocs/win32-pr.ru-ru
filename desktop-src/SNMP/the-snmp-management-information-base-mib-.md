---
title: База данных управления SNMP (MIB)
description: База данных управления (MIB) описывает набор управляемых объектов. Консольное приложение управления SNMP может управлять объектами на определенном компьютере, если в службе SNMP есть библиотека DLL агента расширения, поддерживающая MIB.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba4612c026aa5a3a1a1574556f58207bad08e06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774363"
---
# <a name="the-snmp-management-information-base-mib"></a><span data-ttu-id="a8f65-104">База данных управления SNMP (MIB)</span><span class="sxs-lookup"><span data-stu-id="a8f65-104">The SNMP Management Information Base (MIB)</span></span>

<span data-ttu-id="a8f65-105">База данных управления (MIB) описывает набор управляемых объектов.</span><span class="sxs-lookup"><span data-stu-id="a8f65-105">A Management Information Base (MIB) describes a set of managed objects.</span></span> <span data-ttu-id="a8f65-106">Консольное приложение управления SNMP может управлять объектами на определенном компьютере, если в службе SNMP есть библиотека DLL агента расширения, поддерживающая MIB.</span><span class="sxs-lookup"><span data-stu-id="a8f65-106">An SNMP management console application can manipulate the objects on a specific computer if the SNMP service has an extension agent DLL that supports the MIB.</span></span>

<span data-ttu-id="a8f65-107">Каждый управляемый объект в MIB имеет уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="a8f65-107">Each managed object in a MIB has a unique identifier.</span></span> <span data-ttu-id="a8f65-108">Идентификатор включает тип объекта (например, счетчик, строка, датчик или адрес), уровень доступа объекта (например, чтение или чтение/запись), ограничения размера и сведения о диапазоне.</span><span class="sxs-lookup"><span data-stu-id="a8f65-108">The identifier includes the object's type (such as counter, string, gauge, or address), the object's access level (such as read or read/write), size restrictions, and range information.</span></span>

<span data-ttu-id="a8f65-109">В следующей таблице содержится частичный список MIB, поставляемых с системой.</span><span class="sxs-lookup"><span data-stu-id="a8f65-109">The following table contains a partial list of the MIBs that ship with the system.</span></span> <span data-ttu-id="a8f65-110">Они устанавливаются вместе со службой SNMP в каталоге% systemroot% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="a8f65-110">They are installed with the SNMP service in the %systemroot%\\system32 directory.</span></span> <span data-ttu-id="a8f65-111">Полный список MIB см. в разделе Windows Resource Kit.</span><span class="sxs-lookup"><span data-stu-id="a8f65-111">For a complete listing of MIBs, refer to the Windows Resource Kit.</span></span>



| <span data-ttu-id="a8f65-112">MIB</span><span class="sxs-lookup"><span data-stu-id="a8f65-112">MIB</span></span>         | <span data-ttu-id="a8f65-113">Описание</span><span class="sxs-lookup"><span data-stu-id="a8f65-113">Description</span></span>                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f65-114">Служба. MIB</span><span class="sxs-lookup"><span data-stu-id="a8f65-114">DHCP.MIB</span></span>    | <span data-ttu-id="a8f65-115">Определяемая корпорацией Майкрософт MIB, которая содержит типы объектов для мониторинга сетевого трафика между удаленными узлами и DHCP-серверами.</span><span class="sxs-lookup"><span data-stu-id="a8f65-115">Microsoft-defined MIB that contains object types for monitoring the network traffic between remote hosts and DHCP servers</span></span>                        |
| <span data-ttu-id="a8f65-116">ХОСТМИБ. MIB</span><span class="sxs-lookup"><span data-stu-id="a8f65-116">HOSTMIB.MIB</span></span> | <span data-ttu-id="a8f65-117">Содержит типы объектов для мониторинга и управления ресурсами узла</span><span class="sxs-lookup"><span data-stu-id="a8f65-117">Contains object types for monitoring and managing host resources</span></span>                                                                                 |
| <span data-ttu-id="a8f65-118">LMMIB2. MIB</span><span class="sxs-lookup"><span data-stu-id="a8f65-118">LMMIB2.MIB</span></span>  | <span data-ttu-id="a8f65-119">Описание служб рабочей станции и сервера</span><span class="sxs-lookup"><span data-stu-id="a8f65-119">Covers workstation and server services</span></span>                                                                                                           |
| <span data-ttu-id="a8f65-120">MIB \_ II. MIB</span><span class="sxs-lookup"><span data-stu-id="a8f65-120">MIB\_II.MIB</span></span> | <span data-ttu-id="a8f65-121">Содержит базу управляющих данных (MIB-II), которая предоставляет простую, работоспособную архитектуру и систему для управления Интернет-клиентами на основе TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="a8f65-121">Contains the Management Information Base (MIB-II), which provides a simple, workable architecture and system for managing TCP/IP-based internets</span></span> |
| <span data-ttu-id="a8f65-122">Адрес. MIB</span><span class="sxs-lookup"><span data-stu-id="a8f65-122">WINS.MIB</span></span>    | <span data-ttu-id="a8f65-123">Определяемая корпорацией Майкрософт MIB для службы Windows Internet Name Service (WINS)</span><span class="sxs-lookup"><span data-stu-id="a8f65-123">Microsoft-defined MIB for the Windows Internet Name Service (WINS)</span></span>                                                                               |



 

<span data-ttu-id="a8f65-124">**Windows NT:** Как правило, можно скопировать MIB из агента расширения SNMP, который поддерживает определенную MIB.</span><span class="sxs-lookup"><span data-stu-id="a8f65-124">**Windows NT:** Typically, you can copy a MIB from the SNMP extension agent that supports the particular MIB.</span></span> <span data-ttu-id="a8f65-125">Некоторые дополнительные MIB доступны в комплекте Windows NT 4,0 Resource Kit.</span><span class="sxs-lookup"><span data-stu-id="a8f65-125">Some additional MIBs are available with the Windows NT 4.0 Resource Kit.</span></span>

<span data-ttu-id="a8f65-126">Библиотеки DLL агента расширения для MIB-II, диспетчера LAN MIB-II и MIB ресурсов узла устанавливаются вместе со службой SNMP.</span><span class="sxs-lookup"><span data-stu-id="a8f65-126">The extension agent DLLs for MIB-II, LAN Manager MIB-II, and the Host Resources MIB are installed with the SNMP service.</span></span> <span data-ttu-id="a8f65-127">Библиотеки DLL агента расширения для других MIB устанавливаются при установке соответствующих служб.</span><span class="sxs-lookup"><span data-stu-id="a8f65-127">The extension agent DLLs for the other MIBs are installed when their respective services are installed.</span></span> <span data-ttu-id="a8f65-128">Во время запуска службы SNMP загружает все библиотеки DLL агента расширения, перечисленные в реестре.</span><span class="sxs-lookup"><span data-stu-id="a8f65-128">At service startup time, the SNMP service loads all of the extension agent DLLs that are listed in the registry.</span></span>

<span data-ttu-id="a8f65-129">Пользователи могут добавлять другие библиотеки DLL агента расширения, которые реализуют дополнительные MIB.</span><span class="sxs-lookup"><span data-stu-id="a8f65-129">Users can add other extension agent DLLs that implement additional MIBs.</span></span> <span data-ttu-id="a8f65-130">Для этого необходимо добавить запись реестра для новой библиотеки DLL в службе SNMP.</span><span class="sxs-lookup"><span data-stu-id="a8f65-130">To do this, they must add a registry entry for the new DLL under the SNMP service.</span></span> <span data-ttu-id="a8f65-131">Кроме того, они должны зарегистрировать новую MIB с помощью консольного приложения управления SNMP.</span><span class="sxs-lookup"><span data-stu-id="a8f65-131">They must also register the new MIB with the SNMP management console application.</span></span> <span data-ttu-id="a8f65-132">Дополнительные сведения см. в документации, входящей в состав консольного приложения управления.</span><span class="sxs-lookup"><span data-stu-id="a8f65-132">For more information, see the documentation included with your management console application.</span></span>

<span data-ttu-id="a8f65-133">Дополнительные сведения см. в разделе [MIB Name Tree](mib-name-tree.md).</span><span class="sxs-lookup"><span data-stu-id="a8f65-133">For more information, see [MIB Name Tree](mib-name-tree.md).</span></span>

 

 




