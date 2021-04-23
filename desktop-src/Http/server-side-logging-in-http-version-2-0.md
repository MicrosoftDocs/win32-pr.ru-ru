---
title: Ведение журнала Server-Side
description: Ведение журнала на стороне сервера доступно в группе URL-адресов или сеансе сервера.
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b76548b296bcdbd343e4e259e0cf3c87537ef5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888728"
---
# <a name="server-side-logging"></a><span data-ttu-id="4a9a9-103">Ведение журнала Server-Side</span><span class="sxs-lookup"><span data-stu-id="4a9a9-103">Server-Side Logging</span></span>

<span data-ttu-id="4a9a9-104">Ведение журнала на стороне сервера доступно в группе URL-адресов или сеансе сервера.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-104">Server-side logging is available on a URL group or server session.</span></span> <span data-ttu-id="4a9a9-105">Если ведение журнала включено в сеансе сервера, оно работает как централизованное ведение журнала для всех групп URL-адресов в сеансе сервера.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-105">When logging is enabled on a server session, it functions as centralized form of logging for all the URL groups under the server session.</span></span> <span data-ttu-id="4a9a9-106">Если ведение журнала включено в группе URL-адресов, ведение журнала выполняется только для запросов, направляемых в группу URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-106">When logging is enabled on a URL group, logging is performed only on requests that are routed to the URL Group.</span></span> <span data-ttu-id="4a9a9-107">API HTTP-сервера поддерживает следующие типы ведения журнала:</span><span class="sxs-lookup"><span data-stu-id="4a9a9-107">The following types of logging are supported by the HTTP Server API:</span></span>

-   <span data-ttu-id="4a9a9-108">[Ведение журнала W3C](w3c-logging.md): доступно в сеансе сервера и группе URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-108">[W3C logging](w3c-logging.md): Available on the server session and URL group.</span></span>
-   <span data-ttu-id="4a9a9-109">[Ведение журнала NCSA](ncsa-logging.md): доступно в группе URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-109">[NCSA logging](ncsa-logging.md): Available on the URL group.</span></span>
-   <span data-ttu-id="4a9a9-110">[Ведение журнала IIS](iis-logging.md): доступно в группе URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-110">[IIS logging](iis-logging.md): Available on the URL group.</span></span>
-   <span data-ttu-id="4a9a9-111">[Централизованное ведение журнала в двоичном формате](centralized-binary-logging.md): доступно в сеансе сервера.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-111">[Centralized binary logging](centralized-binary-logging.md): Available on the server session.</span></span>

<span data-ttu-id="4a9a9-112">Чтобы воспользоваться функцией ведения журнала HTTP, приложение включает и настраивает один тип ведения журнала в сеансе сервера или группе URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-112">To take advantage of the HTTP logging feature, the application enables and configures one type of logging on the server session or URL group.</span></span> <span data-ttu-id="4a9a9-113">Дополнительные сведения см. в разделе [Настройка и включение ведения журнала на стороне сервера](configuring-and-enabling-server-side-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="4a9a9-113">For more information, see [Configuring and Enabling Server Side Logging](configuring-and-enabling-server-side-logging.md)</span></span>

 

 




