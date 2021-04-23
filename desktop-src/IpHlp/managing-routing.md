---
description: Вспомогательная служба IP предоставляет функции для управления сетевой маршрутизацией. Используйте следующие функции для управления таблицей IP-маршрутизации и получения других сведений о маршрутизации.
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: Управление маршрутизацией
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec199de19b4c8d724fbe6a2e77c3fac7dc19b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897205"
---
# <a name="managing-routing"></a><span data-ttu-id="8478d-104">Управление маршрутизацией</span><span class="sxs-lookup"><span data-stu-id="8478d-104">Managing Routing</span></span>

<span data-ttu-id="8478d-105">Вспомогательная служба IP предоставляет функции для управления сетевой маршрутизацией.</span><span class="sxs-lookup"><span data-stu-id="8478d-105">IP Helper provides features to manage network routing.</span></span> <span data-ttu-id="8478d-106">Используйте следующие функции для управления таблицей IP-маршрутизации и получения других сведений о маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="8478d-106">Use the following functions to manage the IP routing table, and to obtain other routing information.</span></span>

<span data-ttu-id="8478d-107">Извлеките содержимое таблицы маршрутизации IP, вызвав функцию [**жетипфорвардтабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) .</span><span class="sxs-lookup"><span data-stu-id="8478d-107">Retrieve the contents of the IP routing table by making a call to the [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) function.</span></span> <span data-ttu-id="8478d-108">Управлять конкретными записями в таблице IP-маршрутизации с помощью функций [**креатеипфорвардентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**делетеипфорвардентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)и [**сетипфорвардентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) .</span><span class="sxs-lookup"><span data-stu-id="8478d-108">Manipulate specific entries in the IP routing table using the [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry), and [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) functions.</span></span> <span data-ttu-id="8478d-109">Используйте функцию **креатеипфорвардентри** для добавления новой записи таблицы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="8478d-109">Use the **CreateIpForwardEntry** function to add a new routing table entry.</span></span> <span data-ttu-id="8478d-110">Используйте функцию **делетеипфорвардентри** для удаления существующей записи.</span><span class="sxs-lookup"><span data-stu-id="8478d-110">Use the **DeleteIpForwardEntry** function to remove an existing entry.</span></span> <span data-ttu-id="8478d-111">Функция **сетипфорвардентри** изменяет существующую запись.</span><span class="sxs-lookup"><span data-stu-id="8478d-111">The **SetIpForwardEntry** function modifies an existing entry.</span></span>

<span data-ttu-id="8478d-112">Возможности управления маршрутизаторами вспомогательного метода IP можно использовать для получения сведений о маршрутизации датаграмм по сети.</span><span class="sxs-lookup"><span data-stu-id="8478d-112">The router management capabilities of IP Helper can be used to retrieve information about how datagrams are routed over the network.</span></span> <span data-ttu-id="8478d-113">Функция [**жетбестрауте**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) получает оптимальный маршрут к указанному адресу назначения.</span><span class="sxs-lookup"><span data-stu-id="8478d-113">The [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) function retrieves the best route to a specified destination address.</span></span> <span data-ttu-id="8478d-114">Функция [**жетбестинтерфаце**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) извлекает индекс интерфейса, используемого лучшим маршрутом, к указанному адресу назначения.</span><span class="sxs-lookup"><span data-stu-id="8478d-114">The [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) function retrieves the index of the interface used by the best route to a specified destination address.</span></span> <span data-ttu-id="8478d-115">Наконец, функция [**жетрттандхопкаунт**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) получает время приема-передачи (RTT) и число прыжков до указанного адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="8478d-115">Lastly, the [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) function retrieves the round-trip time (RTT) and number of hops to a specified destination address.</span></span>

 

 



