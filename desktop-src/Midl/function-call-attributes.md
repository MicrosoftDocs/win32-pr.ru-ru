---
title: Атрибуты вызова функции
description: Программы могут использовать эти атрибуты для отдельных функций в интерфейсе и влиять только на эту функцию.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- IDL-MIDL, атрибуты, вызов функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d53407abf464d7b201c49d9cb2b1d3f3625b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779619"
---
# <a name="function-call-attributes"></a><span data-ttu-id="50973-104">Атрибуты вызова функции</span><span class="sxs-lookup"><span data-stu-id="50973-104">Function Call Attributes</span></span>

<span data-ttu-id="50973-105">Программы могут использовать эти атрибуты для отдельных функций в интерфейсе и влиять только на эту функцию.</span><span class="sxs-lookup"><span data-stu-id="50973-105">Programs can use these attributes on individual functions within the interface, and affect only that function.</span></span>



| <span data-ttu-id="50973-106">attribute</span><span class="sxs-lookup"><span data-stu-id="50973-106">Attribute</span></span>                        | <span data-ttu-id="50973-107">Использование</span><span class="sxs-lookup"><span data-stu-id="50973-107">Usage</span></span>                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50973-108">**Сообщение**</span><span class="sxs-lookup"><span data-stu-id="50973-108">**message**</span></span>](message.md)       | <span data-ttu-id="50973-109">Удаленный вызов процедур обрабатывается как асинхронное сообщение от клиента серверу.</span><span class="sxs-lookup"><span data-stu-id="50973-109">The remote procedure call is to be treated as an asynchronous message from the client to the server.</span></span> <span data-ttu-id="50973-110">Клиент делает вызов и возвращается немедленно, в то время как фактический вызов обрабатывается транспортом очереди сообщений ([**нкадг \_ MQ**](ncadg-mq.md)).</span><span class="sxs-lookup"><span data-stu-id="50973-110">The client makes the call and returns immediately, while the actual call is handled by the message-queuing transport ([**ncadg\_mq**](ncadg-mq.md)).</span></span> |
| [<span data-ttu-id="50973-111">**Ну**</span><span class="sxs-lookup"><span data-stu-id="50973-111">**maybe**</span></span>](maybe.md)           | <span data-ttu-id="50973-112">Клиент, выполняющий этот удаленный вызов процедуры, не ждет ответа, указывающего на доставку или завершение вызова.</span><span class="sxs-lookup"><span data-stu-id="50973-112">The client making this remote procedure call does not expect any response indicating delivery or completion of the call.</span></span> <span data-ttu-id="50973-113">Это отличается от операций с [**сообщениями**](message.md) , в которых нет ожидаемого ответа, но гарантируется доставка.</span><span class="sxs-lookup"><span data-stu-id="50973-113">This is in contrast to [**message**](message.md) operations where no response is expected but the delivery is guaranteed.</span></span>        |
| [<span data-ttu-id="50973-114">**транслировать**</span><span class="sxs-lookup"><span data-stu-id="50973-114">**broadcast**</span></span>](broadcast.md)   | <span data-ttu-id="50973-115">Удаленный вызов процедуры отправляется всем серверам в сети.</span><span class="sxs-lookup"><span data-stu-id="50973-115">The remote procedure call is to be sent to all of the servers on the network.</span></span> <span data-ttu-id="50973-116">Клиент принимает первый возврат, последующие ответы от других серверов отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="50973-116">The client accepts the first return, subsequent replies from other servers are discarded.</span></span>                                                                                    |
| [<span data-ttu-id="50973-117">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="50973-117">**idempotent**</span></span>](idempotent.md) | <span data-ttu-id="50973-118">Вызов не изменяет состояние и возвращает одну и ту же информацию каждый раз при вызове с теми же входными параметрами.</span><span class="sxs-lookup"><span data-stu-id="50973-118">The call does not change state and returns the same information each time it is called with the same input parameters.</span></span>                                                                                                                                     |
| [<span data-ttu-id="50973-119">**обратный вызов**</span><span class="sxs-lookup"><span data-stu-id="50973-119">**callback**</span></span>](callback.md)     | <span data-ttu-id="50973-120">Определяет функцию, которая находится в клиентском приложении, которое может вызывать сервер для получения сведений от клиента.</span><span class="sxs-lookup"><span data-stu-id="50973-120">Designates a function that resides in the client application, which the server can call to obtain information from the client.</span></span>                                                                                                                             |
| [<span data-ttu-id="50973-121">**вызвать \_ как**</span><span class="sxs-lookup"><span data-stu-id="50973-121">**call\_as**</span></span>](call-as.md)      | <span data-ttu-id="50973-122">Сопоставляет неудаленную функцию с удаленным вызовом процедуры.</span><span class="sxs-lookup"><span data-stu-id="50973-122">Maps a nonremotable function to a remote procedure call.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="50973-123">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="50973-123">**local**</span></span>](local.md)           | <span data-ttu-id="50973-124">Обозначает локальную процедуру, для которой MIDL не создает код-заглушку.</span><span class="sxs-lookup"><span data-stu-id="50973-124">Designates a local procedure for which MIDL does not generate stub code.</span></span>                                                                                                                                                                                   |



 

<span data-ttu-id="50973-125">В [**необъектных**](object.md) интерфейсах для определения характеристик возвращаемого значения можно также применить атрибут [**\_ Handle**](context-handle.md) для функции.</span><span class="sxs-lookup"><span data-stu-id="50973-125">On non-[**object**](object.md) interfaces, you can also apply the [**context\_handle**](context-handle.md) attribute to a function to specify characteristics of the return value.</span></span>

 

 




