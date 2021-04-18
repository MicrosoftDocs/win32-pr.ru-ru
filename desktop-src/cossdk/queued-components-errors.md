---
description: Ошибки компонентов в очереди
ms.assetid: 29a1bf52-7252-4f8a-bdb7-61b152fb907e
title: Ошибки компонентов в очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422ea9c7ff77f2d69633d6db8b8d48c63fabc071
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710759"
---
# <a name="queued-components-errors"></a><span data-ttu-id="6eb87-103">Ошибки компонентов в очереди</span><span class="sxs-lookup"><span data-stu-id="6eb87-103">Queued Components Errors</span></span>

<span data-ttu-id="6eb87-104">При сбое вызова компонента из очереди из-за сбоя передачи на сервер (ошибка на стороне клиента) или из-за сбоя выполнения при поступлении (ошибка на стороне сервера) соответствующее сообщение [очереди сообщений](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) называется *подозрительным сообщением*.</span><span class="sxs-lookup"><span data-stu-id="6eb87-104">When a call to a queued component fails, either because it could not be transmitted to the server (a client-side failure) or because it failed to execute when it arrived (a server-side failure), the corresponding [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) message is called a *poison message*.</span></span>

<span data-ttu-id="6eb87-105">Служба очередей компонентов COM+ обрабатывает подозрительные сообщения с помощью серии очередей повтора.</span><span class="sxs-lookup"><span data-stu-id="6eb87-105">The COM+ queued components service handles poison messages by using a series of retry queues.</span></span> <span data-ttu-id="6eb87-106">После нескольких попыток сообщение перемещается в конечную очередь RESTful.</span><span class="sxs-lookup"><span data-stu-id="6eb87-106">After several retries, the message is moved to a final resting queue.</span></span> <span data-ttu-id="6eb87-107">Сообщения остаются в очереди RESTful, пока они не будут перемещены вручную с помощью программы перемещения сообщений компонентов в очереди.</span><span class="sxs-lookup"><span data-stu-id="6eb87-107">Messages stay in the resting queue until they are moved manually by using the queued components message mover utility.</span></span> <span data-ttu-id="6eb87-108">Дополнительные сведения об использовании программы перемещения сообщений см. в разделе [Обработка ошибок](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="6eb87-108">For more information about using the message mover, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

<span data-ttu-id="6eb87-109">Подробное описание последовательности событий, возникающих для различных видов ошибок, можно найти в разделах, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6eb87-109">Detailed descriptions of the sequence of events that occurs for various sorts of errors can be found in the topics described in the following table.</span></span>



| <span data-ttu-id="6eb87-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="6eb87-110">Topic</span></span>                                                                             | <span data-ttu-id="6eb87-111">Описание</span><span class="sxs-lookup"><span data-stu-id="6eb87-111">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6eb87-112">Ошибки на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="6eb87-112">Server-Side Errors</span></span>](server-side-errors.md)<br/>                           | <span data-ttu-id="6eb87-113">Подробное описание ответа службы очередей компонентов COM+ к сбою на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="6eb87-113">Describes in detail the response of the COM+ queued components service to a server-side failure.</span></span><br/>             |
| [<span data-ttu-id="6eb87-114">Ошибки на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="6eb87-114">Client-Side Errors</span></span>](client-side-errors.md)<br/>                           | <span data-ttu-id="6eb87-115">Подробное описание ответа службы очередей компонентов COM+ к сбою на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="6eb87-115">Describes in detail the response of the COM+ queued components service to a client-side failure.</span></span><br/>             |
| [<span data-ttu-id="6eb87-116">Постоянные сбои Client-Side</span><span class="sxs-lookup"><span data-stu-id="6eb87-116">Persistent Client-Side Failures</span></span>](persistent-client-side-failures.md)<br/> | <span data-ttu-id="6eb87-117">Подробное описание ответа службы очередей компонентов COM+ на повторяющиеся сбои на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="6eb87-117">Describes in the detail the response of the COM+ queued components service to repeated client-side failures.</span></span><br/> |



 

 

 




