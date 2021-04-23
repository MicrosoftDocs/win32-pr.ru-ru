---
description: Служба событий COM+ используется для управления доставкой событий от издателей подписчикам.
ms.assetid: 0945163b-1276-47f6-ae7f-9d932a1b586d
title: Использование событий COM+ с компонентами в очереди COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be31dd1088b720902295738c23173c28145cef2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710789"
---
# <a name="using-com-events-with-com-queued-components"></a><span data-ttu-id="f4bc9-103">Использование событий COM+ с компонентами в очереди COM+</span><span class="sxs-lookup"><span data-stu-id="f4bc9-103">Using COM+ Events with COM+ Queued Components</span></span>

<span data-ttu-id="f4bc9-104">Служба событий COM+ используется для управления доставкой событий от издателей подписчикам.</span><span class="sxs-lookup"><span data-stu-id="f4bc9-104">The COM+ events service is used to manage the delivery of events from publishers to subscribers.</span></span> <span data-ttu-id="f4bc9-105">Службу очередей компонентов COM+ можно использовать для того, чтобы время обработки издателя и подписчика не зависело от постановки в очередь сообщения издателя и последующего его воспроизведения на подписчике.</span><span class="sxs-lookup"><span data-stu-id="f4bc9-105">The COM+ queued components service can be used to make the publisher and subscriber processing time independent by queuing the publisher's message and later replaying it to the subscriber.</span></span> <span data-ttu-id="f4bc9-106">Необходимость использования службы очередей компонентов зависит от базовой бизнес-логики приложения.</span><span class="sxs-lookup"><span data-stu-id="f4bc9-106">Whether or not you need to use the queued components service depends on the underlying business logic of your application.</span></span> <span data-ttu-id="f4bc9-107">Если требуется, чтобы события не зависели от времени, их можно создать с помощью службы COM+ Events в службе очередей компонентов COM+.</span><span class="sxs-lookup"><span data-stu-id="f4bc9-107">If you need to have events that are time independent, you can create them by using the COM+ events service with COM+ queued components service.</span></span>

> [!Note]  
> <span data-ttu-id="f4bc9-108">Дополнительные сведения об использовании службы очередей компонентов COM+ см. в разделе [com+ Queued Components](com--queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="f4bc9-108">For additional information about using the COM+ queued components service, see [COM+ Queued Components](com--queued-components.md).</span></span>

 

<span data-ttu-id="f4bc9-109">Служба очередей компонентов поддерживает порядок вызова методов в одном сообщении.</span><span class="sxs-lookup"><span data-stu-id="f4bc9-109">The queued components service maintains order-of-method invocation within a single message.</span></span> <span data-ttu-id="f4bc9-110">Средство записи выполняет пакетную обработку всех вызовов методов в сообщении, после чего проигрыватель вызывает эти методы по порядку при обработке сообщения.</span><span class="sxs-lookup"><span data-stu-id="f4bc9-110">The recorder batches all method invocations into a message, and then the player invokes those methods in order when the message is processed.</span></span>

<span data-ttu-id="f4bc9-111">Устройство записи и проигрыватель с очередями можно разместить в одном из следующих двух мест:</span><span class="sxs-lookup"><span data-stu-id="f4bc9-111">A queued components recorder and player can be positioned in either of the following two places:</span></span>

-   <span data-ttu-id="f4bc9-112">Между издателем и объектом события</span><span class="sxs-lookup"><span data-stu-id="f4bc9-112">Between the publisher and event object</span></span>
-   <span data-ttu-id="f4bc9-113">Между объектом события и подписчиком</span><span class="sxs-lookup"><span data-stu-id="f4bc9-113">Between the event object and subscriber</span></span>

<span data-ttu-id="f4bc9-114">При размещении средства записи и проигрывателя между издателем и объектом события выполняется создание компонента [класса событий](the-com--event-class-object.md) куеуабле.</span><span class="sxs-lookup"><span data-stu-id="f4bc9-114">If you position the recorder and player between the publisher and event object, you are making the [event class](the-com--event-class-object.md) component queuable.</span></span> <span data-ttu-id="f4bc9-115">Компонент класса событий должен быть помечен для постановки в очередь и активироваться проигрывателем в процессе, отдельном от издателя.</span><span class="sxs-lookup"><span data-stu-id="f4bc9-115">The event class component must be marked for queuing and be activated by the player in a process that is separate from the publisher.</span></span>

<span data-ttu-id="f4bc9-116">Для асинхронной доставки событий создайте устройство записи и проигрыватель между объектом события и подписчиком и установите атрибут queued объекта Subscription.</span><span class="sxs-lookup"><span data-stu-id="f4bc9-116">To deliver events asynchronously, compose the recorder and player between the event object and subscriber and set the Queued attribute of the subscription object.</span></span> <span data-ttu-id="f4bc9-117">Это задает Субскрибермоникер следующим образом: "очередь:/New:/ {12345678-1234-1234-1234-123456789012} ".</span><span class="sxs-lookup"><span data-stu-id="f4bc9-117">This sets SubscriberMoniker as follows: "queue:/new:/{12345678-1234-1234-1234-123456789012}".</span></span>

<span data-ttu-id="f4bc9-118">При использовании компонентов в очереди в ситуации с событиями необходимо учитывать порядок доставки.</span><span class="sxs-lookup"><span data-stu-id="f4bc9-118">There is an order of delivery implication to consider when using queued components in an event situation.</span></span> <span data-ttu-id="f4bc9-119">Так как служба очередей компонентов записывает и воспроизводит все вызовы в течение всего времени существования одного объекта в одном сообщении, все вызовы воспроизводятся в том порядке, в котором они были сделаны.</span><span class="sxs-lookup"><span data-stu-id="f4bc9-119">Because the queued components service records and plays back all calls within the lifetime of a single object in one message, all calls are replayed in the order in which they were made.</span></span> <span data-ttu-id="f4bc9-120">Однако, если имеется несколько сеансов с несколькими объектами, порядок гарантировать нельзя.</span><span class="sxs-lookup"><span data-stu-id="f4bc9-120">However, if there is more than one session with more than one object, order cannot be guaranteed.</span></span> <span data-ttu-id="f4bc9-121">Если важен порядок, убедитесь, что вызовы, которые должны воспроизводиться в последовательном порядке, находятся на одном и том же экземпляре объекта.</span><span class="sxs-lookup"><span data-stu-id="f4bc9-121">If order is important, make sure that calls that need to be played back in order reside on the same object instance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4bc9-122">См. также</span><span class="sxs-lookup"><span data-stu-id="f4bc9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4bc9-123">Фильтрация событий в COM+</span><span class="sxs-lookup"><span data-stu-id="f4bc9-123">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="f4bc9-124">Публикация и доставка событий в COM+</span><span class="sxs-lookup"><span data-stu-id="f4bc9-124">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="f4bc9-125">Подписки</span><span class="sxs-lookup"><span data-stu-id="f4bc9-125">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="f4bc9-126">Объект класса событий COM+</span><span class="sxs-lookup"><span data-stu-id="f4bc9-126">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> </dl>

 

 



