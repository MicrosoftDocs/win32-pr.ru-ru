---
title: Время ожидания поиска
description: Клиент также может применить ограничение времени, которое будет ожидать, пока сервер вернет результирующий набор.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- Поиск по времени ожидания в ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfdc63dd4490a840a16eb61598b2461c3e1a40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328360"
---
# <a name="search-time-out"></a><span data-ttu-id="e144b-104">Время ожидания поиска</span><span class="sxs-lookup"><span data-stu-id="e144b-104">Search Time Out</span></span>

<span data-ttu-id="e144b-105">Клиент также может применить ограничение времени, которое будет ожидать, пока сервер вернет результирующий набор.</span><span class="sxs-lookup"><span data-stu-id="e144b-105">A client can also impose a time limit that it will wait for a server to return the result set.</span></span> <span data-ttu-id="e144b-106">Значение параметра "время ожидания при поиске" указывает это ограничение.</span><span class="sxs-lookup"><span data-stu-id="e144b-106">The value of the "search time out" option specifies this limit.</span></span> <span data-ttu-id="e144b-107">Если серверу не удается ответить на запрос в течение указанного периода времени, клиент может прерывать Поиск и повторить попытку позже.</span><span class="sxs-lookup"><span data-stu-id="e144b-107">When the server fails to respond to a query within the specified time period, the client can stop the search and try again later.</span></span>

<span data-ttu-id="e144b-108">Свойство времени ожидания полезно, когда клиент запрашивает асинхронный поиск.</span><span class="sxs-lookup"><span data-stu-id="e144b-108">The time-out property is useful when a client requests an asynchronous search.</span></span> <span data-ttu-id="e144b-109">При асинхронном поиске клиент выполняет запрос, а затем переходит к другим задачам, ожидая возврата результатов сервером.</span><span class="sxs-lookup"><span data-stu-id="e144b-109">In an asynchronous search, the client makes a request and then proceeds with other tasks while waiting for the server to return the results.</span></span> <span data-ttu-id="e144b-110">Возможно, сервер может переключиться в режим «вне сети» без уведомления клиента.</span><span class="sxs-lookup"><span data-stu-id="e144b-110">It is possible that the server can go offline without notifying the client.</span></span> <span data-ttu-id="e144b-111">В этом случае клиент не может распознать, что сервер все еще обрабатывает запрос, или если он перестал быть активным.</span><span class="sxs-lookup"><span data-stu-id="e144b-111">In this case, the client has no way of recognizing that the server is still processing the query, or if it has ceased to be live.</span></span> <span data-ttu-id="e144b-112">Свойство времени ожидания предоставляет клиенту некоторый контроль в таких случаях.</span><span class="sxs-lookup"><span data-stu-id="e144b-112">The time-out property provides the client some control in such instances.</span></span>

<span data-ttu-id="e144b-113">Дополнительные сведения об использовании параметра времени ожидания поиска с конкретным интерфейсом поиска см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="e144b-113">For more information about using the search time-out option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="e144b-114">Ограничение времени клиента с помощью IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="e144b-114">Client Time Limit with IDirectorySearch</span></span>](client-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="e144b-115">Поиск с помощью объекты данных ActiveX</span><span class="sxs-lookup"><span data-stu-id="e144b-115">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="e144b-116">Поиск с помощью OLE DB</span><span class="sxs-lookup"><span data-stu-id="e144b-116">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




