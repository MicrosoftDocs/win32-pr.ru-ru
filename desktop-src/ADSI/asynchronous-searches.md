---
title: Асинхронный поиск
description: Включение асинхронного поиска (Async) приведет к вызову Жетфирстров или первому вызову GetNextRow блокируется до тех пор, пока не будет возвращена первая запись с сервера.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- Асинхронный поиск ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8b8fff875af18b85cdffa4ce67d631d94ed14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986120"
---
# <a name="asynchronous-searches"></a><span data-ttu-id="8fe26-104">Асинхронный поиск</span><span class="sxs-lookup"><span data-stu-id="8fe26-104">Asynchronous Searches</span></span>

<span data-ttu-id="8fe26-105">Включение асинхронного поиска (Async) приведет к вызову **жетфирстров** или первому вызову **GetNextRow** блокируется до тех пор, пока не будет возвращена первая запись с сервера.</span><span class="sxs-lookup"><span data-stu-id="8fe26-105">Enabling asynchronous (async) search results in a call to **GetFirstRow** or the first call to **GetNextRow** blocks until the first entry is returned from the server.</span></span> <span data-ttu-id="8fe26-106">То есть, если для поиска на сервере требуется много времени, первые несколько результатов быстро возвращаются.</span><span class="sxs-lookup"><span data-stu-id="8fe26-106">That is, if the search on the server requires much time, the first few results are returned quickly.</span></span> <span data-ttu-id="8fe26-107">Это может помочь при заполнении списка результатами поиска.</span><span class="sxs-lookup"><span data-stu-id="8fe26-107">This can help when populating a list box with search results.</span></span> <span data-ttu-id="8fe26-108">Результаты поиска отображаются по мере их возврата.</span><span class="sxs-lookup"><span data-stu-id="8fe26-108">Search results are displayed as they are returned.</span></span>

<span data-ttu-id="8fe26-109">Если функция Async отключена, первый вызов **жетфирстров** или **GetNextRow** будет блокироваться до тех пор, пока сервер не вычислит весь результирующий набор и не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="8fe26-109">If async is disabled, the first call to **GetFirstRow** or **GetNextRow** will block until the server computes the entire result set and returns.</span></span> <span data-ttu-id="8fe26-110">Возвращается только первая строка.</span><span class="sxs-lookup"><span data-stu-id="8fe26-110">Only then is the first row returned.</span></span> <span data-ttu-id="8fe26-111">Это не рекомендуется, если результирующий набор должен быть большим.</span><span class="sxs-lookup"><span data-stu-id="8fe26-111">This is not recommended if the result set is expected to be large.</span></span>

<span data-ttu-id="8fe26-112">Если включены и разбиение на страницы, и async, первый вызов **жетфирстров** или **GetNextRow** будет блокироваться до тех пор, пока сервер не создаст и не отправит первую страницу результатов.</span><span class="sxs-lookup"><span data-stu-id="8fe26-112">If both paging and async are enabled, the first call to **GetFirstRow** or **GetNextRow** will block until the server generates and sends the first page of results.</span></span> <span data-ttu-id="8fe26-113">Если был задан приемлемый размер страницы, результаты будут отображаться немедленно.</span><span class="sxs-lookup"><span data-stu-id="8fe26-113">If a reasonable page size was set, results will appear immediately.</span></span> <span data-ttu-id="8fe26-114">Что более важно, если результаты поиска должны быть очень большими и вы ищете определенную запись, не требуется запрашивать дополнительные результаты с сервера после того, как вы нашли интересующие вас записи.</span><span class="sxs-lookup"><span data-stu-id="8fe26-114">More importantly, if the search results are expected to be very large, and you search for a particular entry, it is not required that you request more results from the server after you have found the entries that interest you.</span></span>

<span data-ttu-id="8fe26-115">Асинхронный поиск с постраничным запросом позволяет точно управлять поиском.</span><span class="sxs-lookup"><span data-stu-id="8fe26-115">A paged async search provides fine control of a search.</span></span> <span data-ttu-id="8fe26-116">Это полезно, если результаты поиска могут быть очень большими и на сервере требуется значительное время.</span><span class="sxs-lookup"><span data-stu-id="8fe26-116">This is useful if the search results may be very large and require extensive time from the server.</span></span>

<span data-ttu-id="8fe26-117">Дополнительные сведения об использовании асинхронных поисков с конкретным интерфейсом поиска см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="8fe26-117">For more information about using asynchronous searches with a specific search interface, see:</span></span>

-   [<span data-ttu-id="8fe26-118">Синхронный и асинхронный поиск с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="8fe26-118">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [<span data-ttu-id="8fe26-119">Поиск с помощью объекты данных ActiveX</span><span class="sxs-lookup"><span data-stu-id="8fe26-119">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="8fe26-120">Поиск с помощью OLE DB</span><span class="sxs-lookup"><span data-stu-id="8fe26-120">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




