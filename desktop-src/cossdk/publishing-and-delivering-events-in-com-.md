---
description: Чтобы опубликовать событие, просто создайте экземпляр объекта класса событий и вызовите нужный метод. подробные инструкции по выполнению этой задачи в коде см. в разделе Публикация события.
ms.assetid: 835c3753-fdcc-4afe-94c3-c954aaf1c832
title: Публикация и доставка событий в COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a444b64501156191590c115d6000f4c0bda153
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807792"
---
# <a name="publishing-and-delivering-events-in-com"></a><span data-ttu-id="ce351-103">Публикация и доставка событий в COM+</span><span class="sxs-lookup"><span data-stu-id="ce351-103">Publishing and Delivering Events in COM+</span></span>

<span data-ttu-id="ce351-104">Чтобы опубликовать событие, просто создайте экземпляр объекта [класса событий](the-com--event-class-object.md) и вызовите нужный метод. подробные инструкции по выполнению этой задачи в коде см. в разделе [Публикация события](publishing-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="ce351-104">To publish an event, simply instantiate an [event class](the-com--event-class-object.md) object and invoke the desired method; for detailed instructions on how to do this in code, see [Publishing an Event](publishing-an-event.md).</span></span>

<span data-ttu-id="ce351-105">Когда издатель запускает событие, служба событий COM+ выполняет поиск в базе данных подписки, чтобы найти всех подписчиков, которые зарегистрировали подписки на класс событий с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="ce351-105">When a publisher fires an event, the COM+ Events service searches the subscription database to find all the subscribers who have registered subscriptions to the instantiated event class.</span></span> <span data-ttu-id="ce351-106">Он подключается к этим подписчикам (путем прямого создания, моникеров или компонентов в очереди) и вызывает метод.</span><span class="sxs-lookup"><span data-stu-id="ce351-106">It connects to those subscribers (by direct creation, monikers, or queued components) and calls the method.</span></span> <span data-ttu-id="ce351-107">Чтобы обеспечить поддержку нескольких уведомлений подписчика для одного события, методы могут содержать только параметры in и должны возвращать только значения **HRESULT** Success или failure.</span><span class="sxs-lookup"><span data-stu-id="ce351-107">To support more than one subscriber notification for an event, methods can contain only in parameters and must return only success or failure **HRESULT** values.</span></span>

> [!Note]  
> <span data-ttu-id="ce351-108">Эта версия событий COM+ не поддерживает распределенное хранилище событий.</span><span class="sxs-lookup"><span data-stu-id="ce351-108">This version of COM+ events does not support a distributed event store.</span></span> <span data-ttu-id="ce351-109">Подписчик должен подписываться на событие на каждом компьютере, с которого он хочет получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="ce351-109">A subscriber must subscribe to an event on each computer from which it wants to receive notification.</span></span> <span data-ttu-id="ce351-110">В качестве альтернативы можно зарегистрировать объект класса событий и подписки на центральном компьютере и создать экземпляр этого объекта класса событий на удаленных компьютерах, на которых публикуются события.</span><span class="sxs-lookup"><span data-stu-id="ce351-110">As an alternative, you can register the event class object and subscriptions on a central computer and instantiate this event class object from the remote computers on which you publish events.</span></span> <span data-ttu-id="ce351-111">Доставка событий предоставляется либо с помощью DCOM, либо с помощью службы очередей компонентов COM+.</span><span class="sxs-lookup"><span data-stu-id="ce351-111">Delivery of events is provided either by DCOM or by the COM+ queued components service.</span></span> <span data-ttu-id="ce351-112">Дополнительные сведения об использовании службы очередей компонентов COM+ см. в разделе [Использование событий COM+ с компонентами, помещенными в очередь com+](using-com--events-with-com--queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="ce351-112">For more information about using the COM+ queued components service, see [Using COM+ Events with COM+ Queued Components](using-com--events-with-com--queued-components.md).</span></span>

 

<span data-ttu-id="ce351-113">По умолчанию служба событий COM+ запускает события по одной за раз, без определенного или повторяемого порядка.</span><span class="sxs-lookup"><span data-stu-id="ce351-113">By default, the COM+ events service fires events one at a time, in no determined or repeatable order.</span></span> <span data-ttu-id="ce351-114">Издатели, которым необходимо управлять порядком, в котором подписчики получают события, могут реализовать фильтр издателя.</span><span class="sxs-lookup"><span data-stu-id="ce351-114">Publishers that need to control the order in which subscribers receive an event can implement a publisher filter.</span></span> <span data-ttu-id="ce351-115">(Дополнительные сведения см. [в разделе Фильтрация событий в com+](filtering-events-in-com-.md).)</span><span class="sxs-lookup"><span data-stu-id="ce351-115">(For more information, see [Filtering Events in COM+](filtering-events-in-com-.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce351-116">См. также</span><span class="sxs-lookup"><span data-stu-id="ce351-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce351-117">Фильтрация событий в COM+</span><span class="sxs-lookup"><span data-stu-id="ce351-117">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="ce351-118">Подписки</span><span class="sxs-lookup"><span data-stu-id="ce351-118">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="ce351-119">Объект класса событий COM+</span><span class="sxs-lookup"><span data-stu-id="ce351-119">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="ce351-120">Использование событий COM+ с компонентами в очереди COM+</span><span class="sxs-lookup"><span data-stu-id="ce351-120">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



