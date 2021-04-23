---
description: Облака используются инфраструктурами группирования и построения одноранговых узлов.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Облака
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d668387c78b3c22e49e98585494a36506cc74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156542"
---
# <a name="clouds"></a><span data-ttu-id="1b1f9-103">Облака</span><span class="sxs-lookup"><span data-stu-id="1b1f9-103">Clouds</span></span>

<span data-ttu-id="1b1f9-104">Облака используются инфраструктурами [группирования](grouping-api.md) и [построения](graphing-api.md) одноранговых узлов.</span><span class="sxs-lookup"><span data-stu-id="1b1f9-104">Clouds are used by the Peer [Grouping](grouping-api.md) and [Graphing](graphing-api.md) Infrastructures.</span></span> <span data-ttu-id="1b1f9-105">[Протокол PNRP](pnrp-namespace-provider-api.md) определяет облако как набор одноранговых узлов, которые могут взаимодействовать в одной области IPv6.</span><span class="sxs-lookup"><span data-stu-id="1b1f9-105">The [Peer Name Resolution Protocol (PNRP)](pnrp-namespace-provider-api.md) identifies a cloud as a set of peers that can communicate within the same IPv6 scope.</span></span> <span data-ttu-id="1b1f9-106">Облака тесно связаны с областями IPv6.</span><span class="sxs-lookup"><span data-stu-id="1b1f9-106">Clouds are closely related to the IPv6 scopes.</span></span> <span data-ttu-id="1b1f9-107">В следующем списке перечислены некоторые из уникальных облачных функций.</span><span class="sxs-lookup"><span data-stu-id="1b1f9-107">The following list identifies some of the unique cloud features:</span></span>

-   <span data-ttu-id="1b1f9-108">Облако идентифицируется по имени, а доступные облака можно перечислить с помощью [**всалукупсервицебегин**](pnrp-and-wsalookupservicebegin.md).</span><span class="sxs-lookup"><span data-stu-id="1b1f9-108">A cloud is identified by a name, and available clouds can be enumerated by using [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).</span></span>
-   <span data-ttu-id="1b1f9-109">Если компьютер подключен к Интернету, он входит в состав глобального облака, который определяется строкой "Global \_ ".</span><span class="sxs-lookup"><span data-stu-id="1b1f9-109">If a computer is connected to the Internet, it is part of a global cloud, which is identified by the string "Global\_".</span></span>
-   <span data-ttu-id="1b1f9-110">Если компьютер подключен к одной или нескольким локальным сетям (LAN), для каждого канала доступны отдельные облака.</span><span class="sxs-lookup"><span data-stu-id="1b1f9-110">If a computer is connected to one or more local area networks (LAN), individual clouds are available for each link.</span></span>
-   <span data-ttu-id="1b1f9-111">Один компьютер может быть подключен к нескольким сетям с помощью нескольких сетевых адаптеров или виртуальной частной сети (VPN). Это означает, что компьютер с одним интерфейсом может быть виден во многих облаках.</span><span class="sxs-lookup"><span data-stu-id="1b1f9-111">One computer can be connected to many networks by having multiple network adapters or by using a virtual private network (VPN), which means that a computer with one interface can be visible in many clouds.</span></span>
-   <span data-ttu-id="1b1f9-112">Протокол PNRP можно использовать для регистрации и разрешения имен одноранговых узлов в определенном облаке.</span><span class="sxs-lookup"><span data-stu-id="1b1f9-112">You can use PNRP to register and resolve peer names in a specific cloud.</span></span>

 

 



