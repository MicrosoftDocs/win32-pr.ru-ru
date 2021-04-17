---
description: Указывает префикс, который находится по ссылке на интерфейс \# 4.
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: Префиксы сайта IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed8a21c59f9b6727c98ccb7fdacf4e9ec6ea5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711018"
---
# <a name="ipv6-site-prefixes"></a><span data-ttu-id="e633f-103">Префиксы сайта IPv6</span><span class="sxs-lookup"><span data-stu-id="e633f-103">IPv6 Site Prefixes</span></span>

<span data-ttu-id="e633f-104">Команда IPv6 рту позволяет публиковать префиксы по ссылке для настройки с длиной префикса сайта.</span><span class="sxs-lookup"><span data-stu-id="e633f-104">The ipv6 rtu command allows published on-link prefixes to be configured with a site prefix length.</span></span> <span data-ttu-id="e633f-105">Если задано значение, длина префикса сайта помещается в параметр сведений о префиксе в объявлениях маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="e633f-105">If specified, the site prefix length is put into a prefix information option in router advertisements.</span></span> <span data-ttu-id="e633f-106">Пример:</span><span class="sxs-lookup"><span data-stu-id="e633f-106">For example:</span></span>

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

<span data-ttu-id="e633f-107">Указывает префикс, который находится по ссылке на интерфейс \# 4.</span><span class="sxs-lookup"><span data-stu-id="e633f-107">specifies a prefix that is on-link to interface \#4.</span></span> <span data-ttu-id="e633f-108">Префикс опубликован, то есть он включается в объявления маршрутизатора, если интерфейс \# 4 является интерфейсом объявления.</span><span class="sxs-lookup"><span data-stu-id="e633f-108">The prefix is published, meaning that it is included in router advertisements if interface \#4 is an advertising interface.</span></span> <span data-ttu-id="e633f-109">Время жизни в параметре "сведения о префиксе" составляет 1800 секунд (30 минут).</span><span class="sxs-lookup"><span data-stu-id="e633f-109">The lifetime in the prefix information option is 1800 seconds (30 minutes).</span></span> <span data-ttu-id="e633f-110">Длина префикса сайта в параметре сведений о префиксе равна 48.</span><span class="sxs-lookup"><span data-stu-id="e633f-110">The site prefix length in the prefix information option is 48.</span></span>

<span data-ttu-id="e633f-111">Параметр получение сведений о префиксе, указывающий префикс сайта, приводит к созданию записи в таблице префиксов сайта, которую можно отобразить с помощью команды IPv6 СПТ.</span><span class="sxs-lookup"><span data-stu-id="e633f-111">The receipt of a prefix information option that specifies a site prefix causes an entry to be created in the site prefix table, which can be displayed by using the ipv6 spt command.</span></span> <span data-ttu-id="e633f-112">Таблица префиксов сайтов используется для удаления недопустимых адресов локального сайта, возвращенных [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) и связанными функциями.</span><span class="sxs-lookup"><span data-stu-id="e633f-112">The site prefix table is used to remove inappropriate site-local addresses from those returned by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and related functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e633f-113">См. также</span><span class="sxs-lookup"><span data-stu-id="e633f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e633f-114">Локальная связь IPv6 и локальные адреса сайтов</span><span class="sxs-lookup"><span data-stu-id="e633f-114">IPv6 Link-local and Site-local Addresses</span></span>](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="e633f-115">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="e633f-115">Netsh.exe</span></span>](netsh-exe.md)
</dt> </dl>

 

 



