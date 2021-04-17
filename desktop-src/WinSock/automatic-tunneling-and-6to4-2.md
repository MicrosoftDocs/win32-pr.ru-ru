---
description: Автоматическое туннелирование с IPv4-совместимыми адресами и 6to4 работают через маршрут для префикса, который находится по ссылке на интерфейс \# 2. Биты 32, следующие за префиксом, извлекаются и используются в качестве адреса назначения IPv4 для инкапсулированного пакета.
ms.assetid: 92261a1b-2b7f-4a76-b98a-2631dc303618
title: Автоматическое туннелирование IPv6 и 6to4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede1179902a7ec3276058e078d56e069603e54a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711047"
---
# <a name="ipv6-automatic-tunneling-and-6to4"></a><span data-ttu-id="598af-104">Автоматическое туннелирование IPv6 и 6to4</span><span class="sxs-lookup"><span data-stu-id="598af-104">IPv6 Automatic Tunneling and 6to4</span></span>

<span data-ttu-id="598af-105">Автоматическое туннелирование с IPv4-совместимыми адресами и 6to4 работают через маршрут для префикса, который находится по ссылке на интерфейс \# 2.</span><span class="sxs-lookup"><span data-stu-id="598af-105">Automatic tunneling with IPv4-compatible addresses and 6to4 both work through a route for a prefix that is on-link to interface \#2.</span></span> <span data-ttu-id="598af-106">Биты 32, следующие за префиксом, извлекаются и используются в качестве адреса назначения IPv4 для инкапсулированного пакета.</span><span class="sxs-lookup"><span data-stu-id="598af-106">The 32 bits following the prefix are extracted and used as an IPv4 destination address for the encapsulated packet.</span></span>

<span data-ttu-id="598af-107">При автоматическом туннелировании используется префикс::/96, который включен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="598af-107">Automatic tunneling uses the ::/96 prefix, which is enabled by default.</span></span> <span data-ttu-id="598af-108">Его можно отключить, удалив маршрут для::/96.</span><span class="sxs-lookup"><span data-stu-id="598af-108">It can be disabled by removing the route for ::/96.</span></span>

<span data-ttu-id="598af-109">6to4 использует префикс 2002::/16, который не включен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="598af-109">6to4 uses the 2002::/16 prefix, which is not enabled by default.</span></span>

 

 



