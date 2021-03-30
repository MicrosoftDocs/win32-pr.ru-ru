---
description: В коде есть ограничение, которое получает инкапсулированные (нисходящее) пакеты и демультиплексирование их к определенному интерфейсу.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: Туннельные пакеты с перенаправлением IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95f88a90a358317cf46516808a96f93b792dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897337"
---
# <a name="ipv6-forwarding-tunneled-packets"></a><span data-ttu-id="5e0be-103">Туннельные пакеты с перенаправлением IPv6</span><span class="sxs-lookup"><span data-stu-id="5e0be-103">IPv6 Forwarding Tunneled Packets</span></span>

<span data-ttu-id="5e0be-104">В коде есть ограничение, которое получает инкапсулированные (нисходящее) пакеты и демультиплексирование их к определенному интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="5e0be-104">There is a limitation in the code that receives encapsulated (tunneled) packets and demultiplexes them to a specific interface.</span></span> <span data-ttu-id="5e0be-105">Если вы хотите пересылать туннельные пакеты, полученные через настроенный туннель, необходимо включить пересылку на всех интерфейсах с 6 по 4, а также через интерфейс \# 2.</span><span class="sxs-lookup"><span data-stu-id="5e0be-105">If you want to forward tunneled packets received through a configured tunnel, then it is necessary to enable forwarding on any 6-over-4 interfaces as well as interface \#2.</span></span> <span data-ttu-id="5e0be-106">Просто включить пересылку в интерфейсе \# 2 не удастся.</span><span class="sxs-lookup"><span data-stu-id="5e0be-106">Just enabling forwarding on interface \#2 will not work.</span></span> <span data-ttu-id="5e0be-107">Как правило, при настройке маршрутизатора необходимо включить пересылку для всех интерфейсов, кроме замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="5e0be-107">Typically when configuring a router, you would enable forwarding on all interfaces except loopback.</span></span>

 

 



