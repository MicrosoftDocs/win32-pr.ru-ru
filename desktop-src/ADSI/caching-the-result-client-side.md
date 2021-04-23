---
title: Кэширование результата (на стороне клиента)
description: Кэширование на стороне клиента сохраняет результирующий набор в памяти клиента, обеспечивая повышение производительности на стороне клиента.
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- Кэширование результата (на стороне клиента) ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb965da1da0c791db215dd7eee925a7c9f67ccf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986115"
---
# <a name="caching-the-result-client-side"></a><span data-ttu-id="733d2-104">Кэширование результата (на стороне клиента)</span><span class="sxs-lookup"><span data-stu-id="733d2-104">Caching the Result (Client Side)</span></span>

<span data-ttu-id="733d2-105">Кэширование на стороне клиента сохраняет результирующий набор в памяти клиента, обеспечивая повышение производительности на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="733d2-105">Client-side caching stores the result set in the client memory, providing performance enhancements for the client side.</span></span> <span data-ttu-id="733d2-106">Клиент может повторно посетить объект, не нажимая на него несколько обращений к серверу.</span><span class="sxs-lookup"><span data-stu-id="733d2-106">A client can revisit an object repeatedly without multiple trips to the server.</span></span> <span data-ttu-id="733d2-107">По умолчанию ADSI кэширует результирующий набор для клиентов.</span><span class="sxs-lookup"><span data-stu-id="733d2-107">By default, ADSI caches the result set for the clients.</span></span> <span data-ttu-id="733d2-108">Это позволяет интерфейсу ADSI предоставлять клиентам поддержку курсоров, аналогичных SQL.</span><span class="sxs-lookup"><span data-stu-id="733d2-108">This enables ADSI to provide clients with SQL-like cursor support.</span></span> <span data-ttu-id="733d2-109">Вы можете несколько раз пройти по заданному результирующему набору.</span><span class="sxs-lookup"><span data-stu-id="733d2-109">You may iterate through a given result set several times.</span></span>

<span data-ttu-id="733d2-110">ADSI также позволяет клиентам отключить кэш, чтобы снизить требования к памяти.</span><span class="sxs-lookup"><span data-stu-id="733d2-110">ADSI also enables clients to turn off the cache to reduce memory requirements.</span></span> <span data-ttu-id="733d2-111">Если кэширование на стороне клиента отключено, клиент не сохраняет результирующий набор в памяти.</span><span class="sxs-lookup"><span data-stu-id="733d2-111">If client-side caching is disabled, the client does not maintain the result set in memory.</span></span> <span data-ttu-id="733d2-112">Каждая строка освобождается после того, как приложение извлекает его.</span><span class="sxs-lookup"><span data-stu-id="733d2-112">Each row is freed after the application retrieves it.</span></span> <span data-ttu-id="733d2-113">Отключение кэширования на стороне клиента может оказаться полезным для снижения требований к памяти на стороне клиента в таких случаях, как если бы вы предполагали только один проход по результирующему набору.</span><span class="sxs-lookup"><span data-stu-id="733d2-113">Disabling client-side caching can be useful for decreasing the client-side memory requirements in such cases as when you intend only to make a single pass through the result set.</span></span> <span data-ttu-id="733d2-114">Однако, когда клиенты отказываются от кэширования результата, они обеспечивают поддержку курсора.</span><span class="sxs-lookup"><span data-stu-id="733d2-114">However, when clients elect not to cache the result, they give up cursor support.</span></span>

<span data-ttu-id="733d2-115">Дополнительные сведения о кэшировании результатов с помощью определенного интерфейса поиска см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="733d2-115">For more information about results caching with a specific search interface, see:</span></span>

-   [<span data-ttu-id="733d2-116">Кэширование результатов с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="733d2-116">Result Caching with IDirectorySearch</span></span>](result-caching-with-idirectorysearch.md)
-   [<span data-ttu-id="733d2-117">Поиск с помощью объекты данных ActiveX</span><span class="sxs-lookup"><span data-stu-id="733d2-117">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="733d2-118">Поиск с помощью OLE DB</span><span class="sxs-lookup"><span data-stu-id="733d2-118">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




