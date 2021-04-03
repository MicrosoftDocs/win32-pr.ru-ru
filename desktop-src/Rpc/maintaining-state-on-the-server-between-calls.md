---
title: Поддержание состояния на сервере между вызовами
description: Часто требуется поддерживать состояние на сервере между отдельными вызовами RPC \ 8212; использование дескрипторов контекста является лучшим способом. Несколько слов о том, как дескрипторы контекста работают внутри, помогают понять, когда лучше работают дескрипторы контекста.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- Удаленный вызов процедур RPC, рекомендации, поддержание состояния между вызовами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00090fb317cba8c33e7b60ac81762d7d21dd4dc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772722"
---
# <a name="maintaining-state-on-the-server-between-calls"></a><span data-ttu-id="606ae-105">Поддержание состояния на сервере между вызовами</span><span class="sxs-lookup"><span data-stu-id="606ae-105">Maintaining State on the Server Between Calls</span></span>

<span data-ttu-id="606ae-106">Часто приходится сохранять состояние на сервере между отдельными вызовами RPC — лучше всего использовать дескрипторы контекста.</span><span class="sxs-lookup"><span data-stu-id="606ae-106">It is often necessary to maintain state on the server between separate RPC calls—using context handles is the best way to do so.</span></span> <span data-ttu-id="606ae-107">Несколько слов о том, как дескрипторы контекста работают внутри, помогают понять, когда лучше работают дескрипторы контекста.</span><span class="sxs-lookup"><span data-stu-id="606ae-107">A few words about how context handles operate internally helps in understanding when context handles work best.</span></span>

<span data-ttu-id="606ae-108">Клиент никогда не получает состояние, сохраненное на сервере.</span><span class="sxs-lookup"><span data-stu-id="606ae-108">The client never receives the state kept on the server.</span></span> <span data-ttu-id="606ae-109">Чаще всего состояние на сервере — это указатель на блок памяти, и у клиента нет сведений о нем.</span><span class="sxs-lookup"><span data-stu-id="606ae-109">Most often the state on the server is a pointer to a memory block, and the client has no information about it.</span></span> <span data-ttu-id="606ae-110">Все получение клиента — это большой уникальный номер с другими связанными с ним сведениями, которые сервер отправляет клиенту и который представляет маркер контекста во всех последующих операциях.</span><span class="sxs-lookup"><span data-stu-id="606ae-110">All the client receives is a large unique number, with other information associated with it, that the server sends to the client and which represents the context handle in all subsequent operations.</span></span> <span data-ttu-id="606ae-111">Когда клиент ссылается на открытый обработчик, он отправляет большое число, полученное от сервера при открытии этого маркера контекста.</span><span class="sxs-lookup"><span data-stu-id="606ae-111">Whenever the client refers to an opened handle, it sends the large number it received from the server when that context handle was opened.</span></span>

<span data-ttu-id="606ae-112">Сервер отслеживает все большие числа, отправляемые клиенту.</span><span class="sxs-lookup"><span data-stu-id="606ae-112">The server keeps track of all large numbers it sends to a client.</span></span> <span data-ttu-id="606ae-113">Когда сервер получает большое число, представляющее дескриптор контекста, он ищет число в коллекции допустимых, необработанных дескрипторов контекста для этого клиента и находит контекст на стороне сервера, соответствующий заданному большому числу.</span><span class="sxs-lookup"><span data-stu-id="606ae-113">When the server receives a large number representing a context handle, it looks up the number in the collection of valid, outstanding context handles for that client, and finds the server-side context corresponding to a given large number.</span></span> <span data-ttu-id="606ae-114">Он передается в серверную подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="606ae-114">This is passed to the server routine.</span></span> <span data-ttu-id="606ae-115">Если большое число не найдено, \_ \_ \_ возникает исключение несоответствия контекста RPC X SS, которое \_ распространяется на клиент.</span><span class="sxs-lookup"><span data-stu-id="606ae-115">If the large number is not found, an RPC\_X\_SS\_CONTEXT\_MISMATCH exception is raised and propagated to the client.</span></span>

<span data-ttu-id="606ae-116">Короллариес этой конструкции выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="606ae-116">The corollaries of this design are as follows:</span></span>

-   <span data-ttu-id="606ae-117">Маркер контекста допустим только в контексте существующего сеанса клиента/сервера.</span><span class="sxs-lookup"><span data-stu-id="606ae-117">A context handle is valid only in the context of the existing client/server session.</span></span> <span data-ttu-id="606ae-118">Он не может быть передан другому клиенту.</span><span class="sxs-lookup"><span data-stu-id="606ae-118">It cannot be passed to another client.</span></span>
-   <span data-ttu-id="606ae-119">Маркер контекста становится недействительным, если сервер перезагружается или в противном случае теряет соединение с клиентом.</span><span class="sxs-lookup"><span data-stu-id="606ae-119">A context handle becomes invalid if the server is rebooted, or otherwise loses its connection to the client.</span></span>
-   <span data-ttu-id="606ae-120">Клиент не может интерпретировать контекстный маркер на сервере.</span><span class="sxs-lookup"><span data-stu-id="606ae-120">The client cannot interpret what the context handle represents on the server.</span></span> <span data-ttu-id="606ae-121">Для клиента все дескрипторы контекста являются просто большими числами.</span><span class="sxs-lookup"><span data-stu-id="606ae-121">To a client, all context handles are simply large numbers.</span></span>

<span data-ttu-id="606ae-122">Если клиент завершается сбоем, сервер получает уведомление и очищает его контекстные дескрипторы с помощью механизма запуска.</span><span class="sxs-lookup"><span data-stu-id="606ae-122">If the client fails, the server will get a notification and will clean up its context handles using the run-down mechanism.</span></span>

 

 




