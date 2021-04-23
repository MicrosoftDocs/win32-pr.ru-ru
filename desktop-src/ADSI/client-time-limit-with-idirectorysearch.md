---
title: Ограничение времени клиента с помощью IDirectorySearch
description: Клиент может установить ограничение по времени, чтобы сервер возвращал результирующий набор. Если серверу не удается ответить на запрос в течение указанного периода времени, клиент может отменить поиск и повторить попытку позже.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Ограничение времени клиента с помощью IDirectorySearch
- ADSI, поиск, IDirectorySearch, другие параметры поиска, ограничение времени клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed25bd8499f7166d7ea494f71e6f78193f9c778a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654145"
---
# <a name="client-time-limit-with-idirectorysearch"></a><span data-ttu-id="d7f14-106">Ограничение времени клиента с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="d7f14-106">Client Time Limit with IDirectorySearch</span></span>

<span data-ttu-id="d7f14-107">Клиент может установить ограничение по времени, чтобы сервер возвращал результирующий набор.</span><span class="sxs-lookup"><span data-stu-id="d7f14-107">A client can impose a time limit for a server to return the result set.</span></span> <span data-ttu-id="d7f14-108">Если серверу не удается ответить на запрос в течение указанного периода времени, клиент может отменить поиск и повторить попытку позже.</span><span class="sxs-lookup"><span data-stu-id="d7f14-108">When the server fails to respond to a query within the specified time period, the client can abandon the search and try it again later.</span></span>

<span data-ttu-id="d7f14-109">Настройка ограничения времени клиента полезна, когда клиент запрашивает асинхронный поиск.</span><span class="sxs-lookup"><span data-stu-id="d7f14-109">The client time limit preference is useful when a client requests an asynchronous search.</span></span> <span data-ttu-id="d7f14-110">При асинхронном поиске клиент выполняет запрос, а затем переходит к другим задачам, ожидая возврата результатов сервером.</span><span class="sxs-lookup"><span data-stu-id="d7f14-110">In an asynchronous search, the client makes a request and then proceeds with other tasks while waiting for the server to return the results.</span></span> <span data-ttu-id="d7f14-111">Возможно, сервер может переключиться в режим «вне сети» без уведомления клиента.</span><span class="sxs-lookup"><span data-stu-id="d7f14-111">It is possible that the server can go offline without notifying the client.</span></span> <span data-ttu-id="d7f14-112">В этом случае клиент не будет иметь уведомления о том, обрабатывается ли сервер запросом или перестает быть активным.</span><span class="sxs-lookup"><span data-stu-id="d7f14-112">In this case, the client will have no notification of whether the server is still processing the query, or if it no longer live.</span></span> <span data-ttu-id="d7f14-113">Настройка предельного времени клиента дает клиенту некоторый контроль над подобными ситуациями.</span><span class="sxs-lookup"><span data-stu-id="d7f14-113">The client time limit preference gives the client some control of situations like this.</span></span>

<span data-ttu-id="d7f14-114">Значение по умолчанию для ограничения по времени клиента не ограничено.</span><span class="sxs-lookup"><span data-stu-id="d7f14-114">The default for the client time limit is no limit.</span></span> <span data-ttu-id="d7f14-115">Чтобы установить предельное время клиента, задайте параметру сеарчпреф поиска по **\_ \_ времени ожидания** с **адстипе \_ целым числом** , которое содержит предельное время клиента (в секундах) в массиве [**\_ \_ сведений об ADS сеарчпреф**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) , переданном в метод [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="d7f14-115">To set a client time limit, set an **ADS\_SEARCHPREF\_TIMEOUT** search option with an **ADSTYPE\_INTEGER** value that contains the client time limit, in seconds, in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="d7f14-116">Ограничение времени клиента, равное нулю, указывает на отсутствие ограничения по времени.</span><span class="sxs-lookup"><span data-stu-id="d7f14-116">A client time limit of zero indicates no time limit.</span></span>

<span data-ttu-id="d7f14-117">В следующем примере кода показано, как задать предельное время клиента.</span><span class="sxs-lookup"><span data-stu-id="d7f14-117">The following code example shows how to set the client time limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




