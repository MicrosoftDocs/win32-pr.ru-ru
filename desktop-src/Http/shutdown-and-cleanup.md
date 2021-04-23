---
title: Завершение работы и очистка
description: Для корректного завершения работы приложения необходимо выполнить следующие операции очистки.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf1c59534b73fee21489439c7818c286874185d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068079"
---
# <a name="shutdown-and-cleanup"></a><span data-ttu-id="febfc-103">Завершение работы и очистка</span><span class="sxs-lookup"><span data-stu-id="febfc-103">Shutdown and Cleanup</span></span>

<span data-ttu-id="febfc-104">Для корректного завершения работы приложения необходимо выполнить следующие операции очистки:</span><span class="sxs-lookup"><span data-stu-id="febfc-104">For an application to terminate gracefully, it must perform the following cleanup operations:</span></span>

-   <span data-ttu-id="febfc-105">Удалите все зарегистрированные URL-адреса из группы URL-адресов, вызвав функцию [**хттпремовеурлфромурлграуп**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) для отмены регистрации URL-адресов, ранее зарегистрированных в вызове [**хттпаддурлтаурлграуп**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).</span><span class="sxs-lookup"><span data-stu-id="febfc-105">Remove all registered URLs from the URL group by calling the [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) function to deregister URLs previously registered in the call to [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).</span></span>
-   <span data-ttu-id="febfc-106">Закройте группу URL-адресов, вызвав функцию [**хттпклосеурлграуп**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) .</span><span class="sxs-lookup"><span data-stu-id="febfc-106">Close the URL Group by calling the [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) function.</span></span> <span data-ttu-id="febfc-107">Перед закрытием сеанса сервера необходимо закрыть все группы URL-адресов, созданные в сеансе сервера.</span><span class="sxs-lookup"><span data-stu-id="febfc-107">All the URL groups created under a server session must be closed before closing the server session.</span></span>
-   <span data-ttu-id="febfc-108">Закройте сеанс сервера, вызвав [**хттпклосесерверсессион**](/windows/desktop/api/Http/nf-http-httpcloseserversession).</span><span class="sxs-lookup"><span data-stu-id="febfc-108">Close the server session by calling [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).</span></span>
-   <span data-ttu-id="febfc-109">Закройте рукоятку очереди запросов, вызвав [**хттпклосерекуесткуеуе**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).</span><span class="sxs-lookup"><span data-stu-id="febfc-109">Close the handle to the request queue by calling [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).</span></span>
-   <span data-ttu-id="febfc-110">Завершите ресурсы, созданные API-сервером HTTP, вызвав функцию [**хттптерминате**](/windows/desktop/api/Http/nf-http-httpterminate) с совпадающими параметрами флагов для каждого вызова приложения, созданного в [**хттпинитиализе**](/windows/desktop/api/Http/nf-http-httpinitialize).</span><span class="sxs-lookup"><span data-stu-id="febfc-110">Terminate the resources created by the HTTP Server API by calling the [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) function with matching flag settings for each call the application originally made to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span></span> <span data-ttu-id="febfc-111">Каждый из этих вызовов завершает все ресурсы, созданные в вызове [**хттпинитиализе**](/windows/desktop/api/Http/nf-http-httpinitialize).</span><span class="sxs-lookup"><span data-stu-id="febfc-111">Each of these calls terminates all resources created in the call to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span></span>

 

 




