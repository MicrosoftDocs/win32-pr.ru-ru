---
description: При отправке на адрес назначения для многоадресной рассылки протокол IPv6 обычно требует, чтобы в приложении был указан исходящий интерфейс.
ms.assetid: dbfeaa1f-a7c5-4a15-90f0-4d1cdaf798e9
title: IPv6-адреса назначения для многоадресной рассылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aa516713fb47f6af03d8564c464a07a19cf0f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497454"
---
# <a name="ipv6-multicast-destination-addresses"></a><span data-ttu-id="c6474-103">IPv6-адреса назначения для многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="c6474-103">IPv6 Multicast Destination Addresses</span></span>

<span data-ttu-id="c6474-104">При отправке на адрес назначения для многоадресной рассылки протокол IPv6 обычно требует, чтобы в приложении был указан исходящий интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c6474-104">When sending to a multicast destination address, the Microsoft IPv6 protocol normally requires that the application have an outgoing interface specified.</span></span> <span data-ttu-id="c6474-105">Это можно сделать с помощью **параметра \_ многоадресная рассылка IPv6 \_ при** использовании сокета или путем привязки сокета к определенному исходному адресу.</span><span class="sxs-lookup"><span data-stu-id="c6474-105">This is done with the **IPV6\_MULTICAST\_IF** socket option or by binding the socket to a specific source address.</span></span>

<span data-ttu-id="c6474-106">Можно также указать интерфейс по умолчанию для конкретного адреса многоадресной рассылки, всю многоадресную область адресов или все адреса многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="c6474-106">You can also specify a default interface for a specific multicast address, an entire multicast address scope, or all multicast addresses.</span></span> <span data-ttu-id="c6474-107">Это делается с помощью маршрута, который помещает префикс многоадресной рассылки в ссылку на нужный исходящий интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c6474-107">This is done with a route that places the multicast prefix on-link to the desired outgoing interface.</span></span> <span data-ttu-id="c6474-108">В следующих примерах показано, как это можно указать:</span><span class="sxs-lookup"><span data-stu-id="c6474-108">For following examples show how this can be specified:</span></span>

``` syntax
ipv6 rtu ff02::5/128 3
ipv6 rtu ff0e::/16 3
ipv6 rtu ff00::/8 3
```

 

 



