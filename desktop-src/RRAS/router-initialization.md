---
title: Инициализация маршрутизатора
description: Сведения о конфигурации маршрутизатора, диспетчеры маршрутизаторов и протоколы маршрутизации и клиенты делятся на глобальные сведения и сведения о интерфейсах, которые хранятся в реестре и файле телефонной книги маршрутизатора, router. pbk.
ms.assetid: c54541c1-6508-448a-a211-5fca634a184a
keywords:
- маршрутизаторы RRAS, инициализация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d45c10ef7b44b6dfe9d2d84149c77c81c5752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772584"
---
# <a name="router-initialization"></a><span data-ttu-id="de091-104">Инициализация маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="de091-104">Router Initialization</span></span>

<span data-ttu-id="de091-105">Сведения о конфигурации маршрутизатора, диспетчеры маршрутизаторов и протоколы маршрутизации и клиенты делятся на глобальные сведения и сведения о интерфейсах, которые хранятся в реестре и файле телефонной книги маршрутизатора, router. pbk.</span><span class="sxs-lookup"><span data-stu-id="de091-105">Configuration information for the router, the router managers and the routing protocols/clients is divided into global information and per interface information and is stored in the registry and the router's phone-book file, Router.pbk.</span></span>

<span data-ttu-id="de091-106">При запуске процесса маршрутизатора DIM (диспетчер динамических интерфейсов) считывает конфигурацию маршрутизатора из реестра.</span><span class="sxs-lookup"><span data-stu-id="de091-106">When the router process starts, DIM (Dynamic Interface Manager) reads the router configuration from the registry.</span></span> <span data-ttu-id="de091-107">DIM создает интерфейсы, заданные сведениями интерфейса.</span><span class="sxs-lookup"><span data-stu-id="de091-107">DIM creates the interfaces that are specified by the interface information.</span></span>

<span data-ttu-id="de091-108">DIM также получает глобальные сведения диспетчера маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="de091-108">DIM also retrieves the global router manager information.</span></span> <span data-ttu-id="de091-109">DIM запускает диспетчеры маршрутизаторов, соответствующие этой информации, и передает их сведения.</span><span class="sxs-lookup"><span data-stu-id="de091-109">DIM starts the router managers that correspond to this information, and passes them the information.</span></span> <span data-ttu-id="de091-110">Например, если DIM находит глобальные сведения для диспетчера IP-маршрутизаторов в реестре, то DIM запускает диспетчер IP-маршрутизаторов и передает ему глобальную информацию.</span><span class="sxs-lookup"><span data-stu-id="de091-110">For example, if DIM finds global information for the IP router manager in the registry, DIM starts the IP router manager and passes it the global information.</span></span> <span data-ttu-id="de091-111">Если в реестре для определенного диспетчера маршрутизаторов нет глобальных сведений, DIM не запускает этот диспетчер маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="de091-111">If no global information is present in the registry for a particular router manager, DIM does not start that router manager.</span></span>

<span data-ttu-id="de091-112">Диспетчеры маршрутизаторов проверяют глобальную информацию, полученную от DIM.</span><span class="sxs-lookup"><span data-stu-id="de091-112">The router managers examine the global information received from DIM.</span></span> <span data-ttu-id="de091-113">Если диспетчер маршрутизатора находит сведения, относящиеся к конкретному клиенту, в глобальной информации, диспетчер маршрутизатора загружает библиотеку DLL для клиента (например IpNAT.dll) и инициализирует клиент, вызывая функции клиента [**регистерпротокол**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) и [**стартпротокол**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) .</span><span class="sxs-lookup"><span data-stu-id="de091-113">If the router manager finds information specific to a particular client within the global information, the router manager loads the DLL for the client (for example IpNAT.dll) and initializes the client by calling the client's [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) and [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) functions.</span></span> <span data-ttu-id="de091-114">Диспетчер маршрутизатора передает клиентские глобальные сведения клиенту в вызове [**стартпротокол**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).</span><span class="sxs-lookup"><span data-stu-id="de091-114">The router manager passes the client-specific global information to the client in the call to [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).</span></span>

<span data-ttu-id="de091-115">На каждом этапе информация, передаваемая следующей сущности, непрозрачна для сущности, предшествующей ей.</span><span class="sxs-lookup"><span data-stu-id="de091-115">At each stage, the information being passed to the next entity is opaque to the entity preceding it.</span></span> <span data-ttu-id="de091-116">То есть, DIM не интерпретирует глобальные сведения для диспетчера IP-маршрутизаторов, помимо того факта, что информация предназначена для диспетчера IP-маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="de091-116">That is, DIM does not interpret the global information for the IP Router Manager, beyond the fact that the information is meant for the IP Router Manager.</span></span> <span data-ttu-id="de091-117">Аналогичным образом диспетчер IP-маршрутизаторов не интерпретирует сведения, относящиеся к OSPF, помимо того факта, что это OSPF-информация.</span><span class="sxs-lookup"><span data-stu-id="de091-117">Similarly, the IP Router Manager does not interpret the OSPF specific information beyond the fact that it is OSPF information.</span></span>

 

 




