---
title: Создание очереди запросов и привязка к ней
description: Очередь запросов — это очередь обслуживания, которая содержит ожидающие запросы для определенного приложения.
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945b8451f9128357b7da0ddc64600b74deffd0d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411193"
---
# <a name="creating-and-binding-to-a-request-queue"></a><span data-ttu-id="7482a-103">Создание очереди запросов и привязка к ней</span><span class="sxs-lookup"><span data-stu-id="7482a-103">Creating and Binding to a Request Queue</span></span>

<span data-ttu-id="7482a-104">Очередь запросов — это очередь обслуживания, которая содержит ожидающие запросы для определенного приложения.</span><span class="sxs-lookup"><span data-stu-id="7482a-104">A request queue is a service queue that holds pending requests for a specific application.</span></span> <span data-ttu-id="7482a-105">Приложение создает очередь запросов независимо от группы URL-адресов или сеанса сервера путем вызова функции [**хттпкреатерекуесткуеуе**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) и задает свойства очереди запросов путем вызова функции [**хттпсетрекуесткуеуепроперти**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) .</span><span class="sxs-lookup"><span data-stu-id="7482a-105">An application creates the request queue independently of the URL group or server session by calling the [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) function, and sets the request queue properties by calling the [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) function.</span></span> <span data-ttu-id="7482a-106">Эти свойства представляют уровень детализации 503 ответов, максимальную длину очереди и состояние действия.</span><span class="sxs-lookup"><span data-stu-id="7482a-106">These properties are the verbosity of 503 responses, the maximum length of the queue, and the activity state.</span></span>

<span data-ttu-id="7482a-107">Чтобы запросы направлялись в очередь запросов, приложение привязывает группу URL-адресов, созданную в процессе [настройки среды выполнения](run-time-configuration.md) , к очереди, вызвав [**хттпсетурлграуппроперти**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) с **хттпсервербиндингпроперти** , указанным в параметре *Property* .</span><span class="sxs-lookup"><span data-stu-id="7482a-107">To cause requests to be routed to its request queue, the application binds the URL group it created as part of [run-time configuration](run-time-configuration.md) to the queue by calling [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) with **HttpServerBindingProperty** specified in the *Property* parameter.</span></span> <span data-ttu-id="7482a-108">Затем входящие запросы от URL-адресов в группе перенаправляются в указанную очередь запросов.</span><span class="sxs-lookup"><span data-stu-id="7482a-108">Incoming requests from the URLs in the group are then routed to the specified request queue.</span></span>

 

 




