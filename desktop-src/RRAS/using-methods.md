---
title: Использование методов
description: Когда клиент регистрируется в диспетчере таблиц маршрутизации, он может экспортировать набор методов. Эти методы используются другими клиентами для получения сведений, относящихся к клиенту. Методы обеспечивают частный обмен данными между клиентами диспетчера таблиц маршрутизации.
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd895fbb3f8f54224522786b5794c5c6c57a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986557"
---
# <a name="using-methods"></a><span data-ttu-id="d1b11-105">Использование методов</span><span class="sxs-lookup"><span data-stu-id="d1b11-105">Using Methods</span></span>

<span data-ttu-id="d1b11-106">Когда клиент регистрируется в диспетчере таблиц маршрутизации, он может экспортировать набор методов.</span><span class="sxs-lookup"><span data-stu-id="d1b11-106">When a client registers with the routing table manager, it can export a set of methods.</span></span> <span data-ttu-id="d1b11-107">Эти методы используются другими клиентами для получения сведений, относящихся к клиенту.</span><span class="sxs-lookup"><span data-stu-id="d1b11-107">These methods are used by other clients to obtain client-specific information.</span></span> <span data-ttu-id="d1b11-108">Методы обеспечивают частный обмен данными между клиентами диспетчера таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="d1b11-108">Methods enable private communication between clients of the routing table manager.</span></span>

<span data-ttu-id="d1b11-109">Клиент может получить список методов, экспортированных другим клиентом.</span><span class="sxs-lookup"><span data-stu-id="d1b11-109">A client can obtain the list of methods exported by another client.</span></span> <span data-ttu-id="d1b11-110">Клиент вызывает функцию [**ртмжетентитимесодс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) , предоставляя маркер целевого клиента.</span><span class="sxs-lookup"><span data-stu-id="d1b11-110">The client calls the [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) function, supplying the target client's handle.</span></span>

<span data-ttu-id="d1b11-111">Каждый метод, экспортированный клиентом, однозначно идентифицируется по его идентификатору метода.</span><span class="sxs-lookup"><span data-stu-id="d1b11-111">Each method exported by a client is uniquely identified by its method identifier.</span></span> <span data-ttu-id="d1b11-112">Каждый клиент может экспортировать до 32 методов.</span><span class="sxs-lookup"><span data-stu-id="d1b11-112">Each client can export up to 32 methods.</span></span> <span data-ttu-id="d1b11-113">Каждый метод соответствует биту, заданному в элементе **месодтипе** структуры [**\_ \_ \_ метода экспорта сущности RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) .</span><span class="sxs-lookup"><span data-stu-id="d1b11-113">Each method corresponds to a bit set in the **MethodType** member of the [**RTM\_ENTITY\_EXPORT\_METHOD**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) structure.</span></span> <span data-ttu-id="d1b11-114">Для вызова нескольких методов клиент должен выполнить логическую операцию или идентификаторы для этих методов.</span><span class="sxs-lookup"><span data-stu-id="d1b11-114">To invoke multiple methods, the client should perform a logical OR of the identifiers for those methods.</span></span> <span data-ttu-id="d1b11-115">Синтаксис и семантика входных и выходных структур для каждого протокола должны быть указаны при реализации протокола.</span><span class="sxs-lookup"><span data-stu-id="d1b11-115">The syntax and semantics of input and output structures for each protocol must be specified when the protocol is implemented.</span></span>

> [!Note]  
> <span data-ttu-id="d1b11-116">Значения идентификатора метода, соответствующие биту, заданному в нижней половине элемента **месодтипе** (младшие 16 бит), зарезервированы корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d1b11-116">Method identifier values that correspond to a bit set in the lower half of the **MethodType** member (the lower 16 bits) are reserved by Microsoft.</span></span>

 

<span data-ttu-id="d1b11-117">Чтобы вызвать второй метод клиента, клиент вызывает функцию [**ртминвокемесод**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) .</span><span class="sxs-lookup"><span data-stu-id="d1b11-117">To invoke a second client's method, a client calls the [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) function.</span></span> <span data-ttu-id="d1b11-118">Диспетчер таблиц маршрутизации единолично все запросы на вызов методов клиента.</span><span class="sxs-lookup"><span data-stu-id="d1b11-118">The routing table manager arbitrates all requests to invoke a client's methods.</span></span> <span data-ttu-id="d1b11-119">Диспетчер таблиц маршрутизации выполняет две функции, когда она единолично между клиентами:</span><span class="sxs-lookup"><span data-stu-id="d1b11-119">The routing table manager performs two functions when it arbitrates between clients:</span></span>

-   <span data-ttu-id="d1b11-120">Запретить второму клиенту вызывать метод для клиента, который отменяет регистрацию.</span><span class="sxs-lookup"><span data-stu-id="d1b11-120">Preventing the second client from invoking a method for a client that is unregistering.</span></span>
-   <span data-ttu-id="d1b11-121">Удержание запроса "Invoke", если методы заблокированы, и разрешение продолжения запроса при разблокировании методов.</span><span class="sxs-lookup"><span data-stu-id="d1b11-121">Holding an "invoke" request when methods are blocked, and allowing the request to continue when the methods are unblocked.</span></span>

<span data-ttu-id="d1b11-122">Если клиент должен запретить другим клиентам выполнять свои методы, клиент может вызвать [**ртмблоккмесодс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods).</span><span class="sxs-lookup"><span data-stu-id="d1b11-122">If a client must prevent other clients from executing its methods, the client can call [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods).</span></span> <span data-ttu-id="d1b11-123">Диспетчер таблиц маршрутизации не позволит обработать вызов [**ртминвокемесод**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) , пока клиент не разблокирует свои методы снова.</span><span class="sxs-lookup"><span data-stu-id="d1b11-123">The routing table manager will not allow a call to [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) to be processed until the client unblocks its methods again.</span></span>

<span data-ttu-id="d1b11-124">Обычно клиенты блокируют методы при внесении изменений в закрытые данные, которыми обмениваются клиенты.</span><span class="sxs-lookup"><span data-stu-id="d1b11-124">Clients typically block methods when making changes to the private data that is exchanged between clients.</span></span> <span data-ttu-id="d1b11-125">Блокирующие методы являются необязательным действием.</span><span class="sxs-lookup"><span data-stu-id="d1b11-125">Blocking methods is an optional action.</span></span> <span data-ttu-id="d1b11-126">Клиент также может использовать внутренние блокировки, чтобы предотвратить вызов методов другими клиентами.</span><span class="sxs-lookup"><span data-stu-id="d1b11-126">A client can also use internal locks to prevent other clients from invoking methods.</span></span>

<span data-ttu-id="d1b11-127">Пример кода, демонстрирующий использование этих функций, см. [в разделе Получение и вызов экспортированных методов для клиента](obtain-and-call-the-exported-methods-for-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="d1b11-127">For sample code that shows how to use these functions, see [Obtain and Call the Exported Methods for a Client](obtain-and-call-the-exported-methods-for-a-client.md).</span></span>

 

 




